<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LORNEX- Creative Director</title>

<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root {
  --bg: #0b0b0b;
  --orange: #ff642d;
  --white: #fff;
  --muted: #aaa;
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
  font-family: 'DM Sans', sans-serif;
  background: #321713;
  color: var(--white);
}

.backdrop {
  position: fixed;
  inset: 0;
  z-index: -1;
  background:
    radial-gradient(ellipse at 12% 14%, rgba(255,91,27,.48), transparent 38%),
    radial-gradient(ellipse at 86% 78%, rgba(116,34,22,.34), transparent 40%),
    linear-gradient(130deg, #7d3218, #080808);
}

.site {
  width: min(1120px, calc(100% - 48px));
  margin: 52px auto 70px;
  overflow: hidden;
  background: var(--bg);
  border-radius: 0 0 42px 42px;
}

/* HERO */

.hero {
  min-height: 610px;
  position: relative;
  padding: 28px 34px;
  overflow: hidden;
  background:
    linear-gradient(90deg, rgba(255,89,25,.95), rgba(109,24,32,.65)),
    url("https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=1800&q=90")
    center 38% / cover;
}

.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.brand {
  font-size: 18px;
  font-weight: 800;
}

.nav-links {
  display: flex;
  gap: 32px;
  font-size: 12px;
}

.nav-links a {
  color: white;
  text-decoration: none;
  transition: .3s;
}

.nav-links a:hover {
  opacity: .6;
}

.pill {
  display: inline-flex;
  align-items: center;
  gap: 12px;
  border: none;
  border-radius: 50px;
  padding: 6px 7px 6px 17px;
  background: white;
  color: #171717;
  font-size: 11px;
  font-weight: 700;
  text-decoration: none;
  cursor: pointer;
  transition: .3s;
}

.pill:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 25px #0004;
}

.pill-icon {
  width: 27px;
  height: 27px;
  display: grid;
  place-items: center;
  border-radius: 50%;
  background: var(--orange);
  color: white;
}

.hero-copy {
  margin-top: 108px;
  position: relative;
  z-index: 2;
}

.eyebrow {
  margin-bottom: 17px;
  font-size: 17px;
  font-weight: 600;
}

h1 {
  font-size: clamp(58px, 8vw, 92px);
  line-height: .91;
  letter-spacing: -5px;
  font-weight: 800;
}

.hero-note {
  position: absolute;
  right: 5.5%;
  top: 48%;
  width: 235px;
}

.hero-note h2 {
  margin-bottom: 12px;
  font-size: 19px;
}

.hero-note p {
  color: #ffffffad;
  font-size: 12px;
  line-height: 1.7;
}

.services {
  position: absolute;
  bottom: 58px;
  left: 34px;
  right: 34px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
}

.service-number {
  display: block;
  margin-bottom: 9px;
  font-size: 11px;
  font-weight: 700;
}

.service-name {
  font-size: 11px;
}

/* CLIENTS */

.trusted {
  min-height: 142px;
  padding: 38px 34px;
  background: #141414;
  border-radius: 0 0 42px 42px;
  display: flex;
  align-items: center;
  gap: 28px;
}

.trusted-label {
  max-width: 170px;
  font-size: 11px;
  line-height: 1.5;
}

.logos {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
}

.logo {
  display: flex;
  align-items: center;
  gap: 9px;
  color: #e6e4e2;
  font-size: 15px;
  font-weight: 700;
  white-space: nowrap;
}

.logo-mark {
  width: 17px;
  height: 17px;
  border: 2px solid white;
  border-radius: 50%;
}

/* ABOUT */

.about {
  padding: 118px 34px 74px;
}

.about-top {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 70px;
  margin-bottom: 76px;
}

.orange-label {
  margin-bottom: 14px;
  color: var(--orange);
  font-size: 16px;
  font-weight: 700;
}

.about h2 {
  max-width: 540px;
  font-size: clamp(34px, 4.1vw, 49px);
  line-height: 1.08;
  letter-spacing: -2px;
}

.about-right h3 {
  margin-bottom: 24px;
  font-size: 22px;
  line-height: 1.35;
}

.about-bottom {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 18px;
}

