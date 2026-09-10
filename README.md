<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,300;9..144,500;9..144,600&family=Work+Sans:wght@300;400;500&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #14171C;
    --bg-alt: #1B1F26;
    --line: #2A2F38;
    --text: #EDE7DA;
    --text-muted: #8B92A0;
    --accent: #C9A227;
  }
  *{ box-sizing: border-box; margin:0; padding:0; }
  html{ scroll-behavior: smooth; }
  body{
    background: var(--bg);
    color: var(--text);
    font-family: 'Work Sans', sans-serif;
    font-weight: 300;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }
  a{ color: inherit; text-decoration: none; }

  .wrap{ max-width: 860px; margin: 0 auto; padding: 0 28px; }

  /* NAV */
  nav{
    position: sticky; top:0; z-index: 10;
    background: rgba(20,23,28,0.85);
    backdrop-filter: blur(8px);
    border-bottom: 1px solid var(--line);
  }
  nav .wrap{ display:flex; align-items:center; justify-content: space-between; height: 64px; }
  .logo{ font-family:'Fraunces', serif; font-size: 1.15rem; letter-spacing: 0.02em; }
  .logo span{ color: var(--accent); }
  .navlinks{ display:flex; gap: 28px; font-size: 0.88rem; color: var(--text-muted); }
  .navlinks a{ transition: color 0.2s ease; }
  .navlinks a:hover{ color: var(--text); }

  /* HERO */
  header.hero{ padding: 120px 0 90px; }
  .eyebrow{
    font-family:'IBM Plex Mono', monospace;
    font-size: 0.82rem;
    color: var(--accent);
    margin-bottom: 22px;
    opacity: 0;
    animation: rise 0.7s ease forwards;
  }
  h1{
    font-family:'Fraunces', serif;
    font-weight: 500;
    font-size: clamp(2.4rem, 6vw, 4.1rem);
    line-height: 1.08;
    letter-spacing: -0.01em;
    max-width: 11ch;
    opacity: 0;
    animation: rise 0.8s ease 0.12s forwards;
  }
  .hero-sub{
    margin-top: 26px;
    max-width: 46ch;
    font-size: 1.08rem;
    color: var(--text-muted);
    opacity: 0;
    animation: rise 0.8s ease 0.24s forwards;
  }
  .hero-cta{
    margin-top: 38px;
    display: inline-flex; align-items: center; gap: 10px;
    font-size: 0.92rem;
    color: var(--text);
    border-bottom: 1px solid var(--accent);
    padding-bottom: 4px;
    opacity: 0;
    animation: rise 0.8s ease 0.36s forwards;
    transition: opacity 0.2s ease;
  }
  .hero-cta:hover{ opacity: 0.7; }

  @keyframes rise{
    from{ opacity:0; transform: translateY(14px); }
    to{ opacity:1; transform: translateY(0); }
  }
  @media (prefers-reduced-motion: reduce){
    .eyebrow, h1, .hero-sub, .hero-cta{ animation: none; opacity: 1; }
  }

  /* SECTION SHARED */
  section{ padding: 70px 0; border-top: 1px solid var(--line); }
  .section-head{
    display:flex; align-items:baseline; justify-content: space-between;
    margin-bottom: 44px;
  }
  h2{
    font-family:'Fraunces', serif;
    font-weight: 500;
    font-size: 1.7rem;
  }
  .section-count{
    font-family:'IBM Plex Mono', monospace;
    font-size: 0.8rem;
    color: var(--text-muted);
  }

  /* PROJECTS — log style rows */
  .project-row{
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 6px 24px;
    padding: 26px 0;
    border-bottom: 1px solid var(--line);
    cursor: pointer;
  }
  .project-row:first-child{ padding-top: 0; }
  .project-title{
    font-family:'Fraunces', serif;
    font-size: 1.28rem;
    font-weight: 500;
    transition: color 0.2s ease;
  }
  .project-row:hover .project-title{ color: var(--accent); }
  .project-link{
    font-family:'IBM Plex Mono', monospace;
    font-size: 0.78rem;
    color: var(--text-muted);
    align-self: start;
  }
  .project-desc{
    grid-column: 1 / -1;
    color: var(--text-muted);
    font-size: 0.95rem;
    max-width: 62ch;
    max-height: 0;
    overflow: hidden;
    opacity: 0;
    transition: max-height 0.35s ease, opacity 0.3s ease, margin 0.35s ease;
  }
  .project-row.open .project-desc{
    max-height: 200px;
    opacity: 1;
    margin-top: 10px;
  }
  .stack{
    grid-column: 1 / -1;
    display: flex; flex-wrap: wrap; gap: 10px;
    max-height: 0; overflow: hidden; opacity: 0;
    transition: max-height 0.35s ease, opacity 0.3s ease, margin 0.35s ease;
  }
  .project-row.open .stack{ max-height: 60px; opacity: 1; margin-top: 14px; }
  .stack span{
    font-family:'IBM Plex Mono', monospace;
    font-size: 0.72rem;
    color: var(--accent);
    border: 1px solid var(--line);
    border-radius: 3px;
    padding: 4px 9px;
  }

  /* GALLERY — auto-scrolling marquee */
  .gallery-section{ padding: 70px 0 76px; border-top: 1px solid var(--line); overflow: hidden; }
  .gallery-mask{
    position: relative;
    cursor: grab;
    -webkit-mask-image: linear-gradient(to right, transparent, black 8%, black 92%, transparent);
    mask-image: linear-gradient(to right, transparent, black 8%, black 92%, transparent);
  }
  .gallery-mask.dragging{ cursor: grabbing; }
  .marquee-track{
    display: flex;
    gap: 22px;
    width: max-content;
    will-change: transform;
  }
  .marquee-track img{
    height: 220px;
    width: 320px;
    object-fit: cover;
    border-radius: 6px;
    border: 1px solid var(--line);
    filter: grayscale(65%) brightness(0.85);
    transition: filter 0.35s ease, transform 0.12s ease-out, box-shadow 0.3s ease;
    transform: perspective(600px) rotateX(0deg) rotateY(0deg);
    will-change: transform;
  }
  .marquee-track img:hover{
    filter: grayscale(0%) brightness(1);
    box-shadow: 0 18px 34px rgba(0,0,0,0.35);
  }
  @media (prefers-reduced-motion: reduce){
    .marquee-track{ transition: none; }
  }
  @media (max-width: 560px){
    .marquee-track img{ height: 160px; width: 230px; }
  }

  /* SKILLS */
  .skills-grid{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 36px;
  }
  .skill-group h3{
    font-family:'IBM Plex Mono', monospace;
    font-size: 0.8rem;
    color: var(--accent);
    margin-bottom: 14px;
  }
  .skill-group ul{ list-style:none; }
  .skill-group li{
    padding: 7px 0;
    border-bottom: 1px solid var(--line);
    font-size: 0.95rem;
    color: var(--text-muted);
  }
  .skill-group li:last-child{ border-bottom: none; }

  /* CONTACT / FOOTER */
  .contact-block{ display:flex; flex-direction: column; gap: 18px; }
  .contact-main{
    font-family:'Fraunces', serif;
    font-size: clamp(1.6rem, 4vw, 2.3rem);
    font-weight: 500;
    max-width: 16ch;
  }
  .contact-main a{ border-bottom: 1px solid var(--accent); }
  .contact-links{ display:flex; gap: 26px; margin-top: 10px; }
  .contact-links a{ color: var(--text-muted); font-size: 0.92rem; transition: color 0.2s ease; }
  .contact-links a:hover{ color: var(--text); }

  footer{ padding: 40px 0 60px; }
  footer .wrap{
    display:flex; justify-content: space-between; align-items:center;
    font-family:'IBM Plex Mono', monospace;
    font-size: 0.75rem;
    color: var(--text-muted);
  }

  @media (max-width: 560px){
    header.hero{ padding: 90px 0 60px; }
    .project-row{ grid-template-columns: 1fr; }
    .project-link{ margin-top: 4px; }
  }
