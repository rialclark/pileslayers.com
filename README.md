
pileslayers.com
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Pile Slayers — Reseller Listing Service</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg: #0a0a0a;
      --surface: #111111;
      --surface2: #181818;
      --border: #222222;
      --accent: #e8ff47;
      --accent2: #ff6b35;
      --text: #f0f0f0;
      --muted: #888888;
      --radius: 4px;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'DM Sans', sans-serif;
      font-weight: 300;
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* ── NAV ── */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      display: flex; align-items: center; justify-content: space-between;
      padding: 1.25rem 4rem;
      background: rgba(10,10,10,0.85);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border);
    }
    .logo {
      font-family: 'Syne', sans-serif;
      font-weight: 800;
      font-size: 1.25rem;
      letter-spacing: -0.02em;
      color: var(--text);
      text-decoration: none;
    }
    .logo span { color: var(--accent); }
    nav ul { list-style: none; display: flex; gap: 2.5rem; }
    nav ul a {
      color: var(--muted);
      text-decoration: none;
      font-size: 0.875rem;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      transition: color 0.2s;
    }
    nav ul a:hover { color: var(--text); }
    .nav-cta {
      background: var(--accent);
      color: #0a0a0a !important;
      padding: 0.5rem 1.25rem;
      border-radius: var(--radius);
      font-weight: 500 !important;
      text-transform: none !important;
      letter-spacing: 0 !important;
      font-size: 0.875rem !important;
      transition: opacity 0.2s !important;
    }
    .nav-cta:hover { opacity: 0.85 !important; color: #0a0a0a !important; }

    /* ── HERO ── */
    #hero {
      min-height: 100vh;
      display: flex; align-items: center;
      padding: 8rem 4rem 4rem;
      position: relative;
      overflow: hidden;
    }
    .hero-bg {
      position: absolute; inset: 0; z-index: 0;
      background:
        radial-gradient(ellipse 60% 50% at 70% 50%, rgba(232,255,71,0.07) 0%, transparent 70%),
        radial-gradient(ellipse 40% 40% at 20% 80%, rgba(255,107,53,0.05) 0%, transparent 60%);
    }
    .hero-grid {
      position: absolute; inset: 0; z-index: 0;
      background-image:
        linear-gradient(var(--border) 1px, transparent 1px),
        linear-gradient(90deg, var(--border) 1px, transparent 1px);
      background-size: 60px 60px;
      opacity: 0.4;
      mask-image: radial-gradient(ellipse 80% 80% at 50% 50%, black 30%, transparent 100%);
    }
    .hero-inner { position: relative; z-index: 1; max-width: 900px; }
    .hero-tag {
      display: inline-flex; align-items: center; gap: 0.5rem;
      background: rgba(232,255,71,0.1);
      border: 1px solid rgba(232,255,71,0.2);
      color: var(--accent);
      font-size: 0.75rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      padding: 0.35rem 0.85rem;
      border-radius: 999px;
      margin-bottom: 2rem;
      animation: fadeUp 0.6s ease both;
    }
    .hero-tag::before { content: '●'; font-size: 0.5rem; }
    h1 {
      font-family: 'Syne', sans-serif;
      font-weight: 800;
      font-size: clamp(3rem, 7vw, 5.5rem);
      line-height: 1.0;
      letter-spacing: -0.03em;
      margin-bottom: 1.5rem;
      animation: fadeUp 0.6s 0.1s ease both;
    }
    h1 em { font-style: normal; color: var(--accent); }
    .hero-sub {
      font-size: 1.2rem;
      color: var(--muted);
      max-width: 560px;
      line-height: 1.7;
      margin-bottom: 2.5rem;
      animation: fadeUp 0.6s 0.2s ease both;
    }
    .hero-actions {
      display: flex; gap: 1rem; flex-wrap: wrap;
      animation: fadeUp 0.6s 0.3s ease both;
    }
    .btn {
      display: inline-block;
      padding: 0.875rem 2rem;
      border-radius: var(--radius);
      font-size: 0.9375rem;
      font-weight: 500;
      text-decoration: none;
      transition: all 0.2s;
      cursor: pointer;
      border: none;
      font-family: 'DM Sans', sans-serif;
    }
    .btn-primary {
      background: var(--accent);
      color: #0a0a0a;
    }
    .btn-primary:hover { opacity: 0.88; transform: translateY(-1px); }
    .btn-ghost {
      background: transparent;
      color: var(--text);
      border: 1px solid var(--border);
    }
    .btn-ghost:hover { border-color: var(--muted); transform: translateY(-1px); }

    .hero-stats {
      display: flex; gap: 3rem; margin-top: 4rem;
      padding-top: 3rem;
      border-top: 1px solid var(--border);
      animation: fadeUp 0.6s 0.4s ease both;
    }
    .stat-num {
      font-family: 'Syne', sans-serif;
      font-size: 2rem;
      font-weight: 700;
      color: var(--accent);
    }
    .stat-label { font-size: 0.8rem; color: var(--muted); text-transform: uppercase; letter-spacing: 0.05em; margin-top: 0.25rem; }

    /* ── HOW IT WORKS ── */
    #how { padding: 6rem 4rem; }
    .section-label {
      font-size: 0.7rem;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 1rem;
    }
    .section-title {
      font-family: 'Syne', sans-serif;
      font-weight: 700;
      font-size: clamp(1.75rem, 3.5vw, 2.75rem);
      letter-spacing: -0.02em;
      margin-bottom: 3.5rem;
      max-width: 500px;
    }
    .steps {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 0;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      overflow: hidden;
    }
    .step {
      padding: 2.5rem;
      border-right: 1px solid var(--border);
      position: relative;
    }
    .step:last-child { border-right: none; }
    .step-num {
      font-family: 'Syne', sans-serif;
      font-size: 3rem;
      font-weight: 800;
      color: var(--border);
      line-height: 1;
      margin-bottom: 1.25rem;
    }
    .step h3 {
      font-family: 'Syne', sans-serif;
      font-weight: 600;
      font-size: 1rem;
      margin-bottom: 0.75rem;
    }
    .step p { font-size: 0.9rem; color: var(--muted); line-height: 1.7; }
    .step-icon {
      width: 36px; height: 36px;
      background: rgba(232,255,71,0.1);
      border: 1px solid rgba(232,255,71,0.2);
      border-radius: var(--radius);
      display: flex; align-items: center; justify-content: center;
      font-size: 1rem;
      margin-bottom: 1.5rem;
    }

    /* ── SERVICES ── */
    #services { padding: 6rem 4rem; background: var(--surface); }
    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1px;
      background: var(--border);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      overflow: hidden;
    }
    .service-card {
      background: var(--surface);
      padding: 2.5rem;
      transition: background 0.2s;
    }
    .service-card:hover { background: var(--surface2); }
    .service-icon {
      font-size: 1.5rem;
      margin-bottom: 1.25rem;
    }
    .service-card h3 {
      font-family: 'Syne', sans-serif;
      font-weight: 600;
      font-size: 1.05rem;
      margin-bottom: 0.75rem;
    }
    .service-card p { font-size: 0.875rem; color: var(--muted); line-height: 1.7; }
    .service-tag {
      display: inline-block;
      margin-top: 1rem;
      font-size: 0.7rem;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: var(--accent);
      border: 1px solid rgba(232,255,71,0.2);
      padding: 0.2rem 0.6rem;
      border-radius: 999px;
    }

    /* ── PRICING ── */
    #pricing { padding: 6rem 4rem; }

    /* Toggle */
    .pricing-header { text-align: center; margin-bottom: 3rem; }
    .pricing-header .section-label { justify-content: center; display: flex; margin-bottom: 0.75rem; }
    .pricing-header h2 { font-family: 'Syne', sans-serif; font-weight: 700; font-size: clamp(1.75rem, 3.5vw, 2.75rem); letter-spacing: -0.02em; margin-bottom: 1.25rem; }
    .toggle-wrap {
      display: inline-flex;
      align-items: center;
      gap: 0.75rem;
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 999px;
      padding: 0.35rem;
      position: relative;
      margin-bottom: 0.75rem;
    }
    .toggle-btn {
      padding: 0.45rem 1.25rem;
      border-radius: 999px;
      border: none;
      background: transparent;
      color: var(--muted);
      font-family: 'DM Sans', sans-serif;
      font-size: 0.875rem;
      font-weight: 500;
      cursor: pointer;
      transition: color 0.2s;
      position: relative; z-index: 1;
    }
    .toggle-btn.active { color: #0a0a0a; }
    .toggle-slider {
      position: absolute;
      top: 0.35rem; bottom: 0.35rem; left: 0.35rem;
      width: calc(50% - 0.35rem);
      background: var(--accent);
      border-radius: 999px;
      transition: transform 0.25s cubic-bezier(.4,0,.2,1);
    }
    .toggle-slider.yearly { transform: translateX(100%); }
    .save-badge {
      display: inline-flex; align-items: center;
      background: rgba(232,255,71,0.12);
      border: 1px solid rgba(232,255,71,0.25);
      color: var(--accent);
      font-size: 0.72rem;
      font-weight: 600;
      letter-spacing: 0.04em;
      padding: 0.2rem 0.6rem;
      border-radius: 999px;
      margin-left: 0.5rem;
      vertical-align: middle;
    }
    .pricing-trial { font-size: 0.82rem; color: var(--muted); margin-top: 0.4rem; }
    .pricing-trial a { color: var(--accent); text-decoration: none; }

    /* Cards */
    .pricing-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.5rem;
      max-width: 1040px;
      margin: 0 auto;
    }
    .pricing-card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 0;
      position: relative;
      transition: border-color 0.2s, transform 0.2s;
      display: flex; flex-direction: column;
    }
    .pricing-card:hover { border-color: var(--muted); transform: translateY(-3px); }
    .pricing-card.featured { border-color: var(--accent); border-width: 2px; background: linear-gradient(160deg, rgba(232,255,71,0.04) 0%, transparent 60%); }
    .featured-badge {
      position: absolute; top: -13px; left: 50%; transform: translateX(-50%);
      background: var(--accent); color: #0a0a0a;
      font-size: 0.65rem; letter-spacing: 0.1em; text-transform: uppercase;
      font-weight: 700; padding: 0.25rem 0.9rem; border-radius: 999px; white-space: nowrap;
    }

    .card-top { padding: 2rem 2rem 1.5rem; border-bottom: 1px solid var(--border); }
    .plan-icon { font-size: 1.4rem; margin-bottom: 0.75rem; }
    .plan-name { font-family: 'Syne', sans-serif; font-weight: 700; font-size: 1.05rem; margin-bottom: 0.3rem; }
    .plan-desc { font-size: 0.8rem; color: var(--muted); line-height: 1.5; margin-bottom: 1.5rem; }
    .plan-price-wrap { display: flex; align-items: flex-end; gap: 0.2rem; margin-bottom: 0.2rem; }
    .plan-price {
      font-family: 'Syne', sans-serif; font-weight: 800;
      font-size: 3rem; letter-spacing: -0.04em; line-height: 1;
      transition: opacity 0.2s;
    }
    .plan-price sup { font-size: 1.3rem; vertical-align: super; line-height: 0; }
    .plan-price-per { font-size: 0.8rem; color: var(--muted); padding-bottom: 0.35rem; }
    .plan-asterisk { font-size: 0.72rem; color: var(--muted); margin-bottom: 1.25rem; min-height: 1rem; }

    .btn-plan {
      width: 100%; text-align: center; display: block;
      padding: 0.8rem; border-radius: 6px;
      font-size: 0.9rem; font-weight: 500; text-decoration: none;
      transition: all 0.2s; cursor: pointer; border: none;
      font-family: 'DM Sans', sans-serif;
    }
    .btn-plan-ghost { background: transparent; color: var(--text); border: 1px solid var(--border); }
    .btn-plan-ghost:hover { border-color: var(--muted); }
    .btn-plan-primary { background: var(--accent); color: #0a0a0a; }
    .btn-plan-primary:hover { opacity: 0.88; }

    /* Feature groups */
    .card-features { padding: 1.5rem 2rem; flex: 1; }
    .feature-group { margin-bottom: 1.5rem; }
    .feature-group:last-child { margin-bottom: 0; }
    .feature-group-label {
      font-size: 0.7rem; letter-spacing: 0.1em; text-transform: uppercase;
      color: var(--muted); font-weight: 600; margin-bottom: 0.75rem;
      padding-bottom: 0.5rem; border-bottom: 1px solid var(--border);
    }
    .feature-item {
      display: flex; align-items: flex-start; gap: 0.6rem;
      padding: 0.45rem 0;
      font-size: 0.845rem; color: var(--text); line-height: 1.4;
    }
    .feature-item .fi-sub { font-size: 0.75rem; color: var(--muted); display: block; margin-top: 0.1rem; }
    .feature-check { color: var(--accent); font-weight: 700; font-size: 0.8rem; flex-shrink: 0; margin-top: 0.15rem; }
    .feature-x { color: #444; font-size: 0.8rem; flex-shrink: 0; margin-top: 0.15rem; }
    .feature-item.dimmed { opacity: 0.4; }

    .popular-note {
      background: rgba(232,255,71,0.07);
      border: 1px solid rgba(232,255,71,0.15);
      border-radius: 6px;
      padding: 0.6rem 0.85rem;
      font-size: 0.78rem;
      color: var(--accent);
      margin-top: 0.75rem;
      line-height: 1.5;
    }
    .popular-note strong { display: block; }

    @media (max-width: 900px) {
      .pricing-grid { grid-template-columns: 1fr; max-width: 420px; }
    }

    /* ── TESTIMONIALS ── */
    #testimonials { padding: 6rem 4rem; background: var(--surface); }
    .testimonials-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 1.5rem;
    }
    .testimonial {
      background: var(--bg);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 2rem;
      transition: border-color 0.2s;
    }
    .testimonial:hover { border-color: rgba(232,255,71,0.2); }
    .stars { color: var(--accent); font-size: 0.75rem; letter-spacing: 0.1em; margin-bottom: 1rem; }
    .testimonial p {
      font-size: 0.9375rem;
      line-height: 1.75;
      color: var(--text);
      margin-bottom: 1.5rem;
      font-style: italic;
    }
    .testimonial-author { display: flex; align-items: center; gap: 0.75rem; }
    .avatar {
      width: 38px; height: 38px;
      border-radius: 50%;
      background: var(--surface2);
      border: 1px solid var(--border);
      display: flex; align-items: center; justify-content: center;
      font-family: 'Syne', sans-serif;
      font-weight: 700;
      font-size: 0.75rem;
      color: var(--accent);
    }
    .author-name { font-size: 0.875rem; font-weight: 500; }
    .author-role { font-size: 0.75rem; color: var(--muted); }

    /* ── CONTACT ── */
    #contact { padding: 6rem 4rem; }
    .contact-wrap {
      display: grid;
      grid-template-columns: 1fr 1.4fr;
      gap: 5rem;
      align-items: start;
    }
    .contact-info h2 {
      font-family: 'Syne', sans-serif;
      font-weight: 700;
      font-size: clamp(1.75rem, 3vw, 2.5rem);
      letter-spacing: -0.02em;
      margin-bottom: 1rem;
    }
    .contact-info p { color: var(--muted); font-size: 0.9375rem; line-height: 1.7; margin-bottom: 2rem; }
    .contact-detail {
      display: flex; align-items: center; gap: 0.75rem;
      font-size: 0.875rem; color: var(--muted);
      margin-bottom: 0.75rem;
    }
    .contact-detail span:first-child { color: var(--accent); font-size: 1rem; }

    form { display: grid; gap: 1rem; }
    .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
    label { display: block; font-size: 0.75rem; letter-spacing: 0.06em; text-transform: uppercase; color: var(--muted); margin-bottom: 0.4rem; }
    input, textarea, select {
      width: 100%;
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 0.75rem 1rem;
      color: var(--text);
      font-family: 'DM Sans', sans-serif;
      font-size: 0.9rem;
      outline: none;
      transition: border-color 0.2s;
    }
    input:focus, textarea:focus, select:focus { border-color: var(--accent); }
    textarea { resize: vertical; min-height: 130px; }
    select option { background: var(--surface); }
    .form-submit {
      background: var(--accent);
      color: #0a0a0a;
      border: none;
      padding: 0.9rem 2rem;
      border-radius: var(--radius);
      font-size: 0.9375rem;
      font-weight: 500;
      font-family: 'DM Sans', sans-serif;
      cursor: pointer;
      transition: opacity 0.2s, transform 0.2s;
      justify-self: start;
    }
    .form-submit:hover { opacity: 0.88; transform: translateY(-1px); }

    /* ── FOOTER ── */
    footer {
      border-top: 1px solid var(--border);
      padding: 2.5rem 4rem;
      display: flex; align-items: center; justify-content: space-between;
    }
    .footer-logo { font-family: 'Syne', sans-serif; font-weight: 800; font-size: 1rem; }
    .footer-logo span { color: var(--accent); }
    footer p { font-size: 0.8rem; color: var(--muted); }

    /* ── ANIMATIONS ── */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(24px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    .reveal {
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 0.6s ease, transform 0.6s ease;
    }
    .reveal.visible { opacity: 1; transform: none; }

    /* ── RESPONSIVE ── */
    @media (max-width: 768px) {
      nav { padding: 1rem 1.5rem; }
      nav ul { display: none; }
      #hero, #how, #services, #pricing, #testimonials, #contact, footer { padding-left: 1.5rem; padding-right: 1.5rem; }
      .hero-stats { gap: 1.5rem; flex-wrap: wrap; }
      .contact-wrap { grid-template-columns: 1fr; gap: 3rem; }
      .form-row { grid-template-columns: 1fr; }
      .step { border-right: none; border-bottom: 1px solid var(--border); }
      .step:last-child { border-bottom: none; }
      .steps { grid-template-columns: 1fr; }
      footer { flex-direction: column; gap: 0.75rem; text-align: center; }
    }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="logo">Pile<span>Slayers</span></a>
  <ul>
    <li><a href="#how">How It Works</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#pricing">Pricing</a></li>
    <li><a href="#contact" class="nav-cta">Get Started</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-inner">
    <div class="hero-tag">Now accepting new resellers</div>
    <h1>Stop listing.<br>Start <em>selling.</em></h1>
    <p class="hero-sub">You take the photos — we handle everything else. Pile Slayers manages expert VAs that list your resale items across eBay and every platform you need, powered by Nifty.</p>
    <div class="hero-actions">
      <a href="#pricing" class="btn btn-primary">See Pricing</a>
      <a href="#how" class="btn btn-ghost">How It Works</a>
    </div>
    <div class="hero-stats">
      <div>
        <div class="stat-num">48hr</div>
        <div class="stat-label">Avg listing turnaround</div>
      </div>
      <div>
        <div class="stat-num">10+</div>
        <div class="stat-label">Platforms covered</div>
      </div>
      <div>
        <div class="stat-num">100%</div>
        <div class="stat-label">Managed for you</div>
      </div>
    </div>
  </div>
</section>

<!-- HOW IT WORKS -->
<section id="how">
  <p class="section-label reveal">The Process</p>
  <h2 class="section-title reveal">Three steps to a cleared pile</h2>
  <div class="steps reveal">
    <div class="step">
      <div class="step-num">01</div>
      <div class="step-icon">📸</div>
      <h3>You Snap the Photos</h3>
      <p>Photograph your resale items on your own time. No special setup needed — just clear shots from your phone.</p>
    </div>
    <div class="step">
      <div class="step-num">02</div>
      <div class="step-icon">📤</div>
      <h3>Upload via Nifty</h3>
      <p>Drop your photos into Nifty. Our VA team picks them up instantly and gets to work building your listings.</p>
    </div>
    <div class="step">
      <div class="step-num">03</div>
      <div class="step-icon">🚀</div>
      <h3>We List. You Profit.</h3>
      <p>Your items go live on eBay and every other platform relevant to your inventory — optimized and ready to sell.</p>
    </div>
    <div class="step">
      <div class="step-num">04</div>
      <div class="step-icon">📊</div>
      <h3>Track Everything</h3>
      <p>Monitor all your active listings and sales in one place through Nifty. Full visibility, zero extra work.</p>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services">
  <p class="section-label reveal">What We Handle</p>
  <h2 class="section-title reveal">Every part of listing, done for you</h2>
  <div class="services-grid reveal">
    <div class="service-card">
      <div class="service-icon">✍️</div>
      <h3>Listing Copywriting</h3>
      <p>Our VAs write SEO-optimized titles, detailed descriptions, and accurate condition notes for every single item.</p>
      <span class="service-tag">Included</span>
    </div>
    <div class="service-card">
      <div class="service-icon">🏷️</div>
      <h3>Category & Pricing Research</h3>
      <p>We research comps, identify the right categories, and price your items competitively to maximize sell-through.</p>
      <span class="service-tag">Included</span>
    </div>
    <div class="service-card">
      <div class="service-icon">🌐</div>
      <h3>Multi-Platform Publishing</h3>
      <p>Listings go live on eBay and all relevant resale platforms — simultaneously, not one at a time.</p>
      <span class="service-tag">Included</span>
    </div>
    <div class="service-card">
      <div class="service-icon">🔄</div>
      <h3>Nifty Workflow Management</h3>
      <p>All communication and task tracking happens inside Nifty so nothing falls through the cracks.</p>
      <span class="service-tag">Included</span>
    </div>
    <div class="service-card">
      <div class="service-icon">📦</div>
      <h3>Inventory Organization</h3>
      <p>We keep your active, sold, and pending inventory neatly tracked so you always know where things stand.</p>
      <span class="service-tag">Included</span>
    </div>
    <div class="service-card">
      <div class="service-icon">💬</div>
      <h3>Buyer Q&A Support</h3>
      <p>Our team handles buyer questions on your listings so you never have to monitor your inbox.</p>
      <span class="service-tag">Pro & Up</span>
    </div>
  </div>
</section>

<!-- PRICING -->
<section id="pricing">
  <div class="pricing-header reveal">
    <p class="section-label">Pricing</p>
    <h2>Ready to clear your pile?</h2>
    <div style="margin-bottom:0.5rem;">
      <div class="toggle-wrap">
        <div class="toggle-slider" id="toggleSlider"></div>
        <button class="toggle-btn active" id="btnMonthly" onclick="setBilling('monthly')">Monthly</button>
        <button class="toggle-btn" id="btnYearly" onclick="setBilling('yearly')">Yearly <span class="save-badge">Save 12%</span></button>
      </div>
    </div>
    <p class="pricing-trial">Start with a <a href="#contact">7-day free trial</a> — no credit card required</p>
  </div>

  <div class="pricing-grid reveal">

    <!-- STARTER -->
    <div class="pricing-card">
      <div class="card-top">
        <div class="plan-icon">📦</div>
        <div class="plan-name">Starter</div>
        <div class="plan-desc">Perfect for resellers just getting started with managed listing.</div>
        <div class="plan-price-wrap">
          <div class="plan-price"><sup>$</sup><span class="price-val" data-monthly="149" data-yearly="131">149</span></div>
          <div class="plan-price-per">/ month</div>
        </div>
        <div class="plan-asterisk price-note" data-monthly="Billed monthly" data-yearly="Billed $1,572 annually">Billed monthly</div>
        <a href="#contact" class="btn-plan btn-plan-ghost">Get Started →</a>
      </div>
      <div class="card-features">
        <div class="feature-group">
          <div class="feature-group-label">Starter ($149/mo)</div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Up to <strong>50 listings</strong> per month</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>eBay + 2 platforms<span class="fi-sub">Poshmark, Mercari, Depop — you pick</span></span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Nifty workflow access<span class="fi-sub">Drop photos, we handle the rest</span></span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>48-hour listing turnaround</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>SEO-optimized titles & descriptions</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Competitive pricing research</span></div>
          <div class="feature-item dimmed"><span class="feature-x">✕</span><span>Buyer Q&A management</span></div>
          <div class="feature-item dimmed"><span class="feature-x">✕</span><span>Priority VA team</span></div>
          <div class="feature-item dimmed"><span class="feature-x">✕</span><span>Inventory sync & auto-delist</span></div>
        </div>
      </div>
    </div>

    <!-- GROWTH (Featured) -->
    <div class="pricing-card featured">
      <div class="featured-badge">Most Popular</div>
      <div class="card-top">
        <div class="plan-icon">🚀</div>
        <div class="plan-name">Growth</div>
        <div class="plan-desc">For active resellers moving real volume across all platforms.</div>
        <div class="plan-price-wrap">
          <div class="plan-price"><sup>$</sup><span class="price-val" data-monthly="299" data-yearly="263">299</span></div>
          <div class="plan-price-per">/ month</div>
        </div>
        <div class="plan-asterisk price-note" data-monthly="Billed monthly" data-yearly="Billed $3,156 annually">Billed monthly</div>
        <a href="#contact" class="btn-plan btn-plan-primary">Get Started →</a>
        <div class="popular-note">
          <strong>⚡ Best value</strong>
          Get full multi-platform coverage + buyer Q&A for less than hiring a part-time VA.
        </div>
      </div>
      <div class="card-features">
        <div class="feature-group">
          <div class="feature-group-label">Growth ($299/mo)</div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Up to <strong>150 listings</strong> per month</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>eBay + <strong>all platforms</strong><span class="fi-sub">Poshmark, Mercari, Depop, Facebook, Etsy & more</span></span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Nifty workflow access</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>24-hour listing turnaround</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>SEO-optimized titles & descriptions</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Competitive pricing research</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Buyer Q&A management<span class="fi-sub">We respond to buyer messages for you</span></span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Inventory sync & auto-delist when sold</span></div>
          <div class="feature-item dimmed"><span class="feature-x">✕</span><span>Priority VA team</span></div>
          <div class="feature-item dimmed"><span class="feature-x">✕</span><span>Dedicated account manager</span></div>
        </div>
      </div>
    </div>

    <!-- SCALE -->
    <div class="pricing-card">
      <div class="card-top">
        <div class="plan-icon">⚡</div>
        <div class="plan-name">Scale</div>
        <div class="plan-desc">High-volume resellers who need maximum throughput and white-glove support.</div>
        <div class="plan-price-wrap">
          <div class="plan-price"><sup>$</sup><span class="price-val" data-monthly="549" data-yearly="483">549</span></div>
          <div class="plan-price-per">/ month</div>
        </div>
        <div class="plan-asterisk price-note" data-monthly="Billed monthly" data-yearly="Billed $5,796 annually">Billed monthly</div>
        <a href="#contact" class="btn-plan btn-plan-ghost">Get Started →</a>
      </div>
      <div class="card-features">
        <div class="feature-group">
          <div class="feature-group-label">Scale ($549/mo)</div>
          <div class="feature-item"><span class="feature-check">✓</span><span><strong>Unlimited listings</strong> per month</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>eBay + <strong>all platforms</strong></span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Nifty workflow access</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Same-day turnaround</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>SEO-optimized titles & descriptions</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Competitive pricing research</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Buyer Q&A management</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Inventory sync & auto-delist when sold</span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Priority VA team<span class="fi-sub">Your listings jump the queue</span></span></div>
          <div class="feature-item"><span class="feature-check">✓</span><span>Dedicated account manager<span class="fi-sub">Direct line, weekly check-ins</span></span></div>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- TESTIMONIALS -->
<section id="testimonials">
  <p class="section-label reveal">Social Proof</p>
  <h2 class="section-title reveal">Resellers love clearing their piles</h2>
  <div class="testimonials-grid reveal">
    <div class="testimonial">
      <div class="stars">★★★★★</div>
      <p>"I was drowning in unlisted inventory. Pile Slayers had my whole backlog live on eBay within a week. I've already made back 3× my monthly fee."</p>
      <div class="testimonial-author">
        <div class="avatar">MR</div>
        <div>
          <div class="author-name">Marcus R.</div>
          <div class="author-role">Electronics reseller, FL</div>
        </div>
      </div>
    </div>
    <div class="testimonial">
      <div class="stars">★★★★★</div>
      <p>"The Nifty workflow is seamless. I drop my photos in at night and wake up to listings ready to go. It genuinely changed how I run my reselling business."</p>
      <div class="testimonial-author">
        <div class="avatar">JT</div>
        <div>
          <div class="author-name">Jamie T.</div>
          <div class="author-role">Thrift reseller, TX</div>
        </div>
      </div>
    </div>
    <div class="testimonial">
      <div class="stars">★★★★★</div>
      <p>"I thought I'd have to train a VA myself. Pile Slayers handles everything — the listings look professional and my sell-through rate is way up."</p>
      <div class="testimonial-author">
        <div class="avatar">SL</div>
        <div>
          <div class="author-name">Sandra L.</div>
          <div class="author-role">Vintage clothing seller, CA</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="contact-wrap">
    <div class="contact-info reveal">
      <p class="section-label">Contact</p>
      <h2>Ready to slay your pile?</h2>
      <p>Tell us a bit about your inventory and current volume. We'll get back to you within 24 hours to get you set up.</p>
      <div class="contact-detail"><span>✉</span><span>hello@pileslayers.com</span></div>
      <div class="contact-detail"><span>⚡</span><span>Managed through Nifty</span></div>
    </div>
    <form class="reveal" onsubmit="handleSubmit(event)">
      <div class="form-row">
        <div>
          <label for="name">Your Name</label>
          <input type="text" id="name" placeholder="Jane Smith" required />
        </div>
        <div>
          <label for="email">Email</label>
          <input type="email" id="email" placeholder="jane@email.com" required />
        </div>
      </div>
      <div>
        <label for="plan">Interested Plan</label>
        <select id="plan">
          <option value="">Select a plan…</option>
          <option>Starter — $99/mo</option>
          <option>Pro — $249/mo</option>
          <option>Scale — $499/mo</option>
          <option>Not sure yet</option>
        </select>
      </div>
      <div>
        <label for="volume">Monthly Listing Volume (approx.)</label>
        <input type="text" id="volume" placeholder="e.g. 50–100 items" />
      </div>
      <div>
        <label for="message">Tell us about your inventory</label>
        <textarea id="message" placeholder="What do you sell? Where are you currently listing?"></textarea>
      </div>
      <button type="submit" class="form-submit">Send Message →</button>
    </form>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Pile<span>Slayers</span></div>
  <p>© 2025 Pile Slayers. All rights reserved.</p>
  <p style="font-size:0.75rem;color:var(--muted)">Powered by Nifty</p>
</footer>

<script>
  // Scroll reveal
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); } });
  }, { threshold: 0.1 });
  document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

  // Billing toggle
  function setBilling(mode) {
    const isYearly = mode === 'yearly';
    document.getElementById('toggleSlider').classList.toggle('yearly', isYearly);
    document.getElementById('btnMonthly').classList.toggle('active', !isYearly);
    document.getElementById('btnYearly').classList.toggle('active', isYearly);

    document.querySelectorAll('.price-val').forEach(el => {
      const val = isYearly ? el.dataset.yearly : el.dataset.monthly;
      el.textContent = val;
    });
    document.querySelectorAll('.price-note').forEach(el => {
      el.textContent = isYearly ? el.dataset.yearly : el.dataset.monthly;
    });
  }

  // Form submit
  function handleSubmit(e) {
    e.preventDefault();
    const btn = e.target.querySelector('.form-submit');
    btn.textContent = 'Sent! We\'ll be in touch ✓';
    btn.style.background = '#333';
    btn.style.color = 'var(--accent)';
    btn.disabled = true;
  }