.about-bottom p {
  color: #777;
  font-size: 11px;
  line-height: 1.6;
}

.orange-pill {
  background: var(--orange);
  color: white;
}

.orange-pill .pill-icon {
  background: white;
  color: var(--orange);
}

/* PROJECTS */

.projects {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}

.project {
  overflow: hidden;
  border-radius: 20px;
  aspect-ratio: .78;
  background: #202020;
  position: relative;
}

.project img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: grayscale(1);
  transition: transform .65s, filter .5s;
}

.project:hover img {
  transform: scale(1.055);
  filter: grayscale(.35);
}

.project-caption {
  position: absolute;
  left: 16px;
  bottom: 15px;
  opacity: 0;
  transition: .3s;
  font-size: 12px;
  font-weight: 700;
}

.project:hover .project-caption {
  opacity: 1;
}

/* FOOTER */

footer {
  padding: 28px 34px 34px;
  border-top: 1px solid #222;
  color: #777;
  display: flex;
  justify-content: space-between;
  font-size: 11px;
}

/* ANIMATIONS */

.reveal {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity .7s ease, transform .7s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

.menu-toggle {
  display: none;
}

/* MOBILE */

@media (max-width: 760px) {

  .site {
    width: calc(100% - 22px);
    margin: 12px auto 25px;
    border-radius: 0 0 28px 28px;
  }

  .hero {
    min-height: 690px;
    padding: 22px;
    background-position: 58% center;
  }

  .nav-links {
    display: none;
    position: absolute;
    top: 48px;
    right: 0;
    padding: 18px;
    border-radius: 18px;
    background: #151515;
    flex-direction: column;
    gap: 18px;
    z-index: 10;
  }

  .nav-links.open {
    display: flex;
  }

  .menu-toggle {
    display: block;
    margin-left: auto;
    margin-right: 10px;
    border: 0;
    background: #ffffff22;
    color: white;
    border-radius: 50%;
    width: 38px;
    height: 38px;
    cursor: pointer;
  }

  .hero-copy {
    margin-top: 125px;
  }

  h1 {
    font-size: clamp(54px, 15vw, 78px);
    letter-spacing: -3.5px;
  }

  .hero-note {
    top: auto;
    bottom: 165px;
    left: 22px;
    width: 230px;
  }

  .services {
    left: 22px;
    right: 22px;
    bottom: 28px;
    grid-template-columns: repeat(2, 1fr);
    row-gap: 18px;
  }

  .trusted {
    padding: 30px 22px;
    display: block;
  }

  .trusted-label {
    margin-bottom: 24px;
  }

  .logos {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px 10px;
  }

  .logo {
    font-size: 13px;
  }

  .about {
    padding: 78px 22px 48px;
  }

  .about-top {
    grid-template-columns: 1fr;
    gap: 35px;
    margin-bottom: 44px;
  }

  .about h2 {
    font-size: 39px;
  }

  .about-right h3 {
    font-size: 20px;
  }

  .projects {
    gap: 10px;
  }

  .project {
    border-radius: 14px;
  }

  footer {
    padding: 24px 22px;
    gap: 12px;
    flex-wrap: wrap;
  }
}

@media (max-width: 420px) {

  .projects {
    grid-template-columns: 1fr;
  }

  .project {
    aspect-ratio: 1.12;
  }

  .project-caption {
    opacity: 1;
  }

  .about h2 {
    font-size: 34px;
  }

  .hero {
    min-height: 720px;
  }
}

@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    scroll-behavior: auto !important;
    transition-duration: .01ms !important;
    animation-duration: .01ms !important;
  }

  .reveal {
    opacity: 1;
    transform: none;
  }
}
</style>
</head>

<body>

<div class="backdrop"></div>

