<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>The Final Projects — India's #1 Final Year Project Store</title>
<link href="https://fonts.googleapis.com/css2?family=Raleway:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,300;1,400&family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=Libre+Baskerville:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet"/>
<style>
  :root {
    --green: #00e87a;
    --blue: #00b4f0;
    --gold: #f5c842;
    --dark: #080c14;
    --darker: #050810;
    --card: #0d1420;
    --card2: #111827;
    --border: rgba(0,232,122,0.18);
    --border2: rgba(0,180,240,0.18);
    --text: #e8f0fe;
    --muted: #7a8fa6;
    --white: #ffffff;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--darker);
    color: var(--text);
    font-family: 'Raleway', 'Gill Sans', 'Gill Sans MT', Calibri, sans-serif;
    font-weight: 400;
    overflow-x: hidden;
    line-height: 1.7;
  }

  /* ── HERO ── */
  .hero {
    position: relative;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 80px 24px 60px;
    overflow: hidden;
    background: radial-gradient(ellipse 80% 60% at 50% 0%, rgba(0,232,122,0.08) 0%, transparent 70%),
                radial-gradient(ellipse 60% 40% at 80% 80%, rgba(0,180,240,0.07) 0%, transparent 60%),
                var(--darker);
  }
  .hero::before {
    content:'';
    position:absolute;
    inset:0;
    background-image:
      linear-gradient(rgba(0,232,122,0.035) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,232,122,0.035) 1px, transparent 1px);
    background-size: 48px 48px;
    pointer-events:none;
  }

  .badge-row {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    margin-bottom: 36px;
  }
  .badge {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 6px 16px;
    border-radius: 100px;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.06em;
    text-transform: uppercase;
  }
  .badge-green { background: rgba(0,232,122,0.1); border: 1px solid rgba(0,232,122,0.3); color: var(--green); }
  .badge-blue  { background: rgba(0,180,240,0.1);  border: 1px solid rgba(0,180,240,0.3);  color: var(--blue); }
  .badge-gold  { background: rgba(245,200,66,0.1);  border: 1px solid rgba(245,200,66,0.3);  color: var(--gold); }

  .hero-eyebrow {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 14px;
    font-weight: 500;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--green);
    margin-bottom: 16px;
  }

  .hero-title {
    font-family: 'Raleway', 'Gill Sans MT', sans-serif;
    font-size: clamp(42px, 7vw, 88px);
    font-weight: 800;
    line-height: 1.05;
    letter-spacing: -0.02em;
    background: linear-gradient(135deg, #ffffff 30%, #a8e6c8 65%, #7dd4f8 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 20px;
  }

  .hero-subtitle {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: clamp(20px, 3vw, 28px);
    font-weight: 300;
    font-style: italic;
    color: var(--muted);
    margin-bottom: 40px;
    max-width: 600px;
  }

  .hero-stats {
    display: flex;
    gap: 48px;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 48px;
  }
  .stat-item { text-align: center; }
  .stat-num {
    display: block;
    font-size: 42px;
    font-weight: 800;
    letter-spacing: -0.02em;
    line-height: 1;
    background: linear-gradient(135deg, var(--green), var(--blue));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  .stat-label {
    font-size: 12px;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--muted);
    margin-top: 4px;
  }

  .hero-cta {
    display: flex;
    gap: 16px;
    justify-content: center;
    flex-wrap: wrap;
  }
  .btn-primary {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 14px 32px;
    background: linear-gradient(135deg, var(--green), #00c97a);
    color: #050810;
    font-family: 'Raleway', sans-serif;
    font-size: 14px;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    border-radius: 8px;
    text-decoration: none;
    transition: transform 0.2s, box-shadow 0.2s;
    box-shadow: 0 0 32px rgba(0,232,122,0.25);
  }
  .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 40px rgba(0,232,122,0.4); }
  .btn-secondary {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 14px 32px;
    border: 1px solid rgba(255,255,255,0.2);
    color: var(--white);
    font-family: 'Raleway', sans-serif;
    font-size: 14px;
    font-weight: 600;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    border-radius: 8px;
    text-decoration: none;
    transition: border-color 0.2s, background 0.2s;
  }
  .btn-secondary:hover { border-color: var(--blue); background: rgba(0,180,240,0.06); }

  /* ── MARQUEE ── */
  .marquee-wrap {
    background: rgba(0,232,122,0.05);
    border-top: 1px solid rgba(0,232,122,0.12);
    border-bottom: 1px solid rgba(0,232,122,0.12);
    padding: 14px 0;
    overflow: hidden;
    white-space: nowrap;
  }
  .marquee-inner {
    display: inline-flex;
    gap: 48px;
    animation: marquee 30s linear infinite;
  }
  .marquee-item {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--green);
    opacity: 0.8;
  }
  .marquee-dot { width: 4px; height: 4px; border-radius: 50%; background: var(--green); flex-shrink: 0; }
  @keyframes marquee { from { transform: translateX(0); } to { transform: translateX(-50%); } }

  /* ── SECTIONS ── */
  section { padding: 100px 24px; max-width: 1100px; margin: 0 auto; }
  .section-eyebrow {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--green);
    margin-bottom: 12px;
  }
  .section-title {
    font-family: 'Raleway', 'Gill Sans MT', sans-serif;
    font-size: clamp(28px, 4vw, 48px);
    font-weight: 800;
    letter-spacing: -0.02em;
    color: var(--white);
    margin-bottom: 16px;
  }
  .section-sub {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 20px;
    font-weight: 300;
    font-style: italic;
    color: var(--muted);
    margin-bottom: 60px;
    max-width: 560px;
  }

  /* ── CATEGORY GRID ── */
  .cat-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 16px;
  }
  .cat-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 28px 24px;
    position: relative;
    overflow: hidden;
    transition: transform 0.25s, border-color 0.25s;
    cursor: default;
  }
  .cat-card::after {
    content:'';
    position:absolute;
    inset:0;
    background: radial-gradient(ellipse 80% 60% at 50% 0%, rgba(0,232,122,0.06), transparent 70%);
    pointer-events:none;
  }
  .cat-card:hover { transform: translateY(-4px); border-color: rgba(0,232,122,0.35); }
  .cat-icon { font-size: 32px; margin-bottom: 14px; }
  .cat-count {
    font-size: 36px;
    font-weight: 800;
    letter-spacing: -0.02em;
    color: var(--green);
    line-height: 1;
    margin-bottom: 4px;
  }
  .cat-name {
    font-size: 15px;
    font-weight: 600;
    color: var(--white);
    margin-bottom: 6px;
  }
  .cat-tech {
    font-size: 12px;
    color: var(--muted);
    line-height: 1.5;
  }

  /* ── FEATURED TABLE ── */
  .projects-table {
    width: 100%;
    border-collapse: collapse;
    border-radius: 16px;
    overflow: hidden;
  }
  .projects-table thead tr {
    background: rgba(0,232,122,0.08);
    border-bottom: 1px solid rgba(0,232,122,0.2);
  }
  .projects-table th {
    padding: 14px 20px;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--green);
    text-align: left;
  }
  .projects-table tbody tr {
    border-bottom: 1px solid rgba(255,255,255,0.04);
    transition: background 0.18s;
  }
  .projects-table tbody tr:hover { background: rgba(255,255,255,0.025); }
  .projects-table td {
    padding: 16px 20px;
    font-size: 14px;
    color: var(--text);
    vertical-align: middle;
  }
  .proj-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 20px;
    font-weight: 300;
    color: rgba(0,232,122,0.4);
    width: 48px;
  }
  .proj-name { font-weight: 600; color: var(--white); }
  .proj-tech { font-size: 12px; color: var(--muted); margin-top: 2px; }
  .proj-tag {
    display: inline-block;
    padding: 4px 10px;
    border-radius: 6px;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.05em;
  }
  .tag-ai    { background: rgba(168,85,247,0.15); color: #c084fc; }
  .tag-web   { background: rgba(0,180,240,0.12);  color: var(--blue); }
  .tag-iot   { background: rgba(245,200,66,0.12);  color: var(--gold); }
  .tag-chain { background: rgba(99,210,173,0.12); color: #5eead4; }
  .tag-ml    { background: rgba(251,146,60,0.12); color: #fb923c; }
  .tag-mob   { background: rgba(244,114,182,0.12); color: #f472b6; }

  /* ── INCLUDES ── */
  .includes-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 16px;
  }
  .include-item {
    display: flex;
    align-items: flex-start;
    gap: 16px;
    padding: 22px 22px;
    background: var(--card);
    border: 1px solid rgba(255,255,255,0.06);
    border-radius: 14px;
    transition: border-color 0.2s;
  }
  .include-item:hover { border-color: rgba(0,232,122,0.25); }
  .include-tick {
    width: 36px;
    height: 36px;
    flex-shrink: 0;
    border-radius: 50%;
    background: rgba(0,232,122,0.1);
    border: 1px solid rgba(0,232,122,0.25);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 16px;
  }
  .include-title { font-size: 14px; font-weight: 600; color: var(--white); margin-bottom: 3px; }
  .include-desc  { font-size: 12px; color: var(--muted); line-height: 1.5; }

  /* ── STEPS ── */
  .steps {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 0;
    position: relative;
  }
  .step {
    padding: 32px 28px;
    border: 1px solid rgba(255,255,255,0.05);
    border-radius: 0;
    background: var(--card2);
    position: relative;
  }
  .step:first-child { border-radius: 16px 0 0 16px; }
  .step:last-child  { border-radius: 0 16px 16px 0; }
  .step-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 64px;
    font-weight: 300;
    line-height: 1;
    color: rgba(0,232,122,0.12);
    margin-bottom: 8px;
  }
  .step-title { font-size: 16px; font-weight: 700; color: var(--white); margin-bottom: 8px; }
  .step-desc  { font-size: 13px; color: var(--muted); line-height: 1.6; }
  .step-arrow {
    position: absolute;
    right: -14px;
    top: 50%;
    transform: translateY(-50%);
    z-index: 2;
    width: 28px;
    height: 28px;
    background: var(--dark);
    border: 1px solid rgba(0,232,122,0.25);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 13px;
    color: var(--green);
  }

  /* ── TECH ── */
  .tech-group { margin-bottom: 36px; }
  .tech-group-label {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 14px;
  }
  .tech-pills { display: flex; flex-wrap: wrap; gap: 8px; }
  .tech-pill {
    padding: 6px 14px;
    background: var(--card);
    border: 1px solid rgba(255,255,255,0.07);
    border-radius: 8px;
    font-size: 13px;
    font-weight: 500;
    color: var(--text);
    transition: border-color 0.18s, color 0.18s;
  }
  .tech-pill:hover { border-color: rgba(0,232,122,0.35); color: var(--green); }

  /* ── CONTACT ── */
  .contact-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 16px;
  }
  .contact-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 12px;
    padding: 36px 24px;
    background: var(--card);
    border: 1px solid rgba(255,255,255,0.07);
    border-radius: 16px;
    text-decoration: none;
    transition: transform 0.22s, border-color 0.22s;
    text-align: center;
  }
  .contact-card:hover { transform: translateY(-4px); }
  .contact-icon {
    width: 52px;
    height: 52px;
    border-radius: 14px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 24px;
  }
  .contact-name { font-size: 15px; font-weight: 700; color: var(--white); }
  .contact-handle { font-size: 12px; color: var(--muted); }

  .wa { background: rgba(37,211,102,0.15); border: 1px solid rgba(37,211,102,0.25); }
  .yt { background: rgba(255,0,0,0.12); border: 1px solid rgba(255,0,0,0.2); }
  .gd { background: rgba(0,180,240,0.12); border: 1px solid rgba(0,180,240,0.2); }
  .tg { background: rgba(0,136,204,0.12); border: 1px solid rgba(0,136,204,0.2); }

  /* ── TESTIMONIAL ── */
  .testimonials { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 16px; }
  .testimonial {
    padding: 28px;
    background: var(--card);
    border: 1px solid rgba(255,255,255,0.06);
    border-radius: 16px;
  }
  .stars { color: var(--gold); font-size: 13px; letter-spacing: 2px; margin-bottom: 14px; }
  .testimonial-text {
    font-family: 'Cormorant Garamond', serif;
    font-size: 17px;
    font-weight: 400;
    font-style: italic;
    color: var(--text);
    line-height: 1.6;
    margin-bottom: 18px;
  }
  .testimonial-author { font-size: 12px; font-weight: 600; color: var(--muted); letter-spacing: 0.08em; text-transform: uppercase; }

  /* ── FOOTER ── */
  footer {
    text-align: center;
    padding: 60px 24px;
    background: var(--darker);
    border-top: 1px solid rgba(255,255,255,0.05);
  }
  footer .f-logo {
    font-family: 'Raleway', 'Gill Sans MT', sans-serif;
    font-size: 22px;
    font-weight: 800;
    letter-spacing: -0.01em;
    background: linear-gradient(135deg, var(--green), var(--blue));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 8px;
  }
  footer .f-tagline {
    font-family: 'Cormorant Garamond', serif;
    font-size: 16px;
    font-style: italic;
    color: var(--muted);
    margin-bottom: 24px;
  }
  footer .f-copy { font-size: 12px; color: rgba(255,255,255,0.2); letter-spacing: 0.05em; }

  /* Divider */
  .divider { width: 60px; height: 2px; background: linear-gradient(90deg, var(--green), var(--blue)); border-radius: 2px; margin-bottom: 20px; }

  /* Full width container */
  .full { max-width: 100%; padding: 0; }
