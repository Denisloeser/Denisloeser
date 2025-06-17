import { useState } from 'react';
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { motion } from "framer-motion";

export default function Home() {
  const [language, setLanguage] = useState<'de' | 'en'>('de');

  const content = {
    de: {
      headline: "Willkommen bei derLöser",
      sub: "Wir lösen Ihre Herausforderungen mit Präzision und Stil.",
      button: "Mehr erfahren",
      contact: {
        title: "Kontaktformular",
        name: "Ihr Name",
        email: "Ihre E-Mail",
        message: "Ihre Nachricht",
        send: "Absenden"
      },
      gallery: "Galerie"
    },
    en: {
      headline: "Welcome to derLöser",
      sub: "We solve your challenges with precision and style.",
      button: "Learn more",
      contact: {
        title: "Contact Form",
        name: "Your Name",
        email: "Your Email",
        message: "Your Message",
        send: "Send"
      },
      gallery: "Gallery"
    },
  };

  return (
    <div className="min-h-screen bg-white text-black dark:bg-black dark:text-white transition-colors duration-500">
      <div className="p-4 flex justify-end">
        <Button variant="ghost" onClick={() => setLanguage(language === 'de' ? 'en' : 'de')}>
          {language === 'de' ? 'EN' : 'DE'}
        </Button>
      </div>

      <main className="flex flex-col items-center justify-center text-center px-4 py-20">
        <motion.h1
          initial={{ opacity: 0, y: 20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.8 }}
          className="text-5xl font-bold mb-4"
        >
          {content[language].headline}
        </motion.h1>
        <motion.p
          initial={{ opacity: 0, y: 10 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ delay: 0.3, duration: 0.6 }}
          className="text-xl mb-8 max-w-xl"
        >
          {content[language].sub}
        </motion.p>

        <Button>{content[language].button}</Button>
      </main>

      <section className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 p-6">
        {[1, 2, 3].map((i) => (
          <Card key={i} className="rounded-2xl shadow-md">
            <CardContent className="p-6">
              <h2 className="text-2xl font-semibold mb-2">Feature {i}</h2>
              <p>
                {language === 'de'
                  ? `Beschreibung des Features ${i} auf Deutsch.`
                  : `Description of feature ${i} in English.`}
              </p>
            </CardContent>
          </Card>
        ))}
      </section>

      <section className="p-6">
        <h2 className="text-3xl font-semibold text-center mb-6">{content[language].gallery}</h2>
        <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
          {[1, 2, 3, 4, 5, 6].map((img) => (
            <div key={img} className="aspect-video bg-gray-300 dark:bg-gray-700 rounded-xl"></div>
          ))}
        </div>
      </section>

      <section className="p-6 max-w-xl mx-auto">
        <h2 className="text-3xl font-semibold text-center mb-6">{content[language].contact.title}</h2>
        <form className="space-y-4">
          <Input placeholder={content[language].contact.name} />
          <Input type="email" placeholder={content[language].contact.email} />
          <Textarea placeholder={content[language].contact.message} rows={5} />
          <Button className="w-full">{content[language].contact.send}</Button>
        </form>
      </section>

      <footer className="text-center p-6 text-sm opacity-70">
        © {new Date().getFullYear()} derLöser
      </footer>
    </div>
  );
}
