<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Denis Löser</title>
  <link href="https://fonts.googleapis.com/css2?family=SF+Pro+Display:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'SF Pro Display', sans-serif;
    }

    body {
      background-color: #fff;
      color: #000;
      line-height: 1.6;
    }

    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 40px;
      background: #f5f5f7;
      border-bottom: 1px solid #ddd;
    }

    header h1 {
      font-size: 1.5rem;
      font-weight: 700;
    }

    nav a {
      margin-left: 20px;
      text-decoration: none;
      color: #333;
      font-weight: 600;
    }

    .hero {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 90vh;
      text-align: center;
      padding: 40px 20px;
    }

    .hero h2 {
      font-size: 3rem;
      font-weight: 700;
      margin-bottom: 20px;
    }

    .hero p {
      font-size: 1.25rem;
      max-width: 600px;
      margin-bottom: 30px;
    }

    .btn {
      padding: 12px 24px;
      background: #000;
      color: #fff;
      text-decoration: none;
      font-weight: 600;
      border-radius: 8px;
      transition: background 0.3s;
    }

    .btn:hover {
      background: #444;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: #f5f5f7;
      color: #666;
      font-size: 0.9rem;
    }
  </style>
</head>
<body>
  <header>
    <h1>Denis Löser</h1>
    <nav>
      <a href="#about">Über mich</a>
      <a href="#services">Leistungen</a>
      <a href="#contact">Kontakt</a>
    </nav>
  </header>

  <section class="hero">
    <h2>Innovative Lösungen für Ihre digitale Zukunft</h2>
    <p>Ich unterstütze Unternehmen dabei, durch intelligentes Marketing und strategische Beratung ihre Ziele zu erreichen.</p>
    <a href="#contact" class="btn">Jetzt Kontakt aufnehmen</a>
  </section>

  <footer>
    &copy; 2025 Denis Löser – Alle Rechte vorbehalten
  </footer>
</body>
</html>