</style>
</head>
<body>

<!-- ═══════════ HERO ═══════════ -->
<div class="hero">
  <div class="badge-row">
    <span class="badge badge-green">🇮🇳 India's #1</span>
    <span class="badge badge-blue">200+ Projects</span>
    <span class="badge badge-gold">⚡ 24hr Delivery</span>
  </div>

  <p class="hero-eyebrow">Est. 2023 · Engineering Project Store</p>

  <h1 class="hero-title">The Final<br/>Projects</h1>

  <p class="hero-subtitle">Complete, working, submission-ready final year projects for engineering students across India</p>

  <div class="hero-stats">
    <div class="stat-item">
      <span class="stat-num">200+</span>
      <span class="stat-label">Projects Ready</span>
    </div>
    <div class="stat-item">
      <span class="stat-num">5</span>
      <span class="stat-label">Tech Domains</span>
    </div>
    <div class="stat-item">
      <span class="stat-num">24hr</span>
      <span class="stat-label">Delivery</span>
    </div>
    <div class="stat-item">
      <span class="stat-num">100%</span>
      <span class="stat-label">Working Code</span>
    </div>
  </div>

  <div class="hero-cta">
    <a href="https://chat.whatsapp.com/BT41x2osFLeAMZFx5QU9qM?mode=gi_t" class="btn-primary" target="_blank">
      💬 Get Your Project Now
    </a>
    <a href="https://www.youtube.com/@TheFinalProjetcs" class="btn-secondary" target="_blank">
      ▶ Watch Demos
    </a>
  </div>
