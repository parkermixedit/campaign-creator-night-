<!DOCTYPE html>
<html lang="en" style="background-color:#000000;">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>VISION X CREATOR NIGHT — Complete Campaign</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Mono:ital,wght@0,300;0,400;0,500;1,300&family=Playfair+Display:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">
<style>
  :root {
    --black: #000000;
    --white: #ffffff;
    --gold: #5bc8d4;
    --gold-light: #7ddde6;
    --gold-dim: #2a7a82;
    --charcoal: #0d0d0d;
    --mid: #111111;
    --border: rgba(91,200,212,0.2);
    --text-dim: rgba(255,255,255,0.45);
    --text-mid: rgba(255,255,255,0.7);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; color: inherit; }

  a { text-decoration: none; color: inherit; }

  strong, em, b, i, span, p, li, td, th, h1, h2, h3, h4, h5, h6, div, label, button { color: inherit; }

  html {
    scroll-behavior: smooth;
    background-color: #000000;
  }

  body {
    background-color: #000000;
    background: #000000;
    color: #ffffff;
    font-family: 'DM Mono', 'Courier New', monospace;
    font-weight: 300;
    line-height: 1.65;
    overflow-x: hidden;
  }

  /* ═══ HERO ═══ */
  .hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    position: relative;
    padding: 60px 24px;
    overflow: hidden;
    background-color: #000000;
  }

  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse 70% 50% at 50% 40%, rgba(91,200,212,0.10) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero-eyebrow {
    font-family: 'DM Mono', 'Courier New', monospace;
    font-size: 11px;
    letter-spacing: 0.35em;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 28px;
    animation: fadeUp 0.8s ease both;
  }

  .hero-title {
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: clamp(72px, 14vw, 160px);
    line-height: 0.9;
    letter-spacing: 0.02em;
    color: var(--white);
    margin-bottom: 12px;
    animation: fadeUp 0.8s 0.1s ease both;
  }

  .hero-title span {
    color: var(--gold);
    display: block;
  }

  .hero-subtitle {
    font-family: 'Playfair Display', Georgia, serif;
    font-style: italic;
    font-size: clamp(16px, 3vw, 26px);
    color: rgba(255,255,255,0.85);
    margin-bottom: 40px;
    animation: fadeUp 0.8s 0.2s ease both;
  }

  .hero-meta {
    display: flex;
    gap: 40px;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 60px;
    animation: fadeUp 0.8s 0.3s ease both;
  }

  .hero-meta-item {
    text-align: center;
  }

  .hero-meta-label {
    font-size: 10px;
    letter-spacing: 0.3em;
    color: var(--gold);
    text-transform: uppercase;
    display: block;
    margin-bottom: 4px;
  }

  .hero-meta-value {
    font-size: 14px;
    color: var(--white);
  }

  .hero-divider {
    width: 100%;
    max-width: 600px;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--gold), transparent);
    margin: 0 auto 40px;
    animation: fadeUp 0.8s 0.35s ease both;
  }

  /* ═══ NAV ═══ */
  .nav {
    position: sticky;
    top: 0;
    z-index: 100;
    background: rgba(0,0,0,0.97);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    padding: 0 24px;
    overflow-x: auto;
    scrollbar-width: none;
  }

  .nav::-webkit-scrollbar { display: none; }

  .nav-inner {
    display: flex;
    gap: 0;
    min-width: max-content;
    max-width: 1400px;
    margin: 0 auto;
  }

  .nav-link {
    font-size: 10px;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--text-dim);
    text-decoration: none;
    padding: 18px 20px;
    transition: color 0.2s;
    white-space: nowrap;
    border-bottom: 2px solid transparent;
  }

  .nav-link:hover {
    color: var(--gold);
    border-bottom-color: var(--gold);
  }

  /* ═══ SECTIONS ═══ */
  .section {
    max-width: 1400px;
    margin: 0 auto;
    padding: 80px 24px;
    border-bottom: 1px solid var(--border);
    background-color: #000000;
  }

  .section-label {
    font-size: 10px;
    letter-spacing: 0.4em;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 16px;
    display: block;
  }

  .section-title {
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: clamp(40px, 6vw, 72px);
    line-height: 1;
    margin-bottom: 40px;
    color: var(--white);
  }

  .section-intro {
    font-size: 15px;
    color: var(--text-mid);
    max-width: 680px;
    margin-bottom: 48px;
    line-height: 1.8;
  }

  /* ═══ STRATEGY BLOCKS ═══ */
  .strategy-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
  }

  .strategy-block {
    background: var(--charcoal);
    padding: 36px;
    transition: background 0.2s;
  }

  .strategy-block:hover { background: var(--mid); }

  .strategy-block-num {
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: 48px;
    color: var(--gold);
    opacity: 0.3;
    line-height: 1;
    margin-bottom: 12px;
  }

  .strategy-block-title {
    font-size: 11px;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 12px;
  }

  .strategy-block-body {
    font-size: 14px;
    color: var(--text-mid);
    line-height: 1.8;
  }

  /* ═══ PILLARS ═══ */
  .pillars {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 24px;
  }

  .pillar {
    border: 1px solid var(--border);
    padding: 32px 24px;
    position: relative;
    overflow: hidden;
    transition: border-color 0.2s;
  }

  .pillar::before {
    content: '';
    position: absolute;
    bottom: 0; left: 0;
    width: 100%; height: 3px;
    background: var(--gold);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s ease;
  }

  .pillar:hover::before { transform: scaleX(1); }
  .pillar:hover { border-color: rgba(91,200,212,0.4); }

  .pillar-icon {
    font-size: 28px;
    margin-bottom: 16px;
    display: block;
  }

  .pillar-title {
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: 22px;
    color: var(--gold);
    margin-bottom: 10px;
    letter-spacing: 0.05em;
  }

  .pillar-body {
    font-size: 13px;
    color: var(--text-mid);
    line-height: 1.7;
  }

  /* ═══ CONTENT CARDS ═══ */
  .tabs {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    margin-bottom: 32px;
  }

  .tab {
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    padding: 10px 20px;
    border: 1px solid var(--border);
    background: transparent;
    color: var(--text-dim);
    cursor: pointer;
    transition: all 0.2s;
    font-family: 'DM Mono', 'Courier New', monospace;
  }

  .tab:hover, .tab.active {
    border-color: var(--gold);
    color: var(--gold);
    background: rgba(91,200,212,0.06);
  }

  .tab-content { display: none; }
  .tab-content.active { display: block; }

  .content-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
    gap: 20px;
  }

  .content-card {
    border: 1px solid var(--border);
    background: var(--charcoal);
    padding: 28px;
    transition: all 0.2s;
    position: relative;
  }

  .content-card:hover {
    border-color: rgba(91,200,212,0.35);
    background: var(--mid);
  }

  .card-num {
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: 36px;
    color: var(--gold);
    opacity: 0.25;
    line-height: 1;
    position: absolute;
    top: 20px;
    right: 20px;
  }

  .card-type {
    font-size: 9px;
    letter-spacing: 0.35em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 12px;
    display: block;
  }

  .card-hook {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: 17px;
    font-style: italic;
    color: var(--white);
    margin-bottom: 16px;
    line-height: 1.5;
    padding-right: 40px;
  }

  .card-row {
    margin-bottom: 10px;
  }

  .card-row-label {
    font-size: 9px;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--gold-dim);
    display: block;
    margin-bottom: 3px;
  }

  .card-row-value {
    font-size: 12px;
    color: var(--text-mid);
    line-height: 1.6;
  }

  .card-cta {
    margin-top: 16px;
    padding: 10px 16px;
    border: 1px solid var(--gold-dim);
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    display: inline-block;
  }

  /* ═══ CALENDAR ═══ */
  .calendar-week {
    margin-bottom: 32px;
  }

  .calendar-week-label {
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: 28px;
    color: var(--gold);
    margin-bottom: 12px;
    letter-spacing: 0.05em;
  }

  .calendar-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 12px;
  }

  .calendar-table th {
    text-align: left;
    padding: 10px 14px;
    font-size: 9px;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--gold);
    border-bottom: 1px solid var(--border);
    background: rgba(91,200,212,0.04);
  }

  .calendar-table td {
    padding: 12px 14px;
    border-bottom: 1px solid rgba(255,255,255,0.04);
    color: var(--text-mid);
    vertical-align: top;
    line-height: 1.5;
  }

  .calendar-table tr:hover td {
    background: rgba(91,200,212,0.03);
    color: var(--white);
  }

  .cal-date {
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: 18px;
    color: var(--white);
    white-space: nowrap;
  }

  .cal-platform {
    display: inline-block;
    padding: 2px 8px;
    font-size: 9px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    border: 1px solid var(--border);
    color: var(--gold);
    white-space: nowrap;
  }

  .priority-high { border-color: var(--gold); color: var(--gold); background: rgba(91,200,212,0.08); }
  .priority-med { border-color: rgba(91,200,212,0.4); color: rgba(91,200,212,0.7); }
  .priority-low { border-color: var(--border); color: var(--text-dim); }

  /* ═══ GUERRILLA ═══ */
  .guerrilla-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 20px;
  }

  .guerrilla-block {
    border: 1px solid var(--border);
    padding: 32px;
    background: var(--charcoal);
  }

  .guerrilla-block-title {
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: 26px;
    color: var(--white);
    margin-bottom: 6px;
    letter-spacing: 0.05em;
  }

  .guerrilla-block-sub {
    font-size: 10px;
    letter-spacing: 0.3em;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 20px;
    display: block;
  }

  .action-list {
    list-style: none;
  }

  .action-list li {
    font-size: 13px;
    color: var(--text-mid);
    padding: 8px 0;
    border-bottom: 1px solid rgba(255,255,255,0.04);
    display: flex;
    gap: 10px;
    line-height: 1.5;
  }

  .action-list li::before {
    content: '→';
    color: var(--gold);
    flex-shrink: 0;
    margin-top: 1px;
  }

  /* ═══ LEAD + FOLLOW-UP ═══ */
  .flow-steps {
    display: flex;
    flex-direction: column;
    gap: 0;
    border: 1px solid var(--border);
  }

  .flow-step {
    display: grid;
    grid-template-columns: 80px 1fr;
    gap: 0;
    border-bottom: 1px solid var(--border);
    transition: background 0.2s;
  }

  .flow-step:last-child { border-bottom: none; }
  .flow-step:hover { background: rgba(91,200,212,0.03); }

  .flow-step-num {
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: 32px;
    color: var(--gold);
    border-right: 1px solid var(--border);
    opacity: 0.5;
    padding: 24px 0;
  }

  .flow-step-body {
    padding: 24px 28px;
  }

  .flow-step-title {
    font-size: 13px;
    color: var(--white);
    margin-bottom: 6px;
    font-weight: 500;
    letter-spacing: 0.05em;
  }

  .flow-step-desc {
    font-size: 12px;
    color: var(--text-mid);
    line-height: 1.7;
  }

  /* ═══ POSITIONING ═══ */
  .big-statement {
    border: 1px solid var(--border);
    padding: 60px 48px;
    text-align: center;
    background: var(--charcoal);
    margin-bottom: 40px;
    position: relative;
    overflow: hidden;
  }

  .big-statement::before {
    content: '"';
    font-family: 'Playfair Display', Georgia, serif;
    font-size: 200px;
    color: var(--gold);
    opacity: 0.04;
    position: absolute;
    top: -20px;
    left: 20px;
    line-height: 1;
  }

  .big-statement-text {
    font-family: 'Playfair Display', Georgia, serif;
    font-size: clamp(20px, 3.5vw, 34px);
    font-style: italic;
    color: var(--white);
    line-height: 1.5;
    position: relative;
    max-width: 800px;
    margin: 0 auto;
  }

  .tagline-block {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 24px;
  }

  .tagline-option {
    text-align: center;
    padding: 28px 40px;
    border: 1px solid var(--border);
    max-width: 600px;
    width: 100%;
    transition: border-color 0.2s;
  }

  .tagline-option:hover { border-color: rgba(91,200,212,0.4); }

  .tagline-option-text {
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: 32px;
    letter-spacing: 0.05em;
    color: var(--white);
    margin-bottom: 8px;
  }

  .tagline-option-note {
    font-size: 11px;
    color: var(--text-dim);
    letter-spacing: 0.1em;
  }

  /* ═══ REEL IDEAS ═══ */
  .reel-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 16px;
  }

  .reel-card {
    border: 1px solid var(--border);
    background: var(--charcoal);
    padding: 24px;
    transition: all 0.2s;
  }

  .reel-card:hover {
    border-color: rgba(91,200,212,0.3);
    transform: translateY(-2px);
  }

  .reel-num {
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: 14px;
    color: var(--gold);
    letter-spacing: 0.2em;
    margin-bottom: 10px;
    display: block;
  }

  .reel-title {
    font-size: 14px;
    color: var(--white);
    margin-bottom: 10px;
    font-weight: 500;
    line-height: 1.4;
  }

  .reel-desc {
    font-size: 12px;
    color: var(--text-mid);
    line-height: 1.65;
  }

  .reel-format {
    margin-top: 12px;
    font-size: 10px;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--gold-dim);
  }

  /* ═══ STORY CARDS ═══ */
  .story-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 16px;
  }

  .story-card {
    border: 1px solid var(--border);
    padding: 28px 22px;
    background: var(--charcoal);
    transition: all 0.2s;
    aspect-ratio: auto;
  }

  .story-card:hover {
    border-color: rgba(91,200,212,0.3);
  }

  .story-day {
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: 40px;
    color: var(--gold);
    opacity: 0.3;
    line-height: 1;
    margin-bottom: 8px;
  }

  .story-title {
    font-size: 13px;
    font-weight: 500;
    color: var(--white);
    margin-bottom: 8px;
    letter-spacing: 0.03em;
  }

  .story-desc {
    font-size: 12px;
    color: var(--text-mid);
    line-height: 1.65;
  }

  /* ═══ COUNTDOWN ═══ */
  .countdown-list {
    display: flex;
    flex-direction: column;
    gap: 0;
    border: 1px solid var(--border);
  }

  .countdown-item {
    display: grid;
    grid-template-columns: 120px 1fr;
    border-bottom: 1px solid var(--border);
    transition: background 0.2s;
  }

  .countdown-item:last-child { border-bottom: none; }
  .countdown-item:hover { background: rgba(91,200,212,0.03); }

  .countdown-days {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border-right: 1px solid var(--border);
    padding: 20px;
  }

  .countdown-days-num {
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: 42px;
    color: var(--gold);
    line-height: 1;
  }

  .countdown-days-label {
    font-size: 9px;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--text-dim);
  }

  .countdown-body {
    padding: 20px 24px;
  }

  .countdown-hook {
    font-size: 14px;
    color: var(--white);
    margin-bottom: 6px;
    font-weight: 500;
  }

  .countdown-desc {
    font-size: 12px;
    color: var(--text-mid);
    line-height: 1.6;
  }

  /* ═══ CONVERSION PATHS ═══ */
  .conversion-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 20px;
  }

  .conversion-card {
    border: 1px solid var(--border);
    padding: 32px 24px;
    background: var(--charcoal);
    text-align: center;
  }

  .conversion-icon {
    font-size: 36px;
    display: block;
    margin-bottom: 16px;
  }

  .conversion-title {
    font-family: 'Bebas Neue', Impact, sans-serif;
    font-size: 24px;
    color: var(--white);
    margin-bottom: 10px;
    letter-spacing: 0.05em;
  }

  .conversion-steps {
    list-style: none;
    text-align: left;
  }

  .conversion-steps li {
    font-size: 12px;
    color: var(--text-mid);
    padding: 6px 0;
    border-bottom: 1px solid rgba(255,255,255,0.05);
    display: flex;
    gap: 8px;
    line-height: 1.5;
  }

  .conversion-steps li::before {
    content: '→';
    color: var(--gold);
    flex-shrink: 0;
  }

  /* ═══ UTILS ═══ */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .gold { color: var(--gold); }
  .italic { font-style: italic; }

  .two-col {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 48px;
    align-items: start;
  }

  @media (max-width: 768px) {
    .two-col { grid-template-columns: 1fr; gap: 32px; }
    .flow-step { grid-template-columns: 60px 1fr; }
    .countdown-item { grid-template-columns: 90px 1fr; }
    .calendar-table { font-size: 11px; }
    .calendar-table th, .calendar-table td { padding: 8px 10px; }
  }

  .divider {
    width: 100%;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--gold), transparent);
    margin: 48px 0;
    opacity: 0.3;
  }

  .highlight-box {
    border: 1px solid var(--gold);
    background: rgba(91,200,212,0.05);
    padding: 28px 32px;
    margin: 24px 0;
  }

  .highlight-box p {
    font-size: 14px;
    color: var(--text-mid);
    line-height: 1.8;
  }

  .highlight-box strong {
    color: var(--gold);
    font-weight: 400;
  }

  footer {
    text-align: center;
    padding: 48px 24px;
    font-size: 11px;
    letter-spacing: 0.2em;
    color: var(--text-dim);
    text-transform: uppercase;
    border-top: 1px solid var(--border);
    background-color: #000000;
  }

  /* ═══ NUCLEAR BLACK BG OVERRIDE — no white anywhere ═══ */
  html, body, .hero, .nav, .nav-inner,
  .section, .strategy-grid, .strategy-block,
  .pillars, .pillar, .tabs, .tab-content,
  .content-grid, .content-card, .reel-grid,
  .reel-card, .story-grid, .story-card,
  .countdown-list, .countdown-item, .countdown-body,
  .flow-steps, .flow-step, .flow-step-body,
  .guerrilla-grid, .guerrilla-block,
  .conversion-grid, .conversion-card,
  .tagline-block, .tagline-option,
  .big-statement, .highlight-box,
  .calendar-week, .two-col, footer {
    background-color: #000000;
  }

  /* Dark card surfaces stay slightly lifted */
  .strategy-block, .content-card, .reel-card,
  .story-card, .guerrilla-block, .conversion-card,
  .big-statement, .flow-step-body {
    background-color: #0d0d0d;
  }

  .highlight-box {
    background-color: rgba(91,200,212,0.06);
  }

  .tagline-option {
    background-color: #0d0d0d;
  }

  /* Calendar table */
  .calendar-table, .calendar-table thead,
  .calendar-table tbody, .calendar-table tr,
  .calendar-table td, .calendar-table th {
    background-color: #000000;
    color: #ffffff;
  }

  .calendar-table th {
    background-color: #0d0d0d;
    color: var(--gold);
  }

  .calendar-table tr:hover td {
    background-color: rgba(91,200,212,0.05);
    color: #ffffff;
  }
</style>
</head>
<body style="background-color:#000000;background:#000000;color:#ffffff;min-height:100vh;">

<!-- HERO -->
<div class="hero">
  <div class="hero-eyebrow">Vision X Studios — Complete Campaign Document</div>
  <div class="hero-title">
    Creator<br><span>Night</span>
  </div>
  <div class="hero-subtitle">Charlotte's Creative Ecosystem — June 27, 2026</div>
  <div class="hero-divider"></div>
  <div class="hero-meta">
    <div class="hero-meta-item">
      <span class="hero-meta-label">Event Date</span>
      <span class="hero-meta-value">June 27, 2026</span>
    </div>
    <div class="hero-meta-item">
      <span class="hero-meta-label">Location</span>
      <span class="hero-meta-value">Vision X Studios, Pineville NC</span>
    </div>
    <div class="hero-meta-item">
      <span class="hero-meta-label">Target</span>
      <span class="hero-meta-value">40+ Attendees</span>
    </div>
    <div class="hero-meta-item">
      <span class="hero-meta-label">Campaign Start</span>
      <span class="hero-meta-value">June 6, 2026</span>
    </div>
  </div>
</div>

