<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Diane Joris — Community Manager</title>

  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Jost:wght@300;400;500&display=swap" rel="stylesheet"/>

  <style>
    :root {
      --cream: #F5EFE0;
      --ivory: #FDF6F0;
      --caramel: #A0714F;
      --caramel-dark: #7A5238;
      --terracotta: #C4724A;
      --blush: #F0C4C4;
      --rose: #E8A0A0;
      --rose-dark: #C47070;
      --rose-pale: #FAE8E8;
      --text: #3D2B1F;
      --text-light: #8B6F5E;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--ivory);
      color: var(--text);
      font-family: 'Jost', sans-serif;
      font-weight: 300;
      overflow-x: hidden;
    }

    #lang-toggle {
      position: fixed;
      top: 1.5rem;
      right: 2rem;
      z-index: 100;
      background: transparent;
      border: 1px solid var(--rose-dark);
      color: var(--rose-dark);
      font-family: 'Jost', sans-serif;
      font-size: 0.75rem;
      letter-spacing: 0.12em;
      padding: 0.4rem 0.9rem;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    #lang-toggle:hover {
      background: var(--rose-dark);
      color: var(--ivory);
    }

    nav {
      position: fixed;
      top: 1.5rem;
      left: 2rem;
      z-index: 100;
      display: flex;
      gap: 2rem;
    }

    nav a {
      font-family: 'Jost', sans-serif;
      font-size: 0.72rem;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      text-decoration: none;
      color: var(--caramel);
      transition: color 0.3s;
    }

    nav a:hover {
      color: var(--rose-dark);
    }

    #hero {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: flex-start;
      padding: 8rem 8vw 4rem;
      position: relative;
      overflow: hidden;
    }

    .hero-bg-circle {
      position: absolute;
      right: -10vw;
      top: 50%;
      transform: translateY(-50%);
      width: 55vw;
      height: 55vw;
      border-radius: 50%;
      background: radial-gradient(circle at 40% 40%, var(--blush) 0%, var(--rose-pale) 50%, transparent 100%);
      opacity: 0.7;
      pointer-events: none;
    }

    .hero-eyebrow {
      font-family: 'Jost', sans-serif;
      font-size: 0.72rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--rose-dark);
      margin-bottom: 1.5rem;
      opacity: 0;
      animation: fadeUp 0.8s ease forwards 0.2s;
    }

    .hero-name {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(4rem, 10vw, 9rem);
      font-weight: 300;
      line-height: 0.9;
      color: var(--caramel-dark);
      opacity: 0;
      animation: fadeUp 0.9s ease forwards 0.4s;
    }

    .hero-name em {
      font-style: italic;
      color: var(--rose-dark);
    }

    .hero-tagline {
      margin-top: 2.5rem;
      font-size: clamp(1rem, 1.8vw, 1.2rem);
      font-weight: 300;
      color: var(--text-light);
      max-width: 460px;
      line-height: 1.7;
      opacity: 0;
      animation: fadeUp 0.9s ease forwards 0.6s;
    }

    .hero-cta {
      margin-top: 2rem;
      display: inline-block;
      text-decoration: none;
      font-family: 'Jost', sans-serif;
      font-size: 0.78rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--ivory);
      background: var(--rose-dark);
      padding: 1rem 2.2rem;
      transition: background 0.3s ease;
    }

    .hero-cta:hover {
      background: var(--caramel-dark);
    }

    section {
      padding: 7rem 8vw;
    }

    .section-label {
      font-size: 0.68rem;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      color: var(--rose-dark);
      margin-bottom: 1rem;
    }

    .section-title {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(2.2rem, 5vw, 3.8rem);
      font-weight: 300;
      color: var(--caramel-dark);
      line-height: 1.1;
      margin-bottom: 3rem;
    }

    @keyframes fadeUp {
      from {
        opacity: 0;
        transform: translateY(24px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media (max-width: 768px) {
      nav {
        display: none;
      }
    }
  </style>
</head>

<body>

<button id="lang-toggle" onclick="toggleLang()">EN</button>

<nav>
  <a href="#hero" data-fr="Accueil" data-en="Home">Accueil</a>
  <a href="#services" data-fr="Services" data-en="Services">Services</a>
  <a href="#about" data-fr="À propos" data-en="About">À propos</a>
  <a href="#contact" data-fr="Contact" data-en="Contact">Contact</a>
</nav>

<section id="hero">
  <div class="hero-bg-circle"></div>

  <p class="hero-eyebrow"
     data-fr="Community Manager"
     data-en="Community Manager">
     Community Manager
  </p>

  <h1 class="hero-name">
    Diane<br>
    <em>Joris</em>
  </h1>

  <p class="hero-tagline"
     data-fr="J'ai fait des réseaux ma spécialité, et je vous en fais profiter."
     data-en="Social media is my speciality — and I'm putting it to work for you.">
     J'ai fait des réseaux ma spécialité, et je vous en fais profiter.
  </p>

  <a href="#contact"
     class="hero-cta"
     data-fr="Travaillons ensemble"
     data-en="Let's work together">
     Travaillons ensemble
  </a>
</section>

<script>
  let currentLang = 'fr';

  function toggleLang() {
    currentLang = currentLang === 'fr' ? 'en' : 'fr';

    document.getElementById('lang-toggle').textContent =
      currentLang === 'fr' ? 'EN' : 'FR';

    document.documentElement.lang = currentLang;

    document.querySelectorAll('[data-fr][data-en]').forEach(el => {
      const val = el.getAttribute('data-' + currentLang);

      if (val) {
        el.innerHTML = val;
      }
    });
  }
</script>

</body>
</html>
