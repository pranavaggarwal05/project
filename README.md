<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vantello — Quartz Kitchen Sinks</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --brown: #5C2E0E;
    --brown-light: #8B4A1F;
    --cream: #F7F3EE;
    --stone: #E8E0D5;
    --charcoal: #1A1714;
    --mid: #6B5F54;
    --white: #FDFAF7;
    --accent: #C4874A;
    --font-display: 'Cormorant Garamond', serif;
    --font-body: 'DM Sans', sans-serif;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: var(--font-body);
    background: var(--white);
    color: var(--charcoal);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 60px;
    height: 72px;
    background: rgba(253,250,247,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(92,46,14,0.08);
  }
  .nav-logo {
    font-family: var(--font-display);
    font-size: 28px;
    font-weight: 600;
    color: var(--brown);
    letter-spacing: 0.04em;
    text-decoration: none;
  }
  .nav-logo span { color: var(--accent); font-style: italic; }
  .nav-links { display: flex; gap: 40px; list-style: none; }
  .nav-links a {
    font-size: 13px; font-weight: 400; letter-spacing: 0.12em;
    text-transform: uppercase; color: var(--mid);
    text-decoration: none; transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--brown); }
  .nav-cta {
    font-size: 12px; font-weight: 500; letter-spacing: 0.14em;
    text-transform: uppercase; color: var(--white);
    background: var(--brown); padding: 10px 24px;
    text-decoration: none; transition: background 0.2s;
  }
  .nav-cta:hover { background: var(--brown-light); }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: grid; grid-template-columns: 1fr 1fr;
    padding-top: 72px;
    background: var(--charcoal);
    overflow: hidden;
  }
  .hero-left {
    display: flex; flex-direction: column; justify-content: center;
    padding: 80px 70px 80px 80px;
    position: relative;
  }
  .hero-eyebrow {
    font-size: 11px; font-weight: 500; letter-spacing: 0.22em;
    text-transform: uppercase; color: var(--accent);
    margin-bottom: 28px;
    display: flex; align-items: center; gap: 14px;
  }
  .hero-eyebrow::before {
    content: ''; width: 40px; height: 1px; background: var(--accent);
  }
  .hero-h1 {
    font-family: var(--font-display);
    font-size: clamp(56px, 6vw, 88px);
    font-weight: 300; line-height: 1.0;
    color: var(--white);
    margin-bottom: 32px;
  }
  .hero-h1 em { font-style: italic; color: var(--accent); }
  .hero-desc {
    font-size: 15px; line-height: 1.8; color: rgba(253,250,247,0.6);
    max-width: 380px; margin-bottom: 50px; font-weight: 300;
  }
  .hero-actions { display: flex; gap: 20px; align-items: center; }
  .btn-primary {
    background: var(--accent); color: var(--white);
    padding: 16px 36px; font-size: 12px; font-weight: 500;
    letter-spacing: 0.16em; text-transform: uppercase;
    text-decoration: none; transition: all 0.25s;
    display: inline-block;
  }
  .btn-primary:hover { background: var(--brown-light); }
  .btn-ghost {
    color: rgba(253,250,247,0.6); font-size: 12px; font-weight: 400;
    letter-spacing: 0.12em; text-transform: uppercase;
    text-decoration: none; display: flex; align-items: center; gap: 10px;
    transition: color 0.2s;
  }
  .btn-ghost::after { content: '→'; transition: transform 0.2s; }
  .btn-ghost:hover { color: var(--white); }
  .btn-ghost:hover::after { transform: translateX(4px); }

  .hero-right {
    position: relative; overflow: hidden;
  }
  .hero-right img {
    width: 100%; height: 100%; object-fit: cover;
    filter: brightness(0.85) saturate(0.9);
    transition: transform 8s ease;
  }
  .hero-right:hover img { transform: scale(1.04); }
  .hero-badge {
    position: absolute; bottom: 40px; left: -20px;
    background: var(--cream); padding: 20px 28px;
    border-left: 3px solid var(--accent);
  }
  .hero-badge-num {
    font-family: var(--font-display); font-size: 42px; font-weight: 300;
    color: var(--brown); line-height: 1;
  }
  .hero-badge-text {
    font-size: 11px; letter-spacing: 0.14em; text-transform: uppercase;
    color: var(--mid); margin-top: 4px;
  }

  /* ── TRUST BAR ── */
  .trust-bar {
    background: var(--cream);
    display: grid; grid-template-columns: repeat(4, 1fr);
    border-top: 1px solid var(--stone); border-bottom: 1px solid var(--stone);
  }
  .trust-item {
    padding: 28px 40px;
    display: flex; align-items: center; gap: 16px;
    border-right: 1px solid var(--stone);
  }
  .trust-item:last-child { border-right: none; }
  .trust-icon {
    width: 36px; height: 36px;
    background: var(--brown); border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
  }
  .trust-icon svg { width: 18px; height: 18px; fill: none; stroke: var(--white); stroke-width: 1.5; }
  .trust-label { font-size: 13px; font-weight: 500; color: var(--charcoal); line-height: 1.3; }
  .trust-sub { font-size: 11px; color: var(--mid); margin-top: 2px; }

  /* ── SECTION HEADER ── */
  .section-header { text-align: center; margin-bottom: 60px; }
  .section-eyebrow {
    font-size: 11px; font-weight: 500; letter-spacing: 0.22em;
    text-transform: uppercase; color: var(--accent);
    margin-bottom: 16px; display: block;
  }
  .section-title {
    font-family: var(--font-display);
    font-size: clamp(38px, 4vw, 58px);
    font-weight: 300; line-height: 1.1; color: var(--charcoal);
  }
  .section-title em { font-style: italic; color: var(--brown); }
  .section-sub {
    font-size: 15px; color: var(--mid); max-width: 520px;
    margin: 16px auto 0; line-height: 1.75; font-weight: 300;
  }

  /* ── COLLECTIONS ── */
  .collections { padding: 100px 80px; background: var(--white); }

  .collection-tabs {
    display: flex; gap: 0; justify-content: center;
    margin-bottom: 60px;
    border: 1px solid var(--stone);
    width: fit-content; margin-left: auto; margin-right: auto;
  }
  .tab-btn {
    padding: 12px 28px; font-size: 12px; font-weight: 500;
    letter-spacing: 0.12em; text-transform: uppercase;
    background: transparent; border: none; cursor: pointer;
    color: var(--mid); transition: all 0.2s;
    border-right: 1px solid var(--stone);
  }
  .tab-btn:last-child { border-right: none; }
  .tab-btn.active { background: var(--brown); color: var(--white); }
  .tab-btn:hover:not(.active) { background: var(--stone); color: var(--charcoal); }

  .products-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2px;
  }

  .product-card {
    position: relative; overflow: hidden; background: var(--cream);
    cursor: pointer; group: true;
  }
  .product-card:first-child { grid-column: span 2; }
  .product-img-wrap {
    aspect-ratio: 4/3; overflow: hidden;
    position: relative;
  }
  .product-card:first-child .product-img-wrap { aspect-ratio: 16/9; }
  .product-img-wrap img {
    width: 100%; height: 100%; object-fit: cover;
    transition: transform 0.6s ease, filter 0.4s ease;
    filter: saturate(0.85);
  }
  .product-card:hover .product-img-wrap img {
    transform: scale(1.06); filter: saturate(1);
  }
  .product-overlay {
    position: absolute; inset: 0;
    background: linear-gradient(to top, rgba(26,23,20,0.7) 0%, transparent 55%);
    opacity: 0; transition: opacity 0.4s;
  }
  .product-card:hover .product-overlay { opacity: 1; }
  .product-info {
    padding: 20px 24px 24px;
    background: var(--cream);
  }
  .product-series {
    font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--accent); font-weight: 500; margin-bottom: 6px;
  }
  .product-name {
    font-family: var(--font-display); font-size: 24px; font-weight: 400;
    color: var(--charcoal); margin-bottom: 8px; line-height: 1.2;
  }
  .product-size {
    font-size: 12px; color: var(--mid); letter-spacing: 0.06em;
  }
  .color-dots {
    display: flex; gap: 6px; margin-top: 12px;
  }
  .dot {
    width: 14px; height: 14px; border-radius: 50%;
    border: 1.5px solid rgba(0,0,0,0.12);
    transition: transform 0.15s;
    cursor: pointer;
  }
  .dot:hover { transform: scale(1.3); }

  /* ── FEATURES ── */
  .features { padding: 100px 80px; background: var(--charcoal); }
  .features .section-title { color: var(--white); }
  .features .section-sub { color: rgba(253,250,247,0.5); }

  .features-grid {
    display: grid; grid-template-columns: repeat(2, 1fr);
    gap: 2px; margin-top: 70px;
  }
  .feature-card {
    padding: 56px 52px;
    background: rgba(255,255,255,0.03);
    border: 1px solid rgba(255,255,255,0.06);
    position: relative; overflow: hidden;
    transition: background 0.3s;
  }
  .feature-card:hover { background: rgba(255,255,255,0.06); }
  .feature-number {
    font-family: var(--font-display); font-size: 72px; font-weight: 300;
    color: rgba(255,255,255,0.04); position: absolute;
    top: 20px; right: 30px; line-height: 1; user-select: none;
  }
  .feature-icon-line {
    width: 40px; height: 2px; background: var(--accent); margin-bottom: 28px;
  }
  .feature-title {
    font-family: var(--font-display); font-size: 28px; font-weight: 400;
    color: var(--white); margin-bottom: 14px; line-height: 1.2;
  }
  .feature-desc {
    font-size: 14px; line-height: 1.8; color: rgba(253,250,247,0.5);
    font-weight: 300; max-width: 340px;
  }

  /* ── SERIES SHOWCASE ── */
  .showcase { padding: 100px 0; background: var(--cream); overflow: hidden; }
  .showcase .section-header { padding: 0 80px; }

  .showcase-strip {
    display: flex; gap: 2px;
    overflow-x: auto; padding: 0 80px;
    scrollbar-width: none;
  }
  .showcase-strip::-webkit-scrollbar { display: none; }
  .showcase-item {
    flex-shrink: 0; width: 320px;
    background: var(--white); cursor: pointer;
    transition: transform 0.3s;
  }
  .showcase-item:hover { transform: translateY(-8px); }
  .showcase-item img {
    width: 100%; aspect-ratio: 4/3; object-fit: cover;
    filter: saturate(0.9); transition: filter 0.3s;
  }
  .showcase-item:hover img { filter: saturate(1.1); }
  .showcase-item-info { padding: 20px 22px; }
  .showcase-item-series {
    font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--accent); margin-bottom: 4px;
  }
  .showcase-item-name {
    font-family: var(--font-display); font-size: 20px; font-weight: 400;
    color: var(--charcoal);
  }
  .showcase-item-size {
    font-size: 12px; color: var(--mid); margin-top: 4px;
  }

  /* ── MATERIAL SECTION ── */
  .material { padding: 100px 80px; background: var(--white); }
  .material-inner {
    display: grid; grid-template-columns: 1fr 1fr; gap: 80px; align-items: center;
  }
  .material-left img {
    width: 100%; aspect-ratio: 4/5; object-fit: cover;
  }
  .material-right { padding: 20px 0; }
  .material-right .section-eyebrow { text-align: left; display: block; margin-bottom: 16px; }
  .material-right .section-title { text-align: left; }
  .material-right .section-sub { text-align: left; margin-left: 0; margin-top: 20px; }
  .material-stats {
    display: grid; grid-template-columns: 1fr 1fr; gap: 0;
    margin-top: 48px; border: 1px solid var(--stone);
  }
  .stat-box {
    padding: 28px 32px; border-right: 1px solid var(--stone);
    border-bottom: 1px solid var(--stone);
  }
  .stat-box:nth-child(2n) { border-right: none; }
  .stat-box:nth-child(3), .stat-box:nth-child(4) { border-bottom: none; }
  .stat-num {
    font-family: var(--font-display); font-size: 42px; font-weight: 300;
    color: var(--brown); line-height: 1;
  }
  .stat-label { font-size: 12px; color: var(--mid); margin-top: 6px; font-weight: 300; letter-spacing: 0.04em; }

  /* ── COLOR FAMILIES ── */
  .colors { padding: 100px 80px; background: var(--cream); }
  .color-grid {
    display: grid; grid-template-columns: repeat(4, 1fr); gap: 2px;
    margin-top: 60px;
  }
  .color-swatch {
    aspect-ratio: 1; position: relative; cursor: pointer;
    overflow: hidden; transition: transform 0.3s;
  }
  .color-swatch:hover { transform: scale(0.98); }
  .swatch-bg { width: 100%; height: 100%; }
  .swatch-label {
    position: absolute; bottom: 0; left: 0; right: 0;
    padding: 16px; background: rgba(26,23,20,0.55);
    font-size: 11px; letter-spacing: 0.14em; text-transform: uppercase;
    color: var(--white); font-weight: 500;
  }

  /* ── CONTACT / INQUIRY ── */
  .inquiry { padding: 100px 80px; background: var(--charcoal); }
  .inquiry-inner {
    display: grid; grid-template-columns: 1fr 1fr; gap: 80px; align-items: start;
  }
  .inquiry-left .section-title { color: var(--white); text-align: left; }
  .inquiry-left .section-sub { color: rgba(253,250,247,0.5); text-align: left; margin-left: 0; }
  .inquiry-left .section-eyebrow { text-align: left; display: block; margin-bottom: 16px; }
  .contact-items { margin-top: 48px; display: flex; flex-direction: column; gap: 24px; }
  .contact-item { display: flex; gap: 16px; align-items: flex-start; }
  .contact-dot {
    width: 8px; height: 8px; background: var(--accent);
    border-radius: 50%; margin-top: 6px; flex-shrink: 0;
  }
  .contact-label { font-size: 11px; letter-spacing: 0.14em; text-transform: uppercase; color: var(--accent); margin-bottom: 4px; }
  .contact-value { font-size: 15px; color: var(--white); font-weight: 300; }

  .inquiry-form { display: flex; flex-direction: column; gap: 20px; }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  .field { display: flex; flex-direction: column; gap: 8px; }
  .field label { font-size: 11px; letter-spacing: 0.14em; text-transform: uppercase; color: rgba(253,250,247,0.4); }
  .field input, .field select, .field textarea {
    background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1);
    color: var(--white); padding: 14px 16px; font-size: 14px;
    font-family: var(--font-body); outline: none; resize: none;
    transition: border-color 0.2s;
  }
  .field input:focus, .field select:focus, .field textarea:focus {
    border-color: var(--accent);
  }
  .field select option { background: var(--charcoal); }
  .submit-btn {
    background: var(--accent); color: var(--white);
    border: none; padding: 18px 40px; font-size: 12px; font-weight: 500;
    letter-spacing: 0.18em; text-transform: uppercase; cursor: pointer;
    font-family: var(--font-body); transition: background 0.2s;
    align-self: flex-start;
  }
  .submit-btn:hover { background: var(--brown-light); }

  /* ── FOOTER ── */
  footer {
    background: #0E0C0A; padding: 60px 80px 40px;
    border-top: 1px solid rgba(255,255,255,0.04);
  }
  .footer-top {
    display: grid; grid-template-columns: 2fr 1fr 1fr 1fr; gap: 60px;
    padding-bottom: 48px; border-bottom: 1px solid rgba(255,255,255,0.06);
  }
  .footer-brand { }
  .footer-logo {
    font-family: var(--font-display); font-size: 28px; font-weight: 600;
    color: var(--white); letter-spacing: 0.04em; display: block; margin-bottom: 16px;
  }
  .footer-logo span { color: var(--accent); font-style: italic; }
  .footer-tagline { font-size: 13px; color: rgba(255,255,255,0.35); line-height: 1.7; font-weight: 300; }
  .footer-col-title {
    font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--accent); margin-bottom: 20px; font-weight: 500;
  }
  .footer-links { list-style: none; display: flex; flex-direction: column; gap: 12px; }
  .footer-links a { font-size: 13px; color: rgba(255,255,255,0.35); text-decoration: none; transition: color 0.2s; }
  .footer-links a:hover { color: var(--white); }
  .footer-bottom {
    padding-top: 32px; display: flex; justify-content: space-between; align-items: center;
  }
  .footer-copy { font-size: 12px; color: rgba(255,255,255,0.2); }
  .footer-tagline-small { font-size: 12px; color: rgba(255,255,255,0.2); font-family: var(--font-display); font-style: italic; }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .hero-left > * { animation: fadeUp 0.8s ease both; }
  .hero-eyebrow { animation-delay: 0.1s; }
  .hero-h1 { animation-delay: 0.25s; }
  .hero-desc { animation-delay: 0.4s; }
  .hero-actions { animation-delay: 0.55s; }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    nav { padding: 0 24px; }
    .nav-links { display: none; }
    .hero { grid-template-columns: 1fr; }
    .hero-right { height: 50vw; }
    .hero-left { padding: 48px 24px; }
    .collections, .features, .material, .colors, .inquiry { padding: 60px 24px; }
    .trust-bar { grid-template-columns: 1fr 1fr; }
    .trust-item { border-right: none; border-bottom: 1px solid var(--stone); }
    .products-grid { grid-template-columns: 1fr; }
    .product-card:first-child { grid-column: span 1; }
    .features-grid { grid-template-columns: 1fr; }
    .material-inner { grid-template-columns: 1fr; }
    .inquiry-inner { grid-template-columns: 1fr; }
    .footer-top { grid-template-columns: 1fr 1fr; gap: 40px; }
    .color-grid { grid-template-columns: repeat(2, 1fr); }
    .showcase .section-header, .showcase-strip { padding: 0 24px; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">Vantello<span>.</span></a>
  <ul class="nav-links">
    <li><a href="#collections">Collections</a></li>
    <li><a href="#features">Why Quartz</a></li>
    <li><a href="#series">Series</a></li>
    <li><a href="#colors">Colours</a></li>
    <li><a href="#inquiry">Contact</a></li>
  </ul>
  <a href="#inquiry" class="nav-cta">Get a Quote</a>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-left">
    <div class="hero-eyebrow">Precision Quartz Engineering</div>
    <h1 class="hero-h1">Designed<br>Beyond<br><em>Utility.</em></h1>
    <p class="hero-desc">Vantello quartz kitchen sinks combine natural stone density with advanced composite technology — delivering surfaces that feel solid, look refined, and perform without compromise.</p>
    <div class="hero-actions">
      <a href="#collections" class="btn-primary">Explore Collections</a>
      <a href="#inquiry" class="btn-ghost">Request a Quote</a>
    </div>
  </div>
  <div class="hero-right">
    <img src="https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=900&q=80" alt="Vantello Quartz Sink in luxury kitchen">
    <div class="hero-badge">
      <div class="hero-badge-num">12+</div>
      <div class="hero-badge-text">Exclusive Series</div>
    </div>
  </div>
</section>

<!-- TRUST BAR -->
<div class="trust-bar">
  <div class="trust-item">
    <div class="trust-icon">
      <svg viewBox="0 0 24 24"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
    </div>
    <div>
      <div class="trust-label">Scratch & Heat Resistant</div>
      <div class="trust-sub">Built for real kitchen conditions</div>
    </div>
  </div>
  <div class="trust-item">
    <div class="trust-icon">
      <svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><path d="M12 8v4l3 3"/></svg>
    </div>
    <div>
      <div class="trust-label">Sound Dampening</div>
      <div class="trust-sub">Natural quartz absorbs vibration</div>
    </div>
  </div>
  <div class="trust-item">
    <div class="trust-icon">
      <svg viewBox="0 0 24 24"><path d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"/></svg>
    </div>
    <div>
      <div class="trust-label">Non-Porous Surface</div>
      <div class="trust-sub">Hygienic, stain-free, effortless clean</div>
    </div>
  </div>
  <div class="trust-item">
    <div class="trust-icon">
      <svg viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
    </div>
    <div>
      <div class="trust-label">Matte Refined Finish</div>
      <div class="trust-sub">Deep colour consistency, timeless look</div>
    </div>
  </div>
</div>

<!-- COLLECTIONS -->
<section class="collections" id="collections">
  <div class="section-header">
    <span class="section-eyebrow">Our Collections</span>
    <h2 class="section-title">Quartz Kitchen <em>Sinks</em></h2>
    <p class="section-sub">Each Vantello sink is engineered from high-density quartz composite — combining natural stone with advanced binding technology for a surface that lasts decades.</p>
  </div>

  <div class="collection-tabs">
    <button class="tab-btn active" onclick="filterProducts('all', this)">All</button>
    <button class="tab-btn" onclick="filterProducts('single', this)">Single Bowl</button>
    <button class="tab-btn" onclick="filterProducts('double', this)">Double Bowl</button>
    <button class="tab-btn" onclick="filterProducts('drainer', this)">With Drainer</button>
  </div>

  <div class="products-grid" id="productGrid">

    <div class="product-card" data-type="single">
      <div class="product-img-wrap">
        <img src="https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=800&q=80" alt="Marvel Series">
        <div class="product-overlay"></div>
      </div>
      <div class="product-info">
        <div class="product-series">Marvel Series</div>
        <div class="product-name">Marvel Black</div>
        <div class="product-size">24 × 18 in · Single Bowl</div>
        <div class="color-dots">
          <div class="dot" style="background:#1a1714" title="Black"></div>
          <div class="dot" style="background:#e0ddd8" title="White"></div>
          <div class="dot" style="background:#8a8780" title="Grey"></div>
          <div class="dot" style="background:#7a3e1e" title="Brown"></div>
        </div>
      </div>
    </div>

    <div class="product-card" data-type="single">
      <div class="product-img-wrap">
        <img src="https://images.unsplash.com/photo-1584622650111-993a426fbf0a?w=600&q=80" alt="Crystal Series">
        <div class="product-overlay"></div>
      </div>
      <div class="product-info">
        <div class="product-series">Crystal Series</div>
        <div class="product-name">Crystal Grey</div>
        <div class="product-size">21 × 18 in · Single Bowl</div>
        <div class="color-dots">
          <div class="dot" style="background:#1a1714" title="Black"></div>
          <div class="dot" style="background:#e0ddd8" title="White"></div>
          <div class="dot" style="background:#8a8780" title="Grey"></div>
          <div class="dot" style="background:#7a3e1e" title="Brown"></div>
        </div>
      </div>
    </div>

    <div class="product-card" data-type="single">
      <div class="product-img-wrap">
        <img src="https://images.unsplash.com/photo-1556909172-54557c7e4fb7?w=600&q=80" alt="Pearl Series">
        <div class="product-overlay"></div>
      </div>
      <div class="product-info">
        <div class="product-series">Pearl Series</div>
        <div class="product-name">Pearl Brown</div>
        <div class="product-size">18 × 16 in · Compact Single</div>
        <div class="color-dots">
          <div class="dot" style="background:#1a1714" title="Black"></div>
          <div class="dot" style="background:#e0ddd8" title="White"></div>
          <div class="dot" style="background:#8a8780" title="Grey"></div>
          <div class="dot" style="background:#7a3e1e" title="Brown"></div>
        </div>
      </div>
    </div>

    <div class="product-card" data-type="drainer">
      <div class="product-img-wrap">
        <img src="https://images.unsplash.com/photo-1556909190-eccf4a8bf97a?w=800&q=80" alt="Imperial Series">
        <div class="product-overlay"></div>
      </div>
      <div class="product-info">
        <div class="product-series">Imperial Series</div>
        <div class="product-name">Imperial White</div>
        <div class="product-size">36 × 18 in · Single + Drainer</div>
        <div class="color-dots">
          <div class="dot" style="background:#1a1714" title="Black"></div>
          <div class="dot" style="background:#e0ddd8" title="White"></div>
          <div class="dot" style="background:#8a8780" title="Grey"></div>
          <div class="dot" style="background:#7a3e1e" title="Brown"></div>
        </div>
      </div>
    </div>

    <div class="product-card" data-type="double">
      <div class="product-img-wrap">
        <img src="https://images.unsplash.com/photo-1556909172-89cf0b43e8c0?w=600&q=80" alt="Royal Series">
        <div class="product-overlay"></div>
      </div>
      <div class="product-info">
        <div class="product-series">Royal Series</div>
        <div class="product-name">Royal White</div>
        <div class="product-size">45 × 20 in · Double Bowl</div>
        <div class="color-dots">
          <div class="dot" style="background:#1a1714" title="Black"></div>
          <div class="dot" style="background:#e0ddd8" title="White"></div>
          <div class="dot" style="background:#8a8780" title="Grey"></div>
          <div class="dot" style="background:#7a3e1e" title="Brown"></div>
        </div>
      </div>
    </div>

    <div class="product-card" data-type="double">
      <div class="product-img-wrap">
        <img src="https://images.unsplash.com/photo-1556911220-bff31c812dba?w=600&q=80" alt="Thar Series">
        <div class="product-overlay"></div>
      </div>
      <div class="product-info">
        <div class="product-series">Thar Series</div>
        <div class="product-name">Thar Almond</div>
        <div class="product-size">40 × 20 in · Double Bowl</div>
        <div class="color-dots">
          <div class="dot" style="background:#c4a882" title="Almond"></div>
          <div class="dot" style="background:#e0ddd8" title="Alaska"></div>
          <div class="dot" style="background:#8a8780" title="Silver"></div>
          <div class="dot" style="background:#d4a0a0" title="Rose"></div>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- WHY QUARTZ -->
<section class="features" id="features">
  <div class="section-header">
    <span class="section-eyebrow">Material Excellence</span>
    <h2 class="section-title">Why <em>Quartz Composite</em></h2>
    <p class="section-sub" style="color:rgba(253,250,247,0.45)">Every Vantello sink is pressed from high-density quartz composite — natural stone fused with advanced resin technology. The result performs where ordinary sinks fail.</p>
  </div>
  <div class="features-grid">
    <div class="feature-card">
      <div class="feature-number">01</div>
      <div class="feature-icon-line"></div>
      <div class="feature-title">Precision Quartz Engineering</div>
      <p class="feature-desc">Combining natural quartz stone with advanced binding technology, the result is a surface that feels solid, looks refined, and performs consistently under daily stress.</p>
    </div>
    <div class="feature-card">
      <div class="feature-number">02</div>
      <div class="feature-icon-line"></div>
      <div class="feature-title">Acoustic Comfort</div>
      <p class="feature-desc">The natural density of quartz absorbs vibrations, significantly reducing the harsh metallic noise common in stainless steel sinks. A calmer, more refined kitchen — every day.</p>
    </div>
    <div class="feature-card">
      <div class="feature-number">03</div>
      <div class="feature-icon-line"></div>
      <div class="feature-title">Thermal Stability</div>
      <p class="feature-desc">Built to handle real kitchen conditions. Vantello sinks maintain their integrity under high temperatures, resisting cracks, warping, and discoloration from hot utensils.</p>
    </div>
    <div class="feature-card">
      <div class="feature-number">04</div>
      <div class="feature-icon-line"></div>
      <div class="feature-title">Hygienic Non-Porous Surface</div>
      <p class="feature-desc">The non-porous structure prevents absorption of liquids, stains, and odors — making cleaning effortless and ensuring a more hygienic kitchen environment, naturally.</p>
    </div>
  </div>
</section>

<!-- SERIES SHOWCASE -->
<section class="showcase" id="series">
  <div class="section-header">
    <span class="section-eyebrow">Complete Series Range</span>
    <h2 class="section-title">Every Kitchen,<br><em>Every Scale</em></h2>
  </div>
  <div class="showcase-strip">
    <div class="showcase-item">
      <img src="https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=400&q=80" alt="Galaxy Series">
      <div class="showcase-item-info">
        <div class="showcase-item-series">Galaxy Series</div>
        <div class="showcase-item-name">Galaxy Grey</div>
        <div class="showcase-item-size">30 × 20 in</div>
      </div>
    </div>
    <div class="showcase-item">
      <img src="https://images.unsplash.com/photo-1584622650111-993a426fbf0a?w=400&q=80" alt="Fusion Series">
      <div class="showcase-item-info">
        <div class="showcase-item-series">Fusion Series</div>
        <div class="showcase-item-name">Fusion White</div>
        <div class="showcase-item-size">31 × 19 in</div>
      </div>
    </div>
    <div class="showcase-item">
      <img src="https://images.unsplash.com/photo-1556909172-54557c7e4fb7?w=400&q=80" alt="Prada Series">
      <div class="showcase-item-info">
        <div class="showcase-item-series">Prada Series</div>
        <div class="showcase-item-name">Prada Silver</div>
        <div class="showcase-item-size">40 × 20 in</div>
      </div>
    </div>
    <div class="showcase-item">
      <img src="https://images.unsplash.com/photo-1556909190-eccf4a8bf97a?w=400&q=80" alt="Fortune Series">
      <div class="showcase-item-info">
        <div class="showcase-item-series">Fortune Series</div>
        <div class="showcase-item-name">Fortune Brown</div>
        <div class="showcase-item-size">36 × 18 in</div>
      </div>
    </div>
    <div class="showcase-item">
      <img src="https://images.unsplash.com/photo-1556909172-89cf0b43e8c0?w=400&q=80" alt="Matrix Series">
      <div class="showcase-item-info">
        <div class="showcase-item-series">Matrix Series</div>
        <div class="showcase-item-name">Matrix Almond</div>
        <div class="showcase-item-size">37 × 18 in</div>
      </div>
    </div>
    <div class="showcase-item">
      <img src="https://images.unsplash.com/photo-1556911220-bff31c812dba?w=400&q=80" alt="Rock Series">
      <div class="showcase-item-info">
        <div class="showcase-item-series">Rock Series</div>
        <div class="showcase-item-name">Rock White</div>
        <div class="showcase-item-size">45 × 20 in</div>
      </div>
    </div>
  </div>
</section>

<!-- MATERIAL STORY -->
<section class="material">
  <div class="material-inner">
    <div class="material-left">
      <img src="https://images.unsplash.com/photo-1565538810643-b5bdb714032a?w=700&q=80" alt="Quartz composite material">
    </div>
    <div class="material-right">
      <span class="section-eyebrow">The Vantello Standard</span>
      <h2 class="section-title">Quiet. Strong.<br><em>Refined.</em></h2>
      <p class="section-sub">Two finish families — Metallic and Granite — each available in eight carefully curated colours. From the deep richness of Marvel Black to the warmth of Pearl Brown, every tone is formulated for lasting depth and consistency.</p>
      <div class="material-stats">
        <div class="stat-box">
          <div class="stat-num">8+</div>
          <div class="stat-label">Colour options per series</div>
        </div>
        <div class="stat-box">
          <div class="stat-num">2</div>
          <div class="stat-label">Finish families — Metallic & Granite</div>
        </div>
        <div class="stat-box">
          <div class="stat-num">12</div>
          <div class="stat-label">Distinct product series</div>
        </div>
        <div class="stat-box">
          <div class="stat-num">∞</div>
          <div class="stat-label">Years of surface consistency</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- COLOUR FAMILIES -->
<section class="colors" id="colors">
  <div class="section-header">
    <span class="section-eyebrow">Colour Families</span>
    <h2 class="section-title">Find Your <em>Perfect Tone</em></h2>
    <p class="section-sub">Vantello sinks are available in two finish families — Metallic and Granite — each with eight colour options engineered for lasting depth and visual consistency.</p>
  </div>
  <div class="color-grid">
    <div class="color-swatch">
      <div class="swatch-bg" style="background:#1a1714;aspect-ratio:1"></div>
      <div class="swatch-label">Black</div>
    </div>
    <div class="color-swatch">
      <div class="swatch-bg" style="background:#e8e5e0;aspect-ratio:1"></div>
      <div class="swatch-label" style="color:#333">White</div>
    </div>
    <div class="color-swatch">
      <div class="swatch-bg" style="background:#8a8780;aspect-ratio:1"></div>
      <div class="swatch-label">Grey</div>
    </div>
    <div class="color-swatch">
      <div class="swatch-bg" style="background:#7a3e1e;aspect-ratio:1"></div>
      <div class="swatch-label">Brown</div>
    </div>
    <div class="color-swatch">
      <div class="swatch-bg" style="background:#d4cfc8;aspect-ratio:1"></div>
      <div class="swatch-label" style="color:#333">Alaska</div>
    </div>
    <div class="color-swatch">
      <div class="swatch-bg" style="background:#b8b5b0;aspect-ratio:1"></div>
      <div class="swatch-label">Silver</div>
    </div>
    <div class="color-swatch">
      <div class="swatch-bg" style="background:#c4a882;aspect-ratio:1"></div>
      <div class="swatch-label" style="color:#333">Almond</div>
    </div>
    <div class="color-swatch">
      <div class="swatch-bg" style="background:#c4929a;aspect-ratio:1"></div>
      <div class="swatch-label">Rose</div>
    </div>
  </div>
</section>

<!-- INQUIRY -->
<section class="inquiry" id="inquiry">
  <div class="inquiry-inner">
    <div class="inquiry-left">
      <span class="section-eyebrow">Get in Touch</span>
      <h2 class="section-title">Engineered for<br><em>Every Kitchen</em></h2>
      <p class="section-sub">Whether you're an architect, interior designer, dealer, or homeowner — we'd love to help you find the right Vantello sink. Reach out and our team will get back to you within 24 hours.</p>
      <div class="contact-items">
        <div class="contact-item">
          <div class="contact-dot"></div>
          <div>
            <div class="contact-label">Website</div>
            <div class="contact-value">www.levistone.in</div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-dot"></div>
          <div>
            <div class="contact-label">For Dealers & Trade</div>
            <div class="contact-value">Wholesale inquiries welcome</div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-dot"></div>
          <div>
            <div class="contact-label">Catalogue</div>
            <div class="contact-value">Full product range available on request</div>
          </div>
        </div>
      </div>
    </div>
    <div class="inquiry-form">
      <div class="form-row">
        <div class="field">
          <label>Full Name</label>
          <input type="text" placeholder="Your name">
        </div>
        <div class="field">
          <label>Phone Number</label>
          <input type="tel" placeholder="+91 00000 00000">
        </div>
      </div>
      <div class="field">
        <label>Email Address</label>
        <input type="email" placeholder="your@email.com">
      </div>
      <div class="field">
        <label>I am a...</label>
        <select>
          <option value="">Select your role</option>
          <option>Homeowner</option>
          <option>Interior Designer</option>
          <option>Architect</option>
          <option>Dealer / Distributor</option>
          <option>Contractor</option>
        </select>
      </div>
      <div class="field">
        <label>Series of Interest</label>
        <select>
          <option value="">Select a series</option>
          <option>Pearl Series — 18×16</option>
          <option>Crystal Series — 21×18</option>
          <option>Marvel Series — 24×18</option>
          <option>Imperial Series — 36×18</option>
          <option>Fortune Series — 36×18</option>
          <option>Fusion Series — 31×19</option>
          <option>Galaxy Series — 30×20</option>
          <option>Matrix Series — 37×18</option>
          <option>Prada Series — 40×20</option>
          <option>Thar Series — 40×20</option>
          <option>Rock Series — 45×20</option>
          <option>Royal Series — 45×20</option>
          <option>Not sure yet</option>
        </select>
      </div>
      <div class="field">
        <label>Message</label>
        <textarea rows="4" placeholder="Tell us about your project or requirements..."></textarea>
      </div>
      <button class="submit-btn" onclick="handleSubmit(event)">Send Inquiry →</button>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-top">
    <div class="footer-brand">
      <span class="footer-logo">Vantello<span>.</span></span>
      <p class="footer-tagline">Precision-engineered quartz kitchen sinks.<br>Built to withstand real use. Designed beyond utility.</p>
    </div>
    <div>
      <div class="footer-col-title">Collections</div>
      <ul class="footer-links">
        <li><a href="#">Pearl Series</a></li>
        <li><a href="#">Crystal Series</a></li>
        <li><a href="#">Marvel Series</a></li>
        <li><a href="#">Imperial Series</a></li>
        <li><a href="#">Royal Series</a></li>
      </ul>
    </div>
    <div>
      <div class="footer-col-title">More Series</div>
      <ul class="footer-links">
        <li><a href="#">Fortune Series</a></li>
        <li><a href="#">Galaxy Series</a></li>
        <li><a href="#">Matrix Series</a></li>
        <li><a href="#">Prada Series</a></li>
        <li><a href="#">Rock Series</a></li>
      </ul>
    </div>
    <div>
      <div class="footer-col-title">Company</div>
      <ul class="footer-links">
        <li><a href="#">About Vantello</a></li>
        <li><a href="#">Why Quartz</a></li>
        <li><a href="#">Dealer Enquiry</a></li>
        <li><a href="#">Download Catalogue</a></li>
        <li><a href="#">Contact Us</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <div class="footer-copy">© 2026 Vantello. All rights reserved.</div>
    <div class="footer-tagline-small">"Quiet. Strong. Refined."</div>
  </div>
</footer>

<script>
  function filterProducts(type, btn) {
    document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
    document.querySelectorAll('.product-card').forEach(card => {
      if (type === 'all' || card.dataset.type === type) {
        card.style.display = '';
      } else {
        card.style.display = 'none';
      }
    });
    const first = document.querySelector('.product-card:not([style*="none"])');
    if (first) {
      const grid = document.getElementById('productGrid');
      const visible = Array.from(grid.querySelectorAll('.product-card')).filter(c => c.style.display !== 'none');
      visible.forEach((c, i) => { c.style.gridColumn = (i === 0 && visible.length > 1) ? 'span 2' : ''; });
    }
  }

  function handleSubmit(e) {
    e.preventDefault();
    const btn = e.target;
    btn.textContent = 'Inquiry Sent ✓';
    btn.style.background = '#2d6a4f';
    setTimeout(() => { btn.textContent = 'Send Inquiry →'; btn.style.background = ''; }, 3000);
  }

  // Scroll reveal
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.style.opacity = '1';
        e.target.style.transform = 'translateY(0)';
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.feature-card, .product-card, .showcase-item, .stat-box').forEach(el => {
    el.style.opacity = '0';
    el.style.transform = 'translateY(24px)';
    el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
    observer.observe(el);
  });
</script>
</body>
</html># project