</style>
</head>
<body>

<nav>
  <div class="wrap">
    <div class="logo">G<span>.</span>B</div>
    <div class="navlinks">
      <a href="#projets">Projets</a>
      <a href="#competences">Compétences</a>
      <a href="#contact">Contact</a>
    </div>
  </div>
</nav>

<header class="hero">
  <div class="wrap">
    <div class="eyebrow">Développeur — basé à Lyon, dispo pour des projets</div>
    <h1>Gabriel, je construis des interfaces qui tiennent debout.</h1>
    <p class="hero-sub">
      Je conçois et développe des produits web, du prototype rapide à l'application en production.
      Ce qui m'intéresse : les détails qu'on ne remarque que quand ils manquent.
    </p>
    <a class="hero-cta" href="#projets">Voir les projets ↓</a>
  </div>
</header>

<section id="projets">
  <div class="wrap">
    <div class="section-head">
      <h2>Projets sélectionnés</h2>
      <span class="section-count">03</span>
    </div>

    <div class="project-row" data-open="false">
      <div class="project-title">https://gabpops69.github.io/novatest</div>
      <div class="project-link">github.com/toi/projet →</div>
      <div class="project-desc">
        Une phrase ou deux sur le problème résolu, le contexte, et ton rôle dans le projet.
      </div>
      <div class="stack"><span>React</span><span>Node.js</span><span>PostgreSQL</span></div>
    </div>

    <div class="project-row" data-open="false">
      <div class="project-title">Nom du projet deux</div>
      <div class="project-link">site sur l'espace →</div>
      <div class="project-desc">
        Description courte du projet : ce qu'il fait, pour qui, et ce que tu en as appris.
      </div>
      <div class="stack"><span>TypeScript</span><span>Next.js</span><span>Docker</span></div>
    </div>

    <div class="project-row" data-open="false">
      <div class="project-title">Nom du projet trois</div>
      <div class="project-link">github.com/toi/projet-trois →</div>
      <div class="project-desc">
        Un projet perso, une contribution open-source, ou une expérience technique notable.
      </div>
      <div class="stack"><span>Python</span><span>FastAPI</span><span>Redis</span></div>
    </div>
  </div>
