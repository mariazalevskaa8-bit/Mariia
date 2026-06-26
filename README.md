<!DOCTYPE html>
<html lang="de">
<head>
  <!-- ═══════════════════════════════════════════════
       TEIL 4: SEO BLOCK
  ═══════════════════════════════════════════════ -->
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="theme-color" content="#1a1410" />

  <!-- Primary Meta -->
  <title>Serenova Wellness Studio München | Premium Massage & Körpertherapie</title>
  <meta name="description" content="Serenova – Ihr exklusives Wellness-Studio in München. Erleben Sie Premium-Massagen, Tiefengewebstherapie und ganzheitliche Körperbehandlungen in entspannter Atmosphäre. Jetzt Termin buchen." />
  <meta name="keywords" content="Massage München, Premium Massage Studio, Wellness München, Tiefengewebsmassage, Aromamassage, Hot Stone Massage, Sportmassage, Entspannung München" />
  <meta name="author" content="Serenova Wellness Studio" />
  <meta name="robots" content="index, follow" />
  <link rel="canonical" href="https://serenova-wellness.de/" />

  <!-- Open Graph -->
  <meta property="og:type" content="website" />
  <meta property="og:title" content="Serenova Wellness Studio München | Premium Massage" />
  <meta property="og:description" content="Ganzheitliche Körpertherapie und Premiumwellness im Herzen Münchens. Buchen Sie Ihre Auszeit noch heute." />
  <meta property="og:url" content="https://serenova-wellness.de/" />
  <meta property="og:locale" content="de_DE" />

  <!-- Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Inter:wght@300;400;500&display=swap" rel="stylesheet" />

  <!-- ═══════════════════════════════════════════════
       TEIL 2: CSS
  ═══════════════════════════════════════════════ -->
  <style>
    /* ── TOKENS ────────────────────────────────── */
    :root {
      --ink:        #1a1410;
      --ink-soft:   #3d3530;
      --sand:       #f5f0e8;
      --sand-mid:   #ede6d9;
      --gold:       #c9a96e;
      --gold-light: #dfc28e;
      --gold-dim:   rgba(201,169,110,.18);
      --sage:       #8a9e8c;
      --white:      #ffffff;
      --overlay:    rgba(26,20,16,.72);

      --ff-display: 'Cormorant Garamond', Georgia, serif;
      --ff-body:    'Inter', system-ui, sans-serif;

      --r-card:  16px;
      --r-btn:   40px;
      --shadow:  0 8px 40px rgba(26,20,16,.12);
      --shadow-lg: 0 20px 80px rgba(26,20,16,.22);

      --nav-h: 76px;
      --section-py: 120px;
      --ease: cubic-bezier(.22,.68,0,1.2);
    }

    /* ── RESET ─────────────────────────────────── */
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; font-size: 16px; }
    body {
      font-family: var(--ff-body);
      background: var(--sand);
      color: var(--ink);
      overflow-x: hidden;
      line-height: 1.6;
    }
    img { display: block; width: 100%; height: 100%; object-fit: cover; }
    a { color: inherit; text-decoration: none; }
    ul { list-style: none; }
    button { cursor: pointer; border: none; background: none; font-family: inherit; }

    /* ── SCROLLBAR ─────────────────────────────── */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: var(--sand); }
    ::-webkit-scrollbar-thumb { background: var(--gold); border-radius: 3px; }

    /* ── UTILITIES ─────────────────────────────── */
    .container {
      width: min(1200px, 100% - 48px);
      margin-inline: auto;
    }
    .section-label {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      font-family: var(--ff-body);
      font-size: .72rem;
      font-weight: 500;
      letter-spacing: .18em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 20px;
    }
    .section-label::before {
      content: '';
      display: block;
      width: 28px;
      height: 1px;
      background: var(--gold);
    }
    .section-title {
      font-family: var(--ff-display);
      font-size: clamp(2.2rem, 4.5vw, 3.6rem);
      font-weight: 300;
      line-height: 1.12;
      color: var(--ink);
    }
    .section-title em {
      font-style: italic;
      color: var(--gold);
    }
    .divider {
      width: 48px;
      height: 1px;
      background: var(--gold);
      margin: 28px 0;
    }

    /* ── BUTTONS ───────────────────────────────── */
    .btn {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 14px 32px;
      border-radius: var(--r-btn);
      font-family: var(--ff-body);
      font-size: .82rem;
      font-weight: 500;
      letter-spacing: .1em;
      text-transform: uppercase;
      transition: all .35s var(--ease);
      white-space: nowrap;
    }
    .btn-primary {
      background: var(--gold);
      color: var(--ink);
    }
    .btn-primary:hover {
      background: var(--gold-light);
      transform: translateY(-2px);
      box-shadow: 0 12px 32px rgba(201,169,110,.4);
    }
    .btn-ghost {
      background: transparent;
      color: var(--white);
      border: 1px solid rgba(255,255,255,.45);
    }
    .btn-ghost:hover {
      background: rgba(255,255,255,.1);
      border-color: var(--white);
      transform: translateY(-2px);
    }
    .btn-outline {
      background: transparent;
      color: var(--gold);
      border: 1px solid var(--gold);
    }
    .btn-outline:hover {
      background: var(--gold);
      color: var(--ink);
      transform: translateY(-2px);
    }
    .btn-arrow::after {
      content: '→';
      font-size: 1rem;
      transition: transform .3s;
    }
    .btn-arrow:hover::after { transform: translateX(4px); }

    /* ── NAVIGATION ────────────────────────────── */
    #nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 1000;
      height: var(--nav-h);
      display: flex;
      align-items: center;
      transition: background .4s, box-shadow .4s;
    }
    #nav.scrolled {
      background: rgba(26,20,16,.96);
      backdrop-filter: blur(16px);
      box-shadow: 0 2px 32px rgba(0,0,0,.25);
    }
    .nav-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      width: 100%;
    }
    .nav-logo {
      display: flex;
      flex-direction: column;
      gap: 2px;
    }
    .nav-logo-name {
      font-family: var(--ff-display);
      font-size: 1.55rem;
      font-weight: 400;
      color: var(--white);
      letter-spacing: .06em;
      line-height: 1;
    }
    .nav-logo-sub {
      font-size: .6rem;
      letter-spacing: .22em;
      text-transform: uppercase;
      color: var(--gold);
      line-height: 1;
    }
    .nav-links {
      display: flex;
      gap: 36px;
      align-items: center;
    }
    .nav-links a {
      font-size: .78rem;
      letter-spacing: .1em;
      text-transform: uppercase;
      color: rgba(255,255,255,.78);
      transition: color .3s;
      position: relative;
    }
    .nav-links a::after {
      content: '';
      position: absolute;
      bottom: -4px; left: 0;
      width: 0; height: 1px;
      background: var(--gold);
      transition: width .3s;
    }
    .nav-links a:hover { color: var(--white); }
    .nav-links a:hover::after { width: 100%; }
    .nav-cta {
      padding: 10px 24px;
      font-size: .74rem;
    }

    /* Burger */
    .burger {
      display: none;
      flex-direction: column;
      gap: 5px;
      padding: 8px;
      z-index: 1100;
    }
    .burger span {
      display: block;
      width: 24px;
      height: 1.5px;
      background: var(--white);
      border-radius: 2px;
      transition: all .35s var(--ease);
      transform-origin: center;
    }
    .burger.open span:nth-child(1) { transform: translateY(6.5px) rotate(45deg); }
    .burger.open span:nth-child(2) { opacity: 0; transform: scaleX(0); }
    .burger.open span:nth-child(3) { transform: translateY(-6.5px) rotate(-45deg); }

    /* Mobile menu */
    .mobile-menu {
      position: fixed;
      inset: 0;
      background: var(--ink);
      z-index: 1050;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 36px;
      opacity: 0;
      pointer-events: none;
      transform: translateY(-100%);
      transition: opacity .4s, transform .4s var(--ease);
    }
    .mobile-menu.open {
      opacity: 1;
      pointer-events: auto;
      transform: translateY(0);
    }
    .mobile-menu a {
      font-family: var(--ff-display);
      font-size: clamp(1.8rem, 6vw, 2.8rem);
      font-weight: 300;
      color: var(--white);
      letter-spacing: .04em;
      transition: color .3s;
    }
    .mobile-menu a:hover { color: var(--gold); }
    .mobile-menu .btn {
      margin-top: 12px;
      font-size: .8rem;
    }

    /* ── HERO ──────────────────────────────────── */
    #hero {
      position: relative;
      min-height: 100dvh;
      display: grid;
      place-items: center;
      overflow: hidden;
      background: var(--ink);
    }
    .hero-bg {
      position: absolute;
      inset: 0;
      background:
        linear-gradient(160deg, rgba(26,20,16,.55) 0%, rgba(26,20,16,.3) 50%, rgba(26,20,16,.75) 100%),
        url('https://images.unsplash.com/photo-1600334089648-b0d9d3028eb2?w=1600&q=80') center/cover no-repeat;
    }
    .hero-bg::after {
      content: '';
      position: absolute;
      bottom: 0; left: 0; right: 0;
      height: 200px;
      background: linear-gradient(transparent, var(--sand));
    }
    .hero-content {
      position: relative;
      z-index: 2;
      text-align: center;
      padding: 120px 24px 80px;
      max-width: 860px;
    }
    .hero-eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 12px;
      font-size: .7rem;
      letter-spacing: .26em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 28px;
    }
    .hero-eyebrow::before,
    .hero-eyebrow::after {
      content: '';
      width: 32px;
      height: 1px;
      background: var(--gold);
    }
    /* H1 */
    .hero-h1 {
      font-family: var(--ff-display);
      font-size: clamp(2.8rem, 8vw, 6rem);
      font-weight: 300;
      color: var(--white);
      line-height: 1.06;
      margin-bottom: 24px;
    }
    .hero-h1 em {
      font-style: italic;
      color: var(--gold-light);
      display: block;
    }
    .hero-sub {
      font-size: clamp(1rem, 2vw, 1.18rem);
      color: rgba(255,255,255,.72);
      max-width: 520px;
      margin: 0 auto 44px;
      font-weight: 300;
      line-height: 1.75;
    }
    .hero-cta {
      display: flex;
      gap: 16px;
      justify-content: center;
      flex-wrap: wrap;
    }
    .hero-scroll {
      position: absolute;
      bottom: 56px;
      left: 50%;
      transform: translateX(-50%);
      z-index: 2;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 8px;
      color: rgba(255,255,255,.45);
      font-size: .65rem;
      letter-spacing: .18em;
      text-transform: uppercase;
    }
    .scroll-line {
      width: 1px;
      height: 52px;
      background: linear-gradient(var(--gold), transparent);
      animation: scrollPulse 2s ease-in-out infinite;
    }
    @keyframes scrollPulse {
      0%, 100% { opacity: .4; transform: scaleY(1); }
      50% { opacity: 1; transform: scaleY(1.15); }
    }

    /* ── STATS BAR ─────────────────────────────── */
    #stats {
      background: var(--ink);
      padding: 48px 0;
    }
    .stats-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 1px;
      background: rgba(255,255,255,.08);
    }
    .stat-item {
      background: var(--ink);
      padding: 36px 24px;
      text-align: center;
      transition: background .3s;
    }
    .stat-item:hover { background: var(--ink-soft); }
    .stat-num {
      font-family: var(--ff-display);
      font-size: clamp(2rem, 4vw, 3rem);
      font-weight: 300;
      color: var(--gold);
      line-height: 1;
      margin-bottom: 8px;
    }
    .stat-label {
      font-size: .72rem;
      letter-spacing: .1em;
      text-transform: uppercase;
      color: rgba(255,255,255,.5);
    }

    /* ── ÜBER UNS ──────────────────────────────── */
    #ueber-uns {
      padding: var(--section-py) 0;
      background: var(--sand);
    }
    .ueber-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 80px;
      align-items: center;
    }
    .ueber-img-wrap {
      position: relative;
      height: 560px;
    }
    .ueber-img-main {
      position: absolute;
      inset: 0;
      border-radius: var(--r-card);
      overflow: hidden;
      background: url('https://images.unsplash.com/photo-1540555700478-4be289fbecef?w=800&q=80') center/cover;
    }
    .ueber-img-accent {
      position: absolute;
      bottom: -32px;
      right: -32px;
      width: 220px;
      height: 220px;
      border-radius: var(--r-card);
      overflow: hidden;
      border: 6px solid var(--sand);
      background: url('https://images.unsplash.com/photo-1515377905703-c4788e51af15?w=400&q=80') center/cover;
      box-shadow: var(--shadow-lg);
    }
    .ueber-gold-bar {
      position: absolute;
      top: -16px;
      left: -16px;
      width: 80px;
      height: 80px;
      background: var(--gold);
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: var(--ff-display);
      font-size: 1.6rem;
      font-weight: 300;
      color: var(--ink);
    }
    .ueber-text p {
      font-size: 1.05rem;
      color: var(--ink-soft);
      line-height: 1.8;
      margin-bottom: 20px;
      font-weight: 300;
    }
    .ueber-features {
      display: flex;
      flex-direction: column;
      gap: 20px;
      margin-top: 40px;
    }
    .ueber-feat {
      display: flex;
      gap: 16px;
      align-items: flex-start;
    }
    .feat-icon {
      width: 44px;
      height: 44px;
      border-radius: 50%;
      background: var(--gold-dim);
      border: 1px solid var(--gold);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.1rem;
      flex-shrink: 0;
      margin-top: 2px;
    }
    .feat-body h4 {
      font-family: var(--ff-display);
      font-size: 1.1rem;
      font-weight: 400;
      margin-bottom: 4px;
    }
    .feat-body p {
      font-size: .85rem;
      color: var(--ink-soft);
      line-height: 1.6;
    }

    /* ── LEISTUNGEN ────────────────────────────── */
    #leistungen {
      padding: var(--section-py) 0;
      background: var(--sand-mid);
    }
    .leistungen-header {
      text-align: center;
      margin-bottom: 72px;
    }
    .leistungen-header .section-label { justify-content: center; }
    .leistungen-header .section-label::before { display: none; }
    .leistungen-header .section-label::after {
      content: '';
      display: block;
      width: 28px;
      height: 1px;
      background: var(--gold);
    }
    .services-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 28px;
    }
    .service-card {
      background: var(--white);
      border-radius: var(--r-card);
      overflow: hidden;
      transition: transform .4s var(--ease), box-shadow .4s;
      box-shadow: var(--shadow);
    }
    .service-card:hover {
      transform: translateY(-8px);
      box-shadow: var(--shadow-lg);
    }
    .service-img {
      height: 220px;
      overflow: hidden;
      position: relative;
    }
    .service-img img {
      transition: transform .6s var(--ease);
    }
    .service-card:hover .service-img img { transform: scale(1.07); }
    .service-tag {
      position: absolute;
      top: 16px;
      left: 16px;
      background: var(--gold);
      color: var(--ink);
      font-size: .65rem;
      letter-spacing: .12em;
      text-transform: uppercase;
      padding: 5px 12px;
      border-radius: 20px;
      font-weight: 500;
    }
    .service-body {
      padding: 28px;
    }
    /* H3 services */
    .service-body h3 {
      font-family: var(--ff-display);
      font-size: 1.4rem;
      font-weight: 400;
      margin-bottom: 10px;
      line-height: 1.25;
    }
    .service-body p {
      font-size: .88rem;
      color: var(--ink-soft);
      line-height: 1.7;
      margin-bottom: 20px;
    }
    .service-footer {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding-top: 16px;
      border-top: 1px solid var(--sand-mid);
    }
    .service-price {
      font-family: var(--ff-display);
      font-size: 1.5rem;
      font-weight: 300;
      color: var(--gold);
    }
    .service-price span {
      font-family: var(--ff-body);
      font-size: .72rem;
      color: var(--ink-soft);
      font-weight: 400;
    }
    .service-duration {
      font-size: .72rem;
      letter-spacing: .08em;
      text-transform: uppercase;
      color: var(--ink-soft);
      background: var(--sand);
      padding: 5px 12px;
      border-radius: 20px;
    }

    /* ── PREISE ────────────────────────────────── */
    #preise {
      padding: var(--section-py) 0;
      background: var(--ink);
      position: relative;
      overflow: hidden;
    }
    #preise::before {
      content: '';
      position: absolute;
      top: -200px;
      left: -200px;
      width: 600px;
      height: 600px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(201,169,110,.08) 0%, transparent 70%);
      pointer-events: none;
    }
    .preise-header { text-align: center; margin-bottom: 72px; }
    .preise-header .section-title { color: var(--white); }
    .preise-header .section-label { justify-content: center; }
    .preise-header .section-label::before { display: none; }
    .preise-header .section-label::after {
      content: '';
      width: 28px;
      height: 1px;
      background: var(--gold);
    }
    .preise-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 24px;
      align-items: start;
    }
    .price-card {
      background: rgba(255,255,255,.04);
      border: 1px solid rgba(255,255,255,.09);
      border-radius: var(--r-card);
      padding: 44px 36px 40px;
      position: relative;
      transition: border-color .3s, background .3s;
    }
    .price-card:hover {
      border-color: rgba(201,169,110,.4);
      background: rgba(255,255,255,.07);
    }
    .price-card.featured {
      background: var(--gold);
      border-color: var(--gold);
      transform: scale(1.04);
      box-shadow: 0 24px 72px rgba(201,169,110,.35);
    }
    .price-card.featured:hover { transform: scale(1.06); }
    .price-badge {
      position: absolute;
      top: -14px;
      left: 50%;
      transform: translateX(-50%);
      background: var(--ink);
      color: var(--gold);
      font-size: .65rem;
      letter-spacing: .16em;
      text-transform: uppercase;
      padding: 6px 16px;
      border-radius: 20px;
      border: 1px solid var(--gold);
      white-space: nowrap;
    }
    /* H2 pricing */
    .price-plan {
      font-family: var(--ff-body);
      font-size: .7rem;
      letter-spacing: .2em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 8px;
    }
    .price-card.featured .price-plan { color: var(--ink); opacity: .7; }
    .price-name {
      font-family: var(--ff-display);
      font-size: 1.6rem;
      font-weight: 300;
      color: var(--white);
      margin-bottom: 28px;
      line-height: 1;
    }
    .price-card.featured .price-name { color: var(--ink); }
    .price-amount {
      display: flex;
      align-items: flex-start;
      gap: 4px;
      margin-bottom: 8px;
    }
    .price-cur {
      font-family: var(--ff-display);
      font-size: 1.2rem;
      font-weight: 300;
      color: var(--gold);
      margin-top: 10px;
    }
    .price-card.featured .price-cur { color: var(--ink); }
    .price-val {
      font-family: var(--ff-display);
      font-size: 3.8rem;
      font-weight: 300;
      color: var(--white);
      line-height: 1;
    }
    .price-card.featured .price-val { color: var(--ink); }
    .price-note {
      font-size: .75rem;
      color: rgba(255,255,255,.4);
      margin-bottom: 32px;
    }
    .price-card.featured .price-note { color: rgba(26,20,16,.55); }
    .price-features {
      display: flex;
      flex-direction: column;
      gap: 12px;
      margin-bottom: 36px;
    }
    .price-feat {
      display: flex;
      gap: 10px;
      align-items: flex-start;
      font-size: .875rem;
      color: rgba(255,255,255,.72);
    }
    .price-card.featured .price-feat { color: var(--ink-soft); }
    .price-feat-check {
      color: var(--gold);
      font-size: .8rem;
      margin-top: 2px;
      flex-shrink: 0;
    }
    .price-card.featured .price-feat-check { color: var(--ink); }
    .price-card .btn { width: 100%; justify-content: center; }
    .price-card:not(.featured) .btn {
      background: transparent;
      color: var(--white);
      border: 1px solid rgba(255,255,255,.22);
    }
    .price-card:not(.featured) .btn:hover {
      border-color: var(--gold);
      color: var(--gold);
    }
    .price-card.featured .btn {
      background: var(--ink);
      color: var(--white);
    }
    .price-card.featured .btn:hover {
      background: var(--ink-soft);
      transform: translateY(-2px);
    }

    /* ── GALERIE ───────────────────────────────── */
    #galerie {
      padding: var(--section-py) 0;
      background: var(--sand);
    }
    .galerie-header { margin-bottom: 52px; }
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(12, 1fr);
      grid-template-rows: repeat(3, 180px);
      gap: 12px;
    }
    .g-item {
      border-radius: 12px;
      overflow: hidden;
      background: var(--sand-mid);
      position: relative;
      cursor: pointer;
    }
    .g-item img {
      transition: transform .6s var(--ease);
      object-position: center;
    }
    .g-item:hover img { transform: scale(1.08); }
    .g-item::after {
      content: '';
      position: absolute;
      inset: 0;
      background: linear-gradient(transparent 50%, rgba(26,20,16,.5));
      opacity: 0;
      transition: opacity .4s;
    }
    .g-item:hover::after { opacity: 1; }
    .g1 { grid-column: 1 / 5; grid-row: 1 / 3; }
    .g2 { grid-column: 5 / 9; grid-row: 1 / 2; }
    .g3 { grid-column: 9 / 13; grid-row: 1 / 2; }
    .g4 { grid-column: 5 / 7; grid-row: 2 / 3; }
    .g5 { grid-column: 7 / 9; grid-row: 2 / 3; }
    .g6 { grid-column: 9 / 13; grid-row: 2 / 3; }
    .g7 { grid-column: 1 / 4; grid-row: 3 / 4; }
    .g8 { grid-column: 4 / 8; grid-row: 3 / 4; }
    .g9 { grid-column: 8 / 13; grid-row: 3 / 4; }

    /* ── TESTIMONIALS ──────────────────────────── */
    #testimonials {
      padding: var(--section-py) 0;
      background: var(--sand-mid);
    }
    .testi-header { text-align: center; margin-bottom: 64px; }
    .testi-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 28px;
    }
    .testi-card {
      background: var(--white);
      border-radius: var(--r-card);
      padding: 36px 32px;
      box-shadow: var(--shadow);
      transition: transform .35s var(--ease);
    }
    .testi-card:hover { transform: translateY(-6px); }
    .testi-stars {
      display: flex;
      gap: 4px;
      margin-bottom: 16px;
    }
    .testi-stars span { color: var(--gold); font-size: 1rem; }
    .testi-text {
      font-family: var(--ff-display);
      font-size: 1.1rem;
      font-weight: 300;
      font-style: italic;
      color: var(--ink);
      line-height: 1.7;
      margin-bottom: 24px;
    }
    .testi-author {
      display: flex;
      gap: 14px;
      align-items: center;
    }
    .testi-avatar {
      width: 46px;
      height: 46px;
      border-radius: 50%;
      background: var(--gold-dim);
      border: 2px solid var(--gold);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: var(--ff-display);
      font-size: 1.1rem;
      color: var(--gold);
      flex-shrink: 0;
    }
    .testi-name {
      font-size: .9rem;
      font-weight: 500;
      color: var(--ink);
    }
    .testi-role {
      font-size: .75rem;
      color: var(--ink-soft);
    }

    /* ── KONTAKT ───────────────────────────────── */
    #kontakt {
      padding: var(--section-py) 0;
      background: var(--sand);
    }
    .kontakt-grid {
      display: grid;
      grid-template-columns: 1fr 1.1fr;
      gap: 80px;
      align-items: start;
    }
    .kontakt-info p {
      font-size: 1rem;
      color: var(--ink-soft);
      line-height: 1.8;
      margin-bottom: 36px;
      font-weight: 300;
    }
    .contact-details {
      display: flex;
      flex-direction: column;
      gap: 16px;
    }
    .contact-detail {
      display: flex;
      gap: 14px;
      align-items: flex-start;
    }
    .contact-icon {
      width: 38px;
      height: 38px;
      background: var(--gold-dim);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: .95rem;
      flex-shrink: 0;
      color: var(--gold);
    }
    .contact-text strong {
      display: block;
      font-size: .8rem;
      letter-spacing: .1em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 2px;
      font-weight: 500;
    }
    .contact-text span {
      font-size: .92rem;
      color: var(--ink-soft);
    }

    /* Form */
    .contact-form {
      background: var(--white);
      border-radius: var(--r-card);
      padding: 44px 40px;
      box-shadow: var(--shadow);
    }
    .contact-form h3 {
      font-family: var(--ff-display);
      font-size: 1.6rem;
      font-weight: 400;
      margin-bottom: 8px;
    }
    .contact-form .form-sub {
      font-size: .85rem;
      color: var(--ink-soft);
      margin-bottom: 28px;
    }
    .form-row {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
    }
    .form-group {
      display: flex;
      flex-direction: column;
      gap: 6px;
      margin-bottom: 16px;
    }
    .form-group label {
      font-size: .72rem;
      letter-spacing: .1em;
      text-transform: uppercase;
      color: var(--ink-soft);
      font-weight: 500;
    }
    .form-group input,
    .form-group select,
    .form-group textarea {
      padding: 13px 16px;
      border: 1px solid var(--sand-mid);
      border-radius: 10px;
      font-family: var(--ff-body);
      font-size: .9rem;
      color: var(--ink);
      background: var(--sand);
      transition: border-color .3s, box-shadow .3s;
      outline: none;
      appearance: none;
    }
    .form-group select {
      background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8' fill='none'%3E%3Cpath d='M1 1l5 5 5-5' stroke='%23c9a96e' stroke-width='1.5' stroke-linecap='round' stroke-linejoin='round'/%3E%3C/svg%3E");
      background-repeat: no-repeat;
      background-position: right 16px center;
      padding-right: 40px;
    }
    .form-group textarea { min-height: 100px; resize: vertical; }
    .form-group input:focus,
    .form-group select:focus,
    .form-group textarea:focus {
      border-color: var(--gold);
      box-shadow: 0 0 0 3px var(--gold-dim);
    }
    .form-btn { width: 100%; justify-content: center; margin-top: 8px; }
    .form-success {
      display: none;
      text-align: center;
      padding: 24px;
      background: rgba(138,158,140,.1);
      border: 1px solid var(--sage);
      border-radius: 10px;
      color: var(--sage);
      font-size: .92rem;
      margin-top: 16px;
    }

    /* ── POPUP ─────────────────────────────────── */
    #popup {
      position: fixed;
      inset: 0;
      z-index: 2000;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 24px;
      opacity: 0;
      pointer-events: none;
      transition: opacity .35s;
    }
    #popup.open {
      opacity: 1;
      pointer-events: auto;
    }
    .popup-overlay {
      position: absolute;
      inset: 0;
      background: rgba(26,20,16,.78);
      backdrop-filter: blur(8px);
      cursor: pointer;
    }
    .popup-box {
      position: relative;
      background: var(--white);
      border-radius: 20px;
      padding: 52px 44px 44px;
      width: min(520px, 100%);
      max-height: 90vh;
      overflow-y: auto;
      box-shadow: var(--shadow-lg);
      transform: translateY(24px) scale(.96);
      transition: transform .4s var(--ease);
    }
    #popup.open .popup-box {
      transform: translateY(0) scale(1);
    }
    .popup-close {
      position: absolute;
      top: 20px;
      right: 20px;
      width: 36px;
      height: 36px;
      border-radius: 50%;
      background: var(--sand);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.1rem;
      color: var(--ink-soft);
      transition: background .3s, color .3s;
    }
    .popup-close:hover { background: var(--gold); color: var(--white); }
    .popup-eyebrow {
      font-size: .68rem;
      letter-spacing: .2em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 8px;
      font-weight: 500;
    }
    .popup-title {
      font-family: var(--ff-display);
      font-size: 2rem;
      font-weight: 300;
      margin-bottom: 6px;
    }
    .popup-sub {
      font-size: .85rem;
      color: var(--ink-soft);
      margin-bottom: 28px;
    }
    .popup-form .form-group { margin-bottom: 14px; }

    /* ── FOOTER ────────────────────────────────── */
    footer {
      background: var(--ink);
      color: rgba(255,255,255,.6);
      padding: 80px 0 32px;
    }
    .footer-grid {
      display: grid;
      grid-template-columns: 1.4fr 1fr 1fr 1fr;
      gap: 48px;
      margin-bottom: 64px;
    }
    .footer-brand .nav-logo-name { font-size: 1.8rem; display: block; margin-bottom: 4px; }
    .footer-brand .nav-logo-sub { display: block; margin-bottom: 20px; }
    .footer-brand p {
      font-size: .85rem;
      line-height: 1.8;
      color: rgba(255,255,255,.45);
      max-width: 260px;
    }
    .footer-socials {
      display: flex;
      gap: 10px;
      margin-top: 24px;
    }
    .social-btn {
      width: 38px;
      height: 38px;
      border-radius: 50%;
      border: 1px solid rgba(255,255,255,.15);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: .85rem;
      color: rgba(255,255,255,.55);
      transition: border-color .3s, color .3s, background .3s;
    }
    .social-btn:hover {
      border-color: var(--gold);
      color: var(--gold);
      background: var(--gold-dim);
    }
    .footer-col h5 {
      font-family: var(--ff-body);
      font-size: .7rem;
      letter-spacing: .18em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 20px;
      font-weight: 500;
    }
    .footer-links {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    .footer-links a {
      font-size: .85rem;
      color: rgba(255,255,255,.5);
      transition: color .3s;
    }
    .footer-links a:hover { color: var(--white); }
    .footer-bottom {
      border-top: 1px solid rgba(255,255,255,.08);
      padding-top: 28px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 12px;
      font-size: .78rem;
    }
    .footer-legal {
      display: flex;
      gap: 24px;
    }
    .footer-legal a {
      color: rgba(255,255,255,.38);
      font-size: .78rem;
      transition: color .3s;
    }
    .footer-legal a:hover { color: var(--gold); }

    /* ── ANIMATIONS ────────────────────────────── */
    .reveal {
      opacity: 0;
      transform: translateY(32px);
      transition: opacity .7s ease, transform .7s var(--ease);
    }
    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }
    .reveal-delay-1 { transition-delay: .1s; }
    .reveal-delay-2 { transition-delay: .2s; }
    .reveal-delay-3 { transition-delay: .3s; }
    .reveal-delay-4 { transition-delay: .4s; }

    /* ── RESPONSIVE ────────────────────────────── */
    @media (max-width: 1024px) {
      :root { --section-py: 80px; }
      .ueber-grid { grid-template-columns: 1fr; gap: 48px; }
      .ueber-img-wrap { height: 400px; }
      .ueber-img-accent { width: 160px; height: 160px; right: -16px; bottom: -16px; }
      .services-grid { grid-template-columns: repeat(2, 1fr); }
      .preise-grid { grid-template-columns: repeat(3, 1fr); gap: 16px; }
      .price-card { padding: 32px 24px 28px; }
      .price-card.featured { transform: scale(1.02); }
      .testi-grid { grid-template-columns: 1fr 1fr; }
      .kontakt-grid { grid-template-columns: 1fr; gap: 48px; }
      .footer-grid { grid-template-columns: 1fr 1fr; gap: 36px; }
      .stats-grid { grid-template-columns: repeat(2, 1fr); }
    }

    @media (max-width: 768px) {
      :root { --section-py: 64px; --nav-h: 66px; }
      .nav-links, .nav-cta { display: none; }
      .burger { display: flex; }
      .services-grid { grid-template-columns: 1fr; }
      .preise-grid { grid-template-columns: 1fr; }
      .price-card.featured { transform: scale(1); }
      .gallery-grid {
        grid-template-columns: 1fr 1fr;
        grid-template-rows: auto;
      }
      .g1,.g2,.g3,.g4,.g5,.g6,.g7,.g8,.g9 {
        grid-column: auto; grid-row: auto;
        height: 180px;
      }
      .testi-grid { grid-template-columns: 1fr; }
      .footer-grid { grid-template-columns: 1fr; gap: 28px; }
      .footer-bottom { flex-direction: column; text-align: center; }
      .footer-legal { justify-content: center; }
      .popup-box { padding: 40px 24px 32px; }
      .form-row { grid-template-columns: 1fr; }
    }

    @media (max-width: 480px) {
      .hero-cta { flex-direction: column; align-items: center; }
      .btn { width: 100%; max-width: 300px; justify-content: center; }
      .stats-grid { grid-template-columns: 1fr 1fr; }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after { animation-duration: .01ms !important; transition-duration: .01ms !important; }
    }
  </style>