</div>

<!-- ═══════════ MARQUEE ═══════════ -->
<div class="marquee-wrap">
  <div class="marquee-inner">
    <span class="marquee-item"><span class="marquee-dot"></span>AI / Machine Learning</span>
    <span class="marquee-item"><span class="marquee-dot"></span>Web Applications</span>
    <span class="marquee-item"><span class="marquee-dot"></span>Mobile Apps</span>
    <span class="marquee-item"><span class="marquee-dot"></span>IoT Systems</span>
    <span class="marquee-item"><span class="marquee-dot"></span>Blockchain</span>
    <span class="marquee-item"><span class="marquee-dot"></span>Full Source Code</span>
    <span class="marquee-item"><span class="marquee-dot"></span>Project Report</span>
    <span class="marquee-item"><span class="marquee-dot"></span>PPT Included</span>
    <span class="marquee-item"><span class="marquee-dot"></span>Viva Q&A Guide</span>
    <span class="marquee-item"><span class="marquee-dot"></span>WhatsApp Support</span>
    <!-- repeat for seamless loop -->
    <span class="marquee-item"><span class="marquee-dot"></span>AI / Machine Learning</span>
    <span class="marquee-item"><span class="marquee-dot"></span>Web Applications</span>
    <span class="marquee-item"><span class="marquee-dot"></span>Mobile Apps</span>
    <span class="marquee-item"><span class="marquee-dot"></span>IoT Systems</span>
    <span class="marquee-item"><span class="marquee-dot"></span>Blockchain</span>
    <span class="marquee-item"><span class="marquee-dot"></span>Full Source Code</span>
    <span class="marquee-item"><span class="marquee-dot"></span>Project Report</span>
    <span class="marquee-item"><span class="marquee-dot"></span>PPT Included</span>
    <span class="marquee-item"><span class="marquee-dot"></span>Viva Q&A Guide</span>
    <span class="marquee-item"><span class="marquee-dot"></span>WhatsApp Support</span>
  </div>