<!-- NAV -->
<nav class="nav">
  <div class="nav-inner">
    <a class="nav-link" href="#strategy">Strategy</a>
    <a class="nav-link" href="#positioning">Positioning</a>
    <a class="nav-link" href="#pillars">Pillars</a>
    <a class="nav-link" href="#content">Content</a>
    <a class="nav-link" href="#reels">Reels</a>
    <a class="nav-link" href="#stories">Stories</a>
    <a class="nav-link" href="#countdown">Countdown</a>
    <a class="nav-link" href="#calendar">Calendar</a>
    <a class="nav-link" href="#guerrilla">Guerrilla</a>
    <a class="nav-link" href="#leads">Lead Capture</a>
    <a class="nav-link" href="#followup">Follow-Up</a>
    <a class="nav-link" href="#meta">Meta Ads</a>
    <a class="nav-link" href="#outreach">CLT Outreach</a>
  </div>
</nav>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION 1: CAMPAIGN STRATEGY -->
<!-- ═══════════════════════════════════════════════ -->
<section class="section" id="strategy">
  <span class="section-label">Section 01</span>
  <h2 class="section-title">Campaign Strategy</h2>
  <p class="section-intro">The lens through which every decision is made. This is not an event campaign. This is the launch of a movement — and Creator Night is the proof of concept Charlotte didn't know it was waiting for.</p>

  <div class="strategy-grid">
    <div class="strategy-block">
      <div class="strategy-block-num">01</div>
      <div class="strategy-block-title">Campaign Theme</div>
      <div class="strategy-block-body">
        <strong style="color:var(--white)">THE ECOSYSTEM OPENS ITS DOORS.</strong><br><br>
        Vision X has been operating. People have been inside. Something has been building. Creator Night is the moment the doors swing open — and the world gets to see what's been here the whole time. The campaign creates FOMO before the event and delivers a transformative experience that converts attendees into long-term ecosystem participants.
      </div>
    </div>
    <div class="strategy-block">
      <div class="strategy-block-num">02</div>
      <div class="strategy-block-title">Core Strategy</div>
      <div class="strategy-block-body">
        Three-phase attack:<br><br>
        <strong style="color:var(--gold)">INTRIGUE</strong> — Tease what's inside without showing everything. Build mystery around the space, the people, and the access.<br><br>
        <strong style="color:var(--gold)">INVITATION</strong> — Make every creator in Charlotte feel personally summoned. Not invited. Summoned.<br><br>
        <strong style="color:var(--gold)">INCLUSION</strong> — During and after, convert presence into participation, participation into clients.
      </div>
    </div>
    <div class="strategy-block">
      <div class="strategy-block-num">03</div>
      <div class="strategy-block-title">Emotional Objective</div>
      <div class="strategy-block-body">
        Every piece of content should trigger one of three feelings:<br><br>
        <strong style="color:var(--gold)">FOMO</strong> — "I need to be there."<br><br>
        <strong style="color:var(--gold)">RECOGNITION</strong> — "This is made for someone like me."<br><br>
        <strong style="color:var(--gold)">ASPIRATION</strong> — "This is the level I want to operate at."<br><br>
        If a post doesn't create at least one of these feelings, it doesn't go out.
      </div>
    </div>
    <div class="strategy-block">
      <div class="strategy-block-num">04</div>
      <div class="strategy-block-title">Platform Priority</div>
      <div class="strategy-block-body">
        <strong style="color:var(--gold)">Instagram</strong> — Primary. Feed posts + Reels for reach, Stories for urgency, DMs for direct conversion.<br><br>
        <strong style="color:var(--gold)">TikTok</strong> — Reels repurposed. Reach younger creators and artists.<br><br>
        <strong style="color:var(--gold)">Facebook</strong> — Event listing + community groups for Charlotte entrepreneurs and business owners.<br><br>
        <strong style="color:var(--gold)">LinkedIn</strong> — Business owners, podcasters, personal brands.<br><br>
        <strong style="color:var(--gold)">SMS / Email</strong> — Existing contacts. Direct. Highest conversion rate.
      </div>
    </div>
    <div class="strategy-block">
      <div class="strategy-block-num">05</div>
      <div class="strategy-block-title">Content Ratio</div>
      <div class="strategy-block-body">
        60% — Show the ecosystem, the space, the people, the culture<br><br>
        25% — Event-specific promotional posts<br><br>
        15% — Direct calls to register / attend<br><br>
        Never lead with selling. Lead with belonging. The content should make people feel like they're already part of something before they've ever walked through the door.
      </div>
    </div>
    <div class="strategy-block">
      <div class="strategy-block-num">06</div>
      <div class="strategy-block-title">Registration System</div>
      <div class="strategy-block-body">
        Free event with required registration. Registration is the first filter and the first lead capture.<br><br>
        Form fields: Name, Instagram handle, phone, what best describes you (multi-select: artist, creator, business, podcaster, etc.), what services are you most interested in (multi-select).<br><br>
        This data segments your post-event outreach from day one.
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION 2: POSITIONING -->
<!-- ═══════════════════════════════════════════════ -->
<section class="section" id="positioning">
  <span class="section-label">Section 02</span>
  <h2 class="section-title">Positioning & Taglines</h2>

  <div class="big-statement">
    <div class="big-statement-text">
      Vision X Creator Night is not a networking event. It's the first time Charlotte's creative underground surfaces — and the room you'll be talking about for the rest of the year.
    </div>
  </div>

  <div class="divider"></div>

  <h3 style="font-family:'Bebas Neue',sans-serif;font-size:32px;color:var(--gold);letter-spacing:0.05em;margin-bottom:24px;">Event Positioning Statement</h3>
  <div class="highlight-box" style="margin-bottom:40px;">
    <p>Vision X Creator Night is the exclusive gathering where Charlotte's most ambitious creators, artists, entrepreneurs, and content professionals get their first real look inside the region's most complete creative ecosystem. This is not a seminar. Not a pitch fest. Not a mixer. This is an <strong>immersive experience</strong> designed to show you what's possible — and introduce you to the people who can help you get there. One night. One space. One shift in what you think is available to you.</p>
  </div>

  <h3 style="font-family:'Bebas Neue',sans-serif;font-size:32px;color:var(--gold);letter-spacing:0.05em;margin-bottom:24px;">Tagline Options</h3>
  <div class="tagline-block">
    <div class="tagline-option" style="border-color:var(--gold);background:rgba(91,200,212,0.06);">
      <div class="tagline-option-text">GET IN THE ROOM.</div>
      <div class="tagline-option-note">⭐ Primary Recommendation — Direct. Exclusive. Command. Dual meaning: be in the physical room and be in the right circles.</div>
    </div>
    <div class="tagline-option">
      <div class="tagline-option-text">THE ECOSYSTEM IS OPEN.</div>
      <div class="tagline-option-note">Brand-forward. Works for long-term use beyond the event.</div>
    </div>
    <div class="tagline-option">
      <div class="tagline-option-text">YOUR CITY. YOUR STUDIO. YOUR NIGHT.</div>
      <div class="tagline-option-note">Community-forward. Creates ownership and belonging.</div>
    </div>
    <div class="tagline-option">
      <div class="tagline-option-text">THIS IS WHAT YOU'VE BEEN MISSING.</div>
      <div class="tagline-option-note">Pure FOMO. Aggressive. Works for late push content.</div>
    </div>
    <div class="tagline-option">
      <div class="tagline-option-text">WHERE CHARLOTTE CREATES.</div>
      <div class="tagline-option-note">Long-term Vision X brand tagline. Plant it here, own it forever.</div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION 3: MESSAGING PILLARS -->
<!-- ═══════════════════════════════════════════════ -->
<section class="section" id="pillars">
  <span class="section-label">Section 03</span>
  <h2 class="section-title">Core Messaging Pillars</h2>
  <p class="section-intro">Every caption, hook, and call to action lives under one of these five pillars. This is your filter. If a piece of content doesn't clearly belong to a pillar, it doesn't go out.</p>

  <div class="pillars">
    <div class="pillar">
      <span class="pillar-icon">🏛️</span>
      <div class="pillar-title">The Access</div>
      <div class="pillar-body">Vision X gives you access to professional tools, a professional team, and a professional environment — without the label deal, the budget, or the gatekeepers. Creator Night is the first step inside. Message: <em>"This exists. It's here. And it's yours."</em></div>
    </div>
    <div class="pillar">
      <span class="pillar-icon">🔥</span>
      <div class="pillar-title">The Standard</div>
      <div class="pillar-body">Vision X is not a budget option. It is the standard of excellence in Charlotte. Every interaction, every photo, every post communicates that this is where serious people come to do serious work. Message: <em>"You've been settling. You don't have to anymore."</em></div>
    </div>
    <div class="pillar">
      <span class="pillar-icon">👥</span>
      <div class="pillar-title">The Community</div>
      <div class="pillar-body">The creators who attend Creator Night are already in the ecosystem. They just don't know each other yet. VX is the connector — the hub where Charlotte's creative talent finds itself. Message: <em>"Your next collaborator is already in this room."</em></div>
    </div>
    <div class="pillar">
      <span class="pillar-icon">⚡</span>
      <div class="pillar-title">The Moment</div>
      <div class="pillar-body">Charlotte is having a creative moment. Music. Content. Brand. The city is producing. Vision X is where that momentum gets professionalized. Creator Night is the flag in the ground. Message: <em>"Charlotte is building something. This is where it lives."</em></div>
    </div>
    <div class="pillar">
      <span class="pillar-icon">🎯</span>
      <div class="pillar-title">The Transformation</div>
      <div class="pillar-body">People don't come to Creator Night for free stuff. They come to be changed — to see what's possible, find their next step, and leave with a clear picture of who they're building toward. Message: <em>"You'll walk in one person and leave with a plan."</em></div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION 4: CONTENT — 30 IG POSTS -->
