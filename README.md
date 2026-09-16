# tahu-<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tahu Isi — Gorengan Rumahan, Rasa Turun-Temurun</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,500&family=Work+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --cream:#F5EFE4;
    --cream-soft:#EFE6D6;
    --brown-dark:#3E2B23;
    --caramel:#8B5E3C;
    --sage:#6B7A5E;
    --beige:#D9C8A9;
    --white:#FFFDF9;
    --max-w:1120px;
  }

  *{ box-sizing:border-box; }
  html{ scroll-behavior:smooth; }
  body{
    margin:0;
    background:var(--cream);
    color:var(--brown-dark);
    font-family:'Work Sans', sans-serif;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,.display{
    font-family:'Fraunces', serif;
    font-weight:500;
    margin:0;
    color:var(--brown-dark);
  }
  p{ margin:0 0 1em; max-width:62ch; }
  a{ color:inherit; }
  img{ max-width:100%; display:block; }
  section{ padding:96px 24px; }
  .wrap{ max-width:var(--max-w); margin:0 auto; }

  /* Focus visibility */
  a:focus-visible, button:focus-visible{
    outline:2px solid var(--caramel);
    outline-offset:3px;
  }

  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
    *{ animation-duration:0.001ms !important; transition-duration:0.001ms !important; }
  }

  /* ---------- NAVBAR ---------- */
  header.nav{
    position:sticky;
    top:0;
    z-index:50;
    background:rgba(245,239,228,0.92);
    backdrop-filter:blur(6px);
    border-bottom:1px solid var(--beige);
  }
  .nav-inner{
    max-width:var(--max-w);
    margin:0 auto;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:16px 24px;
  }
  .brand{
    font-family:'Fraunces', serif;
    font-size:1.25rem;
    font-weight:600;
    letter-spacing:0.01em;
    text-decoration:none;
    color:var(--brown-dark);
  }
  .navlinks{
    display:flex;
    gap:28px;
    list-style:none;
    margin:0;
    padding:0;
  }
  .navlinks a{
    text-decoration:none;
    font-size:0.95rem;
    color:var(--brown-dark);
    position:relative;
    padding-bottom:4px;
  }
  .navlinks a::after{
    content:'';
    position:absolute;
    left:0; bottom:0;
    width:0; height:2px;
    background:var(--caramel);
    transition:width .25s ease;
  }
  .navlinks a:hover::after,
  .navlinks a:focus-visible::after{ width:100%; }

  .nav-toggle{
    display:none;
    background:none;
    border:1px solid var(--brown-dark);
    border-radius:6px;
    padding:6px 10px;
    font-size:1.1rem;
    cursor:pointer;
    color:var(--brown-dark);
  }

  @media (max-width:760px){
    .navlinks{
      position:absolute;
      top:100%;
      left:0; right:0;
      background:var(--cream);
      border-bottom:1px solid var(--beige);
      flex-direction:column;
      gap:0;
      display:none;
      padding:8px 24px 16px;
    }
    .navlinks.open{ display:flex; }
    .navlinks a{ padding:12px 0; border-bottom:1px solid var(--beige); }
    .nav-toggle{ display:inline-block; }
  }

  /* ---------- PHOTO PLACEHOLDER ---------- */
  .photo-placeholder{
    background:repeating-linear-gradient(135deg, var(--beige), var(--beige) 10px, var(--cream-soft) 10px, var(--cream-soft) 20px);
    border:1px dashed var(--caramel);
    border-radius:4px;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    color:var(--caramel);
    font-size:0.9rem;
    padding:16px;
    min-height:220px;
  }
  .photo-placeholder span{
    background:var(--white);
    padding:6px 12px;
    border-radius:4px;
    border:1px solid var(--caramel);
  }

  /* ---------- HERO ---------- */
  .hero{
    padding-top:64px;
    display:grid;
    grid-template-columns:1.1fr 1fr;
    gap:56px;
    align-items:center;
  }
  .hero-big-word{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:clamp(3.2rem, 9vw, 6.5rem);
    line-height:0.9;
    color:var(--caramel);
    opacity:0.9;
    letter-spacing:0.02em;
    margin-bottom:8px;
  }
  .hero h1{
    font-size:clamp(2.4rem, 4.2vw, 3.6rem);
    line-height:1.08;
    margin-bottom:20px;
  }
  .hero p.lead{
    font-size:1.1rem;
    color:#5a473d;
  }
  .hero-cta{
    margin-top:28px;
    display:inline-flex;
    align-items:center;
    gap:10px;
    background:var(--caramel);
    color:var(--white);
    text-decoration:none;
    padding:13px 26px;
    border-radius:4px;
    font-size:0.98rem;
    transition:background .2s ease;
  }
  .hero-cta:hover{ background:#734a2c; }
  .hero-photo .photo-placeholder{ min-height:380px; border-radius:6px; }

  @media (max-width:820px){
    .hero{ grid-template-columns:1fr; }
    .hero-photo{ order:-1; }
  }

  /* ---------- SECTION HEADINGS ---------- */
  .section-head{ margin-bottom:48px; max-width:56ch; }
  .section-head h2{ font-size:clamp(1.8rem, 3vw, 2.4rem); margin-bottom:14px; }
  .section-head p{ color:#5a473d; }

  /* ---------- ABOUT ---------- */
  .about{ background:var(--cream-soft); }
  .about-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:56px;
    align-items:start;
  }
  .about-tagline{
    font-family:'Fraunces', serif;
    font-style:italic;
    font-size:1.4rem;
    color:var(--caramel);
    margin-bottom:20px;
    line-height:1.4;
  }
  .about-photo .photo-placeholder{ min-height:320px; border-radius:6px; }

  .about-culture{
    margin-top:64px;
    max-width:74ch;
  }
  .about-panel{ display:none; }
  .about-panel.active{ display:block; }
  .about-panel h4{
    font-size:1.05rem;
    margin:26px 0 10px;
    color:var(--caramel);
    font-family:'Work Sans', sans-serif;
    font-weight:600;
  }
  .about-panel p{ color:#4a3a30; font-size:0.97rem; }
  .about-panel ul{ padding-left:20px; margin:0 0 1em; }
  .about-panel li{ color:#4a3a30; font-size:0.97rem; margin-bottom:8px; }

  .reviews{
    margin-top:64px;
  }
  .reviews h3{ font-size:1.3rem; margin-bottom:24px; }
  .review-grid{
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    gap:20px;
  }
  .review-card{
    background:var(--white);
    border:1px solid var(--beige);
    border-radius:6px;
    padding:22px;
  }
  .review-stars{ color:var(--caramel); font-size:0.95rem; margin-bottom:10px; letter-spacing:2px; }
  .review-card p{ font-size:0.95rem; color:#4a3a30; margin-bottom:14px; }
  .review-name{ font-size:0.88rem; color:var(--sage); }

  @media (max-width:820px){
    .about-grid{ grid-template-columns:1fr; }
    .review-grid{ grid-template-columns:1fr; }
  }

  /* ---------- RECIPE ---------- */
  .recipe-photo{ margin-bottom:40px; }
  .recipe-photo .photo-placeholder{ min-height:260px; border-radius:6px; }

  .recipe-toggle{
    display:inline-flex;
    border:1px solid var(--caramel);
    border-radius:999px;
    overflow:hidden;
    margin-bottom:40px;
  }
  .recipe-toggle button{
    border:none;
    background:transparent;
    color:var(--caramel);
    padding:9px 22px;
    font-family:'Work Sans', sans-serif;
    font-size:0.92rem;
    cursor:pointer;
  }
  .recipe-toggle button.active{
    background:var(--caramel);
    color:var(--white);
  }

  .recipe-panel{ display:none; }
  .recipe-panel.active{ display:grid; grid-template-columns:1fr 1.3fr; gap:56px; }

  .recipe-col h3{
    font-size:1.15rem;
    margin-bottom:16px;
    color:var(--sage);
  }
  .recipe-col ul, .recipe-col ol{
    padding-left:20px;
    margin:0;
  }
  .recipe-col li{ margin-bottom:10px; color:#4a3a30; }

  @media (max-width:820px){
    .recipe-panel.active{ grid-template-columns:1fr; }
  }

  /* ---------- PROCESS ---------- */
  .process{ background:var(--cream-soft); }
  .video-frame{
    aspect-ratio:16/9;
    width:100%;
    border-radius:6px;
    overflow:hidden;
    margin-bottom:56px;
  }
  .video-frame .photo-placeholder{ height:100%; min-height:unset; border-radius:6px; }

  .steps{
    display:grid;
    grid-template-columns:repeat(4, 1fr);
    gap:24px;
  }
  .step{
    background:var(--white);
    border:1px solid var(--beige);
    border-radius:6px;
    padding:20px;
  }
  .step-num{
    font-family:'Fraunces', serif;
    font-size:1.6rem;
    color:var(--caramel);
    margin-bottom:10px;
  }
  .step h4{ font-size:1rem; margin-bottom:8px; font-weight:600; font-family:'Work Sans', sans-serif; }
  .step p{ font-size:0.9rem; color:#5a473d; margin:0; }

  @media (max-width:900px){
    .steps{ grid-template-columns:1fr 1fr; }
  }
  @media (max-width:560px){
    .steps{ grid-template-columns:1fr; }
  }

  /* ---------- PRICES ---------- */
  .price-grid{
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    gap:24px;
  }
  .price-card{
    background:var(--white);
    border:1px solid var(--beige);
    border-radius:6px;
    padding:32px 28px;
    display:flex;
    flex-direction:column;
  }
  .price-card.featured{
    border-color:var(--caramel);
    box-shadow:0 0 0 1px var(--caramel);
  }
  .price-card h3{ font-size:1.2rem; margin-bottom:6px; }
  .price-card .price-tag{
    font-family:'Fraunces', serif;
    font-size:2rem;
    color:var(--caramel);
    margin:12px 0 18px;
  }
  .price-card .price-tag small{
    font-family:'Work Sans', sans-serif;
    font-size:0.9rem;
    color:#5a473d;
  }
  .price-card ul{
    list-style:none;
    padding:0;
    margin:0 0 24px;
    flex-grow:1;
  }
  .price-card li{
    font-size:0.92rem;
    color:#4a3a30;
    padding:7px 0;
    border-bottom:1px solid var(--cream-soft);
  }
  .price-badge{
    align-self:flex-start;
    background:var(--sage);
    color:var(--white);
    font-size:0.75rem;
    padding:4px 10px;
    border-radius:999px;
    margin-bottom:14px;
  }

  @media (max-width:900px){
    .price-grid{ grid-template-columns:1fr; }
  }

  /* ---------- FOOTER ---------- */
  footer{
    background:var(--brown-dark);
    color:var(--cream);
    padding:48px 24px;
  }
  .footer-inner{
    max-width:var(--max-w);
    margin:0 auto;
    display:flex;
    justify-content:space-between;
    align-items:center;
    flex-wrap:wrap;
    gap:16px;
  }
  footer .brand{ color:var(--cream); }
  footer p{ margin:0; font-size:0.88rem; color:#cbb9a6; }
</style>
</head>
<body>

<header class="nav">
  <div class="nav-inner">
    <a href="#home" class="brand">Tahu Isi</a>
    <button class="nav-toggle" id="navToggle" aria-label="Buka menu" aria-expanded="false">☰</button>
    <ul class="navlinks" id="navLinks">
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About Food</a></li>
      <li><a href="#recipe">Recipe</a></li>
      <li><a href="#process">Cooking Process</a></li>
      <li><a href="#prices">Prices</a></li>
    </ul>
  </div>
</header>

<!-- ================= HOME ================= -->
<section id="home" class="hero wrap">
  <div class="hero-copy">
    <div class="hero-big-word">TAHU</div>
    <h1>Tahu isi hangat,<br>renyah di luar, penuh rasa di dalam.</h1>
  </div>
  <div class="hero-photo">
    <img src="data:image/jpeg;base64,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