</div>

<!-- ═══════════ CATEGORIES ═══════════ -->
<section>
  <p class="section-eyebrow">What We Offer</p>
  <h2 class="section-title">Browse by Domain</h2>
  <p class="section-sub">From AI to IoT — every major engineering discipline, all submission-ready</p>

  <div class="cat-grid">
    <div class="cat-card">
      <div class="cat-icon">🤖</div>
      <div class="cat-count">50+</div>
      <div class="cat-name">AI / Machine Learning</div>
      <div class="cat-tech">Python · TensorFlow · Keras · OpenCV · Scikit-learn</div>
    </div>
    <div class="cat-card">
      <div class="cat-icon">🌐</div>
      <div class="cat-count">80+</div>
      <div class="cat-name">Web Applications</div>
      <div class="cat-tech">React · Node.js · Django · Spring Boot · PHP</div>
    </div>
    <div class="cat-card">
      <div class="cat-icon">📱</div>
      <div class="cat-count">30+</div>
      <div class="cat-name">Mobile Apps</div>
      <div class="cat-tech">Flutter · Android · Kotlin · React Native</div>
    </div>
    <div class="cat-card">
      <div class="cat-icon">🔌</div>
      <div class="cat-count">20+</div>
      <div class="cat-name">IoT Projects</div>
      <div class="cat-tech">Arduino · Raspberry Pi · ESP32 · Python</div>
    </div>
    <div class="cat-card">
      <div class="cat-icon">⛓️</div>
      <div class="cat-count">20+</div>
      <div class="cat-name">Blockchain</div>
      <div class="cat-tech">Solidity · Web3.js · Ethereum · Smart Contracts</div>
    </div>
  </div>