<main class="site">

  <section class="hero" id="home">

    <nav class="nav">

      <a class="brand" href="#home">Folioblox</a>

      <button class="menu-toggle" id="menuToggle">☰</button>

      <div class="nav-links" id="navLinks">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#projects">Projects</a>
      </div>

      <a class="pill" href="mailto:hello@folioblox.com">
        Get in touch
        <span class="pill-icon">→</span>
      </a>

    </nav>

    <div class="hero-copy">
      <p class="eyebrow">Hey, I'm a</p>
      <h1>Creative<br>Director</h1>
    </div>

    <div class="hero-note">
      <h2>Great design should<br>feel invisible.</h2>
      <p>
        From logo to language, I build brands
        that connect and convert.
      </p>
    </div>

    <div class="services">

      <div>
        <span class="service-number">#01</span>
        <span class="service-name">Brand Strategy</span>
      </div>

      <div>
        <span class="service-number">#02</span>
        <span class="service-name">Brand Identity Design</span>
      </div>

      <div>
        <span class="service-number">#03</span>
        <span class="service-name">Packaging Design</span>
      </div>

      <div>
        <span class="service-number">#04</span>
        <span class="service-name">Creative Direction</span>
      </div>

    </div>

  </section>

  <section class="trusted reveal">

    <div class="trusted-label">
      Trusted by Brands I've<br>
      Helped Shape
    </div>

    <div class="logos">

      <div class="logo">
        <span class="logo-mark"></span>
        Supa Blox
      </div>

      <div class="logo">
        <span class="logo-mark"></span>
        Hype Blox
      </div>

      <div class="logo">
        <span class="logo-mark"></span>
        Frame Blox
      </div>

      <div class="logo">
        <span class="logo-mark"></span>
        Ultra Blox
      </div>

    </div>

  </section>

  <section class="about" id="about">

    <div class="about-top reveal">

      <div>
        <p class="orange-label">Behind the Designs</p>
        <h2>Shaping Experiences That Make Life Simpler</h2>
      </div>

      <div class="about-right">

        <h3>
          I'm a product designer focused on
          building clean, intuitive interfaces
          that solve real-world problems.
        </h3>

        <div class="about-bottom">

          <p>
            Let's Build Something<br>
            Meaningful Together
          </p>

          <a class="pill orange-pill" href="mailto:hello@folioblox.com">
            Get in touch
            <span class="pill-icon">→</span>
          </a>

        </div>

      </div>

    </div>

    <div class="projects reveal" id="projects">

      <article class="project">
        <img
          src="https://images.unsplash.com/photo-1543076447-215ad9ba6923?auto=format&fit=crop&w=900&q=85"
          alt="Fashion product"
          loading="lazy"
        >
        <div class="project-caption">
          01 / Product & Apparel
        </div>
      </article>

      <article class="project">
        <img
          src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?auto=format&fit=crop&w=900&q=85"
          alt="Portrait photography"
          loading="lazy"
        >
        <div class="project-caption">
          02 / Campaign Direction
        </div>
      </article>

      <article class="project">
        <img
          src="https://images.unsplash.com/photo-1608571423902-eed4a5ad8108?auto=format&fit=crop&w=900&q=85"
          alt="Skincare product"
          loading="lazy"
        >
        <div class="project-caption">
          03 / Packaging Design
        </div>
      </article>

    </div>

  </section>

  <footer>
    <span>© <span id="year"></span> Folioblox Studio</span>
    <span>Thoughtful design. Clear impact.</span>
  </footer>

</main>

<script>

const menuToggle = document.getElementById("menuToggle");
const navLinks = document.getElementById("navLinks");

menuToggle.addEventListener("click", () => {

  const isOpen = navLinks.classList.toggle("open");

  menuToggle.setAttribute(
    "aria-expanded",
    String(isOpen)
  );

  menuToggle.textContent = isOpen ? "×" : "☰";

});

navLinks.querySelectorAll("a").forEach(link => {

  link.addEventListener("click", () => {

    navLinks.classList.remove("open");

    menuToggle.setAttribute(
      "aria-expanded",
      "false"
    );

    menuToggle.textContent = "☰";

  });

});

document.getElementById("year").textContent =
  new Date().getFullYear();

const observer = new IntersectionObserver(
  (entries, observer) => {

    entries.forEach(entry => {

      if (entry.isIntersecting) {

        entry.target.classList.add("visible");

        observer.unobserve(entry.target);

      }

    });

  },
  { threshold: 0.12 }
);

document.querySelectorAll(".reveal").forEach(element => {
  observer.observe(element);
});

</script>

</body>
</html>