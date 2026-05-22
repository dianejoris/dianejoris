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

```
* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  background: var(--ivory);
  color: var(--text);
  font-family: 'Jost', sans-serif;
  font-weight: 300;
  overflow-x: hidden;
}

/* ── LANG TOGGLE ── */
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

/* ── NAV ── */
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
nav a:hover { color: var(--rose-dark); }

/* ── HERO ── */
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

/* ── GRATUIT BANNER ── */
.hero-gratuit {
  margin-top: 2rem;
  display: inline-flex;
  align-items: center;
  gap: 0.8rem;
  background: var(--rose-pale);
  border-left: 3px solid var(--rose-dark);
  padding: 0.9rem 1.4rem;
  max-width: 460px;
  opacity: 0;
  animation: fadeUp 0.9s ease forwards 0.75s;
}
.hero-gratuit-icon {
  font-size: 1.1rem;
  flex-shrink: 0;
}
.hero-gratuit-text {
  font-size: 0.82rem;
  color: var(--caramel-dark);
  line-height: 1.5;
}
.hero-gratuit-text strong {
  color: var(--rose-dark);
  font-weight: 500;
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
  opacity: 0;
  animation: fadeUp 0.9s ease forwards 0.9s;
}
.hero-cta:hover { background: var(--caramel-dark); }

.hero-scroll {
  position: absolute;
  bottom: 2.5rem;
  left: 8vw;
  display: flex;
  align-items: center;
  gap: 0.8rem;
  opacity: 0;
  animation: fadeUp 0.9s ease forwards 1.2s;
}
.hero-scroll span {
  font-size: 0.65rem;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--text-light);
}
.scroll-line {
  width: 40px;
  height: 1px;
  background: var(--rose);
  position: relative;
  overflow: hidden;
}
.scroll-line::after {
  content: '';
  position: absolute;
  left: -100%;
  top: 0;
  width: 100%;
  height: 100%;
  background: var(--rose-dark);
  animation: slideLine 2s ease infinite;
}

/* ── SECTION BASE ── */
section { padding: 7rem 8vw; }

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
.section-title em { font-style: italic; color: var(--rose-dark); }

/* ── SERVICES ── */
#services { background: var(--rose-pale); }

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 2px;
}

.service-card {
  background: var(--ivory);
  padding: 2.8rem 2.2rem;
  position: relative;
  overflow: hidden;
  transition: transform 0.3s ease;
}
.service-card:hover { transform: translateY(-4px); }

.service-card::before {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 3px;
  background: var(--rose-dark);
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 0.4s ease;
}
.service-card:hover::before { transform: scaleX(1); }

.service-name {
  font-family: 'Cormorant Garamond', serif;
  font-size: 1.5rem;
  font-weight: 400;
  color: var(--caramel-dark);
  margin-bottom: 0.8rem;
}

.service-desc {
  font-size: 0.88rem;
  color: var(--text-light);
  line-height: 1.75;
}

/* ── ABOUT ── */
#about {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 6rem;
  align-items: center;
}

.about-visual { position: relative; }

.about-rect {
  width: 100%;
  aspect-ratio: 3/4;
  background: linear-gradient(135deg, var(--blush) 0%, var(--rose-pale) 100%);
  position: relative;
}
.about-rect::after {
  content: '';
  position: absolute;
  bottom: -1.5rem;
  right: -1.5rem;
  width: 60%;
  height: 60%;
  border: 2px solid var(--rose);
  opacity: 0.5;
}

.about-initials {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(5rem, 10vw, 8rem);
  font-weight: 300;
  font-style: italic;
  color: var(--rose-dark);
  opacity: 0.25;
  pointer-events: none;
}

.about-content p {
  font-size: 0.95rem;
  color: var(--text-light);
  line-height: 1.9;
  margin-bottom: 1.2rem;
}
.about-content strong {
  color: var(--caramel-dark);
  font-weight: 500;
}

.about-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.6rem;
  margin-top: 2rem;
}
.about-tag {
  font-size: 0.7rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  border: 1px solid var(--rose);
  color: var(--rose-dark);
  padding: 0.35rem 0.9rem;
}

/* ── CONTACT ── */
#contact { background: var(--caramel-dark); }

#contact .section-label { color: var(--blush); }
#contact .section-title { color: var(--ivory); }
#contact .section-title em { color: var(--rose); }

.contact-lead {
  font-size: 0.95rem;
  color: var(--blush);
  line-height: 1.8;
  max-width: 480px;
  margin-bottom: 3rem;
  opacity: 0.85;
}

.contact-links {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.contact-link {
  display: flex;
  align-items: center;
  gap: 1.2rem;
  text-decoration: none;
  color: var(--ivory);
  font-size: 0.9rem;
  letter-spacing: 0.05em;
  transition: color 0.3s;
}
.contact-link:hover { color: var(--rose); }

.contact-link-line {
  width: 30px;
  height: 1px;
  background: var(--rose);
  opacity: 0.5;
  flex-shrink: 0;
}

/* ── FOOTER ── */
footer {
  background: var(--text);
  padding: 1.5rem 8vw;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
footer span {
  font-size: 0.7rem;
  letter-spacing: 0.1em;
  color: var(--text-light);
}

/* ── ANIMATIONS ── */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(24px); }
  to   { opacity: 1; transform: translateY(0); }
}
@keyframes slideLine {
  0%   { left: -100%; }
  50%  { left: 100%; }
  100% { left: 100%; }
}

/* ── RESPONSIVE ── */
@media (max-width: 768px) {
  nav { display: none; }
  #about { grid-template-columns: 1fr; gap: 3rem; }
  .about-visual { max-width: 300px; }
}
```

  </style>