</section>

<!-- ═══════════ FEATURED PROJECTS ═══════════ -->
<section style="background: rgba(255,255,255,0.015); border-radius:24px; margin: 0 24px; padding: 80px 48px;">
  <p class="section-eyebrow">Featured</p>
  <h2 class="section-title">Popular Projects</h2>
  <p class="section-sub">Hand-picked top sellers — all come with source code, report & demo video</p>

  <table class="projects-table">
    <thead>
      <tr>
        <th style="width:48px">#</th>
        <th>Project</th>
        <th>Category</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td class="proj-num">01</td>
        <td>
          <div class="proj-name">Face Recognition Attendance System</div>
          <div class="proj-tech">Python · OpenCV · CNN · Flask</div>
        </td>
        <td><span class="proj-tag tag-ai">AI / CV</span></td>
      </tr>
      <tr>
        <td class="proj-num">02</td>
        <td>
          <div class="proj-name">Disease Prediction System</div>
          <div class="proj-tech">Python · Scikit-learn · Flask · MySQL</div>
        </td>
        <td><span class="proj-tag tag-ml">ML</span></td>
      </tr>
      <tr>
        <td class="proj-num">03</td>
        <td>
          <div class="proj-name">E-Commerce Full Stack Platform</div>
          <div class="proj-tech">MERN Stack · MongoDB · Stripe API</div>
        </td>
        <td><span class="proj-tag tag-web">Web App</span></td>
      </tr>
      <tr>
        <td class="proj-num">04</td>
        <td>
          <div class="proj-name">Smart College Portal</div>
          <div class="proj-tech">Java · Spring Boot · MySQL · React</div>
        </td>
        <td><span class="proj-tag tag-web">Full Stack</span></td>
      </tr>
      <tr>
        <td class="proj-num">05</td>
        <td>
          <div class="proj-name">AI Chatbot with NLP</div>
          <div class="proj-tech">Python · NLTK · TensorFlow · Flask</div>
        </td>
        <td><span class="proj-tag tag-ai">AI / NLP</span></td>
      </tr>
      <tr>
        <td class="proj-num">06</td>
        <td>
          <div class="proj-name">Vehicle Number Plate Detection</div>
          <div class="proj-tech">Python · OpenCV · EasyOCR</div>
        </td>
        <td><span class="proj-tag tag-ai">Computer Vision</span></td>
      </tr>
      <tr>
        <td class="proj-num">07</td>
        <td>
          <div class="proj-name">Supply Chain on Blockchain</div>
          <div class="proj-tech">Solidity · Web3.js · React · Truffle</div>
        </td>
        <td><span class="proj-tag tag-chain">Blockchain</span></td>
      </tr>
      <tr>
        <td class="proj-num">08</td>
        <td>
          <div class="proj-name">Smart Home IoT System</div>
          <div class="proj-tech">Arduino · Raspberry Pi · Python · MQTT</div>
        </td>
        <td><span class="proj-tag tag-iot">IoT</span></td>
      </tr>
      <tr>
        <td class="proj-num">09</td>
        <td>
          <div class="proj-name">Food Delivery Mobile App</div>
          <div class="proj-tech">Flutter · Firebase · Google Maps API</div>
        </td>
        <td><span class="proj-tag tag-mob">Mobile</span></td>
      </tr>
      <tr>
        <td class="proj-num">10</td>
        <td>
          <div class="proj-name">Online Banking System</div>
          <div class="proj-tech">Java · JSP · MySQL · Bootstrap</div>
        </td>
        <td><span class="proj-tag tag-web">Web App</span></td>
      </tr>
    </tbody>
  </table>

  <p style="margin-top:28px; font-size:14px; color:var(--muted); text-align:center;">
    💡 Don't see your topic? We have 200+ projects. <a href="https://chat.whatsapp.com/BT41x2osFLeAMZFx5QU9qM?mode=gi_t" style="color:var(--green); text-decoration:none; font-weight:600;">DM us on WhatsApp →</a>
  </p>