</section>

<section class="gallery-section">
  <div class="wrap">
    <div class="section-head">
      <h2>Aperçus</h2>
      <span class="section-count">captures</span>
    </div>
  </div>
  <div class="gallery-mask">
    <div class="marquee-track">
      <img src="https://picsum.photos/seed/proj1/320/220" alt="Aperçu du projet 1">
      <img src="https://picsum.photos/seed/proj2/320/220" alt="Aperçu du projet 2">
      <img src="https://picsum.photos/seed/proj3/320/220" alt="Aperçu du projet 3">
      <img src="https://picsum.photos/seed/proj4/320/220" alt="Aperçu du projet 4">
      <img src="https://picsum.photos/seed/proj5/320/220" alt="Aperçu du projet 5">
      <img src="https://picsum.photos/seed/proj6/320/220" alt="Aperçu du projet 6">
      <!-- duplication pour boucle infinie sans coupure -->
      <img src="https://picsum.photos/seed/proj1/320/220" alt="Aperçu du projet 1">
      <img src="https://picsum.photos/seed/proj2/320/220" alt="Aperçu du projet 2">
      <img src="https://picsum.photos/seed/proj3/320/220" alt="Aperçu du projet 3">
      <img src="https://picsum.photos/seed/proj4/320/220" alt="Aperçu du projet 4">
      <img src="https://picsum.photos/seed/proj5/320/220" alt="Aperçu du projet 5">
      <img src="https://picsum.photos/seed/proj6/320/220" alt="Aperçu du projet 6">
    </div>
  </div>
</section>

<section id="competences">
  <div class="wrap">
    <div class="section-head">
      <h2>Compétences</h2>
    </div>
    <div class="skills-grid">
      <div class="skill-group">
        <h3>Frontend</h3>
        <ul>
          <li>React / Vue</li>
          <li>TypeScript</li>
          <li>CSS avancé</li>
        </ul>
      </div>
      <div class="skill-group">
        <h3>Backend</h3>
        <ul>
          <li>Node.js</li>
          <li>Python</li>
          <li>Bases de données SQL</li>
        </ul>
      </div>
      <div class="skill-group">
        <h3>Outils</h3>
        <ul>
          <li>Git</li>
          <li>Docker</li>
          <li>CI / CD</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<section id="contact">
  <div class="wrap">
    <div class="contact-block">
      <div class="contact-main">Une idée de projet ? <a href="mailto:toi@example.com">Écris-moi.</a></div>
      <div class="contact-links">
        <a href="#">GitHub</a>
        <a href="#">LinkedIn</a>
        <a href="#">CV</a>
      </div>
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    <span>© 2026 — [Ton Nom]</span>
    <span>fait à la main</span>
  </div>