<!-- ═══════════════════════════════════════════════ -->
<section class="section" id="content">
  <span class="section-label">Section 04</span>
  <h2 class="section-title">Content Library</h2>

  <div class="tabs">
    <button class="tab active" onclick="showTab('ig-posts')">30 IG Posts</button>
    <button class="tab" onclick="showTab('giveaways')">10 Giveaway Posts</button>
    <button class="tab" onclick="showTab('community')">10 Community Posts</button>
    <button class="tab" onclick="showTab('bts')">10 BTS Posts</button>
  </div>

  <!-- IG POSTS -->
  <div id="ig-posts" class="tab-content active">
    <div class="content-grid">

      <!-- POST 1 -->
      <div class="content-card">
        <div class="card-num">01</div>
        <span class="card-type">Announcement / Pillar: The Access</span>
        <div class="card-hook">"The doors are opening."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">June 27. Vision X Studios. One night where Charlotte's creative ecosystem opens its doors to the people who belong inside it. Creators. Artists. Producers. Podcasters. Entrepreneurs. You're invited. Creator Night. Free. One night only. Link in bio to register.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Wide shot of the studio — dark, moody, one warm light source. No people. Just the space breathing.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Announce the event. Create intrigue.</span></div>
        <div class="card-cta">Register Now — Link in Bio</div>
      </div>

      <!-- POST 2 -->
      <div class="content-card">
        <div class="card-num">02</div>
        <span class="card-type">Social Proof / Pillar: The Standard</span>
        <div class="card-hook">"This isn't your typical studio."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">SSL console. Treated rooms. Pro lighting rigs. Content studio. Podcast booth. Mixing suite. All of it. One address. Vision X Creator Night — June 27. Come see it for yourself.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Carousel: one room per slide. Each shot cinematic. Minimal copy overlaid.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Establish credibility of the space.</span></div>
        <div class="card-cta">Secure Your Spot</div>
      </div>

      <!-- POST 3 -->
      <div class="content-card">
        <div class="card-num">03</div>
        <span class="card-type">Audience Call-Out / Pillar: The Community</span>
        <div class="card-hook">"This post was written for you."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">If you're a photographer in Charlotte who shoots alone. A producer who can't find the right artists. An entrepreneur who needs content but doesn't know where to start. A podcaster who's been recording in their closet. Creator Night was built for you. June 27. Vision X Studios.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Text-forward graphic. Gold on black. Each line drops with a comma pause.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Specific audience identification. High share rate.</span></div>
        <div class="card-cta">Tag someone who needs to be in this room</div>
      </div>

      <!-- POST 4 -->
      <div class="content-card">
        <div class="card-num">04</div>
        <span class="card-type">FOMO / Pillar: The Moment</span>
        <div class="card-hook">"Charlotte is building. Vision X is where it's happening."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">The city is moving. New music. New brands. New creators. And most of them don't know each other yet. That changes June 27. Creator Night. Vision X Studios, Pineville.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Fast-cut video montage of Charlotte skyline, studio sessions, content shoots. Ends on VX logo.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Cultural relevance. Position VX at the center of Charlotte's moment.</span></div>
        <div class="card-cta">Be Part of It — Register Free</div>
      </div>

      <!-- POST 5 -->
      <div class="content-card">
        <div class="card-num">05</div>
        <span class="card-type">Activity Reveal / Pillar: The Access</span>
        <div class="card-hook">"Free headshots. From a pro. At Creator Night."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">One of the activities at Creator Night: a professional headshot station. Walk in, get shot, leave with content you actually want to use. No booking. No fees. One night only. June 27, Vision X Studios.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Before/after style — phone selfie vs. professional studio headshot. Split screen.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Tangible value = attendance driver. Every creator needs headshots.</span></div>
        <div class="card-cta">Get your spot — link in bio</div>
      </div>

      <!-- POST 6 -->
      <div class="content-card">
        <div class="card-num">06</div>
        <span class="card-type">Activity Reveal / Pillar: The Access</span>
        <div class="card-hook">"What if your podcast had a real home?"</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night includes Creator Hot Seat — live podcast interviews, recorded in Vision X's podcast studio. You're the guest. We handle everything else. One night. Real content. Register before it fills up.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Inside the podcast booth. Mics up. Lights warm. Nobody in it yet — the empty seat is the invitation.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Drive podcasters and content creators to register.</span></div>
        <div class="card-cta">Claim your seat</div>
      </div>

      <!-- POST 7 -->
      <div class="content-card">
        <div class="card-num">07</div>
        <span class="card-type">Behind the Vision / Pillar: The Transformation</span>
        <div class="card-hook">"Why we're doing this."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Vision X wasn't built to be a secret. It was built to change the way Charlotte creates. Creator Night is us opening the door and saying: come see what this is. Come see what you have access to. Free. June 27. Pineville, NC.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Founder-to-camera. Real. Not scripted. Talking to one person.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Build personal connection with the brand. Authenticity drives trust.</span></div>
        <div class="card-cta">Register Free — Link in Bio</div>
      </div>

      <!-- POST 8 -->
      <div class="content-card">
        <div class="card-num">08</div>
        <span class="card-type">Ecosystem Intro / Pillar: The Standard</span>
        <div class="card-hook">"One roof. Every service you need."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Recording. Mixing. Mastering. Podcasting. Photography. Video. Content. Artist Development. Management. Label. Community. Brand strategy. All of it. Vision X. One studio. One ecosystem. Creator Night — June 27 — is your first look inside.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Designed graphic listing all services in gold text. Luxury minimalist layout.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Scope revelation. Most people don't know everything VX offers.</span></div>
        <div class="card-cta">See It In Person — Register Now</div>
      </div>

      <!-- POST 9 -->
      <div class="content-card">
        <div class="card-num">09</div>
        <span class="card-type">Opportunity Wall Reveal / Pillar: The Community</span>
        <div class="card-hook">"The wall that might change your career."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night has an Opportunity Wall. Two columns: I NEED / I OFFER. Every attendee writes on it. A videographer who needs an artist to shoot. A producer who needs an engineer. A business owner who needs content. The room becomes a marketplace. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Mock-up of the wall with sticky notes filled in. Real and raw.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Make the collaboration angle tangible and urgent.</span></div>
        <div class="card-cta">What will you write on the wall?</div>
      </div>

      <!-- POST 10 -->
      <div class="content-card">
        <div class="card-num">10</div>
        <span class="card-type">Artist Spotlight / Pillar: The Community</span>
        <div class="card-hook">"Charlotte has artists. They just need the right room."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night will feature live Artist Spotlights — Charlotte artists performing and introducing their work to an audience of creators, entrepreneurs, and industry insiders. Are you an artist? Apply to be featured. [Application link in bio]</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Performer in studio, low light, microphone close. Cinematic. Raw energy.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Drive artist registrations. Create anticipation for live performance element.</span></div>
        <div class="card-cta">Apply to Perform — Link in Bio</div>
      </div>

      <!-- POST 11 -->
      <div class="content-card">
        <div class="card-num">11</div>
        <span class="card-type">Creator Passport Reveal / Pillar: The Access</span>
        <div class="card-hook">"One stamp at a time."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night comes with a Creator Passport. Every room you explore, every activity you complete — stamped. Complete your passport and unlock exclusive giveaway entries. It's not just an event. It's an experience. June 27, Vision X Studios.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Close-up of a passport card with VX branding and empty stamp boxes. Clean, premium design.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Gamification drives full engagement with all rooms/services.</span></div>
        <div class="card-cta">Register to Get Yours</div>
      </div>

      <!-- POST 12 -->
      <div class="content-card">
        <div class="card-num">12</div>
        <span class="card-type">Vision X Bar Feature / Pillar: The Moment</span>
        <div class="card-hook">"The Vision X Bar hits different at night."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">The studio has a bar. That's not the flex. The flex is who's standing at it. Producers. Photographers. Artists. Entrepreneurs. One room. June 27. Creator Night. You should be there.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">VX Bar — blue lights, clean setup, nobody there yet. The calm before. Then a version with people in conversation, laughing, real.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">The bar is VX's most powerful visual asset. Use it to establish the vibe.</span></div>
        <div class="card-cta">Be In That Room — Register Free</div>
      </div>

      <!-- POST 13 -->
      <div class="content-card">
        <div class="card-num">13</div>
        <span class="card-type">Social Proof / Pillar: The Standard</span>
        <div class="card-hook">"Real people. Real work. Real results."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">[Client testimonial — real words, no polish]. Vision X has been changing how Charlotte's creators build. On June 27, you get to see it firsthand. Creator Night. Free. Register.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Client quote in large type. Then BTS of their session at VX. Real photos, not mock-ups.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Third-party credibility. Let existing clients sell the room.</span></div>
        <div class="card-cta">See It For Yourself</div>
      </div>

      <!-- POST 14 -->
      <div class="content-card">
        <div class="card-num">14</div>
        <span class="card-type">Urgency / Pillar: The Moment</span>
        <div class="card-hook">"Spots are limited. The room has a capacity."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night is free. It's also limited. We're not trying to pack a venue — we're curating a room. When we hit capacity, registration closes. If you've been thinking about it: now is the time.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Simple text graphic. Black. Gold text. "LIMITED SPOTS." Clean, direct.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Create urgency without fake countdown pressure.</span></div>
        <div class="card-cta">Register Before It Closes</div>
      </div>

      <!-- POST 15 -->
      <div class="content-card">
        <div class="card-num">15</div>
        <span class="card-type">Studio Tour Tease / Pillar: The Access</span>
        <div class="card-hook">"You've never had a tour like this."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Guided Studio Tours are part of Creator Night. Every room. Every piece of gear. Every service — explained and experienced. You don't read about it. You walk through it. June 27. Vision X Studios, Pineville.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Walking POV video through the studio — like a first-person discovery. Door opens, room revealed, move to the next.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Make the tour feel like an exclusive experience, not a formality.</span></div>
        <div class="card-cta">Book Your Spot on the Tour</div>
      </div>

      <!-- POSTS 16-30 condensed for readability with full data -->
      <div class="content-card">
        <div class="card-num">16</div>
        <span class="card-type">Vision X Records / Pillar: The Transformation</span>
        <div class="card-hook">"Vision X Records is looking."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night is also a Vision X Records showcase night. Our A&R eyes are open. If you're an artist who's been building — this is your room. June 27. Registration required. Perform, connect, get seen.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">VX Records branding + artist silhouette in studio. Dramatic. Aspirational.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Drive artist registrations. Create label-level credibility.</span></div>
        <div class="card-cta">Get in the Room — Register Now</div>
      </div>

      <div class="content-card">
        <div class="card-num">17</div>
        <span class="card-type">Membership Tease / Pillar: The Access</span>
        <div class="card-hook">"What if this was your studio every month?"</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night is free. Membership is the next level. On June 27, get a first look at what Vision X membership includes — recurring studio time, content resources, community access, and more. Come curious. Leave subscribed.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Split screen: creator grinding in bad setup vs. creator in VX space looking focused and relaxed.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Membership interest pre-event = conversion post-event.</span></div>
        <div class="card-cta">Register — Ask About Membership at the Door</div>
      </div>

      <div class="content-card">
        <div class="card-num">18</div>
        <span class="card-type">Call Out / Pillar: The Community</span>
        <div class="card-hook">"Charlotte photographers — where are you?"</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night has space for every kind of creator. Photographers — you belong here. Whether you're freelance, building a brand, or looking for studio time and collaboration. June 27. Come through.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Photography studio setup at VX — lights, backdrops, gear. Camera close-up.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Targeted audience segment. Repeat for each creator type throughout the campaign.</span></div>
        <div class="card-cta">Tag a Charlotte photographer</div>
      </div>

      <div class="content-card">
        <div class="card-num">19</div>
        <span class="card-type">Entrepreneur Call-Out / Pillar: The Transformation</span>
        <div class="card-hook">"Your business needs content. We have the space."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Business owners — your brand is only as strong as how it looks online. Vision X builds brand content for businesses that take themselves seriously. Creator Night is where you find out what's possible. June 27. Free.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Behind-the-scenes of a brand shoot at VX. Professional, clean, impressive.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Attract business owners — highest LTV client segment.</span></div>
        <div class="card-cta">Register — Bring Your Business</div>
      </div>

      <div class="content-card">
        <div class="card-num">20</div>
        <span class="card-type">Contrast Post / Pillar: The Standard</span>
        <div class="card-hook">"Bedroom studio vs. Vision X. You decide."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Nothing wrong with starting in your bedroom. But at some point — the work demands a better environment. Creator Night shows you what that environment looks like. June 27. Vision X Studios.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Side-by-side: amateur DIY setup vs. VX professional studio. Not mocking — just contrasting.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Create aspiration without alienation. You belong here too.</span></div>
        <div class="card-cta">Step Up. Register Free.</div>
      </div>

      <div class="content-card">
        <div class="card-num">21</div>
        <span class="card-type">FAQ Post / Pillar: The Access</span>
        <div class="card-hook">"Yes, it's really free. Yes, you really need to register."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Q: Is Creator Night really free? A: Yes. Q: Do I need to register? A: Yes — space is limited. Q: What if I'm not an artist? A: Good — we need creators, photographers, podcasters, and business owners too. June 27. Vision X Studios, Pineville. Link in bio.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Q&A format graphic. Clean. Readable. One Q&A per slide in carousel.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Remove friction / objections before they happen.</span></div>
        <div class="card-cta">Got questions? DM us.</div>
      </div>

      <div class="content-card">
        <div class="card-num">22</div>
        <span class="card-type">Giveaway Tease / Pillar: The Transformation</span>
        <div class="card-hook">"We're giving away something you actually need."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night giveaways include studio time, a professional mix & master, a content consultation, Vision X merch, and a membership trial. But here's the thing — the people who win aren't the lucky ones. They're the ones who showed up. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Styled flat lay of giveaway items — merch, studio access card, design mockups of each prize.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Drive registrations with tangible incentives.</span></div>
        <div class="card-cta">Register to Win — Link in Bio</div>
      </div>

      <div class="content-card">
        <div class="card-num">23</div>
        <span class="card-type">Collaboration Story / Pillar: The Community</span>
        <div class="card-hook">"Two creators. One room. One collaboration."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">A producer walked into Vision X. An artist came to record. They'd never met. Now they have a song. That's what happens when the right people share the right room. Creator Night is built for that moment. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Two people in studio. Candid. Real. Laughing or deep in work.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Make the collaboration opportunity feel tangible and inevitable.</span></div>
        <div class="card-cta">Find Your Collaborator — Register Now</div>
      </div>

      <div class="content-card">
        <div class="card-num">24</div>
        <span class="card-type">Event Detail / Pillar: The Access</span>
        <div class="card-hook">"Here's exactly what the night looks like."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night runs on June 27 at Vision X Studios. Doors open at [time]. Guided tours, headshot station, podcast hot seat, artist spotlights, giveaways, networking, and Vision X Records showcase. Free. One night. Register at the link in bio.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Designed event schedule card. Gold on black. Clean and premium.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Reduce uncertainty. Give people the full picture.</span></div>
        <div class="card-cta">Register — Add to Calendar</div>
      </div>

      <div class="content-card">
        <div class="card-num">25</div>
        <span class="card-type">Day-of Prep / Pillar: The Moment</span>
        <div class="card-hook">"Here's how to get the most out of Creator Night."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Bring business cards. Bring your questions. Bring an open mind. Leave with contacts, content, and clarity on your next move. That's the play for June 27. See you inside.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Checklist graphic — items a creator should bring. Clean. Actionable.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Pre-event engagement from registered attendees. Share and save trigger.</span></div>
        <div class="card-cta">Share this with someone attending</div>
      </div>

      <div class="content-card">
        <div class="card-num">26</div>
        <span class="card-type">Identity Post / Pillar: The Standard</span>
        <div class="card-hook">"Vision X is not a studio. Say it again."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">There's a recording studio down the street. There are recording studios everywhere. Vision X is a creative ecosystem. There's a difference. Come find out what that difference means for your career on June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Text graphic. Bold. "NOT A STUDIO." Crossed out. "A CREATIVE ECOSYSTEM." Below it.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Brand differentiation. Repositioning in every scroll.</span></div>
        <div class="card-cta">See the difference — June 27</div>
      </div>

      <div class="content-card">
        <div class="card-num">27</div>
        <span class="card-type">Student Outreach / Pillar: The Community</span>
        <div class="card-hook">"If you're a student building your creative career — read this."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">You don't need a degree to be in the room. You need to show up. Creator Night is free, open to all, and one of the most real career-development experiences a creative student in Charlotte can have. June 27. See you there.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Young creator in professional studio environment. Not posed — working.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Target college students + young creatives. High share rate in that demo.</span></div>
        <div class="card-cta">Tag a creative student in Charlotte</div>
      </div>

      <div class="content-card">
        <div class="card-num">28</div>
        <span class="card-type">Influencer Angle / Pillar: The Access</span>
        <div class="card-hook">"Content creators — your next shoot location just opened up."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Content creators in Charlotte: stop shooting in the same three locations. Vision X has professional lighting, multiple rooms, a full photo/video production setup, and now — Creator Night on June 27. Come see what's possible.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Influencer-style shot IN the VX space — natural, aspirational, not over-produced. The space sells itself.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Drive content creator attendance. These people become organic promoters.</span></div>
        <div class="card-cta">Book your Creator Night spot</div>
      </div>

      <div class="content-card">
        <div class="card-num">29</div>
        <span class="card-type">Final Push / Pillar: The Moment</span>
        <div class="card-hook">"This is the last time we're going to say it."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night. June 27. Vision X Studios. This is the last call post. If you're registered — share this. If you're not — now or never. Charlotte's most important creative night of the year starts in [X] days. Don't be the person who says "I should have gone."</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Date graphic. Large. Dramatic. Nothing else.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Final conversion push 48 hours before event.</span></div>
        <div class="card-cta">Register NOW — Closes Soon</div>
      </div>

      <div class="content-card">
        <div class="card-num">30</div>
        <span class="card-type">Day-Of / Pillar: The Moment</span>
        <div class="card-hook">"Tonight is the night."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Today. June 27. Vision X Studios. Doors open at [time]. If you're registered — we'll see you in the room. If you didn't get your spot: we're already thinking about next time. But you should be here for this one.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Studio being set up — the anticipation. Chairs in place. Lights on. Ready.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Build excitement on event day. Drive last-minute walk-ins.</span></div>
        <div class="card-cta">Doors open tonight. [Address]</div>
      </div>

    </div>
  </div>

  <!-- GIVEAWAY POSTS -->
  <div id="giveaways" class="tab-content">
    <div class="content-grid">

      <div class="content-card">
        <div class="card-num">G1</div>
        <span class="card-type">Giveaway Reveal</span>
        <div class="card-hook">"We're giving away studio time. Real studio time."</div>
        <div class="card-row"><span class="card-row-label">Prize</span><span class="card-row-value">4 Hours of Studio Recording Time at Vision X</span></div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">One attendee at Creator Night walks out with 4 hours in the Vision X recording studio. No purchase necessary. Just show up, complete your Creator Passport, and you're automatically entered. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Recording booth — SSL console in frame. Lit dramatically. Prize text overlaid in gold.</span></div>
        <div class="card-cta">Register to Enter — Link in Bio</div>
      </div>

      <div class="content-card">
        <div class="card-num">G2</div>
        <span class="card-type">Pre-Event Giveaway (IG Engagement)</span>
        <div class="card-hook">"Can't make it? Win studio time anyway."</div>
        <div class="card-row"><span class="card-row-label">Prize</span><span class="card-row-value">Mix & Master of One Song</span></div>
        <div class="card-row"><span class="card-row-label">Rules</span><span class="card-row-value">Follow @visionxstudios. Like this post. Tag 2 artists in Charlotte who need to be in this room. Winner announced June 26.</span></div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Your song. Our engineers. Professional mix and master — no charge. This is how we introduce Vision X to Charlotte. Enter below. Creator Night is June 27. You should also just show up.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Waveform close-up on a screen. Engineer hands at console. Process revealed.</span></div>
        <div class="card-cta">Enter in the comments</div>
      </div>

      <div class="content-card">
        <div class="card-num">G3</div>
        <span class="card-type">Merch Giveaway / Brand Building</span>
        <div class="card-hook">"Vision X gear. Only at Creator Night."</div>
        <div class="card-row"><span class="card-row-label">Prize</span><span class="card-row-value">Vision X Merch Package</span></div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">The Vision X merch isn't for sale tonight. It's earned. Show up. Complete your Creator Passport. Multiple winners drawn throughout the night. Don't just come for the gear — but the gear is real. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Clean flat lay of merch — hoodie, hat, tee. Styled on dark background. Premium feel.</span></div>
        <div class="card-cta">Register for Creator Night — Win on Site</div>
      </div>

      <div class="content-card">
        <div class="card-num">G4</div>
        <span class="card-type">Strategy Session Giveaway</span>
        <div class="card-hook">"One session. One plan. One shift."</div>
        <div class="card-row"><span class="card-row-label">Prize</span><span class="card-row-value">60-Min Creator Strategy Session with VX Team</span></div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Not studio time. Not mixing. This is strategy. One attendee at Creator Night wins a dedicated 60-minute session with the Vision X team — content strategy, artist development, or business branding. Walk out with a plan. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Two people at a table, notebooks and screens. Strategic conversation. Collaborative energy.</span></div>
        <div class="card-cta">Register — Win the Session</div>
      </div>

      <div class="content-card">
        <div class="card-num">G5</div>
        <span class="card-type">Membership Trial Giveaway</span>
        <div class="card-hook">"What if you had access every month?"</div>
        <div class="card-row"><span class="card-row-label">Prize</span><span class="card-row-value">30-Day Vision X Membership Trial</span></div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">One Creator Night attendee wins a 30-day Vision X membership trial — full access to the ecosystem, community, resources, and discounted rates. No strings. Just come see what it's like to be a member. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Membership card mockup — premium design, VX branding. Tactile and aspirational.</span></div>
        <div class="card-cta">Register to Win — Free Event</div>
      </div>

      <div class="content-card">
        <div class="card-num">G6</div>
        <span class="card-type">Content Consultation Giveaway</span>
        <div class="card-hook">"Your Instagram. Rebuilt. On the house."</div>
        <div class="card-row"><span class="card-row-label">Prize</span><span class="card-row-value">Content Audit + Strategy Consultation</span></div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">One business owner or creator at Creator Night wins a full content audit — what's working, what's not, and what to post next. This isn't generic advice. This is specific to your brand. June 27, Vision X Studios.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Phone screen with Instagram grid before/after transformation. Visual and compelling.</span></div>
        <div class="card-cta">Businesses — Get Registered Now</div>
      </div>

      <div class="content-card">
        <div class="card-num">G7</div>
        <span class="card-type">Mid-Event Giveaway Hype</span>
        <div class="card-hook">"You won't know what we're giving away until you're in the room."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">There are giveaways throughout the night at Creator Night. Some we've announced. Some we haven't. You have to be in the room. June 27. Vision X Studios. Register. Show up. Stay.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Mystery box — literally a wrapped package with a question mark. Or dark graphic with "???" in gold.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Maintain giveaway suspense. Drives people to attend AND stay the full event.</span></div>
        <div class="card-cta">You have to be there to win</div>
      </div>

      <div class="content-card">
        <div class="card-num">G8</div>
        <span class="card-type">Share-to-Win (Pre-Event)</span>
        <div class="card-hook">"Share this. Win studio time."</div>
        <div class="card-row"><span class="card-row-label">Prize</span><span class="card-row-value">2 Hours Studio Recording Time</span></div>
        <div class="card-row"><span class="card-row-label">Rules</span><span class="card-row-value">Share this post to your Story, tag @visionxstudios, add "See you at Creator Night June 27" to your caption. Winner drawn June 25.</span></div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">You share. We give you studio time. Simple. Creator Night is June 27 at Vision X Studios. Share this post, tag us in your story, and win. Every share also helps Charlotte's creative community find out this exists.</span></div>
        <div class="card-cta">Share Now — Win Studio Time</div>
      </div>

      <div class="content-card">
        <div class="card-num">G9</div>
        <span class="card-type">Artist-Specific Giveaway</span>
        <div class="card-hook">"Artists — this one's for you specifically."</div>
        <div class="card-row"><span class="card-row-label">Prize</span><span class="card-row-value">Professional Mix & Master + Artist Development Consultation</span></div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">At Creator Night, we're giving away a professional mix & master session PLUS a one-on-one with our artist development team. If you're an artist who's been building independently — this conversation might be what changes everything. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Artist recording — authentic moment. Not posed. Deep in the session.</span></div>
        <div class="card-cta">Artists — Register Now</div>
      </div>

      <div class="content-card">
        <div class="card-num">G10</div>
        <span class="card-type">Grand Prize Reveal</span>
        <div class="card-hook">"The biggest giveaway of the night drops at the end."</div>
        <div class="card-row"><span class="card-row-label">Prize</span><span class="card-row-value">[Grand Prize — determine internally: could be 10hrs studio + VX Records meeting + merch bundle]</span></div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">The last giveaway of Creator Night is the biggest one. We're not announcing it until the room is full. What we'll say: it's worth staying for. June 27. Vision X Studios. Don't leave early.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Dark, dramatic. "GRAND PRIZE." Nothing else. Gold on black. The mystery IS the hook.</span></div>
        <div class="card-cta">Register. Attend. Win.</div>
      </div>

    </div>
  </div>

  <!-- COMMUNITY POSTS -->
  <div id="community" class="tab-content">
    <div class="content-grid">

      <div class="content-card">
        <div class="card-num">C1</div>
        <span class="card-type">Community / Belonging</span>
        <div class="card-hook">"Charlotte's creative community deserves a home."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Every major city has a creative hub. A place where the artists, the producers, the photographers, and the entrepreneurs all end up. Charlotte's creative hub is Vision X. Creator Night is the official opening. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Group shot inside VX — diverse, animated, real. Not a posed team photo.</span></div>
        <div class="card-cta">Come find your community</div>
      </div>

      <div class="content-card">
        <div class="card-num">C2</div>
        <span class="card-type">Community / Collaboration</span>
        <div class="card-hook">"Your next collab is already in Charlotte."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">The photographer who makes your music video. The producer who finishes your album. The videographer who builds your brand. They're already here. You just haven't met them yet. Creator Night changes that. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Two different creators shown in split screen — they haven't met yet. Then a single frame of them working together. Timeline frame.</span></div>
        <div class="card-cta">Register — Meet the Room</div>
      </div>

      <div class="content-card">
        <div class="card-num">C3</div>
        <span class="card-type">Community / Pride</span>
        <div class="card-hook">"CLT creators: this one's for us."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Charlotte doesn't need to go to Atlanta for a professional creative experience. It doesn't need to go to LA. Vision X is here. Creator Night is proof. June 27 — we show the city what we've been building.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Charlotte skyline + VX studio interior in split. "Right here." overlay.</span></div>
        <div class="card-cta">CLT — this is yours. Register.</div>
      </div>

      <div class="content-card">
        <div class="card-num">C4</div>
        <span class="card-type">Community / Opportunity Wall Feature</span>
        <div class="card-hook">"Post what you need. Find what you need."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">The Opportunity Wall at Creator Night is one of the most powerful elements of the night. I need a: videographer / featured artist / content strategy / podcast producer / music producer. I offer: photography / beats / mixing / event production / social media. The room becomes a marketplace. Come with your list. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Opportunity Wall mockup — real sticky notes, real needs, real offers. Authentic.</span></div>
        <div class="card-cta">What will you put on the wall?</div>
      </div>

      <div class="content-card">
        <div class="card-num">C5</div>
        <span class="card-type">Community / Invitation</span>
        <div class="card-hook">"Who should be in this room that doesn't know it exists?"</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">You know someone in Charlotte who should be at Creator Night. An artist grinding. A photographer who needs better clients. A business that needs content. Tag them. Don't let them miss this. June 27, Vision X Studios. Free. Registration required.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Empty chair in the studio with "YOUR SEAT" written on it. Invitation energy.</span></div>
        <div class="card-cta">Tag someone who belongs here</div>
      </div>

      <div class="content-card">
        <div class="card-num">C6</div>
        <span class="card-type">Community / Creator Spotlight</span>
        <div class="card-hook">"Meet one of the people already inside the ecosystem."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">[Name] has been working at Vision X for [X months]. Here's what they've built. [Brief story.] Creator Night is about introducing more people like [Name] to what's possible here. Are you next? June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Client/creator portrait in studio. Professional. Authentic quote.</span></div>
        <div class="card-cta">Register — June 27</div>
      </div>

      <div class="content-card">
        <div class="card-num">C7</div>
        <span class="card-type">Community / Challenge</span>
        <div class="card-hook">"If you're serious about your craft — prove it."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Serious creators show up for opportunities. Creator Night is an opportunity. Free admission. Professional studio. Network of creatives. Giveaways. The room is ready. The question is whether you are. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Direct-to-camera statement. No fluff. Just the challenge.</span></div>
        <div class="card-cta">Prove it — Register Now</div>
      </div>

      <div class="content-card">
        <div class="card-num">C8</div>
        <span class="card-type">Community / Post-Event Vision</span>
        <div class="card-hook">"Creator Night isn't the destination. It's the beginning."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night is a single night. But the relationships you build, the services you discover, and the community you join — that's ongoing. This is how the Vision X ecosystem starts for you. June 27 is day one.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Long exposure of the studio at night — motion, possibility, warmth. "Day One." in type.</span></div>
        <div class="card-cta">Start Here — Register Free</div>
      </div>

      <div class="content-card">
        <div class="card-num">C9</div>
        <span class="card-type">Community / Diversity of Creators</span>
        <div class="card-hook">"Every kind of creator. One room."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night is not just for musicians. It's for podcasters. Photographers. Videographers. Business owners. Influencers. Entrepreneurs. Producers. Engineers. If you create anything — this room was built for you. June 27. Come as you are.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Mosaic of different creator types — each in their element. Collage format. Real energy.</span></div>
        <div class="card-cta">Find your people — Register Now</div>
      </div>

      <div class="content-card">
        <div class="card-num">C10</div>
        <span class="card-type">Community / Post-Event Momentum</span>
        <div class="card-hook">"After Creator Night, Charlotte won't be the same."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">The city's most complete creative ecosystem. One night. The people who attend will build things together. Start businesses together. Release music together. Film together. That starts June 27. Be one of them.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Final event promotional image — bold, high contrast, unmistakable. Event details clear.</span></div>
        <div class="card-cta">Register at the link in bio</div>
      </div>

    </div>
  </div>

  <!-- BTS POSTS -->
  <div id="bts" class="tab-content">
    <div class="content-grid">

      <div class="content-card">
        <div class="card-num">B1</div>
        <span class="card-type">BTS / Studio Setup</span>
        <div class="card-hook">"We've been in here building. June 27, you see it."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Last few weeks at Vision X — preparing the space for Creator Night. Every room. Every detail. This isn't a rental hall. It's a working creative ecosystem. Come experience the difference. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Studio being set up — equipment being arranged, lights being dialed in, the bar being prepared. Real and honest prep footage.</span></div>
        <div class="card-cta">Register — Link in Bio</div>
      </div>

      <div class="content-card">
        <div class="card-num">B2</div>
        <span class="card-type">BTS / Team Prep</span>
        <div class="card-hook">"The team is locked in."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">This is what the Vision X team looks like two weeks before Creator Night. Planning. Building. Making sure June 27 delivers. We're not winging this. Every element of the night has been designed for you. Come see the results.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Team working — planning boards, laptops, conversation. Real, candid energy.</span></div>
        <div class="card-cta">June 27 — Register Now</div>
      </div>

      <div class="content-card">
        <div class="card-num">B3</div>
        <span class="card-type">BTS / Gear Feature</span>
        <div class="card-hook">"The gear alone is worth the visit."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Walking through what Vision X has available to its clients. SSL console. Pro mics. Lighting rigs. Camera setups. Podcast booths. All of it accessible through our services and membership. Creator Night — June 27 — is your first look at all of it in person.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Close-up reel of every piece of significant gear in the studio. Each shot — 2 seconds. Fast and impressive.</span></div>
        <div class="card-cta">Come see it — Register Free</div>
      </div>

      <div class="content-card">
        <div class="card-num">B4</div>
        <span class="card-type">BTS / Creator Passport Design</span>
        <div class="card-hook">"We designed something for Creator Night you've never seen at an event."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">The Creator Passport is unique to Vision X Creator Night. Every activity, every room, every stamp — it maps your experience through the ecosystem. Come complete yours. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">The actual passport being printed or designed. Show the design process.</span></div>
        <div class="card-cta">Register — Get Your Passport</div>
      </div>

      <div class="content-card">
        <div class="card-num">B5</div>
        <span class="card-type">BTS / Day-Before</span>
        <div class="card-hook">"Tomorrow night, this room is yours."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">One day out. Vision X is ready. The studio is set. The team is locked in. Tomorrow night — Creator Night officially opens. If you're registered, we'll see you in the room. If you're not — registration closes at midnight tonight.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Studio fully prepared — empty, beautiful, waiting. Golden hour lighting if possible.</span></div>
        <div class="card-cta">Last Chance to Register</div>
      </div>

      <div class="content-card">
        <div class="card-num">B6</div>
        <span class="card-type">BTS / Recording Session in Progress</span>
        <div class="card-hook">"This is a normal Tuesday at Vision X. Creator Night is a whole other level."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">We don't stop working for Creator Night. We keep working. This is a live session at Vision X this week — the same energy, the same quality, the same studio you'll walk through on June 27. Come see it firsthand.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Active recording session — engineer at console, artist behind glass. Real work happening.</span></div>
        <div class="card-cta">Register — June 27</div>
      </div>

      <div class="content-card">
        <div class="card-num">B7</div>
        <span class="card-type">BTS / The VX Bar</span>
        <div class="card-hook">"The Vision X Bar is a whole vibe on its own."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">A lot of important conversations happen at the bar. At Creator Night, that bar is yours. Come for the studios. Stay for the community. And yes — the bar hits different when you're surrounded by Charlotte's best creators. June 27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">The VX Bar — blue lights, styled beautifully, clean. Shot from multiple angles. This is the most shareable aesthetic in the studio.</span></div>
        <div class="card-cta">See you at the bar — Register Free</div>
      </div>

      <div class="content-card">
        <div class="card-num">B8</div>
        <span class="card-type">BTS / Headshot Station Setup</span>
        <div class="card-hook">"The headshot station at Creator Night is dialed in."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Professional backdrop. Professional lighting. Professional photographer. All of it — part of Creator Night. You show up. You leave with headshots you can actually use. June 27, Vision X Studios. Free.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Headshot setup being built out — lights, backdrop, camera placement. Behind the scenes of the behind the scenes.</span></div>
        <div class="card-cta">Register — Get Your Headshots</div>
      </div>

      <div class="content-card">
        <div class="card-num">B9</div>
        <span class="card-type">BTS / Team Introduction</span>
        <div class="card-hook">"Meet the people who built this."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">Creator Night is being put together by the Vision X team. [Brief team description.] They're the people you'll meet on June 27. Professionals. Creatives. People who take this seriously. Come meet them.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Individual team portraits in studio. One per slide in carousel. Each with name and role.</span></div>
        <div class="card-cta">Meet the team on June 27</div>
      </div>

      <div class="content-card">
        <div class="card-num">B10</div>
        <span class="card-type">BTS / Event Night Recap (Post-Event)</span>
        <div class="card-hook">"This is what Creator Night looked like."</div>
        <div class="card-row"><span class="card-row-label">Caption</span><span class="card-row-value">June 27. Creator Night. This is what happened when Charlotte's creative community came through Vision X Studios. If you were in the room — thank you. If you weren't — Creator Night 2 is already being planned. Follow @visionxstudios to be first to know.</span></div>
        <div class="card-row"><span class="card-row-label">Visual</span><span class="card-row-value">Full event recap video. Best moments, energy, faces, giveaway reactions, performances. Professionally edited.</span></div>
        <div class="card-cta">Follow for Creator Night 2</div>
      </div>

    </div>
  </div>