</section>

<!-- ═══════════ WHAT'S INCLUDED ═══════════ -->
<section>
  <p class="section-eyebrow">Every Package</p>
  <h2 class="section-title">What You Get</h2>
  <p class="section-sub">Everything you need from code to viva — zero hassle</p>

  <div class="includes-grid">
    <div class="include-item">
      <div class="include-tick">💻</div>
      <div>
        <div class="include-title">Complete Source Code</div>
        <div class="include-desc">Clean, commented, and ready to run — no broken dependencies</div>
      </div>
    </div>
    <div class="include-item">
      <div class="include-tick">📄</div>
      <div>
        <div class="include-title">Project Report</div>
        <div class="include-desc">Full documentation, 20–80 pages, IEEE-format ready</div>
      </div>
    </div>
    <div class="include-item">
      <div class="include-tick">📝</div>
      <div>
        <div class="include-title">Synopsis / Abstract</div>
        <div class="include-desc">Ready-to-submit synopsis in standard engineering format</div>
      </div>
    </div>
    <div class="include-item">
      <div class="include-tick">🗄️</div>
      <div>
        <div class="include-title">Database / Schema</div>
        <div class="include-desc">SQL dump or DB file included and configured</div>
      </div>
    </div>
    <div class="include-item">
      <div class="include-tick">🖥️</div>
      <div>
        <div class="include-title">PPT Presentation</div>
        <div class="include-desc">Professional slides designed for your viva defence</div>
      </div>
    </div>
    <div class="include-item">
      <div class="include-tick">🎬</div>
      <div>
        <div class="include-title">Demo Video</div>
        <div class="include-desc">Full working walkthrough video of the project in action</div>
      </div>
    </div>
    <div class="include-item">
      <div class="include-tick">📋</div>
      <div>
        <div class="include-title">Installation Guide</div>
        <div class="include-desc">Step-by-step setup for Windows, Linux & Mac</div>
      </div>
    </div>
    <div class="include-item">
      <div class="include-tick">🎓</div>
      <div>
        <div class="include-title">Viva Q&A Guide</div>
        <div class="include-desc">Most-asked examiner questions with model answers</div>
      </div>
    </div>
    <div class="include-item">
      <div class="include-tick">💬</div>
      <div>
        <div class="include-title">WhatsApp Support</div>
        <div class="include-desc">Personal support until your project is submitted & approved</div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════ HOW TO BUY ═══════════ -->