</footer>

<script>
  // Galerie : défilement automatique + glisser-déposer manuel
  const track = document.querySelector('.marquee-track');
  const mask = document.querySelector('.gallery-mask');
  const reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

  let posX = 0;
  let isHover = false;
  let isDragging = false;
  let dragStartX = 0;
  let dragStartPos = 0;
  const speed = 0.55; // px par frame

  function tick(){
    if(!isDragging && !isHover && !reduceMotion){
      posX -= speed;
    }
    const halfWidth = track.scrollWidth / 2;
    if(halfWidth > 0){
      if(posX <= -halfWidth) posX += halfWidth;
      if(posX > 0) posX -= halfWidth;
    }
    track.style.transform = `translateX(${posX}px)`;
    requestAnimationFrame(tick);
  }
  requestAnimationFrame(tick);

  mask.addEventListener('mouseenter', () => { isHover = true; });
  mask.addEventListener('mouseleave', () => { isHover = false; isDragging = false; mask.classList.remove('dragging'); });

  function startDrag(clientX){
    isDragging = true;
    dragStartX = clientX;
    dragStartPos = posX;
    mask.classList.add('dragging');
  }
  function duringDrag(clientX){
    if(!isDragging) return;
    posX = dragStartPos + (clientX - dragStartX);
  }
  function endDrag(){
    isDragging = false;
    mask.classList.remove('dragging');
  }

  mask.addEventListener('mousedown', e => startDrag(e.clientX));
  window.addEventListener('mousemove', e => duringDrag(e.clientX));
  window.addEventListener('mouseup', endDrag);

  mask.addEventListener('touchstart', e => startDrag(e.touches[0].clientX), { passive: true });
  mask.addEventListener('touchmove', e => duringDrag(e.touches[0].clientX), { passive: true });
  mask.addEventListener('touchend', endDrag);

  document.querySelectorAll('.marquee-track img').forEach(img => {
    const maxTilt = 10;
    img.addEventListener('mousemove', (e) => {
      const rect = img.getBoundingClientRect();
      const x = (e.clientX - rect.left) / rect.width;
      const y = (e.clientY - rect.top) / rect.height;
      const rotateY = (x - 0.5) * maxTilt * 2;
      const rotateX = (0.5 - y) * maxTilt * 2;
      img.style.transform = `perspective(600px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) scale(1.04)`;
    });
    img.addEventListener('mouseleave', () => {
      img.style.transform = 'perspective(600px) rotateX(0deg) rotateY(0deg) scale(1)';
    });
  });

  document.querySelectorAll('.project-row').forEach(row => {
    row.addEventListener('click', () => {
      const isOpen = row.classList.contains('open');
      document.querySelectorAll('.project-row').forEach(r => r.classList.remove('open'));
      if(!isOpen) row.classList.add('open');
    });
  });
</script>

</body>
</html>