</head>
<body>

<button id="lang-toggle" onclick="toggleLang()">EN</button>

  <nav>
    <a href="#hero"     data-fr="Accueil"  data-en="Home">Accueil</a>
    <a href="#services" data-fr="Services" data-en="Services">Services</a>
    <a href="#about"    data-fr="À propos" data-en="About">À propos</a>
    <a href="#contact"  data-fr="Contact"  data-en="Contact">Contact</a>
  </nav>

  <!-- HERO -->

  <section id="hero">
    <div class="hero-bg-circle"></div>
    <p class="hero-eyebrow" data-fr="Community Manager" data-en="Community Manager">Community Manager</p>
    <h1 class="hero-name">Diane<br><em>Joris</em></h1>
    <p class="hero-tagline"
       data-fr="J'ai fait des réseaux ma spécialité, et je vous en fais profiter."
       data-en="Social media is my speciality — and I'm putting it to work for you.">
      J'ai fait des réseaux ma spécialité, et je vous en fais profiter.
    </p>
    <div class="hero-gratuit">
      <span class="hero-gratuit-icon">✦</span>
      <p class="hero-gratuit-text"
         data-fr="<strong>Prestations gratuites.</strong> Je construis mon portfolio et cherche à collaborer avec des structures qui ont quelque chose à montrer. Profitez-en."
         data-en="<strong>Free of charge.</strong> I'm building my portfolio and looking to work with people who have something worth sharing. Take advantage of it.">
        <strong>Prestations gratuites.</strong> Je construis mon portfolio et cherche à collaborer avec des structures qui ont quelque chose à montrer. Profitez-en.
      </p>
    </div>
    <a href="#contact" class="hero-cta"
       data-fr="Travaillons ensemble"
       data-en="Let's work together">Travaillons ensemble</a>
    <div class="hero-scroll">
      <div class="scroll-line"></div>
      <span data-fr="Découvrir" data-en="Discover">Découvrir</span>
    </div>
  </section>

  <!-- SERVICES -->

  <section id="services">
    <p class="section-label" data-fr="Ce que je fais" data-en="What I do">Ce que je fais</p>
    <h2 class="section-title" data-fr="Mes <em>services</em>" data-en="My <em>services</em>">Mes <em>services</em></h2>
    <div class="services-grid">