<section style="max-width:900px;">
  <p class="section-eyebrow">Simple Process</p>
  <h2 class="section-title">How to Buy</h2>
  <p class="section-sub">Four steps from browsing to receiving your complete project</p>

  <div class="steps">
    <div class="step">
      <div class="step-num">01</div>
      <div class="step-title">Browse & Choose</div>
      <div class="step-desc">Browse 200+ projects or tell us your topic and we'll match you perfectly</div>
      <div class="step-arrow">→</div>
    </div>
    <div class="step">
      <div class="step-num">02</div>
      <div class="step-title">Contact Us</div>
      <div class="step-desc">DM us on WhatsApp, Instagram, or email with your project requirement</div>
      <div class="step-arrow">→</div>
    </div>
    <div class="step">
      <div class="step-num">03</div>
      <div class="step-title">Make Payment</div>
      <div class="step-desc">Pay via UPI, PhonePe, or Bank Transfer — secure and instant</div>
      <div class="step-arrow">→</div>
    </div>
    <div class="step">
      <div class="step-num">04</div>
      <div class="step-title">Receive in 24hr</div>
      <div class="step-desc">Get your full project package delivered within 24 hours — ready to submit ✅</div>
    </div>
  </div>
</section>

<!-- ═══════════ TECH STACK ═══════════ -->
<section style="background: rgba(255,255,255,0.015); border-radius:24px; margin: 0 24px; padding: 80px 48px;">
  <p class="section-eyebrow">Technologies</p>
  <h2 class="section-title">Tech Stack We Cover</h2>
  <p class="section-sub">Every major language, framework and database used in engineering curricula</p>

  <div class="tech-group">
    <div class="tech-group-label">Languages</div>
    <div class="tech-pills">
      <span class="tech-pill">Python</span>
      <span class="tech-pill">Java</span>
      <span class="tech-pill">JavaScript</span>
      <span class="tech-pill">PHP</span>
      <span class="tech-pill">Kotlin</span>
      <span class="tech-pill">Dart</span>
      <span class="tech-pill">Solidity</span>
      <span class="tech-pill">C / C++</span>
    </div>
  </div>

  <div class="tech-group">
    <div class="tech-group-label">Frameworks & Libraries</div>
    <div class="tech-pills">
      <span class="tech-pill">React</span>
      <span class="tech-pill">Node.js</span>
      <span class="tech-pill">Django</span>
      <span class="tech-pill">Flask</span>
      <span class="tech-pill">Spring Boot</span>
      <span class="tech-pill">Flutter</span>
      <span class="tech-pill">TensorFlow</span>
      <span class="tech-pill">OpenCV</span>
      <span class="tech-pill">Keras</span>
      <span class="tech-pill">Scikit-learn</span>
      <span class="tech-pill">Web3.js</span>
    </div>
  </div>

  <div class="tech-group" style="margin-bottom:0">
    <div class="tech-group-label">Databases & Platforms</div>
    <div class="tech-pills">
      <span class="tech-pill">MySQL</span>
      <span class="tech-pill">MongoDB</span>
      <span class="tech-pill">Firebase</span>
      <span class="tech-pill">PostgreSQL</span>
      <span class="tech-pill">Arduino</span>
      <span class="tech-pill">Raspberry Pi</span>
      <span class="tech-pill">ESP32</span>
      <span class="tech-pill">Ethereum</span>
    </div>
  </div>