</section>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION 5: 20 REEL IDEAS -->
<!-- ═══════════════════════════════════════════════ -->
<section class="section" id="reels">
  <span class="section-label">Section 05</span>
  <h2 class="section-title">20 Reel Ideas</h2>
  <p class="section-intro">Every reel should be filmable with a phone and a plan. Production quality matters — but authenticity matters more. The best performing content from a studio will always be people doing real things in a real space.</p>

  <div class="reel-grid">

    <div class="reel-card">
      <span class="reel-num">REEL 01</span>
      <div class="reel-title">"POV: You just walked into Vision X for the first time."</div>
      <div class="reel-desc">First-person walk-through from parking lot to bar. Discover each room one door at a time. No narration. Just the space. Music: moody instrumental. End card: Creator Night, June 27.</div>
      <div class="reel-format">Format: POV walkthrough / 30-45s / Trending audio or original</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 02</span>
      <div class="reel-title">"Recording studio vs. Vision X. Charlotte creators deserve better."</div>
      <div class="reel-desc">Quick comparison of what most Charlotte creatives are working with versus Vision X. Not mean — just honest. "You've been doing this with this? Come see what this looks like." Fast cuts, text overlays.</div>
      <div class="reel-format">Format: Comparison / 20-30s / High-energy audio</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 03</span>
      <div class="reel-title">"Everything Vision X can do for you in 60 seconds."</div>
      <div class="reel-desc">One second per service. Recording → mixing → mastering → podcast → photo → video → content → branding → artist dev → management → label → community. Boom. Each word hits on the beat.</div>
      <div class="reel-format">Format: Rapid fire / 60s / Beat-synced edit</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 04</span>
      <div class="reel-title">"Day in the life at Vision X. Real session. No script."</div>
      <div class="reel-desc">Follow one creator through a real Vision X session. Wake up, drive in, set up, create, finish, leave with the product. Authentic. Show the professional environment naturally.</div>
      <div class="reel-format">Format: Day in the life / 60-90s / Vlog style with music bed</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 05</span>
      <div class="reel-title">"The Vision X Bar at night. Nobody else in Charlotte has this."</div>
      <div class="reel-desc">Just the bar. Blue lights. Still. Then the energy comes in — people arriving, laughing, creating. Quick transition. This is the vibe. Creator Night June 27.</div>
      <div class="reel-format">Format: Atmosphere / 15-20s / Minimal, atmospheric audio</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 06</span>
      <div class="reel-title">"Charlotte photographers — you have a studio home."</div>
      <div class="reel-desc">Feature the photography/content studio at VX. Setup, lighting, backdrop options. One photographer walks in, sets up, shoots. Clean and professional. End: "Creator Night, June 27. Come see your new workspace."</div>
      <div class="reel-format">Format: Feature / 30-45s / Music bed</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 07</span>
      <div class="reel-title">"What happens when you put Charlotte's best creators in one room."</div>
      <div class="reel-desc">Simulation or real footage of different creator types interacting — producer and artist, photographer and influencer, podcaster and entrepreneur. Show the natural collisions that happen. Creator Night June 27.</div>
      <div class="reel-format">Format: Story / 45-60s / Cinematic</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 08</span>
      <div class="reel-title">"We're giving away studio time at Creator Night. Here's how to win."</div>
      <div class="reel-desc">Quick explainer. Direct to camera. "Show up. Get your passport. Complete it. You're entered." Keep it simple. The access angle — the giveaway is just the hook, the ecosystem is the prize.</div>
      <div class="reel-format">Format: Direct / 15-20s / Talking head</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 09</span>
      <div class="reel-title">"Bedroom studio to Vision X. Same artist. Different level."</div>
      <div class="reel-desc">Show an artist recording in a basic home setup. Cut to: same artist, same song, recording at Vision X. The difference is visible. The quality is audible. End with: "Creator Night, June 27."</div>
      <div class="reel-format">Format: Before/After / 30-45s / Dramatic cut</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 10</span>
      <div class="reel-title">"The Creator Passport. Explained in 20 seconds."</div>
      <div class="reel-desc">Show the physical passport. Quick demo of stamps. "Every room. Every activity. Every stamp. Complete it and you're entered to win big. Creator Night, June 27."</div>
      <div class="reel-format">Format: Product demo / 20s / Clean and direct</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 11</span>
      <div class="reel-title">"If you're a producer in Charlotte, watch this."</div>
      <div class="reel-desc">Direct call-out. "Producer. Charlotte. No studio to bring artists? No professional mixing room? Vision X has all of it. Creator Night is June 27. Come see your new home base." Then room tour.</div>
      <div class="reel-format">Format: Targeted call-out / 30s / Talking head + b-roll</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 12</span>
      <div class="reel-title">"Business owners: what your brand content should look like."</div>
      <div class="reel-desc">Quick contrast: typical DIY business content vs. Vision X professional brand shoot. No narration needed. The visuals tell the story. End: "Creator Night. Come talk to us about your brand. June 27."</div>
      <div class="reel-format">Format: Visual comparison / 30s / Trending audio</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 13</span>
      <div class="reel-title">"What does $0 get you at Creator Night?"</div>
      <div class="reel-desc">List format Reel. "Free headshots. Studio tour. Podcast Hot Seat. Artist spotlights. Giveaways. Networking. Opportunity Wall. Access to Vision X Records information." Text on screen, each line builds. "All of it. Free. June 27."</div>
      <div class="reel-format">Format: List reveal / 30s / Music bed</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 14</span>
      <div class="reel-title">"This is Charlotte's creative ecosystem. And it's been here the whole time."</div>
      <div class="reel-desc">Longer form Reel. Studio walk-through with voiceover from the founder — raw, real, explaining the vision behind Vision X and why Creator Night matters. Personal. Authentic. This builds the most trust.</div>
      <div class="reel-format">Format: Founder story / 60-90s / No music, just voice</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 15</span>
      <div class="reel-title">"Register for Creator Night in 30 seconds."</div>
      <div class="reel-desc">Screen recording of the registration process — how quick and easy it is. "Takes 30 seconds. June 27. Vision X Studios. Do it now." Remove every barrier to registering.</div>
      <div class="reel-format">Format: Tutorial / 30s / Upbeat audio</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 16</span>
      <div class="reel-title">"Interview with a Charlotte creator who's already in the Vision X ecosystem."</div>
      <div class="reel-desc">Quick testimonial Reel. Real creator, real words: what VX has done for their work and why Creator Night matters. One take, authentic, no teleprompter.</div>
      <div class="reel-format">Format: Testimonial / 45-60s / Natural sound</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 17</span>
      <div class="reel-title">"48 hours until Creator Night."</div>
      <div class="reel-desc">Countdown Reel. Studio being finalized. Excitement building. Quick cuts. "48 hours. Vision X Studios. June 27. Register now or wait until next year." Energy. Urgency.</div>
      <div class="reel-format">Format: Countdown / 20s / High energy</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 18</span>
      <div class="reel-title">"Day-of Reel. Shot at Creator Night in real time."</div>
      <div class="reel-desc">Live event Reel — the energy of the room, the headshot station in action, the performances, the conversations. Real people, real night. Post during or immediately after the event. This becomes the proof and the FOMO driver for Creator Night 2.</div>
      <div class="reel-format">Format: Event coverage / 60-90s / Best moments only</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 19</span>
      <div class="reel-title">"What Charlotte's creative scene looks like from inside Vision X."</div>
      <div class="reel-desc">Wide view. Different creators in different rooms simultaneously. The podcast booth active, the recording room running, the photo studio lit, the bar populated. One night. The whole ecosystem running at once. Creator Night.</div>
      <div class="reel-format">Format: Multi-scene / 30-45s / Cinematic</div>
    </div>

    <div class="reel-card">
      <span class="reel-num">REEL 20</span>
      <div class="reel-title">"If you missed Creator Night, here's what you missed."</div>
      <div class="reel-desc">Post-event. Full recap. The best shots, the biggest giveaway moments, the performances, the conversations. Caption: "Creator Night 2 is coming. Follow to be first in line." This drives long-term community growth.</div>
      <div class="reel-format">Format: Post-event recap / 60-90s / Emotional music</div>
    </div>

  </div>
</section>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION 6: 10 STORY CAMPAIGNS -->
<!-- ═══════════════════════════════════════════════ -->
<section class="section" id="stories">
  <span class="section-label">Section 06</span>
  <h2 class="section-title">10 Story Campaigns</h2>
  <p class="section-intro">Stories are your urgency machine. They disappear in 24 hours — that scarcity is your tool. Use Stories for polls, countdowns, link clicks, DM conversations, and event day updates.</p>

  <div class="story-grid">

    <div class="story-card">
      <div class="story-day">01</div>
      <div class="story-title">The Poll Series — "Are You a Creator?"</div>
      <div class="story-desc">Multi-day poll story: "Are you a Charlotte creator?" → "What do you create?" (artist/podcaster/photographer/other) → "Do you have access to professional studio space?" → "What would change for your career if you did?" → Final slide: Creator Night, June 27. Register now. The polls capture data and build self-awareness.</div>
    </div>

    <div class="story-card">
      <div class="story-day">02</div>
      <div class="story-title">Room-by-Room Reveal Series</div>
      <div class="story-desc">One story per day, one room per story. "Before we drop anything else this week — here's what's behind door #1 at Vision X." Recording studio. Podcast booth. Content studio. Photography space. The bar. Each day ends: "Creator Night, June 27." Build intrigue one room at a time.</div>
    </div>

    <div class="story-card">
      <div class="story-day">03</div>
      <div class="story-title">Countdown Sticker Series</div>
      <div class="story-desc">Daily countdown story starting June 20 (7 days out). Each day: new countdown sticker + one reason to attend. Day 7: The headshots. Day 6: The recordings. Day 5: The networking. Day 4: The giveaways. Day 3: The performances. Day 2: The community. Day 1: The vibe. Simple. Visual. Consistent.</div>
    </div>

    <div class="story-card">
      <div class="story-day">04</div>
      <div class="story-title">"DM Me If This Is You" Story</div>
      <div class="story-desc">Text-heavy story: "DM me if you're a Charlotte artist who hasn't been able to afford consistent studio time. I want to tell you about something." Then the reply is information about Creator Night and VX membership. Personalized. Direct. High conversion rate on DMs.</div>
    </div>

    <div class="story-card">
      <div class="story-day">05</div>
      <div class="story-title">Giveaway Announcement Story Series</div>
      <div class="story-desc">Each giveaway gets its own story. Prize reveal → how to enter → swipe up/link → urgency. Run one per day starting June 13. Build cumulative excitement so every day there's a new reason to attend. "Yesterday we announced studio time. Today we're announcing this."</div>
    </div>

    <div class="story-card">
      <div class="story-day">06</div>
      <div class="story-title">Testimonial/Social Proof Story</div>
      <div class="story-desc">Reposts from attendees who registered — their excitement, their reason for attending. "When creators share why they're coming — share it." Use UGC and reshares to build social proof organically. Real people sharing builds more trust than any branded content.</div>
    </div>

    <div class="story-card">
      <div class="story-day">07</div>
      <div class="story-title">"Behind the Scenes" Weekly Story</div>
      <div class="story-desc">Every Sunday/Monday — BTS of VX event prep. Short clips, real footage. Makes followers feel like insiders watching something build. Creates investment in the event before it happens. "You've been watching this build. June 27 is where it arrives."</div>
    </div>

    <div class="story-card">
      <div class="story-day">08</div>
      <div class="story-title">Q&A Story — "Ask Us Anything About Creator Night"</div>
      <div class="story-desc">Question box in stories. Answer them honestly. Is it really free? Yes. Can I bring someone? Yes, have them register. What should I wear? Come as you are. Will there be food? Come find out. The Q&A builds trust and removes friction.</div>
    </div>

    <div class="story-card">
      <div class="story-day">09</div>
      <div class="story-title">Day-Of Story Marathon</div>
      <div class="story-desc">June 27, post continuously: Studio setup → doors opening → first attendees → headshot station live → podcast hot seat recording → artist spotlight → giveaway winner reactions → energy of the room. This is the content that makes people want Creator Night 2 before Creator Night ends.</div>
    </div>

    <div class="story-card">
      <div class="story-day">10</div>
      <div class="story-title">Post-Event Story Campaign</div>
      <div class="story-desc">June 28 onward — story recap series. Photos from the night. Winner announcements. "If you missed it — here's what happened." Links to follow-up booking forms. "The next step from Creator Night: book your first session." Conversion continues after the event closes.</div>
    </div>

  </div>