</script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Real Client Results — Pile Slayers</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&display=swap" rel="stylesheet" />
  <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.js"></script>
  <style>
    :root {
      --bg: #f5f7fa;
      --white: #ffffff;
      --blue: #4285F4;
      --red: #EA4335;
      --yellow: #FBBC04;
      --green: #34A853;
      --purple: #9B59B6;
      --teal: #00ACC1;
      --text: #202124;
      --muted: #5F6368;
      --border: #E8EAED;
      --shadow: 0 2px 12px rgba(0,0,0,0.08), 0 1px 3px rgba(0,0,0,0.05);
      --shadow-hover: 0 8px 24px rgba(0,0,0,0.12), 0 2px 6px rgba(0,0,0,0.06);
      --radius: 20px;
      --radius-sm: 12px;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body { background: var(--bg); color: var(--text); font-family: 'Nunito', sans-serif; font-weight: 400; line-height: 1.6; min-height: 100vh; }

    /* ── NAV ── */
    nav {
      background: var(--white);
      border-bottom: 2px solid var(--border);
      display: flex; align-items: center; justify-content: space-between;
      padding: 1rem 2.5rem;
    }
    .logo { font-weight: 900; font-size: 1.2rem; text-decoration: none; color: var(--text); letter-spacing: -0.01em; }
    .logo .s1 { color: var(--blue); }
    .logo .s2 { color: var(--red); }
    .logo .s3 { color: var(--yellow); }
    .logo .s4 { color: var(--green); }
    .nav-back {
      font-size: 0.82rem; font-weight: 700; color: var(--muted);
      text-decoration: none; display: flex; align-items: center; gap: 0.35rem;
      background: var(--bg); border: 2px solid var(--border); border-radius: 999px;
      padding: 0.35rem 0.9rem; transition: border-color 0.2s;
    }
    .nav-back:hover { border-color: var(--blue); color: var(--blue); }

    /* ── GATE ── */
    #gate { max-width: 780px; margin: 0 auto; padding: 3.5rem 1.5rem 2rem; }

    .gate-eyebrow {
      display: inline-flex; align-items: center; gap: 0.5rem;
      background: #E8F0FE; color: var(--blue);
      font-size: 0.75rem; font-weight: 800; letter-spacing: 0.06em; text-transform: uppercase;
      padding: 0.35rem 0.85rem; border-radius: 999px; margin-bottom: 1.25rem;
    }
    .gate-eyebrow::before { content: '📊'; font-size: 0.85rem; }

    .gate-title {
      font-weight: 900; font-size: clamp(2rem, 5.5vw, 3.5rem);
      letter-spacing: -0.02em; line-height: 1.1; margin-bottom: 1rem; color: var(--text);
    }
    .gate-title .word-self { color: var(--red); }
    .gate-title .word-ps { color: var(--green); }
    .gate-sub { color: var(--muted); font-size: 1.05rem; max-width: 520px; line-height: 1.65; margin-bottom: 2.5rem; font-weight: 600; }

    /* Teaser split */
    .teaser-split {
      display: grid; grid-template-columns: 1fr auto 1fr;
      gap: 0; margin-bottom: 1.5rem; border-radius: var(--radius); overflow: hidden;
      box-shadow: var(--shadow);
    }
    .teaser-half { padding: 1.75rem 1.5rem; background: var(--white); }
    .teaser-half.t-before { border-top: 5px solid var(--red); }
    .teaser-half.t-after  { border-top: 5px solid var(--green); background: #F6FEF9; }
    .teaser-chip {
      display: inline-block; font-size: 0.68rem; font-weight: 800; letter-spacing: 0.07em;
      text-transform: uppercase; padding: 0.2rem 0.65rem; border-radius: 999px; margin-bottom: 0.6rem;
    }
    .chip-red   { background: #FDECEA; color: var(--red); }
    .chip-green { background: #E6F4EA; color: var(--green); }
    .teaser-month { font-weight: 800; font-size: 0.95rem; color: var(--muted); margin-bottom: 0.4rem; }
    .teaser-val { font-weight: 900; font-size: 2rem; letter-spacing: -0.03em; filter: blur(9px); user-select: none; }
    .teaser-sub { font-size: 0.75rem; color: var(--muted); filter: blur(6px); user-select: none; margin-top: 0.15rem; }
    .teaser-arrow {
      background: var(--text); display: flex; align-items: center; justify-content: center;
      padding: 0 1rem; color: var(--yellow); font-size: 1.5rem; font-weight: 900;
    }

    /* Blurred preview chart */
    .preview-chart-wrap {
      background: var(--white); border-radius: var(--radius); box-shadow: var(--shadow);
      padding: 1.5rem; margin-bottom: 1.5rem; position: relative; overflow: hidden;
    }
    .preview-chart-label { font-size: 0.8rem; font-weight: 700; color: var(--muted); margin-bottom: 0.75rem; }
    .preview-chart-blur { filter: blur(5px); pointer-events: none; }
    .preview-chart-overlay {
      position: absolute; inset: 0; display: flex; align-items: center; justify-content: center;
      background: rgba(255,255,255,0.55); backdrop-filter: blur(2px);
    }
    .lock-badge {
      display: flex; align-items: center; gap: 0.5rem;
      background: var(--text); color: #fff; border-radius: 999px;
      padding: 0.55rem 1.2rem; font-size: 0.82rem; font-weight: 700;
      box-shadow: var(--shadow);
    }

    /* Gate form */
    .gate-form-wrap {
      background: var(--white); border-radius: var(--radius); box-shadow: var(--shadow);
      padding: 2rem 2rem; border-top: 5px solid var(--blue);
    }
    .gate-form-title { font-weight: 900; font-size: 1.15rem; margin-bottom: 0.3rem; color: var(--text); }
    .gate-form-sub   { font-size: 0.88rem; color: var(--muted); font-weight: 600; margin-bottom: 1.5rem; }
    .gate-form { display: grid; grid-template-columns: 1fr 1fr auto; gap: 0.75rem; align-items: end; }
    label { display: block; font-size: 0.72rem; font-weight: 800; letter-spacing: 0.06em; text-transform: uppercase; color: var(--muted); margin-bottom: 0.35rem; }
    input[type="text"], input[type="email"] {
      width: 100%; background: var(--bg); border: 2px solid var(--border); border-radius: var(--radius-sm);
      padding: 0.7rem 1rem; color: var(--text); font-family: 'Nunito', sans-serif;
      font-size: 0.95rem; font-weight: 600; outline: none; transition: border-color 0.2s;
    }
    input:focus { border-color: var(--blue); }
    .btn-unlock {
      background: var(--blue); color: #fff; border: none;
      padding: 0.75rem 1.5rem; border-radius: var(--radius-sm); font-size: 0.95rem;
      font-weight: 800; font-family: 'Nunito', sans-serif; cursor: pointer;
      white-space: nowrap; transition: transform 0.15s, box-shadow 0.15s; height: 44px;
      box-shadow: 0 4px 12px rgba(66,133,244,0.35);
    }
    .btn-unlock:hover { transform: translateY(-2px); box-shadow: 0 6px 18px rgba(66,133,244,0.45); }
    .form-fine { font-size: 0.72rem; color: var(--muted); margin-top: 0.75rem; font-weight: 600; }

    /* ── DASHBOARD ── */
    #dashboard { display: none; opacity: 0; padding: 2rem 1.5rem 4rem; max-width: 1100px; margin: 0 auto; transition: opacity 0.5s ease; }
    #dashboard.faded { opacity: 1; }

    /* Before/After banner */
    .ba-banner {
      display: grid; grid-template-columns: 1fr auto 1fr;
      border-radius: var(--radius); overflow: hidden; box-shadow: var(--shadow); margin-bottom: 1.5rem;
    }
    .ba-side { padding: 2rem; }
    .ba-side.before { background: #FDECEA; border-top: 6px solid var(--red); }
    .ba-side.after  { background: #E6F4EA; border-top: 6px solid var(--green); }
    .ba-divider {
      background: var(--text); display: flex; flex-direction: column;
      align-items: center; justify-content: center; padding: 0 1.25rem; gap: 0.5rem;
    }
    .ba-divider-arrow { color: var(--yellow); font-size: 1.6rem; font-weight: 900; }
    .ba-divider-label { font-size: 0.58rem; letter-spacing: 0.12em; text-transform: uppercase; color: #aaa; writing-mode: vertical-rl; }
    .ba-chip { display: inline-block; font-size: 0.65rem; font-weight: 800; letter-spacing: 0.08em; text-transform: uppercase; padding: 0.2rem 0.65rem; border-radius: 999px; margin-bottom: 0.6rem; }
    .ba-month { font-weight: 900; font-size: 0.95rem; margin-bottom: 1rem; }
    .ba-stats { display: flex; gap: 1.5rem; flex-wrap: wrap; }
    .ba-stat-val { font-weight: 900; font-size: 1.7rem; letter-spacing: -0.02em; line-height: 1; }
    .ba-stat-sub { font-size: 0.7rem; font-weight: 700; color: var(--muted); margin-top: 0.15rem; }
    .before .ba-stat-val { color: var(--red); }
    .after .ba-stat-val  { color: var(--green); }
    .before .ba-month { color: #C5221F; }
    .after .ba-month  { color: #137333; }

    /* Callout stats */
    .callout-row {
      display: grid; grid-template-columns: repeat(4, 1fr); gap: 1rem; margin-bottom: 1.5rem;
    }
    .callout-card {
      background: var(--white); border-radius: var(--radius); box-shadow: var(--shadow);
      padding: 1.25rem 1.5rem; border-top: 5px solid var(--border);
      transition: transform 0.2s, box-shadow 0.2s;
    }
    .callout-card:hover { transform: translateY(-3px); box-shadow: var(--shadow-hover); }
    .callout-card.c-blue   { border-top-color: var(--blue); }
    .callout-card.c-green  { border-top-color: var(--green); }
    .callout-card.c-yellow { border-top-color: var(--yellow); }
    .callout-card.c-purple { border-top-color: var(--purple); }
    .callout-label { font-size: 0.65rem; font-weight: 800; letter-spacing: 0.08em; text-transform: uppercase; color: var(--muted); margin-bottom: 0.5rem; }
    .callout-val { font-weight: 900; font-size: 2rem; letter-spacing: -0.02em; line-height: 1; }
    .c-blue   .callout-val { color: var(--blue); }
    .c-green  .callout-val { color: var(--green); }
    .c-yellow .callout-val { color: #B06000; }
    .c-purple .callout-val { color: var(--purple); }
    .callout-sub { font-size: 0.72rem; font-weight: 600; color: var(--muted); margin-top: 0.3rem; }

    /* Monthly cards */
    .monthly-bars { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1rem; margin-bottom: 1.5rem; }
    .month-card {
      background: var(--white); border-radius: var(--radius); box-shadow: var(--shadow);
      padding: 1.5rem; border-top: 6px solid var(--border);
      transition: transform 0.2s, box-shadow 0.2s;
    }
    .month-card:hover { transform: translateY(-3px); box-shadow: var(--shadow-hover); }
    .month-card.m-before { border-top-color: var(--red); }
    .month-card.m-ps1    { border-top-color: var(--blue); }
    .month-card.m-ps2    { border-top-color: var(--green); }
    .month-chip { display: inline-block; font-size: 0.62rem; font-weight: 800; letter-spacing: 0.08em; text-transform: uppercase; padding: 0.2rem 0.6rem; border-radius: 999px; margin-bottom: 0.6rem; }
    .chip-before { background: #FDECEA; color: var(--red); }
    .chip-ps1    { background: #E8F0FE; color: var(--blue); }
    .chip-ps2    { background: #E6F4EA; color: var(--green); }
    .month-name  { font-weight: 900; font-size: 1.05rem; margin-bottom: 0.1rem; }
    .month-revenue { font-weight: 900; font-size: 2.1rem; letter-spacing: -0.03em; margin: 0.4rem 0 0.1rem; }
    .m-before .month-revenue { color: var(--red); }
    .m-ps1    .month-revenue { color: var(--blue); }
    .m-ps2    .month-revenue { color: var(--green); }
    .month-profit { font-size: 0.8rem; font-weight: 700; color: var(--muted); margin-bottom: 1rem; }
    .month-pills { display: flex; flex-wrap: wrap; gap: 0.5rem; }
    .month-pill { font-size: 0.72rem; font-weight: 700; background: var(--bg); border-radius: 999px; padding: 0.2rem 0.65rem; color: var(--muted); border: 2px solid var(--border); }

    /* Chart row */
    .charts-row { display: grid; grid-template-columns: 1.6fr 1fr; gap: 1rem; margin-bottom: 1rem; }
    .chart-card {
      background: var(--white); border-radius: var(--radius); box-shadow: var(--shadow);
      padding: 1.5rem;
    }
    .chart-title { font-weight: 900; font-size: 0.95rem; margin-bottom: 0.2rem; }
    .chart-sub   { font-size: 0.75rem; font-weight: 600; color: var(--muted); margin-bottom: 1rem; }

    /* Bottom row */
    .bottom-row { display: grid; grid-template-columns: 1fr 1.2fr 1fr; gap: 1rem; margin-bottom: 1rem; }

    .brands-list { margin-top: 0.25rem; }
    .brand-row { display: flex; align-items: center; gap: 0.75rem; margin-bottom: 0.7rem; }
    .brand-name { font-size: 0.8rem; font-weight: 700; color: var(--muted); width: 90px; text-align: right; flex-shrink: 0; }
    .brand-bar-wrap { flex: 1; background: var(--bg); border-radius: 999px; height: 10px; overflow: hidden; border: 2px solid var(--border); }
    .brand-bar { height: 100%; border-radius: 999px; transition: width 1s cubic-bezier(.4,0,.2,1); }
    .brand-count { font-size: 0.8rem; font-weight: 800; width: 28px; }

    .treemap { display: grid; grid-template-rows: 1fr 1fr; gap: 6px; height: 175px; margin-top: 0.5rem; }
    .treemap-row { display: flex; gap: 6px; }
    .treemap-cell { border-radius: 12px; display: flex; align-items: center; justify-content: center; font-size: 0.75rem; font-weight: 800; text-align: center; padding: 0.5rem; line-height: 1.3; flex: var(--flex,1); }

    .avg-legend { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-bottom: 0.75rem; }
    .avg-dot    { display: flex; align-items: center; gap: 0.35rem; font-size: 0.7rem; font-weight: 700; color: var(--muted); }
    .avg-dot-circle { width: 9px; height: 9px; border-radius: 50%; flex-shrink: 0; }
    .avg-row { margin-bottom: 1.1rem; }
    .avg-row-label { font-size: 0.72rem; font-weight: 700; color: var(--muted); margin-bottom: 0.15rem; }
    .avg-row-val   { font-weight: 900; font-size: 1.05rem; margin-bottom: 0.4rem; color: var(--text); }
    .avg-dots-row  { display: flex; align-items: center; height: 14px; position: relative; background: var(--bg); border-radius: 999px; border: 2px solid var(--border); }
    .avg-dot-marker { width: 12px; height: 12px; border-radius: 50%; position: absolute; transform: translateX(-50%); border: 2px solid white; box-shadow: 0 1px 3px rgba(0,0,0,0.2); }

    /* Legend row */
    .legend-row { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 0.75rem; }
    .legend-pill { display: flex; align-items: center; gap: 5px; font-size: 11px; font-weight: 700; color: var(--muted); }
    .legend-sq   { width: 10px; height: 10px; border-radius: 3px; display: inline-block; flex-shrink: 0; }

    /* CTA */
    .download-bar {
      background: var(--blue); border-radius: var(--radius); padding: 1.75rem 2rem;
      display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 1rem;
      box-shadow: 0 8px 24px rgba(66,133,244,0.3);
    }
    .download-bar h3 { font-weight: 900; font-size: 1.1rem; color: #fff; margin-bottom: 0.25rem; }
    .download-bar p  { font-size: 0.85rem; font-weight: 600; color: rgba(255,255,255,0.75); }
    .btn-cta {
      background: var(--yellow); color: var(--text); border: none;
      padding: 0.85rem 1.75rem; border-radius: var(--radius-sm); font-size: 0.95rem;
      font-weight: 900; font-family: 'Nunito', sans-serif; cursor: pointer;
      white-space: nowrap; text-decoration: none; display: inline-block;
      transition: transform 0.15s, box-shadow 0.15s;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
    }
    .btn-cta:hover { transform: translateY(-2px); box-shadow: 0 6px 18px rgba(0,0,0,0.25); }

    @media(max-width:768px){
      nav { padding: 1rem 1.25rem; }
      #gate { padding: 2rem 1rem 1rem; }
      .gate-form-wrap { padding: 1.25rem; }
      .gate-form { grid-template-columns: 1fr; }
      .teaser-split { grid-template-columns: 1fr; }
      .teaser-arrow { padding: 0.75rem; font-size: 1.2rem; writing-mode: horizontal-tb; }
      .ba-banner { grid-template-columns: 1fr; }
      .ba-divider { flex-direction: row; padding: 0.75rem; writing-mode: horizontal-tb; }
      .ba-divider-label { writing-mode: horizontal-tb; }
      .callout-row { grid-template-columns: 1fr 1fr; }
      .monthly-bars, .charts-row, .bottom-row { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

<nav>
  <a href="index.html" class="logo">
    <span class="s1">P</span><span class="s2">i</span><span class="s3">l</span><span class="s4">e</span>&nbsp;Slayers
  </a>
  <a href="index.html" class="nav-back">← Back to site</a>
</nav>

<!-- ═══ GATE ═══ -->
<section id="gate">
  <div class="gate-eyebrow">Real client data · 3-month case study</div>
  <h1 class="gate-title">
    What happens when you stop<br>
    doing it <span class="word-self">yourself</span> and let<br>
    <span class="word-ps">Pile Slayers</span> take over?
  </h1>
  <p class="gate-sub">This client listed on their own in March using Nifty. They handed it off to us in April. The numbers tell the whole story — enter your email to see them.</p>

  <!-- Teaser -->
  <div class="teaser-split">
    <div class="teaser-half t-before">
      <div class="teaser-chip chip-red">Before · March</div>
      <div class="teaser-month">Self-managed on Nifty</div>
      <div class="teaser-val" style="color:var(--red)">$1,044</div>
      <div class="teaser-sub">186 items listed · 36 sold</div>
    </div>
    <div class="teaser-arrow">→</div>
    <div class="teaser-half t-after">
      <div class="teaser-chip chip-green">After · Apr + May</div>
      <div class="teaser-month">Managed by Pile Slayers</div>
      <div class="teaser-val" style="color:var(--green)">$14,216</div>
      <div class="teaser-sub">1,220 items listed · 373 sold</div>
    </div>
  </div>

  <!-- Blurred chart -->
  <div class="preview-chart-wrap">
    <div class="preview-chart-label">📈 Weekly revenue — March through May</div>
    <div class="preview-chart-blur">
      <canvas id="previewChart" height="110" role="img" aria-label="Blurred revenue chart preview">Enter email to view.</canvas>
    </div>
    <div class="preview-chart-overlay">
      <div class="lock-badge">🔒 Enter your email to unlock the full breakdown</div>
    </div>
  </div>

  <!-- Form -->
  <div class="gate-form-wrap">
    <div class="gate-form-title">Get the full 3-month breakdown — it's free 🎉</div>
    <div class="gate-form-sub">Every platform. Every week. Real numbers, before and after Pile Slayers.</div>
    <form class="gate-form" id="gateForm" onsubmit="unlockDashboard(event)">
      <div>
        <label for="gname">First Name</label>
        <input type="text" id="gname" placeholder="Jane" required />
      </div>
      <div>
        <label for="gemail">Email Address</label>
        <input type="email" id="gemail" placeholder="jane@email.com" required />
      </div>
      <button type="submit" class="btn-unlock">See Results →</button>
    </form>
    <p class="form-fine">🔒 No spam, ever. Unsubscribe any time.</p>
  </div>
</section>

<!-- ═══ DASHBOARD ═══ -->
<div id="dashboard">

  <!-- Before / After -->
  <div class="ba-banner">
    <div class="ba-side before">
      <div class="ba-chip chip-red">Before Pile Slayers</div>
      <div class="ba-month">March — Self-Managed on Nifty</div>
      <div class="ba-stats">
        <div><div class="ba-stat-val">$1,044</div><div class="ba-stat-sub">Revenue</div></div>
        <div><div class="ba-stat-val">186</div><div class="ba-stat-sub">Listed</div></div>
        <div><div class="ba-stat-val">36</div><div class="ba-stat-sub">Sold</div></div>
        <div><div class="ba-stat-val">19.4%</div><div class="ba-stat-sub">Sell-through</div></div>
      </div>
    </div>
    <div class="ba-divider">
      <div class="ba-divider-arrow">→</div>
      <div class="ba-divider-label">Pile Slayers starts</div>
    </div>
    <div class="ba-side after">
      <div class="ba-chip chip-green">After Pile Slayers (Apr + May)</div>
      <div class="ba-month">April & May — Managed by Pile Slayers</div>
      <div class="ba-stats">
        <div><div class="ba-stat-val">$14,216</div><div class="ba-stat-sub">Revenue</div></div>
        <div><div class="ba-stat-val">1,220</div><div class="ba-stat-sub">Listed</div></div>
        <div><div class="ba-stat-val">373</div><div class="ba-stat-sub">Sold</div></div>
        <div><div class="ba-stat-val">30.6%</div><div class="ba-stat-sub">Sell-through</div></div>
      </div>
    </div>
  </div>

  <!-- Callout stats -->
  <div class="callout-row">
    <div class="callout-card c-green">
      <div class="callout-label">Revenue growth</div>
      <div class="callout-val">13.6×</div>
      <div class="callout-sub">March $1,044 → May $9,640</div>
    </div>
    <div class="callout-card c-blue">
      <div class="callout-label">More listings/month</div>
      <div class="callout-val">+556%</div>
      <div class="callout-sub">186 → 620 items listed</div>
    </div>
    <div class="callout-card c-yellow">
      <div class="callout-label">3-month profit</div>
      <div class="callout-val">$10,757</div>
      <div class="callout-sub">74% average margin</div>
    </div>
    <div class="callout-card c-purple">
      <div class="callout-label">Platforms active</div>
      <div class="callout-val">6</div>
      <div class="callout-sub">eBay, Poshmark, Mercari + more</div>
    </div>
  </div>

  <!-- Month cards -->
  <div class="monthly-bars">
    <div class="month-card m-before">
      <div class="month-chip chip-before">Self-managed</div>
      <div class="month-name">March</div>
      <div class="month-revenue">$1,044</div>
      <div class="month-profit">$731 profit · 70% margin</div>
      <div class="month-pills">
        <div class="month-pill">186 listed</div>
        <div class="month-pill">36 sold</div>
        <div class="month-pill">~6/day</div>
        <div class="month-pill">19.4% sell-through</div>
      </div>
    </div>
    <div class="month-card m-ps1">
      <div class="month-chip chip-ps1">Pile Slayers · Month 1</div>
      <div class="month-name">April</div>
      <div class="month-revenue">$4,576</div>
      <div class="month-profit">$3,203 profit · 70% margin</div>
      <div class="month-pills">
        <div class="month-pill">600 listed</div>
        <div class="month-pill">143 sold</div>
        <div class="month-pill">20/day</div>
        <div class="month-pill">23.8% sell-through</div>
      </div>
    </div>
    <div class="month-card m-ps2">
      <div class="month-chip chip-ps2">Pile Slayers · Month 2</div>
      <div class="month-name">May</div>
      <div class="month-revenue">$9,640</div>
      <div class="month-profit">$6,748 profit · 70% margin</div>
      <div class="month-pills">
        <div class="month-pill">620 listed</div>
        <div class="month-pill">230 sold</div>
        <div class="month-pill">20/day</div>
        <div class="month-pill">37.1% sell-through</div>
      </div>
    </div>
  </div>

  <!-- Charts -->
  <div class="charts-row">
    <div class="chart-card">
      <div class="chart-title">Revenue vs. Profit — weekly</div>
      <div class="chart-sub">Shaded region = Pile Slayers active. Revenue grew 13.6× from March to May.</div>
      <div class="legend-row">
        <div class="legend-pill"><span class="legend-sq" style="background:#4285F4"></span>Revenue</div>
        <div class="legend-pill"><span class="legend-sq" style="background:#34A853"></span>Profit</div>
        <div class="legend-pill"><span class="legend-sq" style="background:rgba(66,133,244,0.1);border:1px solid #4285F4"></span>Pile Slayers period</div>
      </div>
      <div style="position:relative;height:230px">
        <canvas id="revenueChart" role="img" aria-label="Line chart showing weekly revenue rising from $186 in March to $2,760 in May, accelerating sharply in April and May.">Revenue grew from $186/week in March to $2,760/week in late May.</canvas>
      </div>
    </div>
    <div class="chart-card">
      <div class="chart-title">Revenue by marketplace</div>
      <div class="chart-sub">Combined April + May (Pile Slayers period only)</div>
      <div class="legend-row">
        <div class="legend-pill"><span class="legend-sq" style="background:#34A853"></span>Profit</div>
        <div class="legend-pill"><span class="legend-sq" style="background:#EA4335"></span>Fees</div>
        <div class="legend-pill"><span class="legend-sq" style="background:#FBBC04"></span>COGS</div>
        <div class="legend-pill"><span class="legend-sq" style="background:#4285F4"></span>Shipping</div>
      </div>
      <div style="position:relative;height:230px">
        <canvas id="platformChart" role="img" aria-label="Stacked bar chart by marketplace. eBay leads at $9,200, followed by Poshmark, Depop, Mercari, Etsy, and Facebook.">eBay generated the most revenue at $9,200 across April and May.</canvas>
      </div>
      <div id="platformLabels" style="display:flex;justify-content:space-around;margin-top:0.4rem;font-size:10px;color:var(--muted);font-weight:700"></div>
    </div>
  </div>

  <!-- Bottom row -->
  <div class="bottom-row">
    <div class="chart-card">
      <div class="chart-title">Top selling brands</div>
      <div class="chart-sub">By units sold · all months</div>
      <div class="brands-list" id="brandsList"></div>
    </div>
    <div class="chart-card">
      <div class="chart-title">Top selling categories</div>
      <div class="chart-sub">By revenue share</div>
      <div class="treemap">
        <div class="treemap-row">
          <div class="treemap-cell" style="--flex:2;background:#E8F0FE;color:#1557B0">Clothing &amp; Shoes</div>
          <div class="treemap-cell" style="--flex:1.1;background:#FCE8E6;color:#B31412">Electronics</div>
          <div class="treemap-cell" style="--flex:0.9;background:#FEF7E0;color:#7A4F00">Video Games</div>
        </div>
        <div class="treemap-row">
          <div class="treemap-cell" style="--flex:1.3;background:#E6F4EA;color:#137333">Toys &amp; Collectibles</div>
          <div class="treemap-cell" style="--flex:1;background:#E4F0FB;color:#185ABC">Handbags</div>
          <div class="treemap-cell" style="--flex:0.8;background:#F3E8FD;color:#6B21A8">Other</div>
        </div>
      </div>
    </div>
    <div class="chart-card">
      <div class="chart-title">Averages by marketplace</div>
      <div class="chart-sub">Sale price, profit, days listed</div>
      <div class="avg-legend">
        <div class="avg-dot"><div class="avg-dot-circle" style="background:#9B59B6"></div>Mercari</div>
        <div class="avg-dot"><div class="avg-dot-circle" style="background:#FBBC04"></div>Facebook</div>
        <div class="avg-dot"><div class="avg-dot-circle" style="background:#34A853"></div>eBay</div>
        <div class="avg-dot"><div class="avg-dot-circle" style="background:#EA4335"></div>Poshmark</div>
        <div class="avg-dot"><div class="avg-dot-circle" style="background:#00ACC1"></div>Depop</div>
      </div>
      <div class="avg-row">
        <div class="avg-row-label">Sale Price</div>
        <div class="avg-row-val">$38.11 avg</div>
        <div class="avg-dots-row">
          <div class="avg-dot-marker" style="left:28%;background:#9B59B6"></div>
          <div class="avg-dot-marker" style="left:36%;background:#FBBC04"></div>
          <div class="avg-dot-marker" style="left:55%;background:#34A853"></div>
          <div class="avg-dot-marker" style="left:48%;background:#EA4335"></div>
          <div class="avg-dot-marker" style="left:42%;background:#00ACC1"></div>
        </div>
      </div>
      <div class="avg-row">
        <div class="avg-row-label">Profit per sale</div>
        <div class="avg-row-val">$28.84 avg</div>
        <div class="avg-dots-row">
          <div class="avg-dot-marker" style="left:22%;background:#9B59B6"></div>
          <div class="avg-dot-marker" style="left:32%;background:#FBBC04"></div>
          <div class="avg-dot-marker" style="left:58%;background:#34A853"></div>
          <div class="avg-dot-marker" style="left:44%;background:#EA4335"></div>
          <div class="avg-dot-marker" style="left:38%;background:#00ACC1"></div>
        </div>
      </div>
      <div class="avg-row">
        <div class="avg-row-label">Days listed before sale</div>
        <div class="avg-row-val">21 days avg</div>
        <div class="avg-dots-row">
          <div class="avg-dot-marker" style="left:36%;background:#9B59B6"></div>
          <div class="avg-dot-marker" style="left:52%;background:#FBBC04"></div>
          <div class="avg-dot-marker" style="left:28%;background:#34A853"></div>
          <div class="avg-dot-marker" style="left:44%;background:#EA4335"></div>
          <div class="avg-dot-marker" style="left:20%;background:#00ACC1"></div>
        </div>
      </div>
    </div>
  </div>

  <div class="download-bar">
    <div>
      <h3>This client now makes more in a week than they used to in a month. 🚀</h3>
      <p>You take the photos. Pile Slayers handles the listings, the platforms, and the buyer questions.</p>
    </div>
    <a href="index.html#pricing" class="btn-cta">Start Your Free Trial →</a>
  </div>

</div>

<script>
const weeks13  = ['Mar W1','Mar W2','Mar W3','Mar W4','Apr W1','Apr W2','Apr W3','Apr W4','May W1','May W2','May W3','May W4'];
const revData  = [186,258,310,290,480,820,1560,1716,2040,2280,2560,2760];
const profData = [130,181,217,203,336,574,1092,1201,1428,1596,1792,1932];

/* Preview chart */
new Chart(document.getElementById('previewChart').getContext('2d'),{
  type:'line',
  data:{labels:weeks13,datasets:[
    {data:revData, borderColor:'#4285F4',borderWidth:2,pointRadius:0,tension:0.4,fill:true,backgroundColor:'rgba(66,133,244,0.08)'},
    {data:profData,borderColor:'#34A853',borderWidth:2,pointRadius:0,tension:0.4}
  ]},
  options:{responsive:true,maintainAspectRatio:false,plugins:{legend:{display:false}},scales:{x:{display:false},y:{display:false}}}
});

function unlockDashboard(e){
  e.preventDefault();
  document.getElementById('gate').style.display='none';
  const dash=document.getElementById('dashboard');
  dash.style.display='block';
  setTimeout(()=>{dash.classList.add('faded');buildDashboard();},50);
  setTimeout(()=>{dash.scrollIntoView({behavior:'smooth'});},100);
}

function buildDashboard(){
  /* Revenue vs Profit */
  new Chart(document.getElementById('revenueChart').getContext('2d'),{
    type:'line',
    data:{labels:weeks13,datasets:[
      {label:'Revenue',data:revData,borderColor:'#4285F4',backgroundColor:'rgba(66,133,244,0.08)',borderWidth:2.5,pointRadius:4,pointBackgroundColor:'#4285F4',tension:0.4,fill:true},
      {label:'Profit', data:profData,borderColor:'#34A853',backgroundColor:'rgba(52,168,83,0.05)',borderWidth:2.5,pointRadius:4,pointBackgroundColor:'#34A853',tension:0.4,fill:false}
    ]},
    plugins:[{id:'psRegion',beforeDraw(c){
      const{ctx,chartArea:ca,scales}=c;if(!ca)return;
      const x0=scales.x.getPixelForValue(4),x1=scales.x.getPixelForValue(11);
      ctx.save();
      ctx.fillStyle='rgba(66,133,244,0.06)';
      ctx.fillRect(x0,ca.top,x1-x0,ca.bottom-ca.top);
      ctx.strokeStyle='rgba(66,133,244,0.4)';ctx.lineWidth=1.5;ctx.setLineDash([5,4]);
      ctx.beginPath();ctx.moveTo(x0,ca.top);ctx.lineTo(x0,ca.bottom);ctx.stroke();
      ctx.setLineDash([]);
      ctx.fillStyle='rgba(66,133,244,0.85)';ctx.font='700 10px Nunito,sans-serif';
      ctx.fillText('Pile Slayers active',x0+8,ca.top+13);
      ctx.restore();
    }}],
    options:{
      responsive:true,maintainAspectRatio:false,
      plugins:{legend:{display:false},tooltip:{callbacks:{label:ctx=>' $'+ctx.parsed.y.toLocaleString()}}},
      scales:{
        x:{grid:{color:'rgba(0,0,0,0.04)'},ticks:{color:'#888',font:{family:'Nunito',size:10,weight:'700'},maxRotation:45}},
        y:{grid:{color:'rgba(0,0,0,0.04)'},ticks:{color:'#888',font:{family:'Nunito',size:10,weight:'700'},callback:v=>'$'+v.toLocaleString()}}
      }
    }
  });

  /* Platform */
  const platforms=['Mercari','Facebook','eBay','Poshmark','Etsy','Depop'];
  const sold=[31,18,156,75,24,60];
  const pL=document.getElementById('platformLabels');
  platforms.forEach((p,i)=>{const s=document.createElement('span');s.textContent=sold[i]+' sold';pL.appendChild(s);});
  new Chart(document.getElementById('platformChart').getContext('2d'),{
    type:'bar',
    data:{labels:platforms,datasets:[
      {label:'Profit',  data:[720,432,6900,2070,528,1276],backgroundColor:'#34A853'},
      {label:'Fees',    data:[144,86,1380,414,105,255],   backgroundColor:'#EA4335'},
      {label:'COGS',    data:[72,50,690,207,60,130],      backgroundColor:'#FBBC04'},
      {label:'Shipping',data:[24,20,230,69,15,19],        backgroundColor:'#4285F4'},
    ]},
    options:{
      responsive:true,maintainAspectRatio:false,
      plugins:{legend:{display:false},tooltip:{callbacks:{label:ctx=>' $'+ctx.parsed.y.toLocaleString()}}},
      scales:{
        x:{stacked:true,grid:{display:false},ticks:{color:'#888',font:{family:'Nunito',size:10,weight:'700'},autoSkip:false,maxRotation:0}},
        y:{stacked:true,grid:{color:'rgba(0,0,0,0.04)'},ticks:{color:'#888',font:{family:'Nunito',size:10,weight:'700'},callback:v=>'$'+(v>=1000?(v/1000).toFixed(1)+'K':v)}}
      }
    }
  });

  /* Brand bars */
  const bColors=['#4285F4','#EA4335','#34A853','#FBBC04','#9B59B6'];
  const brands=[{n:'Unbranded',c:42},{n:'Nike',c:28},{n:'Nintendo',c:22},{n:"Levi's",c:17},{n:'Disney',c:13}];
  const bl=document.getElementById('brandsList');
  brands.forEach((b,i)=>{
    const pct=Math.round((b.c/42)*100);
    bl.innerHTML+=`<div class="brand-row">
      <div class="brand-name">${b.n}</div>
      <div class="brand-bar-wrap"><div class="brand-bar" style="width:0%;background:${bColors[i]}" data-w="${pct}%"></div></div>
      <div class="brand-count" style="color:${bColors[i]}">${b.c}</div>
    </div>`;
  });
  setTimeout(()=>{document.querySelectorAll('.brand-bar').forEach(bar=>{bar.style.width=bar.dataset.w;});},300);
}
</script>
</body>
</html>