</section>

<!-- ═══════════ TESTIMONIALS ═══════════ -->
<section>
  <p class="section-eyebrow">Student Reviews</p>
  <h2 class="section-title">What Students Say</h2>
  <p class="section-sub">Real feedback from engineering students who submitted with us</p>

  <div class="testimonials">
    <div class="testimonial">
      <div class="stars">★★★★★</div>
      <div class="testimonial-text">"Got my AI attendance system project within 12 hours. The viva Q&A guide was incredibly helpful — my examiner was impressed."</div>
      <div class="testimonial-author">Arjun S. · VIT Chennai · CSE Final Year</div>
    </div>
    <div class="testimonial">
      <div class="stars">★★★★★</div>
      <div class="testimonial-text">"The MERN stack e-commerce project was complete with everything. Source code, report, PPT and even a demo video. Highly recommend!"</div>
      <div class="testimonial-author">Priya R. · Anna University · IT Department</div>
    </div>
    <div class="testimonial">
      <div class="stars">★★★★★</div>
      <div class="testimonial-text">"WhatsApp support was super fast. They helped me set up the project on my laptop step by step. Submitted with zero issues."</div>
      <div class="testimonial-author">Karthik M. · SRM Institute · ECE Branch</div>
    </div>
  </div>
</section>

<!-- ═══════════ CONTACT ═══════════ -->
<section style="max-width:800px; text-align:center;">
  <p class="section-eyebrow">Get in Touch</p>
  <h2 class="section-title">Contact Us Now</h2>
  <p class="section-sub" style="margin:0 auto 40px;">We respond within minutes on WhatsApp — pick your preferred channel</p>

  <div class="contact-grid">
    <a href="https://chat.whatsapp.com/BT41x2osFLeAMZFx5QU9qM?mode=gi_t" class="contact-card" target="_blank">
      <div class="contact-icon wa">💬</div>
      <div class="contact-name">WhatsApp</div>
      <div class="contact-handle">Join our group</div>
    </a>
    <a href="https://www.youtube.com/@TheFinalProjetcs" class="contact-card" target="_blank">
      <div class="contact-icon yt">▶</div>
      <div class="contact-name">YouTube</div>
      <div class="contact-handle">@TheFinalProjetcs</div>
    </a>
    <a href="https://drive.google.com/file/d/1FLHEiPEBpyR7ZWxoamL0yl_yd7MFfwL5/view" class="contact-card" target="_blank">
      <div class="contact-icon gd">📁</div>
      <div class="contact-name">Project List</div>
      <div class="contact-handle">Browse all titles</div>
    </a>
    <a href="https://t.me/thefinalprojects" class="contact-card" target="_blank">
      <div class="contact-icon tg">✈</div>
      <div class="contact-name">Telegram</div>
      <div class="contact-handle">@thefinalprojects</div>
    </a>
  </div>
</section>

<!-- ═══════════ FOOTER ═══════════ -->
<footer>
  <div class="f-logo">The Final Projects</div>
  <div class="f-tagline">Built with care for engineering students across India</div>
  <div class="f-copy">© 2025 The Final Projects · 200+ Projects · 24hr Delivery · WhatsApp Support</div>
</footer>

</body>
</html>