</section>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION 7: 10 COUNTDOWN POSTS -->
<!-- ═══════════════════════════════════════════════ -->
<section class="section" id="countdown">
  <span class="section-label">Section 07</span>
  <h2 class="section-title">10 Countdown Posts</h2>

  <div class="countdown-list">

    <div class="countdown-item">
      <div class="countdown-days"><span class="countdown-days-num">21</span><span class="countdown-days-label">Days Out</span></div>
      <div class="countdown-body">
        <div class="countdown-hook">21 days. Registration is open.</div>
        <div class="countdown-desc">First countdown post. Drops June 6. "Creator Night is 21 days away. Registration is open. This is the room Charlotte's creative community has been waiting for. Link in bio." Visual: Large "21" in Bebas. Gold on black. VX branding.</div>
      </div>
    </div>

    <div class="countdown-item">
      <div class="countdown-days"><span class="countdown-days-num">14</span><span class="countdown-days-label">Days Out</span></div>
      <div class="countdown-body">
        <div class="countdown-hook">2 weeks. Half of the spots are gone.</div>
        <div class="countdown-desc">"Two weeks from tonight, Vision X Studios will be full of Charlotte's most ambitious creators. Half the spots are already taken. Register before the room closes." Visual: "14 DAYS" + progress bar showing registration filling up.</div>
      </div>
    </div>

    <div class="countdown-item">
      <div class="countdown-days"><span class="countdown-days-num">10</span><span class="countdown-days-label">Days Out</span></div>
      <div class="countdown-body">
        <div class="countdown-hook">10 days. The room is building.</div>
        <div class="countdown-desc">"10 days until Creator Night. We're watching the registration list grow — photographers, producers, podcasters, artists, entrepreneurs. The room is building itself. Are you in it?" Visual: Silhouette montage of creator types. Countdown in corner.</div>
      </div>
    </div>

    <div class="countdown-item">
      <div class="countdown-days"><span class="countdown-days-num">7</span><span class="countdown-days-label">Days Out</span></div>
      <div class="countdown-body">
        <div class="countdown-hook">One week. Seven reasons to be in the room.</div>
        <div class="countdown-desc">Carousel: 7 slides, one reason per slide. Headshots. Studio tours. Podcast hot seat. Artist spotlights. Opportunity Wall. Giveaways. The community. Each slide — one bold visual, one sentence. Final slide: "7 days. Register now."</div>
      </div>
    </div>

    <div class="countdown-item">
      <div class="countdown-days"><span class="countdown-days-num">5</span><span class="countdown-days-label">Days Out</span></div>
      <div class="countdown-body">
        <div class="countdown-hook">5 days. We're announcing the full giveaway list.</div>
        <div class="countdown-desc">"5 days from tonight. We're dropping the full giveaway lineup: studio time, mix & master, content consultation, membership trial, merch, strategy session, and the grand prize we haven't announced yet. You have to be in the room. Register now."</div>
      </div>
    </div>

    <div class="countdown-item">
      <div class="countdown-days"><span class="countdown-days-num">3</span><span class="countdown-days-label">Days Out</span></div>
      <div class="countdown-body">
        <div class="countdown-hook">72 hours. Final registration push.</div>
        <div class="countdown-desc">"72 hours. Vision X Studios. Creator Night. Charlotte — if you've been sitting on it, this is your moment to commit. Registration doesn't guarantee admission after capacity is hit. 3 days. Link in bio."</div>
      </div>
    </div>

    <div class="countdown-item">
      <div class="countdown-days"><span class="countdown-days-num">2</span><span class="countdown-days-label">Days Out</span></div>
      <div class="countdown-body">
        <div class="countdown-hook">48 hours. The space is ready.</div>
        <div class="countdown-desc">BTS countdown: studio being set up. The space in final prep mode. "48 hours and Vision X is ready for you. See you Saturday." Human and real. Less promotional. Let the visual do the work.</div>
      </div>
    </div>

    <div class="countdown-item">
      <div class="countdown-days"><span class="countdown-days-num">1</span><span class="countdown-days-label">Day Out</span></div>
      <div class="countdown-body">
        <div class="countdown-hook">Tomorrow night. This is it.</div>
        <div class="countdown-desc">"Tomorrow night. June 27. Vision X Studios, Pineville NC. Doors open at [time]. If you're registered — we'll see you inside. If you're not — this is your absolute last chance." Then: address, time, dress code, what to bring. Practical. Final.</div>
      </div>
    </div>

    <div class="countdown-item">
      <div class="countdown-days"><span class="countdown-days-num">0</span><span class="countdown-days-label">Day-Of</span></div>
      <div class="countdown-body">
        <div class="countdown-hook">Tonight. Don't be late.</div>
        <div class="countdown-desc">"Vision X Creator Night starts tonight. Doors open at [time]. Studio is ready. The team is ready. Charlotte — come through. Vision X Studios, [address]." Fire post. Simple. Confident. Then all hands on deck for content at the event itself.</div>
      </div>
    </div>

    <div class="countdown-item">
      <div class="countdown-days"><span class="countdown-days-num">+1</span><span class="countdown-days-label">Day After</span></div>
      <div class="countdown-body">
        <div class="countdown-hook">Creator Night is done. Here's what it built.</div>
        <div class="countdown-desc">Day-after recap post. Attendance numbers. Energy recap. "Charlotte showed up. [X] creators. One night. One ecosystem. Thank you to everyone who came through Vision X. The next step is waiting for you — link in bio." Immediately begins follow-up conversion.</div>
      </div>
    </div>

  </div>
</section>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION 8: POSTING CALENDAR -->
<!-- ═══════════════════════════════════════════════ -->
<section class="section" id="calendar">
  <span class="section-label">Section 08</span>
  <h2 class="section-title">Posting Calendar</h2>
  <p class="section-intro">June 6 — June 27 + post-event. 21 days of strategic, intentional content. This is not a suggestion. This is the operating schedule.</p>

  <div class="calendar-week">
    <div class="calendar-week-label">WEEK 1 — LAUNCH &amp; AWARENESS / June 6–12</div>
    <table class="calendar-table">
      <thead>
        <tr><th>Date</th><th>Content</th><th>Platform</th><th>Format</th><th>Goal</th></tr>
      </thead>
      <tbody>
        <tr>
          <td><span class="cal-date">SAT 6/6</span></td>
          <td>Event announcement — Post #1 "The doors are opening" + Reel 01 (POV walkthrough)</td>
          <td><span class="cal-platform priority-high">IG</span></td>
          <td>Feed Post + Reel</td>
          <td>Initial awareness, registration link launch</td>
        </tr>
        <tr>
          <td><span class="cal-date">SAT 6/6</span></td>
          <td>21-Day countdown Story + registration link</td>
          <td><span class="cal-platform priority-high">Stories</span></td>
          <td>Story</td>
          <td>Drive registration clicks</td>
        </tr>
        <tr>
          <td><span class="cal-date">SUN 6/7</span></td>
          <td>Post #8 — "One roof. Every service." (ecosystem overview)</td>
          <td><span class="cal-platform priority-high">IG</span></td>
          <td>Designed Carousel</td>
          <td>Brand education, establish scope</td>
        </tr>
        <tr>
          <td><span class="cal-date">SUN 6/7</span></td>
          <td>Room Reveal Story #1 — Recording Studio</td>
          <td><span class="cal-platform priority-med">Stories</span></td>
          <td>Story</td>
          <td>Intrigue, room tease</td>
        </tr>
        <tr>
          <td><span class="cal-date">MON 6/8</span></td>
          <td>Post #3 — Audience call-out (artist/photographer/podcaster/entrepreneur)</td>
          <td><span class="cal-platform priority-high">IG + LinkedIn</span></td>
          <td>Text graphic</td>
          <td>Specific audience targeting, tag-a-friend</td>
        </tr>
        <tr>
          <td><span class="cal-date">TUE 6/9</span></td>
          <td>Reel 03 — Everything VX can do in 60 seconds</td>
          <td><span class="cal-platform priority-high">IG + TikTok</span></td>
          <td>Reel</td>
          <td>Reach, ecosystem awareness</td>
        </tr>
        <tr>
          <td><span class="cal-date">TUE 6/9</span></td>
          <td>Room Reveal Story #2 — Podcast Booth</td>
          <td><span class="cal-platform priority-med">Stories</span></td>
          <td>Story</td>
          <td>Podcaster targeting</td>
        </tr>
        <tr>
          <td><span class="cal-date">WED 6/10</span></td>
          <td>G2 Pre-Event Giveaway Post — Mix & Master</td>
          <td><span class="cal-platform priority-high">IG</span></td>
          <td>Feed Post</td>
          <td>Engagement, follower growth, artist targeting</td>
        </tr>
        <tr>
          <td><span class="cal-date">THU 6/11</span></td>
          <td>Post #7 — Behind the Vision (founder post)</td>
          <td><span class="cal-platform priority-high">IG</span></td>
          <td>Video or photo</td>
          <td>Brand connection, trust building</td>
        </tr>
        <tr>
          <td><span class="cal-date">THU 6/11</span></td>
          <td>Room Reveal Story #3 — Content Studio / Photo Setup</td>
          <td><span class="cal-platform priority-med">Stories</span></td>
          <td>Story</td>
          <td>Photographer/creator targeting</td>
        </tr>
        <tr>
          <td><span class="cal-date">FRI 6/12</span></td>
          <td>Reel 05 — The Vision X Bar at night</td>
          <td><span class="cal-platform priority-high">IG + TikTok</span></td>
          <td>Reel</td>
          <td>Vibe/FOMO, high shareability</td>
        </tr>
        <tr>
          <td><span class="cal-date">FRI 6/12</span></td>
          <td>Poll Story Series begins — "Are you a Charlotte creator?"</td>
          <td><span class="cal-platform priority-med">Stories</span></td>
          <td>Poll Story</td>
          <td>Engagement, audience data collection</td>
        </tr>
      </tbody>
    </table>
  </div>

  <div class="calendar-week">
    <div class="calendar-week-label">WEEK 2 — ACTIVATION &amp; GIVEAWAYS / June 13–19</div>
    <table class="calendar-table">
      <thead>
        <tr><th>Date</th><th>Content</th><th>Platform</th><th>Format</th><th>Goal</th></tr>
      </thead>
      <tbody>
        <tr>
          <td><span class="cal-date">SAT 6/13</span></td>
          <td>14-Day Countdown + G1 Giveaway Post (Studio Time)</td>
          <td><span class="cal-platform priority-high">IG</span></td>
          <td>Feed Post</td>
          <td>Urgency + giveaway excitement</td>
        </tr>
        <tr>
          <td><span class="cal-date">SAT 6/13</span></td>
          <td>BTS Weekly Story — Event prep in progress</td>
          <td><span class="cal-platform priority-med">Stories</span></td>
          <td>Story</td>
          <td>Insider feel, investment in event</td>
        </tr>
        <tr>
          <td><span class="cal-date">SUN 6/14</span></td>
          <td>Post #5 — Headshot Station reveal</td>
          <td><span class="cal-platform priority-high">IG</span></td>
          <td>Feed Post</td>
          <td>Activity-specific attendance driver</td>
        </tr>
        <tr>
          <td><span class="cal-date">MON 6/15</span></td>
          <td>Reel 11 — "If you're a producer in Charlotte, watch this"</td>
          <td><span class="cal-platform priority-high">IG + TikTok</span></td>
          <td>Reel</td>
          <td>Targeted reach to producers</td>
        </tr>
        <tr>
          <td><span class="cal-date">MON 6/15</span></td>
          <td>G3 Giveaway Story — Merch Package</td>
          <td><span class="cal-platform priority-med">Stories</span></td>
          <td>Story + Link</td>
          <td>Engagement, registration drive</td>
        </tr>
        <tr>
          <td><span class="cal-date">TUE 6/16</span></td>
          <td>Post #9 — Opportunity Wall feature</td>
          <td><span class="cal-platform priority-high">IG</span></td>
          <td>Feed Post</td>
          <td>Community angle, collaboration hook</td>
        </tr>
        <tr>
          <td><span class="cal-date">WED 6/17</span></td>
          <td>Reel 14 — Founder story. Real and raw.</td>
          <td><span class="cal-platform priority-high">IG + LinkedIn</span></td>
          <td>Reel / Long Video</td>
          <td>Trust, credibility, personal connection</td>
        </tr>
        <tr>
          <td><span class="cal-date">WED 6/17</span></td>
          <td>Q&A Story — Ask us anything about Creator Night</td>
          <td><span class="cal-platform priority-med">Stories</span></td>
          <td>Question Box</td>
          <td>Friction removal, engagement</td>
        </tr>
        <tr>
          <td><span class="cal-date">THU 6/18</span></td>
          <td>Post #12 — Vision X Bar feature</td>
          <td><span class="cal-platform priority-high">IG</span></td>
          <td>Multi-image post</td>
          <td>FOMO / aesthetic appeal</td>
        </tr>
        <tr>
          <td><span class="cal-date">THU 6/18</span></td>
          <td>G4 Giveaway — Strategy Session announcement</td>
          <td><span class="cal-platform priority-med">Stories</span></td>
          <td>Story</td>
          <td>Business owner targeting</td>
        </tr>
        <tr>
          <td><span class="cal-date">FRI 6/19</span></td>
          <td>Post #16 — Vision X Records is looking</td>
          <td><span class="cal-platform priority-high">IG + TikTok</span></td>
          <td>Reel or Feed Post</td>
          <td>Artist attendance driver</td>
        </tr>
        <tr>
          <td><span class="cal-date">FRI 6/19</span></td>
          <td>G8 — Share-to-win Story Campaign launch</td>
          <td><span class="cal-platform priority-high">Stories</span></td>
          <td>Story</td>
          <td>Viral sharing, organic reach</td>
        </tr>
        <tr>
          <td><span class="cal-date">SAT 6/20</span></td>
          <td>10-Day countdown post + 7-reason carousel goes out</td>
          <td><span class="cal-platform priority-high">IG</span></td>
          <td>Carousel</td>
          <td>Recap value props, drive final registrations</td>
        </tr>
        <tr>
          <td><span class="cal-date">SAT 6/20</span></td>
          <td>Countdown Sticker Story begins — Day 7 (Headshots)</td>
          <td><span class="cal-platform priority-high">Stories</span></td>
          <td>Story</td>
          <td>Daily urgency building</td>
        </tr>
      </tbody>
    </table>
  </div>

  <div class="calendar-week">
    <div class="calendar-week-label">WEEK 3 — FINAL PUSH / June 20–27</div>
    <table class="calendar-table">
      <thead>
        <tr><th>Date</th><th>Content</th><th>Platform</th><th>Format</th><th>Goal</th></tr>
      </thead>
      <tbody>
        <tr>
          <td><span class="cal-date">SUN 6/21</span></td>
          <td>Post #24 — Full event details. Schedule. Time. Location.</td>
          <td><span class="cal-platform priority-high">IG + FB</span></td>
          <td>Feed Post + Event</td>
          <td>Practical information, registration reminder</td>
        </tr>
        <tr>
          <td><span class="cal-date">MON 6/22</span></td>
          <td>Reel 17 — "5 days until Creator Night"</td>
          <td><span class="cal-platform priority-high">IG + TikTok</span></td>
          <td>Reel</td>
          <td>Final reach push</td>
        </tr>
        <tr>
          <td><span class="cal-date">MON 6/22</span></td>
          <td>G5 Giveaway — Membership Trial story</td>
          <td><span class="cal-platform priority-med">Stories</span></td>
          <td>Story</td>
          <td>Membership awareness pre-event</td>
        </tr>
        <tr>
          <td><span class="cal-date">TUE 6/23</span></td>
          <td>Post #19 — Entrepreneur call-out post</td>
          <td><span class="cal-platform priority-high">IG + LinkedIn</span></td>
          <td>Feed Post</td>
          <td>Business owner targeting, final push</td>
        </tr>
        <tr>
          <td><span class="cal-date">WED 6/24</span></td>
          <td>Post #13 — "What $0 gets you at Creator Night" (full value breakdown)</td>
          <td><span class="cal-platform priority-high">IG + TikTok</span></td>
          <td>Reel or Carousel</td>
          <td>Overcome last objections, drive registration</td>
        </tr>
        <tr>
          <td><span class="cal-date">WED 6/24</span></td>
          <td>G10 Grand Prize tease Story</td>
          <td><span class="cal-platform priority-high">Stories</span></td>
          <td>Story</td>
          <td>Maximum suspense before event</td>
        </tr>
        <tr>
          <td><span class="cal-date">THU 6/25</span></td>
          <td>Mix & Master giveaway winner announced (G2) + Creator Night 48-hr push</td>
          <td><span class="cal-platform priority-high">IG</span></td>
          <td>Feed Post + Story</td>
          <td>Winner announcement = social proof + urgency</td>
        </tr>
        <tr>
          <td><span class="cal-date">FRI 6/26</span></td>
          <td>Post #29 — "Last time we're going to say it" final push</td>
          <td><span class="cal-platform priority-high">IG + All Platforms</span></td>
          <td>Feed Post</td>
          <td>Final conversion, all-platform push</td>
        </tr>
        <tr>
          <td><span class="cal-date">FRI 6/26</span></td>
          <td>Day-before Story — Studio is ready, countdown sticker: 1 day</td>
          <td><span class="cal-platform priority-high">Stories</span></td>
          <td>Story</td>
          <td>Anticipation, practical reminder</td>
        </tr>
        <tr>
          <td><span class="cal-date">SAT 6/27</span></td>
          <td>Post #30 — Day-of post "Tonight is the night"</td>
          <td><span class="cal-platform priority-high">IG + All</span></td>
          <td>Feed Post</td>
          <td>Day-of excitement, last-minute attendees</td>
        </tr>
        <tr>
          <td><span class="cal-date">SAT 6/27</span></td>
          <td>Live Stories throughout the event — doors open, activities, performances, giveaways</td>
          <td><span class="cal-platform priority-high">Stories</span></td>
          <td>Live Stories</td>
          <td>FOMO for those not there, content capture</td>
        </tr>
        <tr>
          <td><span class="cal-date">SAT 6/27</span></td>
          <td>Reel 18 — Live event Reel posted during or end of night</td>
          <td><span class="cal-platform priority-high">IG + TikTok</span></td>
          <td>Reel</td>
          <td>Real-time proof of experience, post-event FOMO</td>
        </tr>
      </tbody>
    </table>
  </div>

  <div class="calendar-week">
    <div class="calendar-week-label">POST-EVENT — June 28+</div>
    <table class="calendar-table">
      <thead>
        <tr><th>Date</th><th>Content</th><th>Platform</th><th>Format</th><th>Goal</th></tr>
      </thead>
      <tbody>
        <tr>
          <td><span class="cal-date">SUN 6/28</span></td>
          <td>BTS 10 — Full event recap video + thank you post</td>
          <td><span class="cal-platform priority-high">IG + TikTok</span></td>
          <td>Reel / Post</td>
          <td>Proof, FOMO for Creator Night 2, community celebration</td>
        </tr>
        <tr>
          <td><span class="cal-date">MON 6/29</span></td>
          <td>Follow-up Story: "Here's your next step from Creator Night"</td>
          <td><span class="cal-platform priority-high">Stories</span></td>
          <td>Story + Link</td>
          <td>Drive post-event bookings and consultations</td>
        </tr>
        <tr>
          <td><span class="cal-date">TUE 6/30</span></td>
          <td>Post: "Creator Night 2 is already in the works. Follow to be first."</td>
          <td><span class="cal-platform priority-high">IG</span></td>
          <td>Feed Post</td>
          <td>Community retention, long-term growth</td>
        </tr>
      </tbody>
    </table>
  </div>
