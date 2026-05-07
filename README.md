<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>คู่มือการเลือกรายการแข่งขันเทคโนโลยีและนวัตกรรม</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Sarabun:wght@300;400;500;600;700;800&family=Prompt:wght@500;600;700;800&display=swap" rel="stylesheet">
<style>
  /* ===== RESET & BASE ===== */
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --c-tier0: #6BA856;
    --c-tier0-bg: #E8F4E0;
    --c-tier1: #2E75B6;
    --c-tier1-bg: #E3EEF8;
    --c-tier2: #C99500;
    --c-tier2-bg: #FFF4D1;
    --c-tier3: #D2691E;
    --c-tier3-bg: #FCEBDA;
    --c-primary: #1F4E79;
    --c-accent: #2E75B6;
    --c-text: #1A1A1A;
    --c-text-soft: #555;
    --c-border: #E5E7EB;
    --c-bg: #F8FAFC;
    --c-card: #FFFFFF;
    --shadow-sm: 0 1px 2px rgba(0,0,0,0.04), 0 1px 3px rgba(0,0,0,0.06);
    --shadow-md: 0 4px 12px rgba(0,0,0,0.08);
    --shadow-lg: 0 12px 36px rgba(0,0,0,0.12);
    --r-sm: 8px;
    --r-md: 12px;
    --r-lg: 18px;
  }
  html { scroll-behavior: smooth; }
  body {
    font-family: "Sarabun", system-ui, -apple-system, "Segoe UI", "Tahoma", sans-serif;
    color: var(--c-text);
    background: var(--c-bg);
    line-height: 1.65;
    font-size: 16px;
  }
  h1, h2, h3, h4 { font-family: "Prompt", "Sarabun", sans-serif; line-height: 1.3; }
  a { color: var(--c-accent); text-decoration: none; }
  a:hover { text-decoration: underline; }

  /* ===== HEADER / HERO ===== */
  .hero {
    background: linear-gradient(135deg, #1F4E79 0%, #2E75B6 60%, #5DA8DC 100%);
    color: white;
    padding: 80px 24px 100px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: "";
    position: absolute; inset: 0;
    background:
      radial-gradient(circle at 20% 30%, rgba(255,255,255,0.12) 0%, transparent 50%),
      radial-gradient(circle at 80% 70%, rgba(255,255,255,0.10) 0%, transparent 50%);
    pointer-events: none;
  }
  .hero-inner { position: relative; max-width: 900px; margin: 0 auto; }
  .hero .eyebrow {
    display: inline-block;
    background: rgba(255,255,255,0.18);
    backdrop-filter: blur(8px);
    padding: 6px 16px;
    border-radius: 999px;
    font-size: 0.9rem;
    font-weight: 500;
    margin-bottom: 18px;
    letter-spacing: 0.5px;
  }
  .hero h1 {
    font-size: clamp(2rem, 4.6vw, 3.4rem);
    font-weight: 800;
    margin-bottom: 18px;
    text-shadow: 0 2px 12px rgba(0,0,0,0.15);
  }
  .hero p.lead {
    font-size: clamp(1rem, 1.6vw, 1.25rem);
    font-weight: 400;
    opacity: 0.92;
    max-width: 720px;
    margin: 0 auto 32px;
  }
  .hero .quick-nav {
    display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;
  }
  .hero .quick-nav a {
    background: rgba(255,255,255,0.16);
    color: white;
    padding: 10px 20px;
    border-radius: 999px;
    font-weight: 500;
    font-size: 0.95rem;
    transition: all 0.2s;
    border: 1px solid rgba(255,255,255,0.22);
  }
  .hero .quick-nav a:hover {
    background: rgba(255,255,255,0.28);
    text-decoration: none;
    transform: translateY(-1px);
  }

  /* ===== STICKY NAV ===== */
  .topnav {
    position: sticky;
    top: 0;
    z-index: 50;
    background: rgba(255,255,255,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--c-border);
    box-shadow: var(--shadow-sm);
  }
  .topnav-inner {
    max-width: 1200px; margin: 0 auto; padding: 12px 24px;
    display: flex; align-items: center; gap: 24px; overflow-x: auto;
    scrollbar-width: thin;
  }
  .topnav-inner a {
    color: var(--c-text-soft);
    font-weight: 500;
    font-size: 0.95rem;
    white-space: nowrap;
    padding: 6px 4px;
    border-bottom: 2px solid transparent;
    transition: all 0.15s;
  }
  .topnav-inner a:hover { color: var(--c-primary); text-decoration: none; border-bottom-color: var(--c-accent); }
  .topnav .brand { font-weight: 700; color: var(--c-primary); font-family: "Prompt", sans-serif; }

  /* ===== LAYOUT ===== */
  .container { max-width: 1200px; margin: 0 auto; padding: 0 24px; }
  section { padding: 64px 0; }
  section h2 {
    font-size: clamp(1.6rem, 3vw, 2.2rem);
    color: var(--c-primary);
    margin-bottom: 12px;
    display: flex; align-items: baseline; gap: 14px;
  }
  section h2 .num {
    background: var(--c-primary); color: white;
    width: 44px; height: 44px;
    display: inline-flex; align-items: center; justify-content: center;
    border-radius: 12px; font-size: 1.2rem;
  }
  section .sub {
    color: var(--c-text-soft);
    font-size: 1.05rem;
    margin-bottom: 32px;
    max-width: 800px;
  }
  section h3 {
    font-size: 1.3rem;
    color: var(--c-primary);
    margin: 32px 0 12px;
  }

  /* ===== TIER CARDS ===== */
  .tiers {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 18px;
  }
  .tier-card {
    background: var(--c-card);
    border-radius: var(--r-lg);
    padding: 26px;
    border: 1px solid var(--c-border);
    box-shadow: var(--shadow-sm);
    transition: transform 0.2s, box-shadow 0.2s;
    position: relative;
    overflow: hidden;
  }
  .tier-card::before {
    content: ""; position: absolute; top: 0; left: 0; right: 0; height: 6px;
  }
  .tier-card.t0::before { background: var(--c-tier0); }
  .tier-card.t1::before { background: var(--c-tier1); }
  .tier-card.t2::before { background: var(--c-tier2); }
  .tier-card.t3::before { background: var(--c-tier3); }
  .tier-card:hover { transform: translateY(-3px); box-shadow: var(--shadow-md); }
  .tier-card .badge {
    display: inline-block; padding: 4px 12px; border-radius: 999px;
    font-size: 0.85rem; font-weight: 700; margin-bottom: 12px;
  }
  .tier-card.t0 .badge { background: var(--c-tier0-bg); color: var(--c-tier0); }
  .tier-card.t1 .badge { background: var(--c-tier1-bg); color: var(--c-tier1); }
  .tier-card.t2 .badge { background: var(--c-tier2-bg); color: var(--c-tier2); }
  .tier-card.t3 .badge { background: var(--c-tier3-bg); color: var(--c-tier3); }
  .tier-card h3 {
    font-size: 1.25rem; color: var(--c-primary); margin: 0 0 10px;
  }
  .tier-card p { font-size: 0.96rem; color: var(--c-text-soft); margin-bottom: 10px; }
  .tier-card .goal {
    font-size: 0.9rem; color: var(--c-text); padding-top: 12px;
    border-top: 1px dashed var(--c-border);
  }

  /* ===== FILTER BAR ===== */
  .filter-bar {
    background: var(--c-card);
    border-radius: var(--r-lg);
    padding: 20px;
    box-shadow: var(--shadow-sm);
    border: 1px solid var(--c-border);
    margin-bottom: 28px;
  }
  .filter-row { display: flex; flex-wrap: wrap; gap: 12px; align-items: center; }
  .search-box {
    flex: 1 1 280px;
    position: relative;
  }
  .search-box input {
    width: 100%;
    padding: 12px 14px 12px 42px;
    border: 1.5px solid var(--c-border);
    border-radius: 10px;
    font-size: 1rem;
    font-family: inherit;
    transition: border-color 0.15s, box-shadow 0.15s;
  }
  .search-box input:focus {
    outline: none;
    border-color: var(--c-accent);
    box-shadow: 0 0 0 3px rgba(46,117,182,0.18);
  }
  .search-box::before {
    content: "🔍"; position: absolute; left: 14px; top: 50%; transform: translateY(-50%);
    font-size: 1.1rem;
  }
  .chips { display: flex; flex-wrap: wrap; gap: 8px; }
  .chip {
    background: white; border: 1.5px solid var(--c-border); color: var(--c-text-soft);
    padding: 8px 14px; border-radius: 999px;
    font-size: 0.9rem; font-weight: 500;
    cursor: pointer; user-select: none;
    transition: all 0.15s;
    font-family: inherit;
  }
  .chip:hover { border-color: var(--c-accent); color: var(--c-primary); }
  .chip.active {
    background: var(--c-primary); border-color: var(--c-primary); color: white;
  }
  .chip[data-tier="0"].active { background: var(--c-tier0); border-color: var(--c-tier0); }
  .chip[data-tier="1"].active { background: var(--c-tier1); border-color: var(--c-tier1); }
  .chip[data-tier="2"].active { background: var(--c-tier2); border-color: var(--c-tier2); }
  .chip[data-tier="3"].active { background: var(--c-tier3); border-color: var(--c-tier3); }

  /* ===== COMPETITION GRID ===== */
  .category {
    background: var(--c-card);
    border-radius: var(--r-lg);
    padding: 28px;
    margin-bottom: 22px;
    box-shadow: var(--shadow-sm);
    border: 1px solid var(--c-border);
  }
  .category-head {
    display: flex; align-items: center; gap: 14px; margin-bottom: 18px;
    padding-bottom: 14px; border-bottom: 2px solid var(--c-border);
  }
  .category-head .icon {
    width: 52px; height: 52px; border-radius: 14px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.7rem;
    background: var(--c-tier1-bg);
  }
  .category-head h3 {
    font-size: 1.4rem;
    color: var(--c-primary);
    margin: 0;
  }
  .category-head p {
    color: var(--c-text-soft);
    font-size: 0.92rem;
    margin: 2px 0 0;
  }
  .competitions {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 14px;
  }
  .comp-card {
    border: 1px solid var(--c-border);
    border-radius: var(--r-md);
    padding: 16px 18px;
    background: var(--c-bg);
    transition: all 0.15s;
    border-left-width: 5px;
    border-left-style: solid;
  }
  .comp-card.t0 { border-left-color: var(--c-tier0); }
  .comp-card.t1 { border-left-color: var(--c-tier1); }
  .comp-card.t2 { border-left-color: var(--c-tier2); }
  .comp-card.t3 { border-left-color: var(--c-tier3); }
  .comp-card:hover {
    background: white;
    box-shadow: var(--shadow-sm);
    transform: translateX(2px);
  }
  .comp-card .top {
    display: flex; justify-content: space-between; align-items: flex-start; gap: 10px;
    margin-bottom: 6px;
  }
  .comp-card h4 {
    font-size: 1.05rem; color: var(--c-primary); margin: 0;
    font-weight: 700;
  }
  .comp-card .tier-tag {
    flex-shrink: 0;
    padding: 2px 10px; border-radius: 999px; font-size: 0.78rem; font-weight: 700;
  }
  .comp-card.t0 .tier-tag { background: var(--c-tier0-bg); color: var(--c-tier0); }
  .comp-card.t1 .tier-tag { background: var(--c-tier1-bg); color: var(--c-tier1); }
  .comp-card.t2 .tier-tag { background: var(--c-tier2-bg); color: var(--c-tier2); }
  .comp-card.t3 .tier-tag { background: var(--c-tier3-bg); color: var(--c-tier3); }
  .comp-card .org {
    font-size: 0.85rem; color: var(--c-text-soft); margin-bottom: 8px;
    font-style: italic;
  }
  .comp-card .desc { font-size: 0.92rem; color: var(--c-text); }

  .empty-msg {
    grid-column: 1 / -1;
    text-align: center;
    padding: 40px 20px;
    color: var(--c-text-soft);
    background: var(--c-bg);
    border-radius: var(--r-md);
    font-size: 1rem;
  }

  /* ===== GUIDE TWO-COL ===== */
  .guides {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 24px;
  }
  .guide-card {
    background: var(--c-card);
    border-radius: var(--r-lg);
    padding: 32px;
    box-shadow: var(--shadow-sm);
    border: 1px solid var(--c-border);
    border-top: 5px solid var(--c-accent);
  }
  .guide-card.parent { border-top-color: #E37B40; }
  .guide-card.teacher { border-top-color: #5BA489; }
  .guide-card .icon-big { font-size: 2.5rem; margin-bottom: 8px; display: block; }
  .guide-card h3 { font-size: 1.5rem; color: var(--c-primary); margin-bottom: 18px; }
  .guide-card h4 {
    font-size: 1.05rem; color: var(--c-primary); margin: 22px 0 8px;
    padding-left: 10px; border-left: 4px solid var(--c-accent);
  }
  .guide-card.parent h4 { border-left-color: #E37B40; }
  .guide-card.teacher h4 { border-left-color: #5BA489; }
  .guide-card ul, .guide-card ol { padding-left: 22px; margin: 6px 0; }
  .guide-card li { padding: 4px 0; font-size: 0.97rem; }
  .guide-card li b { color: var(--c-primary); }

  /* ===== AGE PATH ===== */
  .age-path {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 14px;
    position: relative;
  }
  .age-card {
    background: var(--c-card);
    border-radius: var(--r-md);
    padding: 20px;
    border: 1px solid var(--c-border);
    border-top: 5px solid;
    position: relative;
  }
  .age-card.t0 { border-top-color: var(--c-tier0); }
  .age-card.t1 { border-top-color: var(--c-tier1); }
  .age-card.t2 { border-top-color: var(--c-tier2); }
  .age-card.t3 { border-top-color: var(--c-tier3); }
  .age-card .age {
    font-family: "Prompt", sans-serif;
    font-weight: 700;
    font-size: 1.3rem;
    color: var(--c-primary);
    margin-bottom: 4px;
  }
  .age-card .tier {
    font-size: 0.9rem;
    margin-bottom: 12px;
    font-weight: 500;
  }
  .age-card.t0 .tier { color: var(--c-tier0); }
  .age-card.t1 .tier { color: var(--c-tier1); }
  .age-card.t2 .tier { color: var(--c-tier2); }
  .age-card.t3 .tier { color: var(--c-tier3); }
  .age-card .skills {
    font-size: 0.88rem;
    color: var(--c-text-soft);
    margin-bottom: 10px;
    padding-bottom: 10px;
    border-bottom: 1px dashed var(--c-border);
  }
  .age-card .examples {
    font-size: 0.88rem;
    color: var(--c-text);
  }

  /* ===== FAQ ===== */
  .faq-list { max-width: 900px; }
  .faq-item {
    background: var(--c-card);
    border: 1px solid var(--c-border);
    border-radius: var(--r-md);
    margin-bottom: 10px;
    overflow: hidden;
    transition: box-shadow 0.15s;
  }
  .faq-item:hover { box-shadow: var(--shadow-sm); }
  .faq-q {
    width: 100%;
    text-align: left;
    padding: 18px 22px;
    background: none;
    border: none;
    font-family: inherit;
    font-size: 1.02rem;
    font-weight: 600;
    color: var(--c-primary);
    cursor: pointer;
    display: flex; justify-content: space-between; align-items: center; gap: 16px;
  }
  .faq-q .arrow { transition: transform 0.25s; flex-shrink: 0; color: var(--c-accent); font-size: 1.4rem; line-height: 1; }
  .faq-item.open .arrow { transform: rotate(180deg); }
  .faq-a {
    max-height: 0; overflow: hidden; transition: max-height 0.3s ease, padding 0.3s ease;
    padding: 0 22px;
    color: var(--c-text);
    line-height: 1.75;
  }
  .faq-item.open .faq-a {
    max-height: 800px; padding: 0 22px 22px;
  }

  /* ===== TIPS ===== */
  .tips-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 18px; }
  .tip-card {
    background: var(--c-card);
    border-radius: var(--r-md);
    padding: 22px;
    border: 1px solid var(--c-border);
    box-shadow: var(--shadow-sm);
  }
  .tip-card h4 { font-size: 1.1rem; color: var(--c-primary); margin-bottom: 12px; }
  .tip-card.warn { background: #FFF7ED; border-color: #FFEDD5; }
  .tip-card.warn h4 { color: #C2410C; }
  .tip-card ol, .tip-card ul { padding-left: 22px; }
  .tip-card li { padding: 4px 0; font-size: 0.96rem; }

  .formula {
    display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 12px; margin-top: 24px;
  }
  .formula-item {
    background: linear-gradient(135deg, var(--c-primary) 0%, var(--c-accent) 100%);
    color: white;
    padding: 22px;
    border-radius: var(--r-md);
    text-align: center;
  }
  .formula-item.b { background: linear-gradient(135deg, #2E75B6 0%, #5DA8DC 100%); }
  .formula-item.c { background: linear-gradient(135deg, #5DA8DC 0%, #9DC3E6 100%); }
  .formula-item h4 { font-size: 1.4rem; margin-bottom: 6px; font-family: "Prompt", sans-serif; }
  .formula-item p { font-size: 0.9rem; opacity: 0.95; margin: 0; }

  /* ===== FOOTER ===== */
  footer {
    background: var(--c-primary);
    color: white;
    padding: 50px 24px 30px;
    margin-top: 60px;
    text-align: center;
  }
  footer p { opacity: 0.9; max-width: 700px; margin: 0 auto 8px; }
  footer .quote { font-style: italic; font-size: 1.1rem; margin-bottom: 16px; }
  footer .meta { font-size: 0.85rem; opacity: 0.7; margin-top: 18px; }

  /* ===== UTILITY ===== */
  .alt { background: white; }
  .anchor-offset { scroll-margin-top: 70px; }

  @media (max-width: 640px) {
    section { padding: 48px 0; }
    .hero { padding: 60px 18px 70px; }
    section h2 .num { width: 36px; height: 36px; font-size: 1rem; }
    .competitions { grid-template-columns: 1fr; }
    .category { padding: 20px; }
  }

  /* hidden state for filter */
  .comp-card.hidden, .category.hidden { display: none; }

  /* back to top */
  .back-to-top {
    position: fixed; bottom: 24px; right: 24px;
    width: 48px; height: 48px;
    background: var(--c-primary); color: white;
    border: none; border-radius: 50%;
    font-size: 1.4rem; cursor: pointer;
    box-shadow: var(--shadow-md);
    display: none;
    transition: transform 0.15s, background 0.15s;
    z-index: 40;
  }
  .back-to-top:hover { background: var(--c-accent); transform: translateY(-2px); }
  .back-to-top.visible { display: block; }
</style>
</head>
<body>

<!-- ============================================================ -->
<!-- HERO -->
<!-- ============================================================ -->
<header class="hero">
  <div class="hero-inner">
    <span class="eyebrow">Impact Tier Guide • 2026</span>
    <h1>คู่มือการเลือกรายการแข่งขัน<br>เทคโนโลยีและนวัตกรรม</h1>
    <p class="lead">เลือกเส้นทางที่ใช่ ติดอาวุธอนาคตของลูกหลาน  จากเวทีโรงเรียน สู่เวทีโลก  สำหรับผู้ปกครองและคุณครูทุกท่าน</p>
    <nav class="quick-nav">
      <a href="#tier">ระบบ Tier</a>
      <a href="#competitions">ค้นหารายการ</a>
      <a href="#parent">ผู้ปกครอง</a>
      <a href="#teacher">คุณครู</a>
      <a href="#age">ตามช่วงวัย</a>
      <a href="#faq">FAQ</a>
    </nav>
  </div>
</header>

<!-- ============================================================ -->
<!-- STICKY NAV -->
<!-- ============================================================ -->
<nav class="topnav">
  <div class="topnav-inner">
    <span class="brand">📘 Impact Tier</span>
    <a href="#tier">Tier</a>
    <a href="#competitions">รายการแข่งขัน</a>
    <a href="#parent">ผู้ปกครอง</a>
    <a href="#teacher">คุณครู</a>
    <a href="#age">ช่วงวัย</a>
    <a href="#faq">FAQ</a>
    <a href="#tips">เคล็ดลับ</a>
  </div>
</nav>

<!-- ============================================================ -->
<!-- SECTION 1: TIER OVERVIEW -->
<!-- ============================================================ -->
<section id="tier" class="anchor-offset">
  <div class="container">
    <h2><span class="num">1</span>ระบบ Impact Tier</h2>
    <p class="sub">Impact Tier คือระบบจัดลำดับ "น้ำหนักของผลงาน" ในการแข่งขันด้านเทคโนโลยีและนวัตกรรม โดยพิจารณาจากการยอมรับของมหาวิทยาลัย ขอบเขตการแข่งขัน และความน่าเชื่อถือของหน่วยงานผู้จัด</p>

    <div class="tiers">
      <div class="tier-card t0">
        <span class="badge">Tier 0</span>
        <h3>ระดับทั่วไป</h3>
        <p>เน้น "ชิมลาง" สร้างความคุ้นเคยกับการแข่งขัน เริ่มต้นเก็บผลงาน</p>
        <div class="goal"><b>เป้าหมาย:</b> ค้นหาความชอบ ฝึกความมั่นใจ สะสมเกียรติบัตรเริ่มต้นใส่พอร์ต</div>
      </div>
      <div class="tier-card t1">
        <span class="badge">Tier 1</span>
        <h3>ระดับชาติ</h3>
        <p>รายการที่มีตราประทับจากหน่วยงานรัฐ (วช., สวทช., สสวท.)</p>
        <div class="goal"><b>เป้าหมาย:</b> ใบเบิกทางสู่มหาวิทยาลัยชั้นนำ ใช้ยื่น TCAS Portfolio ได้</div>
      </div>
      <div class="tier-card t2">
        <span class="badge">Tier 2</span>
        <h3>ระดับเอเชีย</h3>
        <p>รายการระดับนานาชาติที่มีประเทศเข้าร่วม 5 ประเทศขึ้นไป</p>
        <div class="goal"><b>เป้าหมาย:</b> สร้าง International Profile ฝึกภาษาอังกฤษ พิสูจน์ฝีมือเทียบกับเอเชีย</div>
      </div>
      <div class="tier-card t3">
        <span class="badge">Tier 3</span>
        <h3>ระดับโลก / โอลิมปิก</h3>
        <p>เวทีระดับโลก รวมถึงการแข่งขันโอลิมปิกวิชาการ</p>
        <div class="goal"><b>เป้าหมาย:</b> เกียรติยศสูงสุด ทุนการศึกษา และการจองตัวจาก Tech ยักษ์ใหญ่</div>
      </div>
    </div>
  </div>
</section>

<!-- ============================================================ -->
<!-- SECTION 2: COMPETITIONS (with search/filter) -->
<!-- ============================================================ -->
<section id="competitions" class="alt anchor-offset">
  <div class="container">
    <h2><span class="num">2</span>ค้นหารายการแข่งขัน</h2>
    <p class="sub">รายการแข่งขันทั้งหมด แบ่งตาม 5 สาย พิมพ์ชื่อรายการ หน่วยงาน หรือคำสำคัญในช่องค้นหา หรือคลิกเลือกระดับ Tier เพื่อกรองข้อมูล</p>

    <div class="filter-bar">
      <div class="filter-row">
        <div class="search-box">
          <input type="search" id="searchInput" placeholder="ค้นหา เช่น สอวน. หุ่นยนต์ ISEF...">
        </div>
        <div class="chips" id="tierChips">
          <button class="chip active" data-tier="all">ทุกระดับ</button>
          <button class="chip" data-tier="0">Tier 0</button>
          <button class="chip" data-tier="1">Tier 1</button>
          <button class="chip" data-tier="2">Tier 2</button>
          <button class="chip" data-tier="3">Tier 3</button>
        </div>
      </div>
    </div>

    <div id="competitionsContainer"></div>
  </div>
</section>

<!-- ============================================================ -->
<!-- SECTION 3: PARENT GUIDE -->
<!-- ============================================================ -->
<section id="parent" class="anchor-offset">
  <div class="container">
    <h2><span class="num">3</span>คู่มือสำหรับผู้ปกครอง &amp; คุณครู</h2>
    <p class="sub">แนวทางที่นำไปใช้ได้ทันที โดยไม่ต้องรู้ลึกเรื่องเทคนิค</p>

    <div class="guides">
      <div class="guide-card parent">
        <span class="icon-big">👨‍👩‍👧</span>
        <h3>สำหรับผู้ปกครอง</h3>

        <h4>4 คำถามก่อนตัดสินใจ</h4>
        <ol>
          <li>ลูก <b>"อยาก"</b> แข่งเอง หรือเรา <b>"อยากให้"</b> แข่ง?</li>
          <li>รายการนี้อยู่ Tier ไหน คุ้มกับเวลาที่ลูกต้องเสียไปหรือไม่?</li>
          <li>ถ้าไม่ชนะ ลูกจะได้อะไรกลับมา?</li>
          <li>ค่าใช้จ่ายและการเดินทางอยู่ในขอบเขตที่รับไหวหรือไม่?</li>
        </ol>

        <h4>สิ่งที่ควรทำ ✓</h4>
        <ul>
          <li><b>เป็นผู้ฟังที่ดี</b> ให้ลูกอธิบายโครงงานแม้จะฟังไม่รู้เรื่อง</li>
          <li><b>สนับสนุนทรัพยากร</b> ค่าสมัคร อุปกรณ์ การเดินทาง</li>
          <li><b>เก็บผลงานเป็น Portfolio</b> ตั้งแต่เนิ่นๆ ตอน ม.6 จะใช้ทั้งหมด</li>
          <li><b>เฉลิมฉลองความพยายาม</b> ไม่ใช่เฉพาะรางวัล</li>
        </ul>

        <h4>สิ่งที่ควรหลีกเลี่ยง ✗</h4>
        <ul>
          <li>เปรียบเทียบลูกกับเด็กคนอื่น</li>
          <li>ทำการบ้าน/โครงงานแทนลูก</li>
          <li>คาดหวัง Tier 3 ตั้งแต่ ม.1</li>
          <li>ส่งหลายรายการพร้อมกันจนเด็กเหนื่อย</li>
        </ul>
      </div>

      <div class="guide-card teacher" id="teacher">
        <span class="icon-big">👩‍🏫</span>
        <h3>สำหรับคุณครู</h3>

        <h4>หลักคัดกรองเด็ก 3 ขั้น</h4>
        <ol>
          <li><b>ขั้นสังเกต (Tier 0)</b> ปล่อยเด็กลอง 1–2 รายการต่อภาคเรียน เพื่อค้นหาสายที่ใช่</li>
          <li><b>ขั้นคัดเลือก (Tier 1)</b> เด็กที่แสดงแวว ส่งเข้ารายการชาติอย่างน้อย 1 รายการต่อปี</li>
          <li><b>ขั้นปั้นดาว (Tier 2–3)</b> เด็กที่ได้รางวัลในระดับชาติ ผลักสู่เวทีนานาชาติ พร้อมโค้ชภาษาอังกฤษ</li>
        </ol>

        <h4>เกณฑ์จัดสรรเด็กลงรายการ</h4>
        <ul>
          <li><b>เก่งคณิต ชอบโจทย์ตรรกะ</b> → คอมพิวเตอร์ / Cybersec  <i>(Bebras → สอวน. → IOI)</i></li>
          <li><b>ชอบประดิษฐ์ ลงมือทำ</b> → หุ่นยนต์ / นวัตกรรม  <i>(Sumo Robot → WRO TH → WRO World)</i></li>
          <li><b>ชอบสำรวจปัญหา</b> → โครงงานวิจัย  <i>(YSC → ISEF / I-New Gen)</i></li>
          <li><b>วาดเก่ง คิดเป็นภาพ</b> → ศิลปะดิจิทัล / UX  <i>(XPPen → ศิลปกรรมแห่งชาติ → Red Dot)</i></li>
          <li><b>ชอบสืบสวน</b> → Cybersecurity  <i>(PicoCTF → Thailand Cyber → DEF CON)</i></li>
        </ul>

        <h4>Checklist ส่งระดับชาติขึ้นไป</h4>
        <ul>
          <li>☐ ตรวจกติกา/คุณสมบัติให้ละเอียด</li>
          <li>☐ ลงทะเบียนล่วงหน้าก่อนปิดรับ 2 สัปดาห์</li>
          <li>☐ เตรียมเอกสาร 4 ชุด (รูป, สำเนาบัตร, หนังสือยินยอม, ใบรับรอง)</li>
          <li>☐ ฝึกพรีเซนต์ภาษาอังกฤษ (Tier 2–3)</li>
          <li>☐ ทำสรุปบทเรียน Lesson Learned ทุกครั้ง</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ============================================================ -->
<!-- SECTION 4: AGE PATH -->
<!-- ============================================================ -->
<section id="age" class="alt anchor-offset">
  <div class="container">
    <h2><span class="num">4</span>เส้นทางตามช่วงวัย</h2>
    <p class="sub">เส้นทางที่ดีที่สุดคือเส้นทางที่ "พอดี" กับวัยและพัฒนาการของเด็ก ไม่เร่งและไม่ช้าเกินไป</p>

    <div class="age-path">
      <div class="age-card t0">
        <div class="age">ป.4 – ป.6</div>
        <div class="tier">เน้น Tier 0</div>
        <div class="skills"><b>ทักษะ:</b> ความคิดเชิงคำนวณ ทำงานเป็นทีม การสำรวจ</div>
        <div class="examples"><b>ตัวอย่าง:</b> Bebras, Code.org, Hour of Code, Scratch contest, ประกวดวาดภาพดิจิทัล</div>
      </div>
      <div class="age-card t0">
        <div class="age">ม.1 – ม.2</div>
        <div class="tier">Tier 0–1</div>
        <div class="skills"><b>ทักษะ:</b> เริ่มเขียนโค้ดจริง ออกแบบหุ่นยนต์เบื้องต้น</div>
        <div class="examples"><b>ตัวอย่าง:</b> สอวน. รอบแรก, WRO Thailand รุ่นเล็ก, School Hackathon, Sumo Robot</div>
      </div>
      <div class="age-card t1">
        <div class="age">ม.3 – ม.4</div>
        <div class="tier">Tier 1</div>
        <div class="skills"><b>ทักษะ:</b> Project-based learning ภาษาอังกฤษเชิงวิชาการ การนำเสนอ</div>
        <div class="examples"><b>ตัวอย่าง:</b> สอวน. ค่าย 1–2, NSC, YSC, I-New Gen Award, Thailand CanSat</div>
      </div>
      <div class="age-card t2">
        <div class="age">ม.5</div>
        <div class="tier">Tier 1–2</div>
        <div class="skills"><b>ทักษะ:</b> พรีเซนต์ระดับนานาชาติ เขียน Paper งานข้ามวัฒนธรรม</div>
        <div class="examples"><b>ตัวอย่าง:</b> APIO, IPITEx, AYIE, ITEX, ASEAN Cyber SEA Game</div>
      </div>
      <div class="age-card t3">
        <div class="age">ม.6</div>
        <div class="tier">Tier 2–3</div>
        <div class="skills"><b>ทักษะ:</b> รวบยอดผลงาน ทำ Portfolio ส่ง TCAS เตรียมสัมภาษณ์</div>
        <div class="examples"><b>ตัวอย่าง:</b> IOI, ISEF, FRC, Imagine Cup, Adobe World Champ</div>
      </div>
    </div>
  </div>
</section>

<!-- ============================================================ -->
<!-- SECTION 5: FAQ -->
<!-- ============================================================ -->
<section id="faq" class="anchor-offset">
  <div class="container">
    <h2><span class="num">5</span>คำถามที่พบบ่อย</h2>
    <p class="sub">คลิกที่คำถามเพื่อดูคำตอบ</p>

    <div class="faq-list" id="faqList"></div>
  </div>
</section>

<!-- ============================================================ -->
<!-- SECTION 6: TIPS -->
<!-- ============================================================ -->
<section id="tips" class="alt anchor-offset">
  <div class="container">
    <h2><span class="num">6</span>เคล็ดลับและข้อแนะนำ</h2>
    <p class="sub">หลักทองและสัญญาณเตือนที่จะช่วยประหยัดทั้งเวลาและงบประมาณ</p>

    <div class="tips-grid">
      <div class="tip-card">
        <h4>🏆 10 หลักทองในการเลือกรายการ</h4>
        <ol>
          <li>เลือกรายการที่ลูก<b>ชอบ</b> มากกว่ารายการที่<b>ดังที่สุด</b></li>
          <li>ลง Tier ที่เหมาะกับวัย ไม่กระโดดข้ามขั้น</li>
          <li>ตรวจสอบ "หน่วยงานผู้จัด" ทุกครั้ง</li>
          <li>อ่านกติกา 2 รอบก่อนเริ่มงาน</li>
          <li>เริ่มเตรียมตัวก่อนวันแข่ง 8–12 สัปดาห์</li>
          <li>เก็บภาพ-วิดีโอกระบวนการอย่างสม่ำเสมอ</li>
          <li>ฝึกซ้อมพรีเซนต์กับคนแปลกหน้า</li>
          <li>คาดหวังกระบวนการ มากกว่าผลลัพธ์</li>
          <li>หลังแข่งทำสรุป Lesson Learned</li>
          <li>เก็บใบเซอร์ฯ ทุกใบ — ตอน ม.6 ใช้ทั้งหมด</li>
        </ol>
      </div>

      <div class="tip-card warn">
        <h4>⚠️ สัญญาณเตือนรายการที่ควรหลีกเลี่ยง</h4>
        <ul>
          <li><b>ค่าสมัครสูงผิดปกติ</b> (หลายพันบาท) โดยไม่มีหน่วยงานรัฐสนับสนุน</li>
          <li><b>ไม่มีกรรมการตัดสินที่เปิดเผยชื่อ</b> หรือมีแค่ภาพถ่ายไม่ระบุตัวตน</li>
          <li><b>ไม่มีรายชื่อผู้ชนะปีก่อนหน้า</b> ให้ตรวจสอบ</li>
          <li>ใช้คำโฆษณาเกินจริง เช่น "การันตีเข้ามหาวิทยาลัย"</li>
          <li>ขอเงินสนับสนุน <b>"เพิ่มเติม"</b> หลังประกาศผล แลกถ้วยรางวัล/ใบเซอร์ฯ <i>(เป็นการทุจริต)</i></li>
        </ul>
      </div>
    </div>

    <h3 style="margin-top:42px; text-align:center; color:var(--c-primary);">สูตรสำเร็จ: เด็ก × ครู × ผู้ปกครอง</h3>
    <div class="formula">
      <div class="formula-item">
        <h4>เด็ก</h4>
        <p>ความสนใจ + วินัย + ลงมือทำ</p>
      </div>
      <div class="formula-item b">
        <h4>ครู</h4>
        <p>องค์ความรู้ + เครือข่าย + การโค้ช</p>
      </div>
      <div class="formula-item c">
        <h4>ผู้ปกครอง</h4>
        <p>เวลา + ทรัพยากร + กำลังใจ</p>
      </div>
    </div>
    <p style="text-align:center; margin-top: 24px; font-style: italic; color: var(--c-text-soft); max-width: 800px; margin-left: auto; margin-right: auto;">
      เมื่อทั้ง 3 ฝ่ายทำหน้าที่ของตัวเองอย่างเต็มที่ ผลลัพธ์ที่ได้จะเกินกว่าผลรวมของแต่ละฝ่ายเสมอ
    </p>
  </div>
</section>

<!-- ============================================================ -->
<!-- FOOTER -->
<!-- ============================================================ -->
<footer>
  <div class="container">
    <p class="quote">การแข่งขันคือ "กระบวนการ" ไม่ใช่ "จุดหมาย"</p>
    <p>เด็กที่ได้เรียนรู้ผ่านการแข่งขัน จะกลายเป็นผู้ใหญ่ที่กล้าคิด กล้าทำ และไม่กลัวความล้มเหลว</p>
    <p class="meta">© คู่มือฉบับสมบูรณ์ • Impact Tier System • สำหรับผู้ปกครองและคุณครู</p>
  </div>
</footer>

<button class="back-to-top" id="backToTop" aria-label="ขึ้นไปด้านบน">↑</button>

<!-- ============================================================ -->
<!-- DATA + LOGIC -->
<!-- ============================================================ -->
<script>
// ===== Data: 5 categories × competitions =====
const categories = [
  {
    id: "cs",
    icon: "💻",
    name: "วิทยาการคอมพิวเตอร์ และการเขียนโปรแกรม",
    desc: "เน้นการแก้ปัญหาเชิงตรรกะและการเขียนโค้ด นิยมและมีน้ำหนักสูงในการรับเข้าวิศวะคอมฯ",
    items: [
      { tier: 3, name: "IOI", full: "International Olympiad in Informatics", org: "สสวท. / นานาชาติ", desc: "จุดสูงสุดของเด็กมัธยม (โอลิมปิกวิชาการ)" },
      { tier: 3, name: "ICPC World Finals", full: "ICPC World Finals", org: "ICPC Foundation", desc: "จุดสูงสุดของนิสิตมหาวิทยาลัย (ทีม 3 คน)" },
      { tier: 3, name: "USACO", full: "USA Computing Olympiad", org: "USACO (Online)", desc: "การแข่งขันออนไลน์ที่ได้รับการยอมรับทั่วโลก" },
      { tier: 2, name: "ICPC Asia Bangkok", full: "ICPC Asia Bangkok Regional", org: "CP Chula (เจ้าภาพ)", desc: "เวทีคัดเลือกทีมเก่งที่สุดในเอเชียสู่ระดับโลก" },
      { tier: 2, name: "APIO", full: "Asia-Pacific Informatics Olympiad", org: "เจ้าภาพหมุนเวียน", desc: "การประลองระดับหัวกะทิในโซนเอเชีย-แปซิฟิก" },
      { tier: 1, name: "สอวน. คอมพิวเตอร์", full: "TOCPC", org: "มูลนิธิ สอวน.", desc: "ใบเบิกทางเข้าวิศวะฯ จุฬาฯ รอบพอร์ตที่ดีที่สุด" },
      { tier: 1, name: "NSC", full: "National Software Contest", org: "สวทช. (NSTDA)", desc: "การแข่งพัฒนาโปรแกรม/AI ที่ใหญ่ที่สุดในไทย" },
      { tier: 1, name: "CEDT Hackathon", full: "CEDT Hackathon", org: "วิศวะคอมฯ จุฬาฯ", desc: "Hackathon หาพันธมิตร พบพี่ ๆ นิสิต" },
      { tier: 0, name: "Bebras Thailand", full: "Bebras Computing Challenge", org: "สสวท. / สากล", desc: "วัดทักษะการคิดเชิงคำนวณ มีใบเซอร์ฯ ทุกระดับชั้น" },
      { tier: 0, name: "Code.org / Hour of Code", full: "Hour of Code", org: "Code.org", desc: "ชั่วโมงเขียนโค้ดโลก เริ่มต้นง่ายที่สุด" },
    ]
  },
  {
    id: "innovation",
    icon: "🚀",
    name: "นวัตกรรม โครงงานวิจัย และสิ่งประดิษฐ์",
    desc: "เน้นการสร้างสรรค์สิ่งใหม่เพื่อแก้ปัญหา ผลงานเห็นเป็นชิ้นและนำเสนอในพอร์ตได้สะดุดตา",
    items: [
      { tier: 3, name: "Regeneron ISEF", full: "International Science and Engineering Fair", org: "Society for Science", desc: "โอลิมปิกโครงงานวิทย์ บันไดสู่ Ivy League" },
      { tier: 3, name: "GENIUS Olympiad", full: "GENIUS Olympiad", org: "RIT (USA)", desc: "เน้นนวัตกรรมสิ่งแวดล้อม ศิลปะ และความเป็นสากล" },
      { tier: 3, name: "Microsoft Imagine Cup", full: "Microsoft Imagine Cup", org: "Microsoft", desc: "นวัตกรรมที่เปลี่ยนเป็นธุรกิจ Tech Startup" },
      { tier: 2, name: "INNOVADEX", full: "INNOVADEX", org: "สมาคมนวัตกรรมไทย / สากล", desc: "เน้นนวัตกรรมที่ล้ำสมัยและตอบโจทย์เชิงพาณิชย์" },
      { tier: 2, name: "IPITEx", full: "International Innovation Exhibition", org: "วช.", desc: "งานแสดงนวัตกรรมที่ฝึกการนำเสนอเป็นภาษาอังกฤษ" },
      { tier: 2, name: "AYIE", full: "ASEAN Young Inventors Exhibition", org: "นานาชาติ (มาเลเซีย)", desc: "เวทีนวัตกรรมเยาวชนอาเซียน" },
      { tier: 2, name: "ITEX", full: "International Invention Exhibition", org: "นานาชาติ", desc: "งานแสดงสิ่งประดิษฐ์ระดับนานาชาติ" },
      { tier: 1, name: "I-New Gen Award", full: "I-New Generation Award", org: "วช.", desc: "รายการยอดฮิต มี 5 กลุ่มเรื่อง ยื่นพอร์ตเด่นมาก" },
      { tier: 1, name: "YSC", full: "Young Scientist Competition", org: "สวทช.", desc: "สนามคัดเลือกตัวแทนประเทศไทยไป ISEF" },
      { tier: 0, name: "School Hackathon", full: "School Hackathon", org: "ภายในโรงเรียน", desc: "เริ่มต้น Project-based learning แบบสนุก" },
      { tier: 0, name: "CCES", full: "Chula Computer Showcase", org: "วิศวะคอมฯ จุฬาฯ", desc: "งานแสดงนวัตกรรมเพื่อหาแรงบันดาลใจและเครือข่าย" },
    ]
  },
  {
    id: "robot",
    icon: "🤖",
    name: "หุ่นยนต์ วิศวกรรม และเทคโนโลยีอวกาศ",
    desc: "เน้นการควบคุม Hardware วิศวกรรมการบิน และเทคโนโลยีอวกาศ เด็กในสายนี้มักทำงานเป็นทีม",
    items: [
      { tier: 3, name: "WRO World Final", full: "World Robot Olympiad", org: "WRO Association", desc: "โอลิมปิกหุ่นยนต์ระดับโลก" },
      { tier: 3, name: "FRC", full: "FIRST Robotics Competition", org: "FIRST (USA)", desc: "หุ่นยนต์ขนาดใหญ่และซับซ้อนระดับมืออาชีพ" },
      { tier: 3, name: "VEX World", full: "VEX Robotics World Championship", org: "VEX (USA)", desc: "การแข่งหุ่นยนต์ระดับโลกที่ใหญ่ที่สุด" },
      { tier: 3, name: "CanSat World", full: "CanSat World Competition", org: "นานาชาติ", desc: "นวัตกรรมดาวเทียมกระป๋องระดับสูงสุด" },
      { tier: 2, name: "ABU Robocon", full: "ABU Asia-Pacific Robot Contest", org: "ABU Broadcasting Union", desc: "หุ่นยนต์ระดับอุดมศึกษาที่มีโจทย์สุดท้าทาย" },
      { tier: 2, name: "WRO APAC", full: "WRO Asia Pacific Championship", org: "WRO", desc: "WRO ระดับเอเชีย-แปซิฟิก" },
      { tier: 1, name: "Thailand CanSat & Rocket", full: "Thailand CanSat & Rocket", org: "อพวช. / GISTDA", desc: "แข่งจรวดประดิษฐ์และดาวเทียม Space Tech" },
      { tier: 1, name: "WRO Thailand", full: "WRO Thailand", org: "สมาคมหุ่นยนต์ฯ", desc: "รายการมาตรฐานเพื่อชิงแชมป์ประเทศไทย" },
      { tier: 1, name: "TPA Robot", full: "TPA Robot Contest", org: "สสท.", desc: "แข่งหุ่นยนต์ระดับชาติที่มีมาอย่างยาวนาน" },
      { tier: 0, name: "Sumo Robot", full: "Sumo Robot (TCAS70)", org: "CP Chula", desc: "ฝึกทำหุ่นยนต์เบื้องต้น สนุก และได้ใบเซอร์ฯ จากจุฬาฯ" },
    ]
  },
  {
    id: "art",
    icon: "🎨",
    name: "ศิลปะดิจิทัล การออกแบบ และมีเดีย",
    desc: "เน้นความสวยงาม UX และความคิดสร้างสรรค์ เปิดโอกาสให้เด็กที่มีหัวศิลปะใช้เทคโนโลยีเป็นเครื่องมือ",
    items: [
      { tier: 3, name: "Adobe Certified Pro World Champ", full: "Adobe Certified Professional World Championship", org: "Certiport (USA)", desc: "วัดความเชี่ยวชาญเครื่องมือ Adobe ระดับโลก" },
      { tier: 3, name: "Red Dot Award (Concept)", full: "Red Dot Design Award", org: "Red Dot (Global)", desc: "มาตรฐานการออกแบบที่ Apple และแบรนด์ดังยอมรับ" },
      { tier: 2, name: "Asian Digital Art Award", full: "Asian Digital Art Award", org: "Fukuoka City (Japan)", desc: "เวทีท็อปของเอเชียสำหรับ Game, Video และ Digital Art" },
      { tier: 1, name: "ศิลปกรรมเด็กและเยาวชนแห่งชาติ", full: "National Children & Youth Art Exhibition", org: "หอศิลป์ร่วมสมัยราชดำเนิน", desc: "มีหมวดดิจิทัลอาร์ตที่มีศักดิ์ศรีระดับชาติ" },
      { tier: 1, name: "MR. D.I.Y. Art Contest", full: "MR. D.I.Y. Art Contest", org: "MR. D.I.Y. (Digital Art)", desc: "แข่งศิลปะดิจิทัลเพื่อสังคมและสิ่งแวดล้อม" },
      { tier: 0, name: "XPPen Art Contest", full: "XPPen Art Contest", org: "XPPen", desc: "ฝึกฝนและสะสมผลงานการออกแบบในระดับต้น" },
      { tier: 0, name: "Wacom Thailand", full: "Wacom Thailand Contest", org: "Wacom", desc: "เวทีศิลปะดิจิทัลเริ่มต้นจากแบรนด์อุปกรณ์วาดเขียน" },
      { tier: 0, name: "Character Design", full: "Character Design Contest", org: "งานคอมมิคต่าง ๆ", desc: "ฝึกออกแบบตัวละครและสไตล์ของตัวเอง" },
    ]
  },
  {
    id: "cyber",
    icon: "🛡️",
    name: "ความมั่นคงปลอดภัยไซเบอร์ และข้อมูล",
    desc: "สายอาชีพที่ขาดแคลนและให้ผลตอบแทนสูงที่สุดในตลาด เด็กตรรกะดี ชอบสืบสวนจะสนุกกับสายนี้",
    items: [
      { tier: 3, name: "DEF CON CTF", full: "DEF CON Capture The Flag", org: "DEF CON (USA)", desc: "World Cup ของแฮกเกอร์ ที่ได้รับการยอมรับสูงสุด" },
      { tier: 2, name: "ASEAN Cyber SEA Game", full: "ASEAN Cyber SEA Game", org: "ASEAN-Japan", desc: "เฟ้นหาสุดยอดนักล่าช่องโหว่ในระดับภูมิภาค" },
      { tier: 1, name: "Thailand Cyber Showcase", full: "Thailand Cyber Showcase", org: "สกมช. (NCSA)", desc: "แข่งแฮกเกอร์ระดับชาติเพื่อสร้างบุคลากรให้รัฐ" },
      { tier: 0, name: "PicoCTF", full: "PicoCTF", org: "CMU (USA)", desc: "แพลตฟอร์มเริ่มเรียนรู้การแฮกอย่างสร้างสรรค์ (Online)" },
    ]
  }
];

const faqs = [
  { q: "ลูก/นักเรียนต้องเริ่มจาก Tier 0 ทุกคนหรือไม่?",
    a: "ไม่จำเป็นเสมอไป หากเด็กมีพื้นฐานชัดเจนแล้ว สามารถเริ่มที่ Tier 1 ได้เลย แต่หากยังไม่แน่ใจในความชอบ Tier 0 จะช่วยลดความเสี่ยงและให้เวลาเด็กได้ \"ลอง\" หลายสายอย่างปลอดภัย" },
  { q: "ส่งหลายรายการพร้อมกันได้ไหม?",
    a: "ทำได้ แต่ไม่แนะนำหากเป็น Tier 1 ขึ้นไป เพราะคุณภาพของผลงานสำคัญกว่าปริมาณ การโฟกัส 1–2 รายการต่อภาคเรียนคือสมดุลที่ดีที่สุด" },
  { q: "ถ้าได้รางวัลจาก Tier 0 หรือ Tier 1 ชาติเล็ก ๆ พอใส่พอร์ตได้ไหม?",
    a: "ได้ครับ/ค่ะ เพียงแต่ Tier 0 จะเป็น \"พอร์ตเสริม\" ในขณะที่ Tier 1 ขึ้นไปเป็น \"พอร์ตหลัก\" ที่กรรมการให้น้ำหนัก รางวัลทุกระดับยังมีค่าหากใส่ได้ตรงสาย" },
  { q: "ค่าใช้จ่ายระดับ Tier 2–3 สูงมากไหม?",
    a: "ขึ้นอยู่กับรายการ บางรายการมีทุนสนับสนุนจากหน่วยงานต้นสังกัดเช่น สวทช. หรือ วช. แต่บางรายการต้องออกค่าเดินทางเอง ผู้ปกครองควรปรึกษาคุณครูล่วงหน้าและเตรียมงบ 30,000–150,000 บาทสำหรับการแข่งระดับโลก" },
  { q: "รายการที่ไม่อยู่ในเอกสารนี้ ใช้ได้ไหม?",
    a: "ใช้ได้ แต่ควรประเมินก่อน 3 ข้อ: (1) หน่วยงานผู้จัดน่าเชื่อถือหรือไม่ (2) มีตัวแทนจากหลายโรงเรียน/หลายประเทศแข่งขันจริงหรือไม่ (3) มหาวิทยาลัยปลายทางยอมรับหรือไม่ หากตอบ \"ไม่ใช่\" 2 ข้อขึ้นไป ให้พิจารณาเปลี่ยนรายการ" },
  { q: "ลูก/นักเรียนแพ้บ่อย ๆ ควรหยุดส่งหรือไม่?",
    a: "ไม่ควรหยุดทันที แต่ควรวิเคราะห์ว่าแพ้เพราะอะไร หากเป็นเพราะยังไม่พร้อมเชิงทักษะ ใช้เวลา 1 ภาคเรียนพัฒนาแล้วลองใหม่ หากเป็นเพราะ \"สายไม่ใช่\" ให้ลองสายอื่น เด็กที่ชนะระดับโลกหลายคนเริ่มจาก \"แพ้ 5–10 ครั้ง\" มาก่อน" },
  { q: "คุณครูเป็นที่ปรึกษาหลายโครงงานพร้อมกันได้กี่โครงงาน?",
    a: "ในทางปฏิบัติ ครู 1 คน ดูแลโครงงานเข้มข้นได้ 2–3 โครงงานต่อภาคเรียน หากมากกว่านี้ ควรกระจายให้ครูในกลุ่มสาระอื่น ๆ เป็นที่ปรึกษาร่วม เพื่อรักษาคุณภาพของงาน" },
  { q: "ผลงานที่ทำเป็นทีม ใส่พอร์ตเฉพาะตัวเองได้ไหม?",
    a: "ได้ครับ/ค่ะ แต่ต้องระบุชัดเจนว่าทีมมีกี่คน และตัวเองรับผิดชอบส่วนใด กรรมการรับเข้าตรวจละเอียดมาก หากระบุไม่ตรงข้อเท็จจริงจะถูกตัดสิทธิ์" },
];

// ===== Render Competitions =====
function tierLabel(t) {
  return ({ 0: "Tier 0", 1: "Tier 1", 2: "Tier 2", 3: "Tier 3" })[t];
}
function tierName(t) {
  return ({ 0: "ทั่วไป", 1: "ชาติ", 2: "เอเชีย", 3: "โลก" })[t];
}

function renderCompetitions() {
  const container = document.getElementById("competitionsContainer");
  container.innerHTML = categories.map(cat => `
    <div class="category" data-cat="${cat.id}">
      <div class="category-head">
        <div class="icon">${cat.icon}</div>
        <div>
          <h3>${cat.name}</h3>
          <p>${cat.desc}</p>
        </div>
      </div>
      <div class="competitions">
        ${cat.items.sort((a,b) => b.tier - a.tier).map(item => `
          <div class="comp-card t${item.tier}"
               data-tier="${item.tier}"
               data-search="${(item.name + ' ' + item.full + ' ' + item.org + ' ' + item.desc).toLowerCase()}">
            <div class="top">
              <h4>${item.name}</h4>
              <span class="tier-tag">${tierLabel(item.tier)} • ${tierName(item.tier)}</span>
            </div>
            <div class="org">${item.full !== item.name ? item.full + ' • ' : ''}${item.org}</div>
            <div class="desc">${item.desc}</div>
          </div>
        `).join('')}
        <div class="empty-msg" style="display:none;">ไม่พบรายการที่ตรงกับเงื่อนไข ลองปรับคำค้นหาหรือเลือกระดับอื่น</div>
      </div>
    </div>
  `).join('');
}

// ===== Render FAQ =====
function renderFaqs() {
  const list = document.getElementById("faqList");
  list.innerHTML = faqs.map((f, i) => `
    <div class="faq-item" data-i="${i}">
      <button class="faq-q" type="button">
        <span><b>Q${i+1}.</b> ${f.q}</span>
        <span class="arrow">⌄</span>
      </button>
      <div class="faq-a">${f.a}</div>
    </div>
  `).join('');
  list.querySelectorAll(".faq-q").forEach(btn => {
    btn.addEventListener("click", () => btn.parentElement.classList.toggle("open"));
  });
}

// ===== Filter / Search =====
let activeTier = "all";
let searchQuery = "";

function applyFilter() {
  const cats = document.querySelectorAll("#competitionsContainer .category");
  cats.forEach(cat => {
    const cards = cat.querySelectorAll(".comp-card");
    let visible = 0;
    cards.forEach(card => {
      const tier = card.dataset.tier;
      const text = card.dataset.search;
      const matchTier = (activeTier === "all" || activeTier === tier);
      const matchSearch = (!searchQuery || text.includes(searchQuery));
      if (matchTier && matchSearch) {
        card.classList.remove("hidden");
        visible++;
      } else {
        card.classList.add("hidden");
      }
    });
    const empty = cat.querySelector(".empty-msg");
    if (empty) empty.style.display = (visible === 0) ? "block" : "none";
    cat.classList.toggle("hidden", visible === 0);
  });
}

// ===== Init =====
document.addEventListener("DOMContentLoaded", () => {
  renderCompetitions();
  renderFaqs();

  // Tier chips
  document.querySelectorAll("#tierChips .chip").forEach(chip => {
    chip.addEventListener("click", () => {
      document.querySelectorAll("#tierChips .chip").forEach(c => c.classList.remove("active"));
      chip.classList.add("active");
      activeTier = chip.dataset.tier;
      applyFilter();
    });
  });

  // Search
  const search = document.getElementById("searchInput");
  search.addEventListener("input", e => {
    searchQuery = e.target.value.trim().toLowerCase();
    applyFilter();
  });

  // Back to top
  const btt = document.getElementById("backToTop");
  window.addEventListener("scroll", () => {
    btt.classList.toggle("visible", window.scrollY > 400);
  });
  btt.addEventListener("click", () => window.scrollTo({ top: 0, behavior: "smooth" }));
});
</script>

</body>
</html>
