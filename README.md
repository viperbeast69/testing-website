<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Marabunta Community</title>

<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">

<style>
:root {
  --blue: #1f6bff;
  --bg1: #050814;
  --bg2: #0b1024;
  --text: #f2f4ff;
  --muted: #aab4ff;
  --glass: rgba(255,255,255,0.06);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Inter", sans-serif;
  background: linear-gradient(180deg, var(--bg1), var(--bg2));
  color: var(--text);
  overflow-x: hidden;
}

/* NAV */
nav {
  position: fixed;
  top: 0;
  width: 100%;
  padding: 15px 40px;
  background: rgba(5,8,20,0.7);
  backdrop-filter: blur(12px);
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 1000;
}

nav strong {
  font-family: Orbitron;
  color: var(--blue);
}

nav a {
  color: var(--muted);
  text-decoration: none;
  margin-left: 20px;
  transition: 0.3s;
}

nav a:hover {
  color: var(--blue);
}

/* HERO */
.hero {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 20px;
}

.hero h1 {
  font-family: Orbitron;
  font-size: 3rem;
  color: var(--blue);
  text-shadow: 0 0 25px var(--blue);
  animation: glow 3s infinite alternate;
}

.hero p {
  margin: 20px auto;
  max-width: 650px;
  color: var(--muted);
}

.btn {
  display: inline-block;
  margin-top: 25px;
  padding: 14px 36px;
  border: 1px solid var(--blue);
  color: var(--blue);
  border-radius: 30px;
  text-decoration: none;
  transition: 0.3s;
}

.btn:hover {
  background: var(--blue);
  color: #000;
  box-shadow: 0 0 25px var(--blue);
}

/* SECTIONS */
section {
  padding: 100px 10%;
}

h2 {
  font-size: 2.2rem;
  color: var(--blue);
  margin-bottom: 30px;
}

/* GRID & CARDS */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px,1fr));
  gap: 25px;
}

.card {
  background: var(--glass);
  backdrop-filter: blur(14px);
  padding: 25px;
  border-radius: 15px;
  transition: 0.4s;
  border: 1px solid transparent;
}

.card:hover {
  transform: translateY(-10px) scale(1.03);
  border-color: var(--blue);
  box-shadow: 0 0 30px rgba(31,107,255,0.4);
}

/* GALLERY */
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px,1fr));
  gap: 25px;
}

.gallery img {
  width: 100%;
  border-radius: 18px;
  transition: 0.4s;
  box-shadow: 0 0 20px rgba(0,0,0,0.6);
}

.gallery img:hover {
  transform: scale(1.05);
  box-shadow: 0 0 35px rgba(31,107,255,0.6);
}

/* FOOTER */
footer {
  text-align: center;
  padding: 40px;
  color: var(--muted);
}

/* SCROLL ANIM */
.fade {
  opacity: 0;
  transform: translateY(40px);
  transition: 0.9s ease;
}

.fade.show {
  opacity: 1;
  transform: translateY(0);
}

@keyframes glow {
  from { text-shadow: 0 0 10px var(--blue); }
  to { text-shadow: 0 0 35px var(--blue); }
}

/* RESPONSIVE */
@media (max-width: 600px) {
  .hero h1 { font-size: 2.2rem; }
}
</style>
</head>

<body>

<nav>
  <strong>MARABUNTA</strong>
  <div>
    <a href="#about">About</a>
    <a href="#community">Community</a>
    <a href="#projects">Projects</a>
    <a href="#gallery">Gallery</a>
    <a href="#join">Join</a>
  </div>
</nav>

<section class="hero">
  <div>
    <h1>MARABUNTA COMMUNITY</h1>
    <p>A powerful ultra-blue community united by loyalty, projects, and presence.</p>
    <a href="#join" class="btn">Join the Movement</a>
  </div>
</section>

<section id="about" class="fade">
  <h2>About Us</h2>
  <p>Marabunta is a tight community built on unity, strength, and shared identity.</p>
</section>

<section id="community" class="fade">
  <h2>Community</h2>
  <div class="grid">
    <div class="card">Strong Brotherhood</div>
    <div class="card">Organized Events</div>
    <div class="card">Unified Style</div>
  </div>
</section>

<section id="projects" class="fade">
  <h2>Projects & Events</h2>
  <div class="grid">
    <div class="card">City Presence</div>
    <div class="card">Group Operations</div>
    <div class="card">Future Expansions</div>
  </div>
</section>

<section id="gallery" class="fade">
  <h2>Gallery</h2>
  <div class="gallery">
    <img src="gallery1.png" alt="Marabunta Gallery 1">
    <img src="gallery2.png" alt="Marabunta Gallery 2">
    <img src="gallery3.png" alt="Marabunta Gallery 3">
  </div>
</section>

<section id="join" class="fade">
  <h2>Join Us</h2>
  <p>Become part of the Marabunta identity.</p>
  <a href="#" class="btn">Apply Now</a>
</section>

<footer>
  © 2026 Marabunta Community
</footer>

<script>
const fades = document.querySelectorAll('.fade');
window.addEventListener('scroll', () => {
  fades.forEach(el => {
    if (el.getBoundingClientRect().top < window.innerHeight - 100) {
      el.classList.add('show');
    }
  });
});
</script>

</body>
</html>