</section>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION 9: GUERRILLA MARKETING -->
<!-- ═══════════════════════════════════════════════ -->
<section class="section" id="guerrilla">
  <span class="section-label">Section 09</span>
  <h2 class="section-title">Guerrilla Marketing Strategy</h2>
  <p class="section-intro">The room doesn't fill itself. Digital is the broadcast. Guerrilla is the handshake. Charlotte is a city where who you know still opens doors. Use that.</p>

  <div class="guerrilla-grid">

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Local Partnerships</div>
      <span class="guerrilla-block-sub">Brick & Mortar Amplification</span>
      <ul class="action-list">
        <li>Charlotte barbershops and salons — flyers and QR codes at stations. This audience overlaps heavily with creators and artists.</li>
        <li>Charlotte coffee shops with creative clientele — leave Creator Night cards or mini flyers. Think: Enderly Coffee, Birdsong area, NoDa spots.</li>
        <li>Local music gear stores — Guitar Center, local independent shops. Bulletin boards and counter cards.</li>
        <li>Charlotte Black-owned businesses — cross-promote. Mutual audiences, mutual trust.</li>
        <li>Photography supply stores and studios — post Creator Night in their community boards.</li>
        <li>Co-working spaces (Hygge, Workshop Charlotte) — post on community boards, ask to email their members.</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">College Outreach</div>
      <span class="guerrilla-block-sub">Student Creator Pipeline</span>
      <ul class="action-list">
        <li>UNCC — Music department, communications, media/film programs. Talk to department heads about sharing the event with students.</li>
        <li>Johnson C. Smith — Creative programs, business school, student entrepreneurs.</li>
        <li>Belmont Abbey, Queens University — music and communications programs.</li>
        <li>Contact student organizations: music clubs, journalism clubs, photography clubs, entrepreneurship clubs.</li>
        <li>Post in Facebook groups for each school: "Charlotte music", "UNCC students", etc.</li>
        <li>Ask 1-2 current student creators to be official campus reps for Creator Night — give them early access or a giveaway entry incentive.</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Artist Outreach</div>
      <span class="guerrilla-block-sub">Direct-to-Creator</span>
      <ul class="action-list">
        <li>Find every Charlotte-based artist on SoundCloud, DistroKid, Spotify for Artists with Charlotte listed — DM each one personally.</li>
        <li>Attend open mics in Charlotte the 2 weeks before Creator Night. Hand out cards. Invite personally. These artists need the room.</li>
        <li>Search Instagram: #CharlotteMusic #CharlotteMusicScene #CharlotteArtist — follow, engage, DM personally.</li>
        <li>Contact Charlotte rap and R&B blogs/pages — offer to feature attending artists in exchange for promotion.</li>
        <li>DM producers on BeatStars, YouTube, Instagram who list Charlotte as their location.</li>
        <li>Reach out to Charlotte music venues — The Fillmore, The Underground, Neighborhood Theatre — ask to include Creator Night in their newsletters.</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Influencer Outreach</div>
      <span class="guerrilla-block-sub">Organic Amplification</span>
      <ul class="action-list">
        <li>Identify 10-15 Charlotte-based creators with 2K-50K followers. Mid-size influencers have better engagement and community trust than large accounts.</li>
        <li>Invite them personally — not a mass DM blast. One message, personalized, with a real reason why they specifically belong in the room.</li>
        <li>Offer: early access to the event, a dedicated headshot slot, potential feature on VX social in exchange for pre-event and day-of Story coverage.</li>
        <li>Target content creators who already talk about Charlotte nightlife, creative culture, entrepreneurship — their audience is your audience.</li>
        <li>Charlotte lifestyle bloggers and vloggers — Creator Night is content for them. Pitch it as an exclusive experience they get to share first.</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Business Owner Outreach</div>
      <span class="guerrilla-block-sub">Highest-LTV Segment</span>
      <ul class="action-list">
        <li>Charlotte Chamber of Commerce events — attend in the 2 weeks prior. Hand out VX cards. Every small business owner needs content.</li>
        <li>Charlotte Black Chamber events — heavily overlapping demographic.</li>
        <li>LinkedIn outreach — search Charlotte + entrepreneur/business owner. Send personalized connection requests with an event invitation message.</li>
        <li>Reach out to Charlotte-area marketing agencies — propose a referral or co-promotion arrangement.</li>
        <li>Target restaurants, boutiques, fitness studios, and personal brands in the Charlotte area — their content needs are immediate and ongoing.</li>
        <li>Charlotte business Facebook groups — post the event, engage authentically.</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Community Groups</div>
      <span class="guerrilla-block-sub">Digital Ground Game</span>
      <ul class="action-list">
        <li>Post in every relevant Charlotte Facebook Group: Charlotte entrepreneurs, Charlotte creatives, Charlotte events, Charlotte musicians, Charlotte photographers, Charlotte networking.</li>
        <li>Charlotte Reddit — r/Charlotte. Post about Creator Night authentically. No spam. Real community post.</li>
        <li>Nextdoor — Charlotte neighborhoods near Pineville especially.</li>
        <li>Eventbrite listing — Creator Night as a free event. High discovery platform for free local events.</li>
        <li>Do512 / Yelp Events / Meetup — list Creator Night on every free event platform in Charlotte.</li>
        <li>Charlotte Observer, Queen City Nerve, Creative Loafing CLT — pitch a story about VX and Creator Night. Position it as a cultural moment, not an advertisement.</li>
      </ul>
    </div>

  </div>
</section>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION 10: LEAD CAPTURE STRATEGY -->
<!-- ═══════════════════════════════════════════════ -->
<section class="section" id="leads">
  <span class="section-label">Section 10</span>
  <h2 class="section-title">Lead Capture Strategy</h2>
  <p class="section-intro">The event is the funnel. Every element of Creator Night is designed to capture meaningful data that converts into long-term revenue. Here's how to do it without being transactional.</p>

  <div class="flow-steps">

    <div class="flow-step">
      <div class="flow-step-num">1</div>
      <div class="flow-step-body">
        <div class="flow-step-title">Pre-Event Registration Form</div>
        <div class="flow-step-desc">Required for admission. Fields: Full name, phone number, Instagram handle, email, how they heard about VX (dropdown), what best describes them (multi-select: artist / producer / photographer / podcaster / videographer / entrepreneur / content creator / student / other), which services they're most interested in (multi-select), current biggest creative challenge (one line text). This is your most valuable data. Segment everything from this form.</div>
      </div>
    </div>

    <div class="flow-step">
      <div class="flow-step-num">2</div>
      <div class="flow-step-body">
        <div class="flow-step-title">Check-In Table — Confirmation + Data Touch</div>
        <div class="flow-step-desc">Check-in station at the door verifies registration and captures any missing data. Hand every attendee their Creator Passport here. Confirm their name, phone number on file. Optional: "Would you like to be added to the Vision X text list for exclusive updates and early access to events?" Checkbox yes/no. Most people say yes at a live event.</div>
      </div>
    </div>

    <div class="flow-step">
      <div class="flow-step-num">3</div>
      <div class="flow-step-body">
        <div class="flow-step-title">Creator Passport — Experience Mapping</div>
        <div class="flow-step-desc">The passport tracks which rooms each attendee visited. This is behavioral data. If someone completed the recording studio stamp and the artist development stamp — they're likely an artist interested in label services. If they hit the content studio and podcast booth — they're a content creator. Use stamp completion patterns to personalize follow-up outreach.</div>
      </div>
    </div>

    <div class="flow-step">
      <div class="flow-step-num">4</div>
      <div class="flow-step-body">
        <div class="flow-step-title">Opportunity Wall — Intent Capture</div>
        <div class="flow-step-desc">Before attendees write their I NEED / I OFFER cards, have them add their Instagram handle or phone number to the back of the card. The wall itself is networking — but the cards are a lead list. Who needs what is business intelligence for follow-up outreach.</div>
      </div>
    </div>

    <div class="flow-step">
      <div class="flow-step-num">5</div>
      <div class="flow-step-body">
        <div class="flow-step-title">Giveaway Entry Form</div>
        <div class="flow-step-desc">To enter giveaways (passport completion unlocks entries), attendees scan a QR code that takes them to a simple form: name, phone, email, which prize interests you most. This is an additional data capture moment that feels organic because they want the prize. This form also includes: "Would you like a follow-up consultation with a VX team member?" Yes / No.</div>
      </div>
    </div>

    <div class="flow-step">
      <div class="flow-step-num">6</div>
      <div class="flow-step-body">
        <div class="flow-step-title">Vision X Records / Artist Development Station</div>
        <div class="flow-step-desc">Dedicated table with a team member. Artists who approach this station fill out a brief artist intake form: name, genre, where they are in their journey, what they're looking for, social links, music links. This is a pre-qualified lead list for VX Records and artist development services.</div>
      </div>
    </div>

    <div class="flow-step">
      <div class="flow-step-num">7</div>
      <div class="flow-step-body">
        <div class="flow-step-title">Membership Interest Table</div>
        <div class="flow-step-desc">Membership station with team member. Sign up for membership info / waitlist at the event. Offer: "Creator Night Exclusive — sign up for a membership trial tonight at [rate] and lock in the Creator Night rate." First-night conversion attempt. Even if they don't sign up: capture email + name for the membership follow-up sequence.</div>
      </div>
    </div>

    <div class="flow-step">
      <div class="flow-step-num">8</div>
      <div class="flow-step-body">
        <div class="flow-step-title">Podcast Hot Seat — Email for Episode Link</div>
        <div class="flow-step-desc">Every Creator Hot Seat interview attendee gives their email to receive the recorded episode. This is a warm lead — they participated in VX content, they want the deliverable, they've experienced the podcast studio. Follow up with "your episode + here's how to book studio time for your own podcast."</div>
      </div>
    </div>

    <div class="flow-step">
      <div class="flow-step-num">9</div>
      <div class="flow-step-body">
        <div class="flow-step-title">Post-Event SMS Capture</div>
        <div class="flow-step-desc">End of night: "Text VISIONX to [number] to receive your event recap, photo gallery access, and exclusive post-event offer." This captures any attendees not already in the system and opens a direct SMS channel for follow-up conversion.</div>
      </div>
    </div>

    <div class="flow-step">
      <div class="flow-step-num">10</div>
      <div class="flow-step-body">
        <div class="flow-step-title">IG Follow Prompt</div>
        <div class="flow-step-desc">At every station, at check-in, on the passport: "Follow @visionxstudios for your event photos, episode links, and exclusive post-event offers." A followed account is the cheapest ongoing marketing channel. Convert every attendee into a follower before they leave the building.</div>
      </div>
    </div>

  </div>
</section>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION 11: FOLLOW-UP STRATEGY -->
<!-- ═══════════════════════════════════════════════ -->
<section class="section" id="followup">
  <span class="section-label">Section 11</span>
  <h2 class="section-title">Post-Event Follow-Up Strategy</h2>
  <p class="section-intro">The event is the introduction. The follow-up is the relationship. Most events lose 90% of their conversion potential in the 72 hours after close. Don't be most events.</p>

  <div class="conversion-grid">

    <div class="conversion-card">
      <span class="conversion-icon">🎙️</span>
      <div class="conversion-title">Converting Artists</div>
      <ul class="conversion-steps">
        <li>Within 24 hours: personal text/DM to every artist who filled out the intake form. "Loved meeting you last night. Your story stuck with me. Can we set up a call this week?"</li>
        <li>Send them a listening link to their Creator Hot Seat interview if applicable.</li>
        <li>Within 72 hours: send a "Vision X Artist Development" overview document via email. What the program includes. What the next step is.</li>
        <li>Within 1 week: invite to a follow-up studio session — either paid booking or a short complimentary session to continue the conversation.</li>
        <li>Within 2 weeks: VX Records artists are identified from this pool. Those conversations move to a separate track — direct meetings with the label side.</li>
      </ul>
    </div>

    <div class="conversion-card">
      <span class="conversion-icon">📱</span>
      <div class="conversion-title">Converting Content Clients</div>
      <ul class="conversion-steps">
        <li>Within 24 hours: email/text all attendees who checked "content" or "photography/video" as interests. "Based on what you saw last night — here's what a content package looks like at Vision X."</li>
        <li>Attach a simple one-pager: three content package options with clear pricing and deliverables.</li>
        <li>Influencers and content creators: follow them, engage with their next post, then DM. "Saw your content — your next shoot should be here. Want to talk?"</li>
        <li>Within 1 week: offer a "Creator Night Exclusive" discount on first content session — expires 7 days post-event.</li>
        <li>Business owners: book a content consultation call. Walk them through what consistent content strategy looks like from Vision X.</li>
      </ul>
    </div>

    <div class="conversion-card">
      <span class="conversion-icon">🏛️</span>
      <div class="conversion-title">Converting Members</div>
      <ul class="conversion-steps">
        <li>Within 24 hours: email to anyone who signed the membership interest list. "You showed interest in Vision X membership last night. Here's what it includes — and here's the Creator Night rate we're holding for 72 hours."</li>
        <li>Membership trial winners get onboarded immediately. Their experience becomes the next testimonial and social proof cycle.</li>
        <li>For interested non-converters: follow up at day 7 with a "last chance at Creator Night rate" message. Urgency closes membership faster than any sales pitch.</li>
        <li>Build a VX Community group (private IG, GroupMe, or Discord) and invite all Creator Night attendees. This is the membership preview — make them feel the community before they pay for it.</li>
        <li>Monthly: send updates about what members are building. Social proof of membership ROI.</li>
      </ul>
    </div>

    <div class="conversion-card">
      <span class="conversion-icon">🎛️</span>
      <div class="conversion-title">Converting Studio Clients</div>
      <ul class="conversion-steps">
        <li>Within 24 hours: email/text all attendees who completed the recording studio stamp. "You spent time in the booth last night. Here's how to book your first session — and here's a Creator Night exclusive rate for your first booking."</li>
        <li>Giveaway winners: get their session booked within 7 days. The session is also a sales opportunity — upsell mix & master, photography for the session, content creation.</li>
        <li>Producers who attended: reach out about booking the studio to bring in their artists. Position VX as their professional home base.</li>
        <li>First session pricing offer: expires 14 days post-event. Create urgency without pressure.</li>
        <li>After first session: follow up with mix & master upsell, membership upsell, content creation upsell.</li>
      </ul>
    </div>

    <div class="conversion-card">
      <span class="conversion-icon">📊</span>
      <div class="conversion-title">Email Sequence — All Attendees</div>
      <ul class="conversion-steps">
        <li>Day 1 (6/28): "Thank you for being in the room." Event recap, photo gallery link, giveaway winner announcement, next steps based on their registration category.</li>
        <li>Day 3 (6/30): Segment-specific email. Artists get artist content. Business owners get brand content info. Content creators get content package options. Personalization drives conversion.</li>
        <li>Day 7 (7/4): "Your Creator Night exclusive offer expires soon." One clear CTA: book a session, join a membership, schedule a consultation. One offer. One link. One deadline.</li>
        <li>Day 14 (7/11): Community update. "Here's what Creator Night alumni are building." Social proof + community belonging. Keeps VX top of mind.</li>
        <li>Day 30 (7/27): Creator Night 2 teaser. "We're already planning it. Follow along." Retention and anticipation for the next event cycle.</li>
      </ul>
    </div>

    <div class="conversion-card">
      <span class="conversion-icon">💬</span>
      <div class="conversion-title">SMS Follow-Up</div>
      <ul class="conversion-steps">
        <li>Day 1: "Thanks for coming through Vision X last night. Your photos are going up at @visionxstudios — tag us if you post. Your next step is here: [link]"</li>
        <li>Day 3: "Quick one — did you get a chance to check out our [service specific to them] options? We're holding the Creator Night rate until [date]. Reply to this to set up a quick call."</li>
        <li>Day 7: "[Name] — last chance on the Creator Night rate. After [date], normal pricing applies. [link]"</li>
        <li>SMS converts at 3-5x email. Use it deliberately, not frequently. Max 3 texts in the first 2 weeks. Every text must have one clear next step.</li>
      </ul>
    </div>

  </div>

  <div class="divider"></div>

  <div class="highlight-box">
    <p><strong>The 48-Hour Rule:</strong> The highest conversion window from any in-person event is within 48 hours of the experience. Every follow-up that happens in the first 48 hours converts at 4-10x the rate of follow-ups sent on day 7 or later. Prioritize speed over perfection. A personal text within 12 hours beats a perfect email on day 5 every single time.</p>
  </div>

  <div class="highlight-box" style="margin-top: 24px;">
    <p><strong>Creator Night 2:</strong> Within 30 days of Creator Night, announce Creator Night 2. A date doesn't need to be confirmed — just signal it's coming. Everyone who attended becomes a word-of-mouth engine when they know there's a next one. Plant that seed while the experience is still fresh. <strong>This is how you build the community, not just the event.</strong></p>
  </div>

