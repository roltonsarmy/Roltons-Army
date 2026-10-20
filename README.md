
<!DOCTYPE html>
<html lang="lv">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#050816">
  <meta name="description" content="Roltons Army — gaming kopiena, projekti un jaunumi.">
  <title>ROLTONS ARMY | Official</title>

  <style>
    :root {
      --bg: #050816;
      --panel: #0b1226;
      --blue: #00c8ff;
      --purple: #8b5cf6;
      --white: #f4f8ff;
      --muted: #98a8c5;
    }

    * { box-sizing: border-box; }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 90px;
    }

    body {
      margin: 0;
      background: var(--bg);
      color: var(--white);
      font-family: Inter, "Segoe UI", Arial, sans-serif;
      overflow-x: hidden;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: -1;
      background:
        radial-gradient(ellipse at 15% 20%, #073b7540, transparent 45%),
        radial-gradient(ellipse at 85% 45%, #5924a52b, transparent 42%);
    }

    a { color: inherit; text-decoration: none; }

    .nav {
      position: sticky;
      top: 0;
      z-index: 10;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
      padding: 18px 7%;
      background: #050816eF;
      backdrop-filter: blur(18px);
      border-bottom: 1px solid #1b2b4b;
    }

    .logo {
      font-size: 18px;
      font-weight: 900;
      letter-spacing: 2px;
    }

    .logo span { color: var(--blue); }

    .nav-links {
      display: flex;
      flex-wrap: wrap;
      gap: 24px;
      color: var(--muted);
      font-size: 13px;
    }

    .nav-links a:hover { color: var(--blue); }

    .hero {
      min-height: 78vh;
      display: grid;
      place-items: center;
      text-align: center;
      padding: 90px 20px;
      position: relative;
      background-image:
        linear-gradient(#05081622, #050816aa),
        linear-gradient(90deg, transparent 49px, #1b65a012 50px),
        linear-gradient(transparent 49px, #1b65a012 50px);
      background-size: auto, 50px 50px, 50px 50px;
    }

    .hero-inner {
      max-width: 850px;
      animation: appear 1s ease both;
    }

    .tag {
      display: inline-block;
      border: 1px solid #00c8ff66;
      border-radius: 99px;
      background: #00c8ff0d;
      color: var(--blue);
      padding: 9px 15px;
      font-size: 11px;
      letter-spacing: 3px;
      font-weight: 800;
    }

    h1 {
      margin: 28px 0 15px;
      font-size: clamp(42px, 9vw, 94px);
      font-weight: 1000;
      line-height: .98;
      letter-spacing: -4px;
      text-shadow: 0 0 35px #008cff38;
    }

    h1 span {
      color: var(--blue);
      text-shadow: 0 0 25px #00c8ff80;
    }

    .hero p {
      max-width: 570px;
      margin: 22px auto 30px;
      line-height: 1.8;
      color: var(--muted);
      font-size: 16px;
    }

    .buttons {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 13px;
    }

    .btn {
      display: inline-block;
      padding: 14px 23px;
      border: 1px solid #00c8ff80;
      border-radius: 8px;
      font-size: 13px;
      font-weight: 800;
      transition: .25s ease;
    }

    .btn-primary {
      color: #00101c;
      background: var(--blue);
      box-shadow: 0 0 22px #00c8ff35;
    }

    .btn-secondary { background: #ffffff05; }

    .btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 0 28px #00c8ff55;
    }

    section { padding: 85px 7%; }

    .section-head {
      text-align: center;
      max-width: 650px;
      margin: 0 auto 42px;
    }

    .eyebrow {
      color: var(--blue);
      font-size: 11px;
      letter-spacing: 4px;
      font-weight: 900;
    }

    h2 {
      font-size: clamp(28px, 5vw, 43px);
      margin: 13px 0;
      letter-spacing: -1px;
    }

    .section-head p, .card p {
      color: var(--muted);
      line-height: 1.8;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 18px;
      max-width: 1100px;
      margin: auto;
    }

    .card {
      background: linear-gradient(145deg, #101a32, #080d1b);
      border: 1px solid #263653;
      border-radius: 15px;
      padding: 28px;
      transition: .25s ease;
    }

    .card:hover {
      transform: translateY(-5px);
      border-color: var(--blue);
      box-shadow: 0 8px 35px #007dff16;
    }

    .card-icon {
      font-size: 28px;
      color: var(--blue);
      text-shadow: 0 0 18px #00c8ff55;
    }

    .card h3 { margin: 19px 0 8px; }

    .card p { font-size: 14px; }

    .community {
      max-width: 900px;
      margin: auto;
      text-align: center;
      border: 1px solid #443a79;
      border-radius: 20px;
      padding: 48px 20px;
      background:
        radial-gradient(ellipse at top, #5531a32b, transparent 65%),
        #0b1022;
      box-shadow: 0 0 60px #582bd20b;
    }

    .community h2 { margin-top: 0; }

    .socials {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 25px;
    }

    .social {
      border: 1px solid #34415e;
      padding: 13px 19px;
      border-radius: 8px;
      font-weight: 700;
      font-size: 13px;
      transition: .2s;
    }

    .social:hover {
      border-color: var(--purple);
      color: #c4a8ff;
      box-shadow: 0 0 20px #8b5cf626;
    }

    footer {
      text-align: center;
      padding: 30px 20px;
      border-top: 1px solid #1b2b4b;
      color: #8291ad;
      font-size: 12px;
      line-height: 2;
    }

    footer strong { color: var(--blue); }

    @keyframes appear {
      from { opacity: 0; transform: translateY(18px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @media (max-width: 760px) {
      .nav { padding: 16px 5%; }
      .nav-links { gap: 12px; font-size: 12px; }
      .logo { font-size: 15px; }
      .grid { grid-template-columns: 1fr; }
      section { padding: 65px 6%; }
      h1 { letter-spacing: -2px; }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after {
        animation: none !important;
        transition: none !important;
        scroll-behavior: auto !important;
      }
    }
  </style>
</head>

<body>
  <nav class="nav">
    <a class="logo" href="#home">ROLTONS<span>ARMY</span></a>
    <div class="nav-links">
      <a href="#home">Sākums</a>
      <a href="#about">Par mums</a>
      <a href="#projects">Projekti</a>
      <a href="#community">Kopiena</a>
    </div>
  </nav>

  <main>
    <header class="hero" id="home">
      <div class="hero-inner">
        <span class="tag">OFFICIAL COMMUNITY WEBSITE</span>
        <h1>WELCOME TO<br><span>ROLTONS ARMY</span></h1>
        <p>
          Viena kopiena. Kopīgi mērķi. Jauni projekti.
          Iepazīsti Roltons Army un seko līdzi mūsu jaunumiem.
        </p>
        <div class="buttons">
          <a class="btn btn-primary" href="#community">PIEVIENOJIES MUMS ↗</a>
          <a class="btn btn-secondary" href="#about">UZZINI VAIRĀK</a>
        </div>
      </div>
    </header>

    <section id="about">
      <div class="section-head">
        <span class="eyebrow">WHO WE ARE</span>
        <h2>Vairāk nekā tikai kopiena.</h2>
        <p>
          Roltons Army ir kopiena, kurā apvienojas spēles,
          radošums un kopīgi projekti. Šī ir mūsu digitālā
          mājvieta.
        </p>
      </div>

      <div class="grid">
        <article class="card">
          <div class="card-icon">◈</div>
          <h3>Kopiena</h3>
          <p>Vieta, kur satikt citus dalībniekus un sekot līdzi kopienas dzīvei.</p>
        </article>

        <article class="card">
          <div class="card-icon">⚡</div>
          <h3>Projekti</h3>
          <p>Jaunas idejas, radoši darbi un projekti, kas attīstās laika gaitā.</p>
        </article>

        <article class="card">
          <div class="card-icon">✦</div>
          <h3>Jaunumi</h3>
          <p>Seko mūsu platformām, lai uzzinātu par jaunumiem un aktivitātēm.</p>
        </article>
      </div>
    </section>

    <section id="projects">
      <div class="section-head">
        <span class="eyebrow">OUR UNIVERSE</span>
        <h2>Mūsu digitālā pasaule.</h2>
        <p>Atrodi mūs platformās, kurās veidojam un kopīgojam saturu.</p>
      </div>

      <div class="grid">
        <article class="card">
          <div class="card-icon">▣</div>
          <h3>Roblox</h3>
          <p>Spēles, piedzīvojumi un kopienas aktivitātes.</p>
          <a class="btn btn-secondary" href="https://www.roblox.com/" target="_blank" rel="noopener noreferrer">Atvērt Roblox ↗</a>
        </article>

        <article class="card">
          <div class="card-icon">▶</div>
          <h3>YouTube</h3>
          <p>Video un saturs no Roltons Army.</p>
          <a class="btn btn-secondary" href="https://www.youtube.com/@roltons_army" target="_blank" rel="noopener noreferrer">Skatīties ↗</a>
        </article>

        <article class="card">
          <div class="card-icon">♪</div>
          <h3>TikTok</h3>
          <p>Īsi video un kopienas jaunumi.</p>
          <a class="btn btn-secondary" href="https://www.tiktok.com/@roltonsarmy" target="_blank" rel="noopener noreferrer">Sekot ↗</a>
        </article>
      </div>
    </section>

    <section id="community">
      <div class="community">
        <span class="eyebrow">JOIN THE MOVEMENT</span>
        <h2>Tava nākamā pietura.</h2>
        <p style="color: var(--muted); line-height: 1.8;">
          Atrodi mūsu saturu un seko līdzi Roltons Army jaunumiem.
        </p>
        <div class="socials">
          <a class="social" href="https://www.youtube.com/@roltons_army" target="_blank" rel="noopener noreferrer">YouTube ↗</a>
          <a class="social" href="https://www.tiktok.com/@roltonsarmy" target="_blank" rel="noopener noreferrer">TikTok ↗</a>
          <a class="social" href="https://www.roblox.com/" target="_blank" rel="noopener noreferrer">Roblox ↗</a>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <strong>ROLTONS ARMY</strong><br>
    Built for the community. Powered by creativity.<br>
    © 2026 Roltons Army. All rights reserved.
  </footer>
</body>
</html>