<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NOVA — Accès</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@500;600;700&family=Inter:wght@300;400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --black: #060607;
    --panel: #0D0E10;
    --line: #232529;
    --white: #F5F5F3;
    --grey: #8A8D93;
    --accent: #E8542A;
    --error: #E85A5A;
  }
  *{ box-sizing:border-box; margin:0; padding:0; }
  body{
    background: var(--black);
    color: var(--white);
    font-family: 'Inter', sans-serif;
    font-weight: 300;
    min-height: 100vh;
    display: flex; align-items: center; justify-content: center;
    padding: 24px;
    position: relative;
    overflow: hidden;
  }
  a{ color: inherit; text-decoration: none; }

  .stars{
    position: absolute; inset: 0;
    background-image:
      radial-gradient(1px 1px at 20% 30%, rgba(255,255,255,0.5) 50%, transparent),
      radial-gradient(1px 1px at 70% 60%, rgba(255,255,255,0.4) 50%, transparent),
      radial-gradient(1px 1px at 40% 80%, rgba(255,255,255,0.35) 50%, transparent),
      radial-gradient(1px 1px at 85% 15%, rgba(255,255,255,0.45) 50%, transparent),
      radial-gradient(1px 1px at 10% 65%, rgba(255,255,255,0.3) 50%, transparent),
      radial-gradient(1px 1px at 60% 25%, rgba(255,255,255,0.4) 50%, transparent),
      radial-gradient(1px 1px at 90% 75%, rgba(255,255,255,0.3) 50%, transparent);
    opacity: 0.8;
  }

  .card{
    position: relative; z-index: 2;
    width: 100%; max-width: 420px;
    background: var(--panel);
    border: 1px solid var(--line);
    border-radius: 4px;
    padding: 44px 38px;
  }
  .brand{
    font-family: 'Barlow Condensed', sans-serif;
    font-weight: 700;
    font-size: 1.4rem;
    letter-spacing: 0.06em;
    text-align: center;
    margin-bottom: 6px;
  }
  .brand span{ color: var(--accent); }
  .subtitle{
    text-align: center;
    font-family: 'IBM Plex Mono', monospace;
    font-size: 0.72rem;
    color: var(--grey);
    letter-spacing: 0.04em;
    margin-bottom: 34px;
  }

  .tabs{
    display: flex;
    border: 1px solid var(--line);
    border-radius: 3px;
    margin-bottom: 30px;
    overflow: hidden;
  }
  .tab{
    flex: 1;
    text-align: center;
    padding: 12px;
    font-size: 0.85rem;
    color: var(--grey);
    cursor: pointer;
    transition: background 0.2s ease, color 0.2s ease;
  }
  .tab.active{ background: var(--accent); color: var(--black); font-weight: 500; }

  form{ display: none; flex-direction: column; gap: 18px; }
  form.active{ display: flex; }

  label{
    font-family: 'IBM Plex Mono', monospace;
    font-size: 0.7rem;
    color: var(--grey);
    letter-spacing: 0.04em;
    text-transform: uppercase;
    margin-bottom: 8px;
    display: block;
  }
  input{
    width: 100%;
    background: var(--black);
    border: 1px solid var(--line);
    color: var(--white);
    padding: 12px 14px;
    font-family: 'Inter', sans-serif;
    font-size: 0.92rem;
    border-radius: 3px;
    outline: none;
    transition: border-color 0.2s ease;
  }
  input:focus{ border-color: var(--accent); }

  .submit-btn{
    background: var(--accent);
    color: var(--black);
    border: none;
    padding: 13px;
    font-family: 'Inter', sans-serif;
    font-size: 0.9rem;
    font-weight: 500;
    border-radius: 3px;
    cursor: pointer;
    transition: opacity 0.2s ease;
    margin-top: 6px;
  }
  .submit-btn:hover{ opacity: 0.88; }
  .submit-btn:disabled{ opacity: 0.5; cursor: not-allowed; }

  .msg{
    font-family: 'IBM Plex Mono', monospace;
    font-size: 0.76rem;
    padding: 10px 12px;
    border-radius: 3px;
    display: none;
  }
  .msg.show{ display: block; }
  .msg.error{ background: rgba(232,90,90,0.1); color: var(--error); border: 1px solid rgba(232,90,90,0.3); }
  .msg.success{ background: rgba(232,84,42,0.1); color: var(--accent); border: 1px solid rgba(232,84,42,0.3); }

  .welcome{ display:none; text-align: center; }
  .welcome.show{ display: block; }
  .welcome h2{
    font-family: 'Barlow Condensed', sans-serif;
    font-weight: 700;
    font-size: 1.8rem;
    text-transform: uppercase;
    margin-bottom: 10px;
  }
  .welcome p{ color: var(--grey); font-size: 0.9rem; margin-bottom: 24px; }
  .logout-btn{
    border: 1px solid var(--line);
    padding: 10px 22px;
    font-size: 0.82rem;
    border-radius: 3px;
    cursor: pointer;
    background: transparent;
    color: var(--white);
  }
  .logout-btn:hover{ border-color: var(--white); }

  .hint{
    text-align: center;
    font-size: 0.75rem;
    color: var(--grey);
    margin-top: 22px;
    line-height: 1.5;
  }
</style>
</head>
<body>

<div class="stars"></div>