```
  <div class="service-card">
    <h3 class="service-name" data-fr="Stratégie éditoriale" data-en="Editorial strategy">Stratégie éditoriale</h3>
    <p class="service-desc"
       data-fr="Planning éditorial, ligne directrice, calendrier de publications adapté à votre audience et vos objectifs."
       data-en="Editorial planning, tone of voice, and a publication calendar tailored to your audience and goals.">
      Planning éditorial, ligne directrice, calendrier de publications adapté à votre audience et vos objectifs.
    </p>
  </div>

  <div class="service-card">
    <h3 class="service-name" data-fr="Couverture d'événements" data-en="Event coverage">Couverture d'événements</h3>
    <p class="service-desc"
       data-fr="Présence sur le terrain, stories en direct, reportage photo/vidéo et bilan de performance."
       data-en="On-site presence, live stories, photo/video coverage and post-event performance report.">
      Présence sur le terrain, stories en direct, reportage photo/vidéo et bilan de performance.
    </p>
  </div>

  <div class="service-card">
    <h3 class="service-name" data-fr="Création de contenu" data-en="Content creation">Création de contenu</h3>
    <p class="service-desc"
       data-fr="Rédaction de posts, légendes, stories et scripts vidéo, pour garder une communauté engagée."
       data-en="Writing posts, captions, stories and video scripts, to keep a community engaged.">
      Rédaction de posts, légendes, stories et scripts vidéo, pour garder une communauté engagée.
    </p>
  </div>

  <div class="service-card">
    <h3 class="service-name" data-fr="Gestion des réseaux" data-en="Social media management">Gestion des réseaux</h3>
    <p class="service-desc"
       data-fr="Animation de vos comptes Instagram, Facebook, TikTok — publications, interactions et modération."
       data-en="Managing your Instagram, Facebook, TikTok accounts — publishing, engaging and moderating.">
      Animation de vos comptes Instagram, Facebook, TikTok — publications, interactions et modération.
    </p>
  </div>

</div>
```

  </section>

  <!-- ABOUT -->

  <section id="about">
    <div class="about-visual">
      <div class="about-rect">
        <span class="about-initials">DJ</span>
      </div>
    </div>
    <div class="about-content">
      <p class="section-label" data-fr="Qui suis-je ?" data-en="Who am I?">Qui suis-je ?</p>
      <h2 class="section-title" data-fr="À <em>propos</em>" data-en="A<em>bout</em>">À <em>propos</em></h2>
      <p data-fr="Je m'appelle Diane et je consacre ma passion pour les réseaux sociaux à faire prospérer vos communautés."
         data-en="My name is Diane, and I channel my passion for social media into helping your communities thrive.">
        Je m'appelle Diane et je consacre ma passion pour les réseaux sociaux à faire prospérer vos communautés.
      </p>
      <p data-fr="<strong>Bilingue français-anglais</strong>, je construis des présences en ligne cohérentes, tout en restant authentiques."
         data-en="<strong>Bilingual in French and English</strong>, I build online presences that are consistent, yet always authentic.">
        <strong>Bilingue français-anglais</strong>, je construis des présences en ligne cohérentes, tout en restant authentiques.
      </p>
      <p data-fr="Je travaille avec des artistes, des communautés, des associations : tous ceux qui ont quelque chose à montrer au monde."
         data-en="I work with artists, communities, and associations — anyone who has something worth showing the world.">
        Je travaille avec des artistes, des communautés, des associations : tous ceux qui ont quelque chose à montrer au monde.
      </p>
      <div class="about-tags">
        <span class="about-tag">Instagram</span>
        <span class="about-tag">Facebook</span>
        <span class="about-tag">TikTok</span>
        <span class="about-tag" data-fr="Rédaction" data-en="Copywriting">Rédaction</span>
        <span class="about-tag" data-fr="Stratégie" data-en="Strategy">Stratégie</span>
        <span class="about-tag" data-fr="Bilingue FR/EN" data-en="Bilingual FR/EN">Bilingue FR/EN</span>
      </div>
    </div>
  </section>

  <!-- CONTACT -->

  <section id="contact">
    <p class="section-label" data-fr="Parlons-en" data-en="Let's talk">Parlons-en</p>
    <h2 class="section-title" data-fr="Me <em>contacter</em>" data-en="Get in <em>touch</em>">Me <em>contacter</em></h2>
    <p class="contact-lead"
       data-fr="Un projet, une question, une idée ? N'hésitez pas à me contacter directement."
       data-en="A project, a question, an idea? Don't hesitate to reach out directly.">
      Un projet, une question, une idée ? N'hésitez pas à me contacter directement.
    </p>
    <div class="contact-links">
      <a href="mailto:votre@email.com" class="contact-link">
        <div class="contact-link-line"></div>
        <span>votre@email.com</span>
      </a>
      <a href="https://instagram.com/" target="_blank" class="contact-link">
        <div class="contact-link-line"></div>
        <span>Instagram</span>
      </a>
      <a href="https://linkedin.com/" target="_blank" class="contact-link">
        <div class="contact-link-line"></div>
        <span>LinkedIn</span>
      </a>
    </div>
  </section>

  <footer>
    <span>© 2025 Diane Joris</span>
    <span data-fr="Community Manager" data-en="Community Manager">Community Manager</span>
  </footer>

  <script>
    let currentLang = 'fr';
    function toggleLang() {
      currentLang = currentLang === 'fr' ? 'en' : 'fr';
      document.getElementById('lang-toggle').textContent = currentLang === 'fr' ? 'EN' : 'FR';
      document.documentElement.lang = currentLang;
      document.querySelectorAll('[data-fr][data-en]').forEach(el => {
        const val = el.getAttribute('data-' + currentLang);
        if (val) el.innerHTML = val;
      });
    }
  </script>

</body>
</html>