</section>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION 12: META ADS STRATEGY -->
<!-- ═══════════════════════════════════════════════ -->
<section class="section" id="meta">
  <span class="section-label">Section 12</span>
  <h2 class="section-title">Meta Ads Strategy</h2>
  <p class="section-intro">Organic gets you seen by people who already follow you. Meta Ads get you in front of Charlotte's creative community who don't know you exist yet. This is your reach engine. Every dollar here should target, intrigue, and convert.</p>

  <!-- BUDGET -->
  <div class="highlight-box" style="margin-bottom:40px;">
    <p><strong>Recommended Budget:</strong> $500–$1,000 total across 21 days. Split: 60% Facebook/Instagram Feed & Reels ads, 25% Story ads, 15% retargeting. Even $300 focused correctly will move the needle on a free event in a city the size of Charlotte. Start at $15–25/day and scale what's working after day 3.</p>
  </div>

  <!-- CAMPAIGN STRUCTURE -->
  <h3 style="font-family:'Bebas Neue',Impact,sans-serif;font-size:36px;color:var(--gold);letter-spacing:0.05em;margin-bottom:24px;">Campaign Structure — 3 Phases</h3>
  <div class="strategy-grid" style="margin-bottom:48px;">

    <div class="strategy-block">
      <div class="strategy-block-num">01</div>
      <div class="strategy-block-title">Phase 1 — Awareness / June 6–13</div>
      <div class="strategy-block-body">
        <strong style="color:var(--white)">Objective: Reach + Brand Awareness</strong><br><br>
        Goal is impressions and top-of-funnel discovery. You want Charlotte's creative community to see Vision X for the first time and immediately think "what is this?"<br><br>
        <strong style="color:var(--gold)">Budget:</strong> $10–15/day<br>
        <strong style="color:var(--gold)">Placements:</strong> Instagram Feed, Instagram Reels, Facebook Feed<br>
        <strong style="color:var(--gold)">Bid Strategy:</strong> Maximize reach<br>
        <strong style="color:var(--gold)">Creative:</strong> Studio interior video, VX Bar shots, the X logo on black — nothing promotional yet. Just intrigue.
      </div>
    </div>

    <div class="strategy-block">
      <div class="strategy-block-num">02</div>
      <div class="strategy-block-title">Phase 2 — Conversion / June 14–24</div>
      <div class="strategy-block-body">
        <strong style="color:var(--white)">Objective: Traffic + Lead Generation</strong><br><br>
        Drive registration clicks. Every ad in this phase has one job: get people to the registration form. This is where you spend the most.<br><br>
        <strong style="color:var(--gold)">Budget:</strong> $20–30/day<br>
        <strong style="color:var(--gold)">Placements:</strong> Instagram Stories, Instagram Reels, Facebook Feed, Messenger<br>
        <strong style="color:var(--gold)">Bid Strategy:</strong> Maximize link clicks or leads<br>
        <strong style="color:var(--gold)">Creative:</strong> Giveaway reveals, activity announcements, "GET IN THE ROOM" direct response ads
      </div>
    </div>

    <div class="strategy-block">
      <div class="strategy-block-num">03</div>
      <div class="strategy-block-title">Phase 3 — Retargeting / June 20–27</div>
      <div class="strategy-block-body">
        <strong style="color:var(--white)">Objective: Retarget + Final Push</strong><br><br>
        Show ads to people who visited the registration page but didn't complete. Also retarget IG profile visitors and video viewers. Close the fence-sitters.<br><br>
        <strong style="color:var(--gold)">Budget:</strong> $15–20/day<br>
        <strong style="color:var(--gold)">Placements:</strong> Instagram Stories, Instagram Feed<br>
        <strong style="color:var(--gold)">Bid Strategy:</strong> Maximize conversions<br>
        <strong style="color:var(--gold)">Creative:</strong> Urgency ads — "Limited spots left," "Closes Friday," countdown-style creative
      </div>
    </div>

  </div>

  <!-- AUDIENCE TARGETING -->
  <h3 style="font-family:'Bebas Neue',Impact,sans-serif;font-size:36px;color:var(--gold);letter-spacing:0.05em;margin-bottom:24px;">Audience Targeting</h3>
  <div class="guerrilla-grid" style="margin-bottom:48px;">

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Core Audience 1</div>
      <span class="guerrilla-block-sub">Artists & Producers</span>
      <ul class="action-list">
        <li><strong style="color:var(--white)">Location:</strong> Charlotte, NC + 25 mile radius (Pineville, Ballantyne, Matthews, Concord, Gastonia)</li>
        <li><strong style="color:var(--white)">Age:</strong> 18–34</li>
        <li><strong style="color:var(--white)">Interests:</strong> Recording studios, music production, SoundCloud, Spotify for Artists, GarageBand, Pro Tools, FL Studio, Logic Pro, BeatStars</li>
        <li><strong style="color:var(--white)">Behaviors:</strong> Engaged shoppers, Small business owners, Content creators</li>
        <li><strong style="color:var(--white)">Estimated Audience:</strong> 40,000–80,000 people in Charlotte metro</li>
        <li><strong style="color:var(--white)">Budget Allocation:</strong> 30% of total ad spend</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Core Audience 2</div>
      <span class="guerrilla-block-sub">Content Creators & Influencers</span>
      <ul class="action-list">
        <li><strong style="color:var(--white)">Location:</strong> Charlotte, NC + 20 mile radius</li>
        <li><strong style="color:var(--white)">Age:</strong> 20–38</li>
        <li><strong style="color:var(--white)">Interests:</strong> Content creation, Instagram, TikTok, YouTube, photography, videography, Adobe Creative Suite, Canva, CapCut, social media marketing</li>
        <li><strong style="color:var(--white)">Behaviors:</strong> Facebook Page admins, Instagram Business accounts, engaged with creator content</li>
        <li><strong style="color:var(--white)">Estimated Audience:</strong> 60,000–120,000</li>
        <li><strong style="color:var(--white)">Budget Allocation:</strong> 25% of total ad spend</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Core Audience 3</div>
      <span class="guerrilla-block-sub">Entrepreneurs & Business Owners</span>
      <ul class="action-list">
        <li><strong style="color:var(--white)">Location:</strong> Charlotte, NC + surrounding suburbs</li>
        <li><strong style="color:var(--white)">Age:</strong> 25–45</li>
        <li><strong style="color:var(--white)">Interests:</strong> Entrepreneurship, small business, personal branding, marketing, digital marketing, LinkedIn, podcasting, brand building</li>
        <li><strong style="color:var(--white)">Behaviors:</strong> Small business owners, self-employed, frequent travelers, higher income bracket</li>
        <li><strong style="color:var(--white)">Estimated Audience:</strong> 80,000–150,000</li>
        <li><strong style="color:var(--white)">Budget Allocation:</strong> 25% of total ad spend</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Core Audience 4</div>
      <span class="guerrilla-block-sub">Podcasters & Speakers</span>
      <ul class="action-list">
        <li><strong style="color:var(--white)">Location:</strong> Charlotte, NC + 30 mile radius</li>
        <li><strong style="color:var(--white)">Age:</strong> 22–50</li>
        <li><strong style="color:var(--white)">Interests:</strong> Podcasting, Spotify, Apple Podcasts, Anchor, public speaking, storytelling, journalism, media production</li>
        <li><strong style="color:var(--white)">Behaviors:</strong> Podcast listeners (heavy), online media consumers</li>
        <li><strong style="color:var(--white)">Estimated Audience:</strong> 30,000–60,000</li>
        <li><strong style="color:var(--white)">Budget Allocation:</strong> 10% of total ad spend</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Retargeting Audience</div>
      <span class="guerrilla-block-sub">Warm Traffic — Highest Priority</span>
      <ul class="action-list">
        <li>People who visited the Creator Night registration page but did not complete</li>
        <li>People who engaged with any VX Instagram post or Reel in the last 30 days</li>
        <li>People who watched 50%+ of any VX video content</li>
        <li>Current email list / SMS list — upload as Custom Audience</li>
        <li>Lookalike audience (1–3%) built from current followers and email list</li>
        <li><strong style="color:var(--white)">Budget Allocation:</strong> 10% of total — highest converting segment</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Lookalike Audiences</div>
      <span class="guerrilla-block-sub">Expand from What's Working</span>
      <ul class="action-list">
        <li>1% Lookalike of VX IG followers — most similar to your current audience</li>
        <li>1% Lookalike of email/SMS list — people who already trusted you with their contact</li>
        <li>2% Lookalike of registration form completers — scale what converted</li>
        <li>Use Advantage+ audience after 3–5 days to let Meta optimize automatically based on early conversions</li>
        <li>Layer with Charlotte geo-targeting to keep all lookalikes local</li>
      </ul>
    </div>

  </div>

  <!-- AD CREATIVE SPECS -->
  <h3 style="font-family:'Bebas Neue',Impact,sans-serif;font-size:36px;color:var(--gold);letter-spacing:0.05em;margin-bottom:24px;">15 Meta Ad Concepts — Full Creative Briefs</h3>

  <div class="tabs">
    <button class="tab active" onclick="showTab('awareness-ads')">Awareness Ads</button>
    <button class="tab" onclick="showTab('conversion-ads')">Conversion Ads</button>
    <button class="tab" onclick="showTab('retargeting-ads')">Retargeting Ads</button>
    <button class="tab" onclick="showTab('story-ads')">Story Ads</button>
  </div>

  <!-- AWARENESS ADS -->
  <div id="awareness-ads" class="tab-content active">
    <div class="content-grid">

      <div class="content-card">
        <div class="card-num">A1</div>
        <span class="card-type">Awareness / Phase 1 / Feed + Reels</span>
        <div class="card-hook">"Something is happening in Charlotte."</div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">15-second Reel / Video</span></div>
        <div class="card-row"><span class="card-row-label">Visual Direction</span><span class="card-row-value">Cinematic walk through Vision X — low light, blue tones, the studio breathing. No words for first 3 seconds. Just the space. Then: "CREATOR NIGHT. JUNE 27." cuts in hard on a beat drop.</span></div>
        <div class="card-row"><span class="card-row-label">Primary Text</span><span class="card-row-value">Charlotte's most complete creative ecosystem is opening its doors. One night. Free. June 27, 2026. Vision X Studios, Pineville NC.</span></div>
        <div class="card-row"><span class="card-row-label">Headline</span><span class="card-row-value">Creator Night — June 27</span></div>
        <div class="card-row"><span class="card-row-label">CTA Button</span><span class="card-row-value">Learn More</span></div>
        <div class="card-row"><span class="card-row-label">Audience</span><span class="card-row-value">Core Audience 1 + 2 combined</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Video views / Brand awareness — get VX on Charlotte's radar</span></div>
      </div>

      <div class="content-card">
        <div class="card-num">A2</div>
        <span class="card-type">Awareness / Phase 1 / Feed</span>
        <div class="card-hook">"Charlotte doesn't have a creative hub. Until now."</div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">Single Image — 1080x1350 (the Creator Night PNG graphic)</span></div>
        <div class="card-row"><span class="card-row-label">Visual Direction</span><span class="card-row-value">The Creator Night event graphic. Black. Teal. Bold. Stops the scroll. No additional graphic treatment needed — the graphic is the ad.</span></div>
        <div class="card-row"><span class="card-row-label">Primary Text</span><span class="card-row-value">Recording. Mixing. Mastering. Photography. Video. Podcasting. Content Creation. Artist Development. Label Services. One studio. One ecosystem. Charlotte — this is Vision X. Creator Night is June 27. Free. Registration required.</span></div>
        <div class="card-row"><span class="card-row-label">Headline</span><span class="card-row-value">Vision X Creator Night — Free Event</span></div>
        <div class="card-row"><span class="card-row-label">CTA Button</span><span class="card-row-value">Sign Up</span></div>
        <div class="card-row"><span class="card-row-label">Audience</span><span class="card-row-value">All Core Audiences — broad awareness phase</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Reach + Impressions</span></div>
      </div>

      <div class="content-card">
        <div class="card-num">A3</div>
        <span class="card-type">Awareness / Phase 1 / Reels</span>
        <div class="card-hook">"POV: You just found out Vision X exists."</div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">Reel — 20-30 seconds</span></div>
        <div class="card-row"><span class="card-row-label">Visual Direction</span><span class="card-row-value">POV walking into Vision X — parking lot to bar. Each room revealed one at a time. Text overlays: "Recording Studio." "Podcast Booth." "Content Studio." "The Bar." Ends on: "CREATOR NIGHT. JUNE 27. FREE." Fast. Addictive. No wasted frame.</span></div>
        <div class="card-row"><span class="card-row-label">Primary Text</span><span class="card-row-value">This is Vision X Studios in Pineville, NC. If you're a Charlotte creator and you've never heard of it — that changes tonight. Creator Night is June 27. Free. Come see what's been here the whole time.</span></div>
        <div class="card-row"><span class="card-row-label">Headline</span><span class="card-row-value">See It For Yourself — June 27</span></div>
        <div class="card-row"><span class="card-row-label">CTA Button</span><span class="card-row-value">Learn More</span></div>
        <div class="card-row"><span class="card-row-label">Audience</span><span class="card-row-value">Core Audiences 1 + 2 — creator-heavy targeting</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Video views — build warm retargeting pool</span></div>
      </div>

      <div class="content-card">
        <div class="card-num">A4</div>
        <span class="card-type">Awareness / Phase 1 / Facebook Feed</span>
        <div class="card-hook">"Charlotte entrepreneurs — your content problem has a solution."</div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">Single Image + Long Copy (Facebook favors longer copy for business audiences)</span></div>
        <div class="card-row"><span class="card-row-label">Visual Direction</span><span class="card-row-value">Professional brand content shoot at VX — clean, aspirational. Not stock. Real. Shows the quality of VX's production environment.</span></div>
        <div class="card-row"><span class="card-row-label">Primary Text</span><span class="card-row-value">If you're a Charlotte business owner and your content isn't where it needs to be — Vision X Creator Night is your first step. On June 27, we're opening the studio to Charlotte's creative community. Come see our photography studio, video production setup, content strategy team, and podcast booth. All under one roof. All accessible. Free entry. Limited capacity. Register now.</span></div>
        <div class="card-row"><span class="card-row-label">Headline</span><span class="card-row-value">Free Entry — Vision X Creator Night</span></div>
        <div class="card-row"><span class="card-row-label">CTA Button</span><span class="card-row-value">Sign Up</span></div>
        <div class="card-row"><span class="card-row-label">Audience</span><span class="card-row-value">Core Audience 3 — Entrepreneurs / Business Owners</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Reach business owner segment on Facebook</span></div>
      </div>

    </div>
  </div>

  <!-- CONVERSION ADS -->
  <div id="conversion-ads" class="tab-content">
    <div class="content-grid">

      <div class="content-card">
        <div class="card-num">C1</div>
        <span class="card-type">Conversion / Phase 2 / Feed + Reels</span>
        <div class="card-hook">"We're giving away studio time at Creator Night. Here's how to get it."</div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">Video — 15 seconds</span></div>
        <div class="card-row"><span class="card-row-label">Visual Direction</span><span class="card-row-value">Recording booth front and center — SSL console, mic, warm light. Text hits: "4 HOURS FREE STUDIO TIME." Then: "Show up June 27. Complete your Creator Passport. You're entered." Fast. Clean. One message.</span></div>
        <div class="card-row"><span class="card-row-label">Primary Text</span><span class="card-row-value">At Vision X Creator Night, one attendee walks out with 4 free hours in our recording studio. All you have to do is show up. June 27. Vision X Studios, Pineville NC. Free event. Registration required — spots are limited.</span></div>
        <div class="card-row"><span class="card-row-label">Headline</span><span class="card-row-value">Win Free Studio Time — Register Now</span></div>
        <div class="card-row"><span class="card-row-label">Description</span><span class="card-row-value">Limited capacity. Registration closes when we hit capacity.</span></div>
        <div class="card-row"><span class="card-row-label">CTA Button</span><span class="card-row-value">Sign Up</span></div>
        <div class="card-row"><span class="card-row-label">Landing Page</span><span class="card-row-value">Registration form — pre-filled with event name. Minimal fields. Name, phone, email, creator type. That's it.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Lead generation / Registration completions</span></div>
      </div>

      <div class="content-card">
        <div class="card-num">C2</div>
        <span class="card-type">Conversion / Phase 2 / Instagram Feed</span>
        <div class="card-hook">"This is what $0 gets you at Creator Night."</div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">Carousel — 5 slides</span></div>
        <div class="card-row"><span class="card-row-label">Slide 1</span><span class="card-row-value">"$0 GETS YOU:" — Black card, teal text. Stops the scroll.</span></div>
        <div class="card-row"><span class="card-row-label">Slide 2</span><span class="card-row-value">Professional headshots — photographer, backdrop, studio lighting. "FREE HEADSHOTS."</span></div>
        <div class="card-row"><span class="card-row-label">Slide 3</span><span class="card-row-value">Podcast booth — mics, lights, professional setup. "PODCAST HOT SEAT."</span></div>
        <div class="card-row"><span class="card-row-label">Slide 4</span><span class="card-row-value">Studio console. "STUDIO TOUR + GIVEAWAY ENTRY."</span></div>
        <div class="card-row"><span class="card-row-label">Slide 5</span><span class="card-row-value">"+ NETWORKING. + ARTIST SPOTLIGHTS. + A COMMUNITY. JUNE 27. FREE. REGISTER NOW." with CTA.</span></div>
        <div class="card-row"><span class="card-row-label">Primary Text</span><span class="card-row-value">Charlotte — Creator Night is free. But look what free gets you. Swipe to see everything happening June 27 at Vision X Studios.</span></div>
        <div class="card-row"><span class="card-row-label">CTA Button</span><span class="card-row-value">Sign Up</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Drive registrations — value stack carousel</span></div>
      </div>

      <div class="content-card">
        <div class="card-num">C3</div>
        <span class="card-type">Conversion / Phase 2 / Artists Segment</span>
        <div class="card-hook">"Vision X Records is watching. Creator Night is June 27."</div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">Single Image or 15s video — dark, dramatic</span></div>
        <div class="card-row"><span class="card-row-label">Visual Direction</span><span class="card-row-value">Artist silhouette behind studio glass. Moody. Cinematic. "VX RECORDS" text overlaid with an eye icon. The visual communicates: serious. Label-level.</span></div>
        <div class="card-row"><span class="card-row-label">Primary Text</span><span class="card-row-value">Vision X Records is looking for Charlotte's next artists. Creator Night on June 27 is a showcase night — perform, connect, and get in front of the label team. Free event. Artist spotlights available. Apply at the link.</span></div>
        <div class="card-row"><span class="card-row-label">Headline</span><span class="card-row-value">Artist Spotlights — Vision X Creator Night</span></div>
        <div class="card-row"><span class="card-row-label">CTA Button</span><span class="card-row-value">Apply Now</span></div>
        <div class="card-row"><span class="card-row-label">Audience</span><span class="card-row-value">Core Audience 1 — Artists & Producers only. Narrow targeting.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Artist registrations + spotlight applications</span></div>
      </div>

      <div class="content-card">
        <div class="card-num">C4</div>
        <span class="card-type">Conversion / Phase 2 / Business Owners</span>
        <div class="card-hook">"Your brand needs better content. Creator Night shows you how."</div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">Single Image — 1080x1080 square</span></div>
        <div class="card-row"><span class="card-row-label">Visual Direction</span><span class="card-row-value">Professional brand content being shot at VX — clean product, clean lighting, real production quality. The visual contrast vs. DIY content is immediate and obvious.</span></div>
        <div class="card-row"><span class="card-row-label">Primary Text</span><span class="card-row-value">Charlotte business owners — your brand is only as strong as how it looks. Vision X Creator Night on June 27 gives you a free look inside our content studio, photo studio, and brand content team. Come see what professional brand content actually looks like. Free. Registration required.</span></div>
        <div class="card-row"><span class="card-row-label">Headline</span><span class="card-row-value">Free Brand Content Consultation — Register Now</span></div>
        <div class="card-row"><span class="card-row-label">CTA Button</span><span class="card-row-value">Sign Up</span></div>
        <div class="card-row"><span class="card-row-label">Audience</span><span class="card-row-value">Core Audience 3 — Business Owners. Facebook + Instagram.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Drive highest-LTV segment to register</span></div>
      </div>

      <div class="content-card">
        <div class="card-num">C5</div>
        <span class="card-type">Conversion / Phase 2 / Testimonial Ad</span>
        <div class="card-hook">"Don't take our word for it."</div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">Video — 30 seconds. Real client on camera.</span></div>
        <div class="card-row"><span class="card-row-label">Script Direction</span><span class="card-row-value">Existing VX client, talking directly to camera. Unscripted. Real words about what VX changed for them. No logo until the end. The testimonial IS the ad. End card: "Creator Night — June 27. Come see for yourself. Free."</span></div>
        <div class="card-row"><span class="card-row-label">Primary Text</span><span class="card-row-value">Charlotte creators are already inside Vision X. On June 27, you get to come see what they've been building. Creator Night is free. Registration is required. Come find out what you've been missing.</span></div>
        <div class="card-row"><span class="card-row-label">Headline</span><span class="card-row-value">Real Results. Real People. Creator Night June 27.</span></div>
        <div class="card-row"><span class="card-row-label">CTA Button</span><span class="card-row-value">Sign Up</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Trust + conversion — social proof is the most powerful converter</span></div>
      </div>

    </div>
  </div>

  <!-- RETARGETING ADS -->
  <div id="retargeting-ads" class="tab-content">
    <div class="content-grid">

      <div class="content-card">
        <div class="card-num">R1</div>
        <span class="card-type">Retargeting / Phase 3 / Page Visitors</span>
        <div class="card-hook">"You looked. Come back."</div>
        <div class="card-row"><span class="card-row-label">Audience</span><span class="card-row-value">People who visited the registration page but did NOT complete registration. 7-day window.</span></div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">Single Image — 1080x1350</span></div>
        <div class="card-row"><span class="card-row-label">Visual Direction</span><span class="card-row-value">The Creator Night PNG graphic — clean, direct. No new creative needed. They already know what it is.</span></div>
        <div class="card-row"><span class="card-row-label">Primary Text</span><span class="card-row-value">You were this close. Creator Night is June 27. Free. Spots are filling up. The registration takes 60 seconds. Finish what you started.</span></div>
        <div class="card-row"><span class="card-row-label">Headline</span><span class="card-row-value">Spots Filling Up — Complete Your Registration</span></div>
        <div class="card-row"><span class="card-row-label">CTA Button</span><span class="card-row-value">Sign Up</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Recover abandoned registrations — highest converting retargeting segment</span></div>
      </div>

      <div class="content-card">
        <div class="card-num">R2</div>
        <span class="card-type">Retargeting / Phase 3 / Video Viewers</span>
        <div class="card-hook">"You watched. Now register."</div>
        <div class="card-row"><span class="card-row-label">Audience</span><span class="card-row-value">People who watched 50%+ of any VX video or Reel in the last 30 days. Warm — they know VX.</span></div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">15-second video — different room than what they already saw</span></div>
        <div class="card-row"><span class="card-row-label">Primary Text</span><span class="card-row-value">You've seen what Vision X looks like. Now come see it in person. Creator Night is June 27. Free event. Limited capacity. The registration is open — but not for much longer.</span></div>
        <div class="card-row"><span class="card-row-label">Headline</span><span class="card-row-value">June 27 — Register Free Before It Closes</span></div>
        <div class="card-row"><span class="card-row-label">CTA Button</span><span class="card-row-value">Sign Up</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Convert warm video viewers to registrants</span></div>
      </div>

      <div class="content-card">
        <div class="card-num">R3</div>
        <span class="card-type">Retargeting / Final 72 Hours / Urgency</span>
        <div class="card-hook">"3 days. That's it."</div>
        <div class="card-row"><span class="card-row-label">Audience</span><span class="card-row-value">All warm audiences — page visitors, video viewers, IG engagers. Everyone who touched VX content but hasn't registered.</span></div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">Single Image — stark. Date-only creative. "JUNE 27." Nothing else.</span></div>
        <div class="card-row"><span class="card-row-label">Primary Text</span><span class="card-row-value">3 days until Creator Night. Vision X Studios. Pineville NC. If you're registered — share this. If you're not — this is your last real chance. Registration closes when we hit capacity. Don't be the person who missed it.</span></div>
        <div class="card-row"><span class="card-row-label">Headline</span><span class="card-row-value">Last Chance — Register for Creator Night</span></div>
        <div class="card-row"><span class="card-row-label">CTA Button</span><span class="card-row-value">Sign Up</span></div>
        <div class="card-row"><span class="card-row-label">Schedule</span><span class="card-row-value">Run June 24–27 only. High frequency acceptable — 3 days, warm audience, urgency context. People expect to see it.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Final conversion squeeze — close every remaining fence-sitter</span></div>
      </div>

    </div>
  </div>

  <!-- STORY ADS -->
  <div id="story-ads" class="tab-content">
    <div class="content-grid">

      <div class="content-card">
        <div class="card-num">S1</div>
        <span class="card-type">Story Ad / Phase 1 / Awareness</span>
        <div class="card-hook">"Full screen. Black. Teal. CREATOR NIGHT."</div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">Story — 1080x1920. 6-second video or static image</span></div>
        <div class="card-row"><span class="card-row-label">Visual Direction</span><span class="card-row-value">Creator Night graphic full screen. Or: Studio room — lights fade up. Text appears: "CREATOR NIGHT." Then: "JUNE 27." Then: "CHARLOTTE." Swipe up. Done in 6 seconds. Maximum punch.</span></div>
        <div class="card-row"><span class="card-row-label">Copy Overlay</span><span class="card-row-value">"Charlotte's creative ecosystem. June 27. Free." — text only, bottom third, small and clean.</span></div>
        <div class="card-row"><span class="card-row-label">CTA</span><span class="card-row-value">Swipe Up → Registration page</span></div>
        <div class="card-row"><span class="card-row-label">Audience</span><span class="card-row-value">Broad Charlotte creative targeting — all 4 core audiences</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Reach / Awareness — Story placement is cheapest per impression</span></div>
      </div>

      <div class="content-card">
        <div class="card-num">S2</div>
        <span class="card-type">Story Ad / Phase 2 / Giveaway Hook</span>
        <div class="card-hook">"Swipe up to enter for free studio time."</div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">Story — 1080x1920. 10-second video</span></div>
        <div class="card-row"><span class="card-row-label">Visual Direction</span><span class="card-row-value">Fast reveal of giveaway prizes — studio time, merch, membership. Each prize 2 seconds. Countdown feel. Ends: "Win at Creator Night. June 27. Swipe Up to Register."</span></div>
        <div class="card-row"><span class="card-row-label">Copy Overlay</span><span class="card-row-value">"Register → Attend → Win. That's the formula." — top of frame, bold.</span></div>
        <div class="card-row"><span class="card-row-label">CTA</span><span class="card-row-value">Swipe Up → Registration page</span></div>
        <div class="card-row"><span class="card-row-label">Audience</span><span class="card-row-value">Core Audiences 1 + 2 — artist and creator targeting</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Registration conversion via giveaway incentive</span></div>
      </div>

      <div class="content-card">
        <div class="card-num">S3</div>
        <span class="card-type">Story Ad / Phase 3 / Urgency Close</span>
        <div class="card-hook">"X days left."</div>
        <div class="card-row"><span class="card-row-label">Ad Format</span><span class="card-row-value">Story — Static image. Updated daily June 24–27.</span></div>
        <div class="card-row"><span class="card-row-label">Visual Direction</span><span class="card-row-value">Black screen. Massive number: "3" or "2" or "1" or "TONIGHT." Teal. That's it. Below: "Days until Creator Night." Below that: "Vision X Studios." Bottom: Register button. The simplicity IS the urgency.</span></div>
        <div class="card-row"><span class="card-row-label">Copy</span><span class="card-row-value">No copy needed beyond what's in the visual. Simplicity converts at this stage.</span></div>
        <div class="card-row"><span class="card-row-label">CTA</span><span class="card-row-value">Swipe Up → Registration page</span></div>
        <div class="card-row"><span class="card-row-label">Audience</span><span class="card-row-value">Retargeting only — warm audiences. Don't show this to cold traffic.</span></div>
        <div class="card-row"><span class="card-row-label">Objective</span><span class="card-row-value">Final registrations — urgency drives action</span></div>
      </div>

    </div>
  </div>

  <!-- AD COPY FORMULAS -->
  <div class="divider"></div>
  <h3 style="font-family:'Bebas Neue',Impact,sans-serif;font-size:36px;color:var(--gold);letter-spacing:0.05em;margin-bottom:24px;">Ad Copy Formulas — Ready to Deploy</h3>
  <div class="flow-steps">

    <div class="flow-step">
      <div class="flow-step-num">1</div>
      <div class="flow-step-body">
        <div class="flow-step-title">The FOMO Formula (best for Reels + Feed)</div>
        <div class="flow-step-desc">[Location]-based creators are already registering for [Event]. [Specific value prop]. [Date]. [Venue]. [Free/cost]. [CTA].<br><br><em>Example: "Charlotte's most ambitious creators are already registered for Creator Night. Professional headshots. Studio tours. Podcast hot seat. Free giveaways. June 27. Vision X Studios, Pineville. Free event — limited spots. Register now."</em></div>
      </div>
    </div>

    <div class="flow-step">
      <div class="flow-step-num">2</div>
      <div class="flow-step-body">
        <div class="flow-step-title">The Problem-Solution Formula (best for Business Owner targeting)</div>
        <div class="flow-step-desc">[Identify the problem they have]. [Agitate it briefly]. [Position VX as the solution]. [Event as the access point]. [CTA].<br><br><em>Example: "Your business is posting content that isn't working. You know it. The issue isn't effort — it's environment and strategy. Vision X Creator Night shows you what professional brand content looks like and how to get it. June 27. Free. Register now."</em></div>
      </div>
    </div>

    <div class="flow-step">
      <div class="flow-step-num">3</div>
      <div class="flow-step-body">
        <div class="flow-step-title">The Direct Value Formula (best for giveaway ads + Story ads)</div>
        <div class="flow-step-desc">[State the exact prize or value]. [How to get it — make it simple]. [Date + location]. [CTA].<br><br><em>Example: "Free studio time. Free professional headshots. Free podcast recording. All at Creator Night — June 27 at Vision X Studios. Show up. That's it. Register free at the link."</em></div>
      </div>
    </div>

    <div class="flow-step">
      <div class="flow-step-num">4</div>
      <div class="flow-step-body">
        <div class="flow-step-title">The Social Proof Formula (best for conversion phase)</div>
        <div class="flow-step-desc">[# of people doing X thing]. [Social validation]. [FOMO trigger]. [CTA].<br><br><em>Example: "[X] Charlotte creators have already registered for Creator Night. Producers. Photographers. Entrepreneurs. Artists. The room is building. Are you in it? June 27. Vision X Studios. Free — but spots are limited. Register now."</em></div>
      </div>
    </div>

    <div class="flow-step">
      <div class="flow-step-num">5</div>
      <div class="flow-step-body">
        <div class="flow-step-title">The Urgency Formula (retargeting + final push only)</div>
        <div class="flow-step-desc">[Time remaining]. [What they'll miss]. [Hard close]. [CTA].<br><br><em>Example: "72 hours. Creator Night closes registration when we hit capacity. Charlotte — this is the last real window. You've been thinking about it. Stop thinking. Register. June 27. Vision X Studios."</em></div>
      </div>
    </div>

  </div>

  <!-- PIXEL + TRACKING -->
  <div class="divider"></div>
  <h3 style="font-family:'Bebas Neue',Impact,sans-serif;font-size:36px;color:var(--gold);letter-spacing:0.05em;margin-bottom:24px;">Pixel Setup & Conversion Tracking</h3>
  <div class="strategy-grid">

    <div class="strategy-block">
      <div class="strategy-block-num">01</div>
      <div class="strategy-block-title">Meta Pixel Installation</div>
      <div class="strategy-block-body">
        Install the Meta Pixel on the Creator Night registration page BEFORE running any ads. This is non-negotiable. Without it, retargeting is impossible and optimization is blind.<br><br>
        Key events to track: PageView (on registration page), Lead (on form submit / thank you page), CompleteRegistration (confirmation).<br><br>
        If using a form tool (Typeform, Jotform, etc.) — use the pixel integration or URL parameter tracking to fire the Lead event on submission.
      </div>
    </div>

    <div class="strategy-block">
      <div class="strategy-block-num">02</div>
      <div class="strategy-block-title">UTM Parameters</div>
      <div class="strategy-block-body">
        Tag every ad link with UTM parameters so you know exactly which ad drove which registration.<br><br>
        Format: ?utm_source=facebook&utm_medium=paid&utm_campaign=creator-night&utm_content=[ad-name]<br><br>
        This lets you see in Google Analytics or the form tool which specific ad creative is converting best — and where to put more budget.
      </div>
    </div>

    <div class="strategy-block">
      <div class="strategy-block-num">03</div>
      <div class="strategy-block-title">Custom Audiences to Build Now</div>
      <div class="strategy-block-body">
        Start building these immediately — they need data before Phase 3:<br><br>
        • Website visitors (anyone who visits visionxstudios.com)<br>
        • Registration page visitors (non-converters)<br>
        • Video viewers 50%+ — from any existing VX content<br>
        • IG profile engagers — 30 and 60 day windows<br>
        • Customer list — upload existing contacts as Custom Audience
      </div>
    </div>

    <div class="strategy-block">
      <div class="strategy-block-num">04</div>
      <div class="strategy-block-title">A/B Testing Plan</div>
      <div class="strategy-block-body">
        Test one variable at a time. Don't change everything at once.<br><br>
        <strong style="color:var(--gold)">Week 1 Test:</strong> Video vs. Static image — which drives more link clicks?<br><br>
        <strong style="color:var(--gold)">Week 2 Test:</strong> Giveaway hook vs. Value stack hook — which registers more?<br><br>
        <strong style="color:var(--gold)">Week 3:</strong> Stop testing. Scale the winner. Urgency creative only.<br><br>
        Budget $20–30 on each variant, give it 3 days, kill the loser.
      </div>
    </div>

    <div class="strategy-block">
      <div class="strategy-block-num">05</div>
      <div class="strategy-block-title">KPIs to Track Daily</div>
      <div class="strategy-block-body">
        <strong style="color:var(--gold)">CPM</strong> — cost per 1,000 impressions. Target under $12 in Charlotte market.<br><br>
        <strong style="color:var(--gold)">CTR</strong> — click-through rate. Target 1.5%+ on feed ads. Under 1% = change the creative.<br><br>
        <strong style="color:var(--gold)">CPL</strong> — cost per lead (registration). Target under $3 for a free event. Under $1 is excellent.<br><br>
        <strong style="color:var(--gold)">ROAS</strong> — not applicable here (free event). Measure cost per registration against LTV of converting 1 attendee to a paying client.
      </div>
    </div>

    <div class="strategy-block">
      <div class="strategy-block-num">06</div>
      <div class="strategy-block-title">Post-Event Meta Strategy</div>
      <div class="strategy-block-body">
        Don't stop ads after the event. The post-event window is a conversion opportunity.<br><br>
        June 28–July 7: Run a "missed it?" ad to people who engaged but didn't attend. Offer a waitlist for Creator Night 2 and a first-session booking offer.<br><br>
        Creative: Event recap video. Real footage. Real energy. "This is what you missed. Don't miss the next one." → VX booking/membership page.<br><br>
        Budget: $5–10/day. Very targeted. High intent audience.
      </div>
    </div>

  </div>

</section>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION 13: FULL CHARLOTTE OUTREACH MAP -->
<!-- ═══════════════════════════════════════════════ -->
<section class="section" id="outreach">
  <span class="section-label">Section 13</span>
  <h2 class="section-title">Charlotte Market Domination Map</h2>
  <p class="section-intro">Every channel, every platform, every tactic — mapped and prioritized. This is the full-court press to make Creator Night the biggest creative event Charlotte has seen.</p>

  <div class="guerrilla-grid">

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Press & Media</div>
      <span class="guerrilla-block-sub">Earned Media Targets</span>
      <ul class="action-list">
        <li>Charlotte Observer — pitch as a cultural story: "Charlotte's Creative Underground is Surfacing." Contact the Arts & Culture desk. This is not an event listing — it's a story about a movement.</li>
        <li>Queen City Nerve — Charlotte's alternative arts publication. Perfect audience match. Pitch directly to their editor.</li>
        <li>Creative Loafing Charlotte — lifestyle + arts coverage. Creator Night fits their editorial perfectly.</li>
        <li>Charlotte Magazine — business/lifestyle. Angle: "The Studio Building Charlotte's Next Generation of Creators."</li>
        <li>WFAE / Charlotte NPR — community events and arts stories. Free event serving Charlotte creatives is a natural fit.</li>
        <li>Charlotte Business Journal — frame as a business story: creator economy, local studio scaling, Vision X as a Charlotte economic asset.</li>
        <li>Local TV (WBTV, WCNC, WSOC) — morning show segment potential. "Free creative event coming to Charlotte" is a feel-good local story. Pitch their community calendar AND their producer directly.</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Digital Platforms</div>
      <span class="guerrilla-block-sub">Free Listing Distribution</span>
      <ul class="action-list">
        <li>Eventbrite — list as free event. High discovery. Charlotte-specific search traffic. Fill all fields, optimize description for "Charlotte creator event" keywords.</li>
        <li>Facebook Events — create official event, invite all followers, boost the event post. Share in every relevant Charlotte group.</li>
        <li>Meetup.com — create a Vision X group + list Creator Night. Charlotte has active Meetup communities for entrepreneurs and creatives.</li>
        <li>Nextdoor — post in Pineville and surrounding neighborhoods. Geo-targeted. Free. Underutilized by event marketers.</li>
        <li>Reddit r/Charlotte — one authentic, non-spammy post about Creator Night. Engage comments genuinely. Charlotte Reddit is active and responsive.</li>
        <li>Do512 Charlotte / Yelp Events / Google Events — list on every aggregator. These pull into Google search results for "Charlotte events June 2026."</li>
        <li>LinkedIn Events — create event on the VX LinkedIn company page. Critical for reaching the entrepreneur and business owner segment.</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">SMS & Email Blast</div>
      <span class="guerrilla-block-sub">Existing Contacts — First Push</span>
      <ul class="action-list">
        <li>Text every phone number in your contacts personally within 24 hours of this campaign launching. Not a mass text — individual messages. "Hey [name] — I'm hosting Creator Night at the studio June 27. Free event, limited spots. You'd be a perfect fit. Want me to send you the link?"</li>
        <li>Email your entire list with the announcement email. Subject line options: "You're invited to Creator Night" / "The studio is opening its doors" / "June 27 — get in the room."</li>
        <li>Past clients: personal outreach by phone or DM. They've already experienced VX quality — they're your best advocates.</li>
        <li>Current members / active bookings: send them to Creator Night and ask them to bring 2 people. Word of mouth from existing clients is worth more than any ad.</li>
        <li>Set up SMS broadcast via SimpleTexting, SlickText, or Klaviyo. Build the list starting now so you have an SMS channel ready for the event and post-event marketing.</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Physical / Street</div>
      <span class="guerrilla-block-sub">On-the-Ground Presence</span>
      <ul class="action-list">
        <li>Design and print 500 Creator Night postcards — 4x6, premium stock, black with teal. QR code to registration. Place at every barbershop, salon, coffee shop, music store, gym, and co-working space in Charlotte and Pineville.</li>
        <li>Design 3-4 large-format flyers (11x17) for community bulletin boards at UNCC, JCSU, coffee shops, and creative spaces.</li>
        <li>Attend every open mic, pop-up market, and creator event in Charlotte from now to June 21. Show up. Hand out cards. Invite personally. The handshake still converts.</li>
        <li>Charlotte music venues — The Underground, Neighborhood Theatre, Stage Door, Petra's — ask to put flyers in their space and in their newsletter.</li>
        <li>Pop-up table at a Charlotte creative market or food/music event in the 2 weeks prior. A small VX presence at an existing event is free brand exposure to your exact target audience.</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Strategic Partnerships</div>
      <span class="guerrilla-block-sub">Amplify Through Others</span>
      <ul class="action-list">
        <li>Charlotte Black Chamber of Commerce — co-promote Creator Night. They have a direct line to Charlotte's Black business community, which is heavily represented in VX's target demographic.</li>
        <li>Charlotte Chamber of Commerce — list in their events calendar and member communications.</li>
        <li>Other Charlotte studios (non-competing services) — propose cross-promotion. You're not competing; you're building the scene together.</li>
        <li>Charlotte creative agencies — invite their creative directors and teams. These are future referral partners and potential content clients.</li>
        <li>University music and media departments — UNCC, JCSU — offer a free student registration block in exchange for promotion through their channels.</li>
        <li>Charlotte music distributors and managers — they work with the exact artists you want at Creator Night. One well-connected manager can bring 10 artists.</li>
      </ul>
    </div>

    <div class="guerrilla-block">
      <div class="guerrilla-block-title">Day-Of Amplification</div>
      <span class="guerrilla-block-sub">Make the Room Loud Online</span>
      <ul class="action-list">
        <li>Create an event hashtag: #VisionXCreatorNight and #VXCreatorNight. Put it on every surface inside the studio — printed signs, the Opportunity Wall, the Creator Passport. Make it easy for attendees to tag it.</li>
        <li>Set up a branded photo moment (step-and-repeat style backdrop or neon sign) that people will naturally want to photograph and post. The VX logo + "Creator Night" on a black wall is enough.</li>
        <li>Designate one team member as the content capture lead — their only job is to film everything from arrival to giveaways. This footage is the campaign for Creator Night 2.</li>
        <li>Live Story the entire event. Every giveaway winner. Every artist spotlight. Every interesting conversation you overhear. The people not there need to feel what they're missing in real time.</li>
        <li>Offer a "post and tag us" incentive — anyone who posts about Creator Night during the event and tags @visionxstudios gets an extra giveaway entry. UGC generation machine.</li>
        <li>End the night with a group photo — everyone still there at the final giveaway. Post it the next morning. "This is who showed up for Creator Night." Community identity + FOMO for Creator Night 2.</li>
      </ul>
    </div>

  </div>
</section>

<footer>
  Vision X Creator Night — Complete Campaign Document<br>
  Built for Vision X Studios, Charlotte NC — June 2026<br>
  <span style="color:var(--gold);margin-top:8px;display:block;">GET IN THE ROOM.</span>
</footer>

<script>
  function showTab(id) {
    const btn = event.target;
    const tabGroup = btn.closest('.tabs');
    // Deactivate all tabs in this group
    tabGroup.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
    // Find the parent section and deactivate all tab-content within it
    const section = btn.closest('.section');
    section.querySelectorAll('.tab-content').forEach(c => c.classList.remove('active'));
    // Activate selected
    document.getElementById(id).classList.add('active');
    btn.classList.add('active');
  }
</script>

</body>
</html>