<div class="card">
  <div id="authView">
    <div class="brand">NOVA<span>.</span></div>
    <div class="subtitle">ACCÈS MISSION CONTROL</div>

    <div class="tabs">
      <div class="tab active" data-tab="login">Se connecter</div>
      <div class="tab" data-tab="signup">Créer un compte</div>
    </div>

    <div class="msg" id="msgBox"></div>

    <form id="loginForm" class="active">
      <div>
        <label>Email</label>
        <input type="email" id="loginEmail" required>
      </div>
      <div>
        <label>Mot de passe</label>
        <input type="password" id="loginPassword" required>
      </div>
      <button type="submit" class="submit-btn">Se connecter</button>
    </form>

    <form id="signupForm">
      <div>
        <label>Nom</label>
        <input type="text" id="signupName" required>
      </div>
      <div>
        <label>Email</label>
        <input type="email" id="signupEmail" required>
      </div>
      <div>
        <label>Mot de passe</label>
        <input type="password" id="signupPassword" required minlength="6">
      </div>
      <button type="submit" class="submit-btn">Créer mon compte</button>
    </form>

    <div class="hint">Compte de démonstration — les identifiants sont stockés pour cet artifact, pas pour un vrai service sécurisé.</div>
  </div>

  <div class="welcome" id="welcomeView">
    <div class="brand" style="margin-bottom:24px;">NOVA<span>.</span></div>
    <h2 id="welcomeName">Bienvenue</h2>
    <p id="welcomeEmail"></p>
    <button class="logout-btn" id="logoutBtn">Se déconnecter</button>
  </div>
</div>

<script>
  const tabs = document.querySelectorAll('.tab');
  const forms = { login: document.getElementById('loginForm'), signup: document.getElementById('signupForm') };
  const msgBox = document.getElementById('msgBox');
  const authView = document.getElementById('authView');
  const welcomeView = document.getElementById('welcomeView');

  tabs.forEach(tab => {
    tab.addEventListener('click', () => {
      tabs.forEach(t => t.classList.remove('active'));
      tab.classList.add('active');
      Object.values(forms).forEach(f => f.classList.remove('active'));
      forms[tab.dataset.tab].classList.add('active');
      hideMsg();
    });
  });

  function showMsg(text, type){
    msgBox.textContent = text;
    msgBox.className = 'msg show ' + type;
  }
  function hideMsg(){
    msgBox.className = 'msg';
  }

  function showWelcome(name, email){
    authView.style.display = 'none';
    welcomeView.classList.add('show');
    document.getElementById('welcomeName').textContent = `Bon retour, ${name}`;
    document.getElementById('welcomeEmail').textContent = email;
  }

  document.getElementById('signupForm').addEventListener('submit', async (e) => {
    e.preventDefault();
    hideMsg();
    const name = document.getElementById('signupName').value.trim();
    const email = document.getElementById('signupEmail').value.trim().toLowerCase();
    const password = document.getElementById('signupPassword').value;
    const btn = e.target.querySelector('.submit-btn');
    btn.disabled = true;

    try{
      let exists = null;
      try{ exists = await window.storage.get('account:' + email, false); } catch(err){ exists = null; }

      if(exists){
        showMsg('Un compte existe déjà avec cet email.', 'error');
        btn.disabled = false;
        return;
      }

      await window.storage.set('account:' + email, JSON.stringify({ name, email, password }), false);
      showMsg('Compte créé avec succès.', 'success');
      setTimeout(() => showWelcome(name, email), 500);
    }catch(err){
      showMsg('Erreur lors de la création du compte. Réessaie.', 'error');
    }
    btn.disabled = false;
  });

  document.getElementById('loginForm').addEventListener('submit', async (e) => {
    e.preventDefault();
    hideMsg();
    const email = document.getElementById('loginEmail').value.trim().toLowerCase();
    const password = document.getElementById('loginPassword').value;
    const btn = e.target.querySelector('.submit-btn');
    btn.disabled = true;

    try{
      let result = null;
      try{ result = await window.storage.get('account:' + email, false); } catch(err){ result = null; }

      if(!result){
        showMsg('Aucun compte trouvé avec cet email.', 'error');
        btn.disabled = false;
        return;
      }
      const account = JSON.parse(result.value);
      if(account.password !== password){
        showMsg('Mot de passe incorrect.', 'error');
        btn.disabled = false;
        return;
      }
      showWelcome(account.name, account.email);
    }catch(err){
      showMsg('Erreur de connexion. Réessaie.', 'error');
    }
    btn.disabled = false;
  });

  document.getElementById('logoutBtn').addEventListener('click', () => {
    welcomeView.classList.remove('show');
    authView.style.display = 'block';
    document.getElementById('loginForm').reset();
    document.getElementById('signupForm').reset();
    hideMsg();
  });
</script>

</body>
</html>