</head>

<body>

  <!-- ═══════════════════════════════════════════
       TEIL 1: HTML – NAVIGATION
  ═══════════════════════════════════════════ -->
  <nav id="nav" role="navigation" aria-label="Hauptnavigation">
    <div class="container nav-inner">
      <a href="#hero" class="nav-logo" aria-label="Serenova Wellness Studio – Startseite">
        <span class="nav-logo-name">Serenova</span>
        <span class="nav-logo-sub">Wellness Studio München</span>
      </a>
      <ul class="nav-links" role="menubar">
        <li role="none"><a href="#ueber-uns" role="menuitem">Über uns</a></li>
        <li role="none"><a href="#leistungen" role="menuitem">Leistungen</a></li>
        <li role="none"><a href="#preise" role="menuitem">Preise</a></li>
        <li role="none"><a href="#galerie" role="menuitem">Galerie</a></li>
        <li role="none"><a href="#kontakt" role="menuitem">Kontakt</a></li>
      </ul>
      <button class="btn btn-primary btn-arrow nav-cta" onclick="openPopup()" aria-label="Termin buchen">
        Termin buchen
      </button>
      <button class="burger" id="burgerBtn" aria-label="Menü öffnen" aria-expanded="false" aria-controls="mobileMenu">
        <span></span><span></span><span></span>
      </button>
    </div>
  </nav>

  <!-- MOBILE MENU -->
  <div class="mobile-menu" id="mobileMenu" role="dialog" aria-modal="true" aria-label="Mobilmenü">
    <a href="#ueber-uns" class="mobile-link">Über uns</a>
    <a href="#leistungen" class="mobile-link">Leistungen</a>
    <a href="#preise" class="mobile-link">Preise</a>
    <a href="#galerie" class="mobile-link">Galerie</a>
    <a href="#kontakt" class="mobile-link">Kontakt</a>
    <button class="btn btn-primary btn-arrow" onclick="openPopup(); closeMobileMenu();">
      Termin buchen
    </button>
  </div>

  <!-- ═══════════════════════════════════════════
       HERO SECTION
  ═══════════════════════════════════════════ -->
  <section id="hero" aria-labelledby="hero-heading">
    <div class="hero-bg" role="img" aria-label="Entspannte Atmosphäre im Serenova Wellness Studio"></div>
    <div class="hero-content">
      <p class="hero-eyebrow">Premium Wellness · München</p>

      <!-- H1 – SEO Primary -->
      <h1 class="hero-h1" id="hero-heading">
        Wo Stille
        <em>zur Sprache wird.</em>
      </h1>

      <p class="hero-sub">
        Entdecken Sie die Kraft ganzheitlicher Körpertherapie – in einem Raum, der ausschließlich für Ihr Wohlbefinden geschaffen wurde.
      </p>
      <div class="hero-cta">
        <button class="btn btn-primary btn-arrow" onclick="openPopup()">
          Termin buchen
        </button>
        <a href="#leistungen" class="btn btn-ghost">
          Unsere Leistungen
        </a>
      </div>
    </div>
    <div class="hero-scroll" aria-hidden="true">
      <div class="scroll-line"></div>
      <span>Entdecken</span>
    </div>
  </section>

  <!-- STATS BAR -->
  <section id="stats" aria-label="Serenova in Zahlen">
    <div class="container">
      <div class="stats-grid">
        <div class="stat-item reveal">
          <div class="stat-num">12+</div>
          <div class="stat-label">Jahre Erfahrung</div>
        </div>
        <div class="stat-item reveal reveal-delay-1">
          <div class="stat-num">4.800+</div>
          <div class="stat-label">Zufriedene Gäste</div>
        </div>
        <div class="stat-item reveal reveal-delay-2">
          <div class="stat-num">98%</div>
          <div class="stat-label">Weiterempfehlungen</div>
        </div>
        <div class="stat-item reveal reveal-delay-3">
          <div class="stat-num">6</div>
          <div class="stat-label">Spezialisierungen</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══════════════════════════════════════════
       ÜBER UNS
  ═══════════════════════════════════════════ -->
  <section id="ueber-uns" aria-labelledby="ueber-heading">
    <div class="container">
      <div class="ueber-grid">
        <div class="ueber-img-wrap reveal">
          <div class="ueber-img-main" role="img" aria-label="Entspannendes Ambiente im Serenova Studio"></div>
          <div class="ueber-img-accent" role="img" aria-label="Detailaufnahme der hochwertigen Massagebehandlung"></div>
          <div class="ueber-gold-bar" aria-hidden="true">✦</div>
        </div>
        <div class="ueber-text">
          <p class="section-label">Über Serenova</p>
          <!-- H2 Über uns -->
          <h2 class="section-title" id="ueber-heading">
            Ein Ort, der <em>heilt</em> –<br>nicht nur entspannt.
          </h2>
          <div class="divider" aria-hidden="true"></div>
          <p class="reveal">
            Serenova wurde 2012 mit einer klaren Vision gegründet: Wellness jenseits des Gewöhnlichen. Unser Studio im Herzen Münchens vereint traditionelle Massagetechniken aus aller Welt mit moderner Körpertherapie – in einem Raum, der Ruhe, Schönheit und Heilung atmet.
          </p>
          <p class="reveal reveal-delay-1">
            Jede Behandlung wird individuell auf Ihre Bedürfnisse abgestimmt. Unsere zertifizierten Therapeuten begleiten Sie auf einem ganzheitlichen Weg zu mehr Vitalität, innerer Balance und körperlichem Wohlbefinden.
          </p>
          <div class="ueber-features">
            <div class="ueber-feat reveal reveal-delay-2">
              <div class="feat-icon" aria-hidden="true">✦</div>
              <div class="feat-body">
                <h4>Zertifizierte Experten</h4>
                <p>Alle Therapeuten verfügen über anerkannte Ausbildungen und langjährige Praxiserfahrung in ihren Fachgebieten.</p>
              </div>
            </div>
            <div class="ueber-feat reveal reveal-delay-3">
              <div class="feat-icon" aria-hidden="true">◈</div>
              <div class="feat-body">
                <h4>Exklusive Produkte</h4>
                <p>Wir arbeiten ausschließlich mit hochwertigen, natürlichen Ölen und Pflegeprodukten renommierter Marken.</p>
              </div>
            </div>
            <div class="ueber-feat reveal reveal-delay-4">
              <div class="feat-icon" aria-hidden="true">○</div>
              <div class="feat-body">
                <h4>Individuelle Betreuung</h4>
                <p>Vor jeder Behandlung führen wir ein ausführliches Gespräch, um Ihre persönlichen Ziele zu verstehen.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══════════════════════════════════════════
       LEISTUNGEN
  ═══════════════════════════════════════════ -->
  <section id="leistungen" aria-labelledby="leistungen-heading">
    <div class="container">
      <div class="leistungen-header reveal">
        <p class="section-label">Unsere Behandlungen</p>
        <!-- H2 Leistungen -->
        <h2 class="section-title" id="leistungen-heading">
          Sechs Wege zur <em>tiefen Entspannung</em>
        </h2>
      </div>
      <div class="services-grid">

        <!-- Service 1 -->
        <article class="service-card reveal">
          <div class="service-img">
            <img src="https://images.unsplash.com/photo-1544161515-4ab6ce6db874?w=600&q=80"
                 alt="Klassische Entspannungsmassage im Serenova Wellness Studio München"
                 loading="lazy" />
            <span class="service-tag">Bestseller</span>
          </div>
          <div class="service-body">
            <!-- H3 Service -->
            <h3>Klassische Entspannungsmassage</h3>
            <p>Die Grundlage aller Massagetechniken – sanfte bis mittlere Griffintensität löst Verspannungen, fördert die Durchblutung und lässt Körper und Geist zur Ruhe kommen.</p>
            <div class="service-footer">
              <div class="service-price">€ 79 <span>/ Sitzung</span></div>
              <span class="service-duration">60 Min</span>
            </div>
          </div>
        </article>

        <!-- Service 2 -->
        <article class="service-card reveal reveal-delay-1">
          <div class="service-img">
            <img src="https://images.unsplash.com/photo-1600334089648-b0d9d3028eb2?w=600&q=80"
                 alt="Tiefengewebsmassage zur Behandlung chronischer Verspannungen"
                 loading="lazy" />
            <span class="service-tag">Therapeutisch</span>
          </div>
          <div class="service-body">
            <h3>Tiefengewebsmassage</h3>
            <p>Gezielte Techniken erreichen tiefe Muskelschichten und Faszien. Ideal bei chronischen Verspannungen, Rückenbeschwerden und zur Regeneration nach dem Sport.</p>
            <div class="service-footer">
              <div class="service-price">€ 99 <span>/ Sitzung</span></div>
              <span class="service-duration">75 Min</span>
            </div>
          </div>
        </article>

        <!-- Service 3 -->
        <article class="service-card reveal reveal-delay-2">
          <div class="service-img">
            <img src="https://images.unsplash.com/photo-1515377905703-c4788e51af15?w=600&q=80"
                 alt="Hot Stone Massage mit erwärmten Basaltsteinen"
                 loading="lazy" />
            <span class="service-tag">Premium</span>
          </div>
          <div class="service-body">
            <h3>Hot Stone Massage</h3>
            <p>Erwärmte Basaltsteine gleiten über den Körper und geben ihre Wärme tief ins Gewebe ab. Diese Behandlung vereint Massage mit Wärmetherapie für maximale Entspannung.</p>
            <div class="service-footer">
              <div class="service-price">€ 119 <span>/ Sitzung</span></div>
              <span class="service-duration">90 Min</span>
            </div>
          </div>
        </article>

        <!-- Service 4 -->
        <article class="service-card reveal">
          <div class="service-img">
            <img src="https://images.unsplash.com/photo-1540555700478-4be289fbecef?w=600&q=80"
                 alt="Aromamassage mit ätherischen Ölen für Körper und Seele"
                 loading="lazy" />
          </div>
          <div class="service-body">
            <h3>Aroma-Wellnessmassage</h3>
            <p>Ausgewählte ätherische Öle werden individuell auf Ihre Bedürfnisse abgestimmt und in eine fließende Ganzkörpermassage eingebunden – ein Erlebnis für alle Sinne.</p>
            <div class="service-footer">
              <div class="service-price">€ 89 <span>/ Sitzung</span></div>
              <span class="service-duration">60 Min</span>
            </div>
          </div>
        </article>

        <!-- Service 5 -->
        <article class="service-card reveal reveal-delay-1">
          <div class="service-img">
            <img src="https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?w=600&q=80"
                 alt="Sportmassage für Athleten und aktive Menschen"
                 loading="lazy" />
            <span class="service-tag">Sport</span>
          </div>
          <div class="service-body">
            <h3>Sporttherapeutische Massage</h3>
            <p>Speziell für aktive Menschen: Vorbereitung auf Belastungen, schnellere Regeneration, gezielte Behandlung von Überbelastungsschäden und Muskelverkürzungen.</p>
            <div class="service-footer">
              <div class="service-price">€ 109 <span>/ Sitzung</span></div>
              <span class="service-duration">75 Min</span>
            </div>
          </div>
        </article>

        <!-- Service 6 -->
        <article class="service-card reveal reveal-delay-2">
          <div class="service-img">
            <img src="https://images.unsplash.com/photo-1591343395082-e120087004b4?w=600&q=80"
                 alt="Ayurvedische Massage nach traditioneller indischer Heilkunst"
                 loading="lazy" />
            <span class="service-tag">Ganzheitlich</span>
          </div>
          <div class="service-body">
            <h3>Ayurvedische Ganzkörpermassage</h3>
            <p>Die jahrtausendealte indische Heilkunst – warmes Kräuteröl, rhythmische Streichungen und Marma-Punkte-Aktivierung bringen Körper, Geist und Seele in Einklang.</p>
            <div class="service-footer">
              <div class="service-price">€ 129 <span>/ Sitzung</span></div>
              <span class="service-duration">90 Min</span>
            </div>
          </div>
        </article>

      </div>
    </div>
  </section>

  <!-- ═══════════════════════════════════════════
       PREISE
  ═══════════════════════════════════════════ -->
  <section id="preise" aria-labelledby="preise-heading">
    <div class="container">
      <div class="preise-header reveal">
        <p class="section-label">Unsere Pakete</p>
        <!-- H2 Preise -->
        <h2 class="section-title" id="preise-heading">
          Investieren Sie in <em>Ihr Wohlbefinden</em>
        </h2>
      </div>
      <div class="preise-grid">

        <!-- Basic -->
        <div class="price-card reveal">
          <p class="price-plan">Essential</p>
          <p class="price-name">Einstieg</p>
          <div class="price-amount">
            <span class="price-cur">€</span>
            <span class="price-val">79</span>
          </div>
          <p class="price-note">pro Einzelbehandlung</p>
          <ul class="price-features" aria-label="Leistungen im Essential-Paket">
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>1 Behandlung nach Wahl (60 Min)</li>
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>Persönliches Vorgespräch</li>
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>Hochwertige Naturöle</li>
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>Tee & Wasser inklusive</li>
            <li class="price-feat" style="opacity:.4"><span class="price-feat-check" aria-hidden="true">—</span>Ruhezeit nach Behandlung</li>
            <li class="price-feat" style="opacity:.4"><span class="price-feat-check" aria-hidden="true">—</span>Pflegeset zum Mitnehmen</li>
          </ul>
          <button class="btn btn-outline btn-arrow" onclick="openPopup()" aria-label="Essential-Paket buchen">
            Jetzt buchen
          </button>
        </div>

        <!-- Standard – FEATURED -->
        <div class="price-card featured reveal reveal-delay-1" aria-label="Empfohlenes Paket">
          <p class="price-badge">Meistgewählt</p>
          <p class="price-plan">Signature</p>
          <p class="price-name">Wellness</p>
          <div class="price-amount">
            <span class="price-cur">€</span>
            <span class="price-val">249</span>
          </div>
          <p class="price-note">3er-Paket · Gültigkeit 3 Monate</p>
          <ul class="price-features" aria-label="Leistungen im Signature-Paket">
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>3 Behandlungen nach Wahl (je 75 Min)</li>
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>Persönlicher Therapieplan</li>
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>Premium-Naturöle & Aromatherapie</li>
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>Ruhezeit in der Entspannungslounge</li>
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>Kräutertee & Snacks inklusive</li>
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>Pflegeset (Wert € 38)</li>
          </ul>
          <button class="btn btn-arrow" onclick="openPopup()" aria-label="Signature-Paket buchen">
            Jetzt buchen
          </button>
        </div>

        <!-- Premium -->
        <div class="price-card reveal reveal-delay-2">
          <p class="price-plan">Prestige</p>
          <p class="price-name">Retreat</p>
          <div class="price-amount">
            <span class="price-cur">€</span>
            <span class="price-val">599</span>
          </div>
          <p class="price-note">10er-Karte · Gültigkeit 12 Monate</p>
          <ul class="price-features" aria-label="Leistungen im Prestige-Paket">
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>10 Behandlungen frei wählbar</li>
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>Ganzheitlicher Wellness-Therapieplan</li>
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>Exklusive Luxuspflegeprodukte</li>
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>Prioritätsbuchung & flexible Zeiten</li>
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>Monatliches Fortschrittsgespräch</li>
            <li class="price-feat"><span class="price-feat-check" aria-hidden="true">✓</span>Exklusiver Gäste-Status & Rabatte</li>
          </ul>
          <button class="btn btn-outline btn-arrow" onclick="openPopup()" aria-label="Prestige-Paket buchen">
            Jetzt buchen
          </button>
        </div>

      </div>
    </div>
  </section>

  <!-- ═══════════════════════════════════════════
       GALERIE
  ═══════════════════════════════════════════ -->
  <section id="galerie" aria-labelledby="galerie-heading">
    <div class="container">
      <div class="galerie-header reveal">
        <p class="section-label">Eindrücke</p>
        <!-- H2 Galerie -->
        <h2 class="section-title" id="galerie-heading">
          Unser <em>Studio</em>
        </h2>
      </div>
      <div class="gallery-grid">
        <div class="g-item g1">
          <img src="https://images.unsplash.com/photo-1600334089648-b0d9d3028eb2?w=800&q=80"
               alt="Eleganter Massageraum mit warmem Licht im Serenova Studio" loading="lazy" />
        </div>
        <div class="g-item g2">
          <img src="https://images.unsplash.com/photo-1544161515-4ab6ce6db874?w=600&q=80"
               alt="Therapeutin bei der Schulter-Nackenmassage" loading="lazy" />
        </div>
        <div class="g-item g3">
          <img src="https://images.unsplash.com/photo-1540555700478-4be289fbecef?w=600&q=80"
               alt="Erholsames Ambiente im Wellnessbereich" loading="lazy" />
        </div>
        <div class="g-item g4">
          <img src="https://images.unsplash.com/photo-1515377905703-c4788e51af15?w=400&q=80"
               alt="Hochwertige Massageöle und Pflegeprodukte" loading="lazy" />
        </div>
        <div class="g-item g5">
          <img src="https://images.unsplash.com/photo-1591343395082-e120087004b4?w=400&q=80"
               alt="Detail-Aufnahme einer professionellen Fußreflexzonenmassage" loading="lazy" />
        </div>
        <div class="g-item g6">
          <img src="https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?w=600&q=80"
               alt="Sportmassage Behandlungsliege im hellen Therapieraum" loading="lazy" />
        </div>
        <div class="g-item g7">
          <img src="https://images.unsplash.com/photo-1519823551278-64ac92734fb1?w=500&q=80"
               alt="Entspannungslounge mit bequemen Sesseln und Naturmaterialien" loading="lazy" />
        </div>
        <div class="g-item g8">
          <img src="https://images.unsplash.com/photo-1470259078422-826894b933aa?w=700&q=80"
               alt="Empfangsbereich des Serenova Studios mit elegantem Design" loading="lazy" />
        </div>
        <div class="g-item g9">
          <img src="https://images.unsplash.com/photo-1583416750470-965b2707b355?w=700&q=80"
               alt="Kräutertee und Wohlfühlambiente nach der Massage" loading="lazy" />
        </div>
      </div>
    </div>
  </section>

  <!-- ═══════════════════════════════════════════
       TESTIMONIALS
  ═══════════════════════════════════════════ -->
  <section id="testimonials" aria-labelledby="testi-heading">
    <div class="container">
      <div class="testi-header reveal">
        <p class="section-label" style="justify-content:center">Das sagen unsere Gäste</p>
        <h2 class="section-title" id="testi-heading">
          Echte <em>Erlebnisse</em>
        </h2>
      </div>
      <div class="testi-grid">

        <div class="testi-card reveal">
          <div class="testi-stars" aria-label="5 von 5 Sternen">
            <span aria-hidden="true">★★★★★</span>
          </div>
          <p class="testi-text">„Nach der Tiefengewebsmassage war mein chronischer Rückenschmerz, der mich seit Monaten begleitet hat, endlich erträglich. Das Team ist einfühlsam, professionell und wirklich kompetent."</p>
          <div class="testi-author">
            <div class="testi-avatar" aria-hidden="true">MK</div>
            <div>
              <p class="testi-name">Markus Kellermann</p>
              <p class="testi-role">München · Stammgast seit 2021</p>
            </div>
          </div>
        </div>

        <div class="testi-card reveal reveal-delay-1">
          <div class="testi-stars" aria-label="5 von 5 Sternen">
            <span aria-hidden="true">★★★★★</span>
          </div>
          <p class="testi-text">„Die Aroma-Wellness-Massage war das Beste, was ich mir je gegönnt habe. Der Raum, die Düfte, das Licht – alles ist perfekt aufeinander abgestimmt. Ich komme seit zwei Jahren regelmäßig."</p>
          <div class="testi-author">
            <div class="testi-avatar" aria-hidden="true">SB</div>
            <div>
              <p class="testi-name">Sophie Baumann</p>
              <p class="testi-role">Schwabing · Wellness-Paket Kundin</p>
            </div>
          </div>
        </div>

        <div class="testi-card reveal reveal-delay-2">
          <div class="testi-stars" aria-label="5 von 5 Sternen">
            <span aria-hidden="true">★★★★★</span>
          </div>
          <p class="testi-text">„Als Leistungssportler war ich anfangs skeptisch. Doch die sporttherapeutische Massage hat meine Regeneration deutlich verbessert. Absolut empfehlenswert für alle Athleten."</p>
          <div class="testi-author">
            <div class="testi-avatar" aria-hidden="true">TH</div>
            <div>
              <p class="testi-name">Thomas Huber</p>
              <p class="testi-role">Maxvorstadt · Triathlet</p>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ═══════════════════════════════════════════
       KONTAKT
  ═══════════════════════════════════════════ -->
  <section id="kontakt" aria-labelledby="kontakt-heading">
    <div class="container">
      <div class="kontakt-grid">
        <div class="kontakt-info">
          <p class="section-label">Kontakt & Buchung</p>
          <!-- H2 Kontakt -->
          <h2 class="section-title" id="kontakt-heading">
            Ihre Auszeit<br><em>beginnt hier.</em>
          </h2>
          <div class="divider" aria-hidden="true"></div>
          <p class="reveal">
            Wir freuen uns, Sie persönlich kennenzulernen. Buchen Sie Ihren Wunschtermin online, telefonisch oder besuchen Sie uns direkt – wir beraten Sie gerne unverbindlich zu allen Behandlungen.
          </p>
          <div class="contact-details">
            <div class="contact-detail reveal">
              <div class="contact-icon" aria-hidden="true">📍</div>
              <div class="contact-text">
                <strong>Adresse</strong>
                <span>Maximilianstraße 42, 80538 München</span>
              </div>
            </div>
            <div class="contact-detail reveal reveal-delay-1">
              <div class="contact-icon" aria-hidden="true">📞</div>
              <div class="contact-text">
                <strong>Telefon</strong>
                <span><a href="tel:+4989123456789" style="color:inherit">+49 89 123 456 789</a></span>
              </div>
            </div>
            <div class="contact-detail reveal reveal-delay-2">
              <div class="contact-icon" aria-hidden="true">✉</div>
              <div class="contact-text">
                <strong>E-Mail</strong>
                <span><a href="mailto:info@serenova-wellness.de" style="color:inherit">info@serenova-wellness.de</a></span>
              </div>
            </div>
            <div class="contact-detail reveal reveal-delay-3">
              <div class="contact-icon" aria-hidden="true">🕐</div>
              <div class="contact-text">
                <strong>Öffnungszeiten</strong>
                <span>Mo–Fr: 9–21 Uhr · Sa–So: 10–19 Uhr</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Kontakt-Formular -->
        <div class="contact-form reveal" role="form" aria-labelledby="form-heading">
          <h3 id="form-heading">Termin anfragen</h3>
          <p class="form-sub">Hinterlassen Sie Ihre Daten – wir melden uns innerhalb von 24 Stunden.</p>
          <div class="form-row">
            <div class="form-group">
              <label for="cf-name">Vorname</label>
              <input type="text" id="cf-name" name="vorname" placeholder="Anna" autocomplete="given-name" required />
            </div>
            <div class="form-group">
              <label for="cf-nachname">Nachname</label>
              <input type="text" id="cf-nachname" name="nachname" placeholder="Müller" autocomplete="family-name" required />
            </div>
          </div>
          <div class="form-group">
            <label for="cf-phone">Telefonnummer</label>
            <input type="tel" id="cf-phone" name="telefon" placeholder="+49 89 …" autocomplete="tel" required />
          </div>
          <div class="form-group">
            <label for="cf-email">E-Mail</label>
            <input type="email" id="cf-email" name="email" placeholder="anna@beispiel.de" autocomplete="email" />
          </div>
          <div class="form-group">
            <label for="cf-service">Gewünschte Behandlung</label>
            <select id="cf-service" name="behandlung" required>
              <option value="" disabled selected>Bitte wählen …</option>
              <option>Klassische Entspannungsmassage (60 Min · €79)</option>
              <option>Tiefengewebsmassage (75 Min · €99)</option>
              <option>Hot Stone Massage (90 Min · €119)</option>
              <option>Aroma-Wellnessmassage (60 Min · €89)</option>
              <option>Sporttherapeutische Massage (75 Min · €109)</option>
              <option>Ayurvedische Ganzkörpermassage (90 Min · €129)</option>
              <option>Wellness-Paket (3er-Karte · €249)</option>
              <option>Retreat-Paket (10er-Karte · €599)</option>
            </select>
          </div>
          <div class="form-group">
            <label for="cf-message">Anmerkungen (optional)</label>
            <textarea id="cf-message" name="anmerkungen" placeholder="Gibt es etwas, das wir wissen sollten? Verletzungen, Allergien, besondere Wünsche …"></textarea>
          </div>
          <button class="btn btn-primary form-btn btn-arrow" type="button" onclick="submitContactForm()" aria-label="Anfrage absenden">
            Anfrage senden
          </button>
          <div class="form-success" id="cfSuccess" role="alert">
            ✓ Vielen Dank! Wir melden uns innerhalb von 24 Stunden bei Ihnen.
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══════════════════════════════════════════
       POPUP BOOKING FORM
  ═══════════════════════════════════════════ -->
  <div id="popup" role="dialog" aria-modal="true" aria-labelledby="popup-title">
    <div class="popup-overlay" onclick="closePopup()" aria-label="Schließen"></div>
    <div class="popup-box">
      <button class="popup-close" onclick="closePopup()" aria-label="Popup schließen">✕</button>
      <p class="popup-eyebrow">Serenova Wellness Studio</p>
      <h2 class="popup-title" id="popup-title">Termin buchen</h2>
      <p class="popup-sub">Wählen Sie Ihre Behandlung und wir bestätigen Ihren Termin innerhalb eines Werktages.</p>
      <div class="popup-form">
        <div class="form-row">
          <div class="form-group">
            <label for="p-name">Vorname *</label>
            <input type="text" id="p-name" placeholder="Anna" autocomplete="given-name" required />
          </div>
          <div class="form-group">
            <label for="p-last">Nachname *</label>
            <input type="text" id="p-last" placeholder="Müller" autocomplete="family-name" required />
          </div>
        </div>
        <div class="form-group">
          <label for="p-phone">Telefon *</label>
          <input type="tel" id="p-phone" placeholder="+49 89 …" autocomplete="tel" required />
        </div>
        <div class="form-group">
          <label for="p-email">E-Mail</label>
          <input type="email" id="p-email" placeholder="anna@beispiel.de" autocomplete="email" />
        </div>
        <div class="form-group">
          <label for="p-service">Behandlung *</label>
          <select id="p-service" required>
            <option value="" disabled selected>Bitte wählen …</option>
            <option>Klassische Entspannungsmassage (60 Min · €79)</option>
            <option>Tiefengewebsmassage (75 Min · €99)</option>
            <option>Hot Stone Massage (90 Min · €119)</option>
            <option>Aroma-Wellnessmassage (60 Min · €89)</option>
            <option>Sporttherapeutische Massage (75 Min · €109)</option>
            <option>Ayurvedische Ganzkörpermassage (90 Min · €129)</option>
            <option>Wellness-Paket (3er · €249)</option>
            <option>Retreat-Paket (10er · €599)</option>
          </select>
        </div>
        <div class="form-group">
          <label for="p-date">Wunschdatum</label>
          <input type="date" id="p-date" />
        </div>
        <button class="btn btn-primary form-btn btn-arrow" type="button" onclick="submitPopupForm()" aria-label="Buchung abschicken">
          Termin verbindlich anfragen
        </button>
        <div class="form-success" id="popupSuccess" role="alert">
          ✓ Danke für Ihre Anfrage! Wir melden uns innerhalb eines Werktages.
        </div>
      </div>
    </div>
  </div>

  <!-- ═══════════════════════════════════════════
       FOOTER
  ═══════════════════════════════════════════ -->
  <footer role="contentinfo">
    <div class="container">
      <div class="footer-grid">
        <div class="footer-brand">
          <span class="nav-logo-name" style="font-family:'Cormorant Garamond',serif;color:var(--white)">Serenova</span>
          <span class="nav-logo-sub">Wellness Studio München</span>
          <p>Ganzheitliche Körpertherapie und Premiumwellness im Herzen Münchens. Wo Stille zur Sprache wird.</p>
          <div class="footer-socials" aria-label="Social Media Links">
            <a href="#" class="social-btn" aria-label="Instagram">in</a>
            <a href="#" class="social-btn" aria-label="Facebook">fb</a>
            <a href="#" class="social-btn" aria-label="Pinterest">pt</a>
          </div>
        </div>
        <div class="footer-col">
          <h5>Leistungen</h5>
          <nav class="footer-links" aria-label="Leistungen Navigation">
            <a href="#leistungen">Klassische Massage</a>
            <a href="#leistungen">Tiefengewebsmassage</a>
            <a href="#leistungen">Hot Stone Massage</a>
            <a href="#leistungen">Aromamassage</a>
            <a href="#leistungen">Sportmassage</a>
            <a href="#leistungen">Ayurveda</a>
          </nav>
        </div>
        <div class="footer-col">
          <h5>Studio</h5>
          <nav class="footer-links" aria-label="Studio Navigation">
            <a href="#ueber-uns">Über uns</a>
            <a href="#preise">Preise & Pakete</a>
            <a href="#galerie">Galerie</a>
            <a href="#testimonials">Kundenstimmen</a>
            <a href="#kontakt">Kontakt</a>
          </nav>
        </div>
        <div class="footer-col">
          <h5>Kontakt</h5>
          <address class="footer-links" style="font-style:normal">
            <a href="https://maps.google.com" target="_blank" rel="noopener noreferrer">
              Maximilianstraße 42<br>80538 München
            </a>
            <a href="tel:+4989123456789">+49 89 123 456 789</a>
            <a href="mailto:info@serenova-wellness.de">info@serenova-wellness.de</a>
            <span style="font-size:.82rem;color:rgba(255,255,255,.35)">Mo–Fr: 9–21 Uhr<br>Sa–So: 10–19 Uhr</span>
          </address>
        </div>
      </div>
      <div class="footer-bottom">
        <p>© 2025 Serenova Wellness Studio GmbH · München</p>
        <nav class="footer-legal" aria-label="Rechtliche Links">
          <a href="#">Impressum</a>
          <a href="#">Datenschutz</a>
          <a href="#">AGB</a>
          <a href="#">Cookie-Einstellungen</a>
        </nav>
      </div>
    </div>
  </footer>

  <!-- ═══════════════════════════════════════════
       TEIL 3: JAVASCRIPT
  ═══════════════════════════════════════════ -->
  <script>
    /* ── NAV: Scroll-State ───────────────────── */
    const nav = document.getElementById('nav');
    let lastY = 0;

    function handleNavScroll() {
      const y = window.scrollY;
      if (y > 60) {
        nav.classList.add('scrolled');
      } else {
        nav.classList.remove('scrolled');
      }
      lastY = y;
    }

    window.addEventListener('scroll', handleNavScroll, { passive: true });
    handleNavScroll();

    /* ── BURGER MENU ─────────────────────────── */
    const burgerBtn = document.getElementById('burgerBtn');
    const mobileMenu = document.getElementById('mobileMenu');
    let menuOpen = false;

    function openMobileMenu() {
      menuOpen = true;
      burgerBtn.classList.add('open');
      mobileMenu.classList.add('open');
      burgerBtn.setAttribute('aria-expanded', 'true');
      document.body.style.overflow = 'hidden';
    }

    function closeMobileMenu() {
      menuOpen = false;
      burgerBtn.classList.remove('open');
      mobileMenu.classList.remove('open');
      burgerBtn.setAttribute('aria-expanded', 'false');
      document.body.style.overflow = '';
    }

    burgerBtn.addEventListener('click', () => {
      if (menuOpen) { closeMobileMenu(); } else { openMobileMenu(); }
    });

    // Close on mobile link click
    document.querySelectorAll('.mobile-link').forEach(link => {
      link.addEventListener('click', closeMobileMenu);
    });

    // Close on Escape
    document.addEventListener('keydown', e => {
      if (e.key === 'Escape') {
        closeMobileMenu();
        closePopup();
      }
    });

    /* ── POPUP BOOKING ───────────────────────── */
    const popup = document.getElementById('popup');

    function openPopup() {
      popup.classList.add('open');
      document.body.style.overflow = 'hidden';
      // focus first input for accessibility
      setTimeout(() => {
        const firstInput = popup.querySelector('input');
        if (firstInput) { firstInput.focus(); }
      }, 400);
    }

    function closePopup() {
      popup.classList.remove('open');
      document.body.style.overflow = '';
    }

    // Trap focus inside popup
    popup.addEventListener('keydown', e => {
      if (e.key !== 'Tab') { return; }
      const focusable = popup.querySelectorAll('input, select, textarea, button');
      const first = focusable[0];
      const last = focusable[focusable.length - 1];
      if (e.shiftKey) {
        if (document.activeElement === first) { e.preventDefault(); last.focus(); }
      } else {
        if (document.activeElement === last) { e.preventDefault(); first.focus(); }
      }
    });

    /* ── FORM VALIDATION HELPER ──────────────── */
    function validateForm(fields) {
      let valid = true;
      fields.forEach(id => {
        const el = document.getElementById(id);
        if (!el) { return; }
        const val = el.value.trim();
        if (!val || val === '') {
          el.style.borderColor = '#c0392b';
          el.style.boxShadow = '0 0 0 3px rgba(192,57,43,.15)';
          valid = false;
          el.addEventListener('input', function once() {
            el.style.borderColor = '';
            el.style.boxShadow = '';
            el.removeEventListener('input', once);
          });
        }
      });
      return valid;
    }

    /* ── CONTACT FORM SUBMIT ─────────────────── */
    function submitContactForm() {
      const ok = validateForm(['cf-name', 'cf-phone', 'cf-service']);
      if (!ok) { return; }
      const btn = document.querySelector('#kontakt .form-btn');
      btn.textContent = 'Wird gesendet …';
      btn.disabled = true;
      // Simulate async send
      setTimeout(() => {
        btn.style.display = 'none';
        document.getElementById('cfSuccess').style.display = 'block';
        // reset
        ['cf-name','cf-nachname','cf-phone','cf-email','cf-service','cf-message'].forEach(id => {
          const el = document.getElementById(id);
          if (el) { el.value = el.tagName === 'SELECT' ? '' : ''; }
        });
      }, 1200);
    }

    /* ── POPUP FORM SUBMIT ───────────────────── */
    function submitPopupForm() {
      const ok = validateForm(['p-name', 'p-phone', 'p-service']);
      if (!ok) { return; }
      const btn = document.querySelector('#popup .form-btn');
      btn.textContent = 'Wird gesendet …';
      btn.disabled = true;
      setTimeout(() => {
        btn.style.display = 'none';
        document.getElementById('popupSuccess').style.display = 'block';
        setTimeout(() => {
          closePopup();
          // reset popup form
          ['p-name','p-last','p-phone','p-email','p-service','p-date'].forEach(id => {
            const el = document.getElementById(id);
            if (el) { el.value = ''; }
          });
          btn.style.display = '';
          btn.disabled = false;
          btn.textContent = '';
          btn.innerHTML = 'Termin verbindlich anfragen <span style="font-size:1rem">→</span>';
          document.getElementById('popupSuccess').style.display = 'none';
        }, 3500);
      }, 1200);
    }

    /* ── SMOOTH SCROLL ───────────────────────── */
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        const target = document.querySelector(this.getAttribute('href'));
        if (!target) { return; }
        e.preventDefault();
        const navH = parseInt(getComputedStyle(document.documentElement).getPropertyValue('--nav-h'));
        const top = target.getBoundingClientRect().top + window.scrollY - navH - 12;
        window.scrollTo({ top, behavior: 'smooth' });
      });
    });

    /* ── SCROLL REVEAL ANIMATIONS ────────────── */
    const revealEls = document.querySelectorAll('.reveal');

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.12, rootMargin: '0px 0px -40px 0px' });

    revealEls.forEach(el => observer.observe(el));

    /* ── HERO PARALLAX (subtle) ──────────────── */
    const heroBg = document.querySelector('.hero-bg');
    if (heroBg && !window.matchMedia('(prefers-reduced-motion: reduce)').matches) {
      window.addEventListener('scroll', () => {
        const y = window.scrollY;
        if (y < window.innerHeight) {
          heroBg.style.transform = `translateY(${y * 0.28}px)`;
        }
      }, { passive: true });
    }

    /* ── STAT COUNTER ANIMATION ──────────────── */
    function animateCounter(el, target, suffix, duration) {
      const start = performance.now();
      const isFloat = target % 1 !== 0;

      function step(ts) {
        const progress = Math.min((ts - start) / duration, 1);
        const eased = 1 - Math.pow(1 - progress, 3);
        const current = eased * target;
        el.textContent = (isFloat ? current.toFixed(0) : Math.floor(current)) + suffix;
        if (progress < 1) { requestAnimationFrame(step); }
      }
      requestAnimationFrame(step);
    }

    const statNums = document.querySelectorAll('.stat-num');
    const counterData = [
      { val: 12, suffix: '+' },
      { val: 4800, suffix: '+' },
      { val: 98, suffix: '%' },
      { val: 6, suffix: '' },
    ];

    const statsObserver = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          statNums.forEach((el, i) => {
            if (counterData[i]) {
              animateCounter(el, counterData[i].val, counterData[i].suffix, 1600);
            }
          });
          statsObserver.disconnect();
        }
      });
    }, { threshold: 0.5 });

    const statsSection = document.getElementById('stats');
    if (statsSection) { statsObserver.observe(statsSection); }
  </script>

</body>
</html>
