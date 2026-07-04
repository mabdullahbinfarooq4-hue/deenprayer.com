<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<title>Deen — Prayer Companion</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500;700&family=Amiri:wght@400;700&family=Noto+Nastaliq+Urdu:wght@400;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #FAFAF8;
    --surface: #FFFFFF;
    --ink: #14342B;
    --ink-soft: #6B7570;
    --accent: #C9A227;
    --accent-soft: #F3E9C9;
    --border: #E4E4DE;
    --shadow: 0 1px 2px rgba(20,52,43,0.05), 0 4px 16px rgba(20,52,43,0.06);
  }
  html[data-theme="dark"]{
    --bg: #0E1A16;
    --surface: #17251F;
    --ink: #F2F0E6;
    --ink-soft: #93A199;
    --accent: #E0BE55;
    --accent-soft: #3A331A;
    --border: #26362F;
    --shadow: 0 1px 2px rgba(0,0,0,0.2), 0 4px 20px rgba(0,0,0,0.25);
  }
  *{box-sizing:border-box; -webkit-tap-highlight-color: transparent;}
  html,body{margin:0; padding:0; height:100%;}
  body{
    background: var(--bg);
    color: var(--ink);
    font-family: 'Inter', sans-serif;
    display:flex;
    justify-content:center;
    transition: background .25s ease, color .25s ease;
  }
  .lang-ur{ font-family:'Noto Nastaliq Urdu', serif; direction:rtl; }
  #app{
    width:100%;
    max-width:480px;
    min-height:100vh;
    background: var(--bg);
    position:relative;
    display:flex;
    flex-direction:column;
  }
  ::selection{ background: var(--accent-soft); }
  button{ font-family:inherit; cursor:pointer; }
  .mono{ font-family:'JetBrains Mono', monospace; }
  .serif{ font-family:'Fraunces', serif; }

  /* ---- Header ---- */
  header{
    padding:20px 20px 14px;
    display:flex;
    align-items:center;
    justify-content:space-between;
  }
  header .dates{ line-height:1.3; }
  header .hijri{ font-size:13px; color:var(--ink-soft); }
  header .greg{ font-size:13px; color:var(--ink-soft); }
  header .brand{
    font-family:'Fraunces', serif;
    font-size:15px;
    font-weight:600;
    letter-spacing:0.02em;
    color:var(--ink);
    display:flex; align-items:center; gap:6px;
  }
  .icon-btn{
    width:38px; height:38px;
    border-radius:50%;
    border:1px solid var(--border);
    background:var(--surface);
    display:flex; align-items:center; justify-content:center;
    color:var(--ink);
    flex-shrink:0;
  }

  main{ flex:1; padding: 0 20px 100px; overflow-y:auto; }
  .view{ display:none; animation: fadein .25s ease; }
  .view.active{ display:block; }
  @keyframes fadein{ from{opacity:0; transform:translateY(4px);} to{opacity:1; transform:none;} }

  /* ---- Bottom Nav ---- */
  nav{
    position:sticky; bottom:0; left:0; right:0;
    background: rgba(250,250,248,0.92);
    backdrop-filter: blur(10px);
    border-top:1px solid var(--border);
    display:flex;
    padding: 8px 6px calc(8px + env(safe-area-inset-bottom));
  }
  nav button{
    flex:1;
    background:none; border:none;
    display:flex; flex-direction:column; align-items:center; gap:4px;
    padding:6px 2px;
    color:var(--ink-soft);
    border-radius:12px;
  }
  nav button.active{ color:var(--ink); }
  nav button svg{ width:22px; height:22px; }
  nav button span{ font-size:10.5px; font-weight:500; }

  /* ---- Home: next prayer card ---- */
  .next-card{
    background: linear-gradient(155deg, #14342B 0%, #1C4638 100%);
    color:#F7F5EC;
    border-radius:22px;
    padding:24px 22px 20px;
    margin: 6px 0 18px;
    box-shadow: var(--shadow);
  }
  .next-card .eyebrow{
    font-size:11.5px; text-transform:uppercase; letter-spacing:0.12em;
    color: #C9DAC9; margin-bottom:6px; font-weight:600;
  }
  .next-card .prayer-name{
    font-family:'Fraunces', serif; font-size:34px; font-weight:600;
    margin:0 0 4px;
  }
  .next-card .countdown{
    font-size:28px; letter-spacing:0.01em; color: var(--accent);
    font-weight:500;
  }
  .next-card .subtext{ font-size:12.5px; color:#B9C7BE; margin-top:4px; }

  /* ---- Day arc (signature element) ---- */
  .arc-wrap{ margin: 4px 0 20px; }
  .arc-wrap svg{ width:100%; height:auto; display:block; }
  .arc-label{ font-size:10px; fill: var(--ink-soft); font-family:'Inter'; }
  .arc-label-active{ fill: var(--ink); font-weight:600; }

  /* ---- Prayer list ---- */
  .prayer-row{
    display:flex; align-items:center; justify-content:space-between;
    padding:13px 4px;
    border-bottom:1px solid var(--border);
  }
  .prayer-row:last-child{ border-bottom:none; }
  .prayer-row .name{ font-size:15px; font-weight:500; display:flex; align-items:center; gap:10px;}
  .prayer-row .time{ font-size:15px; }
  .prayer-row.active .name, .prayer-row.active .time{ color: var(--accent); font-weight:600; }
  .dot{ width:6px; height:6px; border-radius:50%; background:var(--border); }
  .prayer-row.active .dot{ background:var(--accent); }

  .section-title{
    font-family:'Fraunces', serif; font-size:19px; font-weight:600;
    margin: 22px 0 10px;
  }
  .card{
    background:var(--surface); border:1px solid var(--border);
    border-radius:16px; padding:16px;
  }

  /* toggle row for settings */
  .setting-row{ display:flex; align-items:center; justify-content:space-between; padding:12px 0; border-bottom:1px solid var(--border); }
  .setting-row:last-child{ border-bottom:none; }
  .setting-row label{ font-size:14px; }
  select{
    font-family:inherit; font-size:13.5px; padding:8px 10px; border-radius:10px;
    border:1px solid var(--border); background:var(--bg); color:var(--ink);
  }
  .switch{ position:relative; width:44px; height:26px; }
  .switch input{ opacity:0; width:0; height:0; }
  .slider{ position:absolute; inset:0; background:var(--border); border-radius:20px; transition:.2s; }
  .slider::before{ content:""; position:absolute; width:20px; height:20px; left:3px; top:3px; background:#fff; border-radius:50%; transition:.2s; }
  input:checked + .slider{ background: var(--ink); }
  input:checked + .slider::before{ transform:translateX(18px); }

  /* ---- Qibla ---- */
  .compass-wrap{ display:flex; flex-direction:column; align-items:center; padding: 20px 0 6px; }
  .compass-wrap svg{ width:260px; height:260px; }
  .qibla-info{ text-align:center; margin-top:10px; }
  .qibla-info .deg{ font-family:'JetBrains Mono', monospace; font-size:32px; font-weight:500; }
  .qibla-info .dist{ font-size:13px; color:var(--ink-soft); margin-top:2px; }
  .perm-btn{
    margin-top:16px; background:var(--ink); color:#fff; border:none;
    padding:11px 20px; border-radius:12px; font-size:14px; font-weight:500;
  }

  /* ---- Quran ---- */
  .search-bar{
    display:flex; align-items:center; gap:8px;
    background:var(--surface); border:1px solid var(--border); border-radius:12px;
    padding:10px 12px; margin: 4px 0 14px;
  }
  .search-bar input{ border:none; outline:none; background:none; font-family:inherit; font-size:14px; flex:1; color:var(--ink); }
  .surah-row{
    display:flex; align-items:center; gap:12px;
    padding:12px 4px; border-bottom:1px solid var(--border); cursor:pointer;
  }
  .surah-num{
    width:32px; height:32px; border-radius:9px; background:var(--accent-soft);
    color:#8a6c14; display:flex; align-items:center; justify-content:center;
    font-size:12.5px; font-weight:700; flex-shrink:0;
  }
  .surah-en{ font-size:15px; font-weight:600; }
  .surah-meta{ font-size:12px; color:var(--ink-soft); }
  .surah-ar{ font-family:'Amiri', serif; font-size:19px; margin-left:auto; color:var(--ink); }

  .ayah{ padding:16px 0; border-bottom:1px solid var(--border); }
  .ayah .num-chip{
    display:inline-flex; width:22px; height:22px; border-radius:50%;
    background:var(--accent-soft); color:#8a6c14; font-size:11px; font-weight:700;
    align-items:center; justify-content:center; margin-bottom:8px;
  }
  .ayah .arabic{ font-family:'Amiri', serif; font-size:23px; text-align:right; direction:rtl; line-height:1.9; color:var(--ink); }
  .ayah .translation{ font-size:14px; color: var(--ink-soft); margin-top:8px; line-height:1.55; }
  .back-btn{ display:flex; align-items:center; gap:6px; color:var(--ink-soft); font-size:13.5px; background:none; border:none; padding:6px 0 12px; }

  /* ---- Tasbih ---- */
  .dhikr-chips{ display:flex; flex-wrap:wrap; gap:8px; margin: 4px 0 20px; }
  .chip{
    padding:8px 14px; border-radius:20px; border:1px solid var(--border);
    background:var(--surface); font-size:13px; color:var(--ink-soft);
  }
  .chip.active{ background:var(--ink); color:#fff; border-color:var(--ink); }
  .tasbih-circle{
    width:220px; height:220px; border-radius:50%;
    background: radial-gradient(circle at 30% 25%, #1C4638, #14342B);
    color:#fff; margin: 10px auto 22px;
    display:flex; flex-direction:column; align-items:center; justify-content:center;
    border:none; box-shadow: var(--shadow);
  }
  .tasbih-circle .count{ font-family:'JetBrains Mono', monospace; font-size:52px; font-weight:500; }
  .tasbih-circle .target{ font-size:12.5px; color:#B9C7BE; margin-top:2px; }
  .tasbih-circle:active{ transform:scale(0.97); }
  .tasbih-controls{ display:flex; justify-content:center; gap:10px; }
  .ghost-btn{
    background:var(--surface); border:1px solid var(--border); color:var(--ink);
    padding:9px 16px; border-radius:12px; font-size:13.5px;
  }

  /* ---- Calendar ---- */
  .cal-nav{ display:flex; align-items:center; justify-content:space-between; margin: 6px 0 14px; }
  .cal-month-title{ font-family:'Fraunces', serif; font-size:18px; font-weight:600; }
  .cal-grid{ display:grid; grid-template-columns:repeat(7,1fr); gap:4px; text-align:center; }
  .cal-dow{ font-size:10.5px; color:var(--ink-soft); padding-bottom:6px; }
  .cal-day{
    aspect-ratio:1; border-radius:10px; display:flex; flex-direction:column;
    align-items:center; justify-content:center; font-size:13px; background:var(--surface);
    border:1px solid var(--border);
  }
  .cal-day .g{ font-size:9px; color:var(--ink-soft); }
  .cal-day.today{ background:var(--ink); color:#fff; border-color:var(--ink); }
  .cal-day.today .g{ color:#C9DAC9; }
  .cal-day.friday:not(.today){ background:var(--accent-soft); border-color:var(--accent-soft); }
  .cal-day.empty{ background:none; border:none; }

  /* modal */
  .modal-backdrop{
    position:fixed; inset:0; background:rgba(20,52,43,0.35); backdrop-filter: blur(2px);
    display:none; align-items:flex-end; justify-content:center; z-index:50;
  }
  .modal-backdrop.open{ display:flex; }
  .modal{
    width:100%; max-width:480px; background:var(--bg); border-radius:22px 22px 0 0;
    padding:20px 20px calc(20px + env(safe-area-inset-bottom)); max-height:85vh; overflow-y:auto;
    animation: slideup .25s ease;
  }
  @keyframes slideup{ from{ transform:translateY(30px); opacity:0; } to{ transform:none; opacity:1; } }
  .modal-title{ font-family:'Fraunces', serif; font-size:19px; font-weight:600; margin-bottom:6px; }
  .modal-close{ display:flex; justify-content:flex-end; }
  .empty-state{ text-align:center; padding:40px 10px; color:var(--ink-soft); font-size:13.5px; }
  .loading-dot{ display:inline-block; width:6px;height:6px;border-radius:50%; background:var(--ink-soft); margin:0 2px; animation:pulse 1s infinite ease-in-out; }
  .loading-dot:nth-child(2){ animation-delay:.15s; } .loading-dot:nth-child(3){ animation-delay:.3s; }
  @keyframes pulse{ 0%,100%{opacity:.25} 50%{opacity:1} }

  /* ---- clock + kaaba icon on next-prayer card ---- */
  .next-card{ position:relative; overflow:hidden; }
  .live-clock{ font-family:'JetBrains Mono', monospace; font-size:14px; color:#B9C7BE; margin-top:2px; letter-spacing:0.02em; }
  .kaaba-icon{ position:absolute; right:14px; top:14px; opacity:0.9; }
  .kaaba-icon svg{ width:46px; height:46px; }

  /* ---- lang toggle chips ---- */
  .lang-toggle{ display:flex; gap:6px; }
  .lang-chip{ padding:6px 12px; border-radius:10px; border:1px solid var(--border); background:var(--bg); color:var(--ink-soft); font-size:12.5px; }
  .lang-chip.active{ background:var(--ink); color:var(--bg); border-color:var(--ink); }

  /* ---- profile row ---- */
  .profile-input{ font-family:inherit; font-size:13.5px; padding:8px 10px; border-radius:10px; border:1px solid var(--border); background:var(--bg); color:var(--ink); width:130px; }
  .link-row{ display:flex; align-items:center; justify-content:space-between; padding:12px 0; border-bottom:1px solid var(--border); }
  .link-row:last-child{ border-bottom:none; }
  .link-row button{ background:none; border:none; color:var(--ink-soft); font-size:13px; text-decoration:underline; }

  /* ---- about modal text ---- */
  .about-text{ font-size:14px; line-height:1.7; color:var(--ink-soft); }
  .about-text.lang-ur{ font-size:17px; line-height:2; text-align:right; }
  .about-signature{ margin-top:14px; font-family:'Fraunces', serif; font-weight:600; color:var(--ink); font-size:15px; }

  /* ---- prayer tracker checklist ---- */
  .track-row{ display:flex; align-items:center; justify-content:space-between; padding:11px 4px; border-bottom:1px solid var(--border); }
  .track-row:last-child{ border-bottom:none; }
  .track-name{ font-size:14.5px; font-weight:500; }
  .yn-btns{ display:flex; gap:6px; }
  .yn-btn{ padding:6px 13px; border-radius:9px; border:1px solid var(--border); background:var(--bg); font-size:12.5px; color:var(--ink-soft); }
  .yn-btn.yes.active{ background:#3F7A5C; color:#fff; border-color:#3F7A5C; }
  .yn-btn.no.active{ background:#B5544A; color:#fff; border-color:#B5544A; }
  .month-progress{ height:8px; border-radius:6px; background:var(--border); overflow:hidden; margin-top:8px; }
  .month-progress .fill{ height:100%; background:var(--accent); border-radius:6px; transition:width .3s ease; }
  .month-stat-label{ font-size:12px; color:var(--ink-soft); margin-top:6px; }

  /* ---- prayer-check prompt modal ---- */
  .prompt-modal{ text-align:center; }
  .prompt-modal .prompt-title{ font-family:'Fraunces', serif; font-size:20px; font-weight:600; margin: 6px 0 4px; }
  .prompt-modal .prompt-sub{ font-size:13.5px; color:var(--ink-soft); margin-bottom:18px; }
  .prompt-modal .yn-btns{ justify-content:center; gap:12px; }
  .prompt-modal .yn-btn{ padding:11px 26px; font-size:14px; border-radius:12px; }

  @media (prefers-reduced-motion: reduce){ *{ animation:none !important; transition:none !important; } }
</style>
</head>
<body>
<div id="app">

  <header>
    <div class="dates">
      <div class="brand">☾ Deen</div>
      <div class="hijri" id="hijriDate">—</div>
    </div>
    <button class="icon-btn" id="settingsBtn" aria-label="Settings">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" width="19" height="19"><circle cx="12" cy="12" r="3"/><path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 1 1-2.83 2.83l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-4 0v-.09a1.65 1.65 0 0 0-1-1.51 1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 1 1-2.83-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1 0-4h.09a1.65 1.65 0 0 0 1.51-1 1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 1 1 2.83-2.83l.06.06a1.65 1.65 0 0 0 1.82.33H9a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 4 0v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 1 1 2.83 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 0 4h-.09a1.65 1.65 0 0 0-1.51 1z"/></svg>
    </button>
  </header>

  <main>
    <!-- HOME -->
    <section class="view active" id="view-home">
      <div class="next-card">
        <div class="kaaba-icon">
          <svg viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg">
            <rect x="10" y="18" width="40" height="34" fill="#1B1B1B" stroke="#000" stroke-width="0.5"/>
            <rect x="10" y="24" width="40" height="7" fill="#C9A227"/>
            <rect x="10" y="24" width="40" height="7" fill="url(#kgrad)" opacity="0.5"/>
            <path d="M10 18 L30 8 L50 18 Z" fill="#111"/>
            <rect x="26" y="38" width="8" height="14" fill="#0B0B0B"/>
            <defs><linearGradient id="kgrad" x1="0" x2="1"><stop offset="0" stop-color="#fff" stop-opacity="0.4"/><stop offset="1" stop-color="#fff" stop-opacity="0"/></linearGradient></defs>
          </svg>
        </div>
        <div class="eyebrow" id="locLabel" data-i18n="locating">Locating…</div>
        <div class="prayer-name" id="nextPrayerName">—</div>
        <div class="countdown mono" id="countdown">--:--:--</div>
        <div class="subtext" id="countdownSub" data-i18n="untilNext">until next prayer</div>
        <div class="live-clock mono" id="liveClock">--:--:-- —</div>
      </div>

      <div class="arc-wrap" id="dayArc"></div>

      <div class="card">
        <div id="prayerList"></div>
      </div>
    </section>

    <!-- QIBLA -->
    <section class="view" id="view-qibla">
      <h2 class="section-title" data-i18n="qiblaTitle">Qibla direction</h2>
      <div class="compass-wrap">
        <svg id="compassSvg" viewBox="0 0 260 260"></svg>
        <div class="qibla-info">
          <div class="deg" id="qiblaDeg">—°</div>
          <div class="dist" id="qiblaDist">calculating distance to Mecca…</div>
        </div>
        <button class="perm-btn" id="compassPermBtn" data-i18n="enableCompass">Enable live compass</button>
      </div>
    </section>

    <!-- QURAN -->
    <section class="view" id="view-quran">
      <h2 class="section-title" data-i18n="quranTitle">Qur'an</h2>
      <div id="quranList">
        <div class="search-bar">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="11" cy="11" r="7"/><path d="m21 21-4.3-4.3"/></svg>
          <input id="surahSearch" data-i18n-placeholder="searchSurah" placeholder="Search a surah…">
        </div>
        <div id="surahListInner"><div class="empty-state"><span class="loading-dot"></span><span class="loading-dot"></span><span class="loading-dot"></span></div></div>
      </div>
      <div id="quranReader" style="display:none;"></div>
    </section>

    <!-- TASBIH -->
    <section class="view" id="view-tasbih">
      <h2 class="section-title" data-i18n="tasbihTitle">Dhikr counter</h2>
      <div class="dhikr-chips" id="dhikrChips"></div>
      <button class="tasbih-circle" id="tasbihBtn">
        <div class="count mono" id="tasbihCount">0</div>
        <div class="target" id="tasbihTarget">target 33</div>
      </button>
      <div class="tasbih-controls">
        <button class="ghost-btn" id="tasbihReset">Reset</button>
        <button class="ghost-btn" id="tasbihTargetBtn">Change target</button>
      </div>
    </section>

    <!-- CALENDAR -->
    <section class="view" id="view-calendar">
      <h2 class="section-title" data-i18n="calendarTitle">Islamic calendar</h2>
      <div class="card" style="margin-bottom:16px;">
        <div style="font-size:12px; color:var(--ink-soft); margin-bottom:2px;">Today</div>
        <div class="serif" style="font-size:20px; font-weight:600;" id="calTodayHijri">—</div>
        <div style="font-size:13px; color:var(--ink-soft);" id="calTodayGreg">—</div>
      </div>
      <div class="cal-nav">
        <button class="icon-btn" id="calPrev">‹</button>
        <div class="cal-month-title" id="calMonthTitle">—</div>
        <button class="icon-btn" id="calNext">›</button>
      </div>
      <div class="cal-grid" id="calGrid"></div>
      <p style="font-size:11.5px; color:var(--ink-soft); margin-top:14px; line-height:1.5;" data-i18n="hijriNote">Dates use the tabular Islamic calendar and are approximate — actual month start depends on local moon sighting and may shift by a day.</p>

      <h2 class="section-title" data-i18n="todaysPrayers">Today's prayers</h2>
      <div class="card" style="margin-bottom:14px;">
        <div id="trackChecklist"></div>
      </div>
      <div class="card">
        <div class="month-stat-label" id="monthStatLabel">—</div>
        <div class="month-progress"><div class="fill" id="monthFill" style="width:0%"></div></div>
      </div>
    </section>
  </main>

  <nav>
    <button class="tab-btn active" data-view="home">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M3 11.5 12 4l9 7.5"/><path d="M5 10v9a1 1 0 0 0 1 1h4v-6h4v6h4a1 1 0 0 0 1-1v-9"/></svg>
      <span data-i18n="nav_home">Home</span>
    </button>
    <button class="tab-btn" data-view="qibla">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><circle cx="12" cy="12" r="9"/><path d="m14.5 9.5-2 5-5 2 2-5z"/></svg>
      <span data-i18n="nav_qibla">Qibla</span>
    </button>
    <button class="tab-btn" data-view="quran">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"/><path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"/></svg>
      <span data-i18n="nav_quran">Qur'an</span>
    </button>
    <button class="tab-btn" data-view="tasbih">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><circle cx="12" cy="12" r="2"/><circle cx="12" cy="4" r="1.6"/><circle cx="19" cy="8.5" r="1.6"/><circle cx="19" cy="15.5" r="1.6"/><circle cx="12" cy="20" r="1.6"/><circle cx="5" cy="15.5" r="1.6"/><circle cx="5" cy="8.5" r="1.6"/></svg>
      <span data-i18n="nav_tasbih">Tasbih</span>
    </button>
    <button class="tab-btn" data-view="calendar">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="3" y="4.5" width="18" height="16" rx="2"/><path d="M3 9.5h18M8 2.5v4M16 2.5v4"/></svg>
      <span data-i18n="nav_calendar">Calendar</span>
    </button>
  </nav>

  <!-- Settings modal -->
  <div class="modal-backdrop" id="settingsModal">
    <div class="modal">
      <div class="modal-close"><button class="icon-btn" id="closeSettings">✕</button></div>
      <div class="modal-title" data-i18n="settingsTitle">Settings</div>
      <div class="setting-row">
        <label data-i18n="alertsLabel">Prayer alerts</label>
        <label class="switch"><input type="checkbox" id="alertToggle"><span class="slider"></span></label>
      </div>
      <div class="setting-row">
        <label data-i18n="calcMethodLabel">Calculation method</label>
        <select id="calcMethod">
          <option value="mwl">Muslim World League</option>
          <option value="isna">ISNA (North America)</option>
          <option value="egypt">Egyptian Authority</option>
          <option value="karachi">University of Karachi</option>
          <option value="makkah">Umm al-Qura (Makkah)</option>
        </select>
      </div>
      <div class="setting-row">
        <label data-i18n="asrLabel">Asr calculation</label>
        <select id="asrMethod">
          <option value="1">Standard (Shafi'i, Maliki, Hanbali)</option>
          <option value="2">Hanafi</option>
        </select>
      </div>
      <div class="setting-row">
        <label data-i18n="locationLabel">Location</label>
        <button class="ghost-btn" id="relocateBtn" data-i18n="useLocation">Use my location</button>
      </div>
      <div class="setting-row">
        <label data-i18n="language">Language</label>
        <div class="lang-toggle">
          <button class="lang-chip" id="langEnBtn">English</button>
          <button class="lang-chip" id="langUrBtn">اردو</button>
        </div>
      </div>
      <div class="setting-row">
        <label data-i18n="theme">Appearance</label>
        <div class="lang-toggle">
          <button class="lang-chip" id="themeLightBtn" data-i18n="light">Light</button>
          <button class="lang-chip" id="themeDarkBtn" data-i18n="dark">Dark</button>
        </div>
      </div>
      <div class="setting-row">
        <label data-i18n="yourName">Your name</label>
        <input class="profile-input" id="profileInput" placeholder="Optional">
      </div>
      <div class="link-row">
        <span style="font-size:13px; color:var(--ink-soft);" data-i18n="madeBy">Made by Muhammad Abdullah bin Farooq</span>
        <button id="aboutBtn" data-i18n="about">About</button>
      </div>
      <p style="font-size:11.5px; color:var(--ink-soft); line-height:1.5; margin-top:14px;" data-i18n="alertNote">Alerts play a chime while this page stays open in your browser — for guaranteed alarms, wrap this site as an app (see the note in chat).</p>
    </div>
  </div>

  <!-- About modal -->
  <div class="modal-backdrop" id="aboutModal">
    <div class="modal">
      <div class="modal-close"><button class="icon-btn" id="closeAbout">✕</button></div>
      <div class="modal-title" data-i18n="aboutTitle">About Deen</div>
      <div class="about-text" id="aboutText"></div>
    </div>
  </div>

  <!-- Prayer-check prompt modal -->
  <div class="modal-backdrop" id="promptModal">
    <div class="modal prompt-modal">
      <div style="font-size:34px;">🕌</div>
      <div class="prompt-title" id="promptTitle">—</div>
      <div class="prompt-sub" data-i18n="promptSub">Mark it so your monthly record stays accurate.</div>
      <div class="yn-btns">
        <button class="yn-btn no" id="promptNo" data-i18n="notYet">Not yet</button>
        <button class="yn-btn yes" id="promptYes" data-i18n="prayed">Prayed</button>
      </div>
    </div>
  </div>

</div>

<script>
(function(){
  "use strict";

  /* ===================== STATE ===================== */
  const state = {
    lat: 21.4225, lng: 39.8262, locName: "Mecca (default)", // fallback until geolocation resolves
    calcMethod: 'mwl', asrMethod: 1, alertsOn: false,
    prayerTimes: null, prayerDate: null,
    calYear:0, calMonth:0, // hijri calendar being viewed
    tasbihDhikr: 'SubhanAllah', tasbihCounts: {}, tasbihTarget: 33,
    lastAlertMinute: null,
    theme: 'light', lang: 'en', profileName: '',
    prayerLog: {}, promptedThisSession: new Set(), pendingPrompt: null,
  };

  const T = {
    en: {
      nav_home:"Home", nav_qibla:"Qibla", nav_quran:"Qur'an", nav_tasbih:"Tasbih", nav_calendar:"Calendar",
      locating:"Locating…", untilNext:"until next prayer", hijriNote:"Dates use the tabular Islamic calendar and are approximate — actual month start depends on local moon sighting and may shift by a day.",
      todaysPrayers:"Today's prayers", language:"Language", theme:"Appearance", light:"Light", dark:"Dark",
      yourName:"Your name", madeBy:"Made by Muhammad Abdullah bin Farooq", about:"About",
      alertNote:"Alerts play a chime while this page stays open in your browser — for guaranteed alarms, wrap this site as an app.",
      aboutTitle:"About Deen", promptSub:"Mark it so your monthly record stays accurate.", notYet:"Not yet", prayed:"Prayed",
      fajr:"Fajr", sunrise:"Sunrise", dhuhr:"Dhuhr", asr:"Asr", maghrib:"Maghrib", isha:"Isha",
      qiblaTitle:"Qibla direction", enableCompass:"Enable live compass", toMecca:"to Mecca",
      quranTitle:"Qur'an", searchSurah:"Search a surah…", tasbihTitle:"Dhikr counter", calendarTitle:"Islamic calendar",
      settingsTitle:"Settings", alertsLabel:"Prayer alerts", calcMethodLabel:"Calculation method", asrLabel:"Asr calculation",
      locationLabel:"Location", useLocation:"Use my location", didYouPray:"Did you pray", allSurahs:"All surahs",
      monthProgress:"prayed this month", greeting:"Assalamu Alaikum",
      aboutBody:"This app was built with care by Muhammad Abdullah bin Farooq, the owner of this website, to help make daily prayer simple and consistent for everyone. May it be of benefit — Ameen."
    },
    ur: {
      nav_home:"ہوم", nav_qibla:"قبلہ", nav_quran:"قرآن", nav_tasbih:"تسبیح", nav_calendar:"کیلنڈر",
      locating:"مقام تلاش ہو رہا ہے…", untilNext:"اگلی نماز تک", hijriNote:"تاریخیں جدولی اسلامی کیلنڈر کے مطابق ہیں اور تخمینی ہیں — مہینے کا آغاز چاند نظر آنے پر منحصر ہے اور ایک دن آگے پیچھے ہو سکتا ہے۔",
      todaysPrayers:"آج کی نمازیں", language:"زبان", theme:"تھیم", light:"لائٹ", dark:"ڈارک",
      yourName:"آپ کا نام", madeBy:"محمد عبداللہ بن فاروق کا بنایا گیا", about:"تعارف",
      alertNote:"جب تک یہ صفحہ کھلا رہے گا، الرٹ ایک دھن بجائے گا — یقینی الارم کے لیے، اس ویب سائٹ کو ایپ کی صورت میں تیار کریں۔",
      aboutTitle:"دین کے بارے میں", promptSub:"درست ماہانہ ریکارڈ کے لیے نشان زد کریں۔", notYet:"ابھی نہیں", prayed:"پڑھ لی",
      fajr:"فجر", sunrise:"طلوعِ آفتاب", dhuhr:"ظہر", asr:"عصر", maghrib:"مغرب", isha:"عشاء",
      qiblaTitle:"قبلہ کا رخ", enableCompass:"لائیو کمپاس فعال کریں", toMecca:"مکہ تک",
      quranTitle:"قرآن", searchSurah:"سورہ تلاش کریں…", tasbihTitle:"ذکر کاؤنٹر", calendarTitle:"اسلامی کیلنڈر",
      settingsTitle:"ترتیبات", alertsLabel:"نماز کی یاد دہانی", calcMethodLabel:"حساب کا طریقہ", asrLabel:"عصر کا حساب",
      locationLabel:"مقام", useLocation:"میرا مقام استعمال کریں", didYouPray:"کیا آپ نے پڑھی", allSurahs:"تمام سورتیں",
      monthProgress:"اس مہینے پڑھی گئیں", greeting:"السلام علیکم",
      aboutBody:"یہ ایپ محمد عبداللہ بن فاروق نے، جو اس ویب سائٹ کے مالک ہیں، محبت اور خلوص سے تیار کی ہے تاکہ روزمرہ کی نماز کو سب کے لیے آسان اور باقاعدہ بنایا جا سکے۔ اللہ اسے صدقہ جاریہ بنائے — آمین۔"
    }
  };
  function t(key){ return (T[state.lang] && T[state.lang][key]) || T.en[key] || key; }

  const METHODS = {
    mwl:    { fajr: 18, isha: 17 },
    isna:   { fajr: 15, isha: 15 },
    egypt:  { fajr: 19.5, isha: 17.5 },
    karachi:{ fajr: 18, isha: 18 },
    makkah: { fajr: 18.5, isha: 90, ishaMinutes: 90 } // isha = maghrib+90min
  };

  /* ===================== ASTRONOMY MATH ===================== */
  function dtr(d){return d*Math.PI/180;}
  function rtd(r){return r*180/Math.PI;}
  function dsin(d){return Math.sin(dtr(d));}
  function dcos(d){return Math.cos(dtr(d));}
  function dtan(d){return Math.tan(dtr(d));}
  function darcsin(x){return rtd(Math.asin(x));}
  function darccos(x){return rtd(Math.acos(x));}
  function darctan2(y,x){return rtd(Math.atan2(y,x));}
  function darccot(x){return rtd(Math.atan2(1,x));}
  function fixAngle(a){a=a-360*Math.floor(a/360); return a<0?a+360:a;}
  function fixHour(h){h=h-24*Math.floor(h/24); return h<0?h+24:h;}

  function julianDate(y,m,d){
    if(m<=2){y-=1;m+=12;}
    const A=Math.floor(y/100), B=2-A+Math.floor(A/4);
    return Math.floor(365.25*(y+4716))+Math.floor(30.6001*(m+1))+d+B-1524.5;
  }
  function sunPosition(jd){
    const D=jd-2451545.0;
    const g=fixAngle(357.529+0.98560028*D);
    const q=fixAngle(280.459+0.98564736*D);
    const L=fixAngle(q+1.915*dsin(g)+0.020*dsin(2*g));
    const e=23.439-0.00000036*D;
    const RA=darctan2(dcos(e)*dsin(L), dcos(L))/15;
    const eqt=q/15-fixHour(RA);
    const decl=darcsin(dsin(e)*dsin(L));
    return {decl, eqt};
  }
  function midDay(jd,time){ return fixHour(12 - sunPosition(jd+time).eqt); }
  function sunAngleTime(jd,time,angle,lat,dir){
    const decl=sunPosition(jd+time).decl;
    const noon=midDay(jd,time);
    const num=-dsin(angle)-dsin(decl)*dsin(lat);
    const den=dcos(decl)*dcos(lat);
    const ratio = num/den;
    if(ratio < -1 || ratio > 1) return null; // sun never reaches this angle (high latitude summer/winter)
    const t=1/15*darccos(ratio);
    return noon+(dir==='ccw'?-t:t);
  }
  function asrTime(jd,time,lat,factor){
    const decl=sunPosition(jd+time).decl;
    const angle=-darccot(factor+dtan(Math.abs(lat-decl)));
    return sunAngleTime(jd,time,angle,lat,'cw');
  }

  function computePrayerTimes(lat,lng,tzOffset,y,m,d,method,asrFactor){
    const cfg = METHODS[method] || METHODS.mwl;
    const jd = julianDate(y,m,d) - lng/(15*24);
    let fajr = sunAngleTime(jd,5/24,cfg.fajr,lat,'ccw');
    let sunrise = sunAngleTime(jd,6/24,0.833,lat,'ccw');
    let dhuhr = midDay(jd,12/24);
    let asr = asrTime(jd,13/24,lat,asrFactor);
    let maghrib = sunAngleTime(jd,18/24,0.833,lat,'cw');
    let isha;
    if(cfg.ishaMinutes){ isha = maghrib===null? null : maghrib + cfg.ishaMinutes/60; }
    else isha = sunAngleTime(jd,18/24,cfg.isha,lat,'cw');

    // high-latitude fallback: seventh-of-night rule if sun angle unreachable
    if(fajr===null || isha===null || sunrise===null || maghrib===null){
      const nightLen = sunrise!==null && maghrib!==null ? (24-(maghrib-sunrise)) : 8;
      if(sunrise!==null && fajr===null) fajr = fixHour(sunrise - nightLen/7);
      if(maghrib!==null && isha===null) isha = fixHour(maghrib + nightLen/7);
      if(fajr===null) fajr = fixHour(dhuhr - 6);
      if(isha===null) isha = fixHour(dhuhr + 6);
      if(sunrise===null) sunrise = fixHour(fajr + 1.5);
      if(maghrib===null) maghrib = fixHour(isha - 1.5);
    }

    const raw = {fajr,sunrise,dhuhr,asr,maghrib,isha};
    const out = {};
    for(const k in raw) out[k] = fixHour(raw[k] + tzOffset - lng/15);
    return out;
  }

  function hoursToDate(baseDate, hourVal){
    const d = new Date(baseDate);
    d.setHours(0,0,0,0);
    d.setMinutes(Math.round(hourVal*60));
    return d;
  }
  function fmtTime(hourVal){
    const h = Math.floor(hourVal); let m = Math.round((hourVal-h)*60);
    let hh=h, mm=m; if(mm===60){mm=0; hh+=1;}
    hh = ((hh%24)+24)%24;
    const ampm = hh>=12?'PM':'AM'; let h12=hh%12; if(h12===0)h12=12;
    return `${h12}:${mm.toString().padStart(2,'0')} ${ampm}`;
  }

  /* ===================== HIJRI CALENDAR ===================== */
  const HIJRI_MONTHS = ["Muharram","Safar","Rabi al-Awwal","Rabi al-Thani","Jumada al-Awwal","Jumada al-Thani","Rajab","Sha'ban","Ramadan","Shawwal","Dhu al-Qa'dah","Dhu al-Hijjah"];
  function gregorianToJDN(y,m,d){
    const a=Math.floor((14-m)/12), y2=y+4800-a, m2=m+12*a-3;
    return d+Math.floor((153*m2+2)/5)+365*y2+Math.floor(y2/4)-Math.floor(y2/100)+Math.floor(y2/400)-32045;
  }
  function jdnToHijri(jdn){
    jdn = jdn - 1948440 + 10632;
    let n = Math.floor((jdn-1)/10631);
    jdn = jdn - 10631*n + 354;
    let j = (Math.floor((10985-jdn)/5316))*(Math.floor((50*jdn)/17719)) + (Math.floor(jdn/5670))*(Math.floor((43*jdn)/15238));
    jdn = jdn - (Math.floor((30-j)/15))*(Math.floor((17719*j)/50)) - (Math.floor(j/16))*(Math.floor((15238*j)/43)) + 29;
    let month = Math.floor((24*jdn)/709);
    let day = jdn - Math.floor((709*month)/24);
    let year = 30*n + j - 30;
    return {year, month, day};
  }
  function hijriToJDN(y,m,d){
    return d + Math.ceil(29.5*(m-1)) + (y-1)*354 + Math.floor((3+11*y)/30) + 1948440 - 385;
  }
  function jdnToGregorian(jdn){
    let a = jdn + 32044, b = Math.floor((4*a+3)/146097), c = a - Math.floor((146097*b)/4);
    let d2 = Math.floor((4*c+3)/1461), e = c - Math.floor((1461*d2)/4), m2 = Math.floor((5*e+2)/153);
    const day = e - Math.floor((153*m2+2)/5) + 1;
    const month = m2 + 3 - 12*Math.floor(m2/10);
    const year = 100*b + d2 - 4800 + Math.floor(m2/10);
    return {year, month, day};
  }

  /* ===================== PERSISTENCE ===================== */
  async function loadPersisted(){
    try{
      const r = await window.storage.get('deen-settings');
      if(r && r.value){
        const s = JSON.parse(r.value);
        Object.assign(state, s);
      }
    }catch(e){ /* no saved settings yet */ }
    try{
      const r2 = await window.storage.get('deen-tasbih-counts');
      if(r2 && r2.value) state.tasbihCounts = JSON.parse(r2.value);
    }catch(e){ /* none yet */ }
  }
  async function savePersisted(){
    try{
      await window.storage.set('deen-settings', JSON.stringify({
        lat: state.lat, lng: state.lng, locName: state.locName,
        calcMethod: state.calcMethod, asrMethod: state.asrMethod, alertsOn: state.alertsOn,
        theme: state.theme, lang: state.lang, profileName: state.profileName
      }));
    }catch(e){}
  }
  async function saveTasbih(){
    try{ await window.storage.set('deen-tasbih-counts', JSON.stringify(state.tasbihCounts)); }catch(e){}
  }

  /* ===================== GEOLOCATION ===================== */
  function locate(){
    document.getElementById('locLabel').textContent = t('locating');
    if(!navigator.geolocation){ finishLocate(state.lat,state.lng,'Location unavailable'); return; }
    navigator.geolocation.getCurrentPosition(
      pos=>{
        finishLocate(pos.coords.latitude, pos.coords.longitude, null);
        reverseGeocodeLabel(pos.coords.latitude, pos.coords.longitude);
      },
      err=>{ finishLocate(state.lat, state.lng, state.locName || 'Location unavailable'); },
      { timeout:8000 }
    );
  }
  function finishLocate(lat,lng,label){
    state.lat=lat; state.lng=lng;
    if(label) state.locName = label;
    document.getElementById('locLabel').textContent = state.locName || 'Somewhere on Earth';
    savePersisted();
    refreshPrayerTimes();
    updateQibla();
  }
  async function reverseGeocodeLabel(lat,lng){
    try{
      const res = await fetch(`https://nominatim.openstreetmap.org/reverse?format=json&lat=${lat}&lon=${lng}&zoom=10`);
      const data = await res.json();
      const a = data.address || {};
      const label = a.city || a.town || a.village || a.county || a.state || 'Your location';
      state.locName = label;
      document.getElementById('locLabel').textContent = label;
      savePersisted();
    }catch(e){ /* keep coordinates-based label */ }
  }

  /* ===================== PRAYER TIMES / HOME VIEW ===================== */
  function refreshPrayerTimes(){
    const now = new Date();
    const tzOffset = -now.getTimezoneOffset()/60;
    state.prayerDate = now;
    state.prayerTimes = computePrayerTimes(state.lat, state.lng, tzOffset, now.getFullYear(), now.getMonth()+1, now.getDate(), state.calcMethod, state.asrMethod);
    renderPrayerList();
    renderDayArc();
    updateCountdown();
    renderHeaderDate();
  }

  const PRAYER_ORDER = ['fajr','sunrise','dhuhr','asr','maghrib','isha'];
  function prayerLabel(k){ return t(k); }

  function currentHourDecimal(){
    const n = new Date();
    return n.getHours() + n.getMinutes()/60 + n.getSeconds()/3600;
  }

  function getNextPrayer(){
    const pt = state.prayerTimes; if(!pt) return null;
    const now = currentHourDecimal();
    const order = ['fajr','dhuhr','asr','maghrib','isha']; // sunrise excluded from "next prayer" targeting
    for(const k of order){ if(pt[k] > now) return k; }
    return 'fajr'; // next day
  }

  function renderPrayerList(){
    const pt = state.prayerTimes; if(!pt) return;
    const next = getNextPrayer();
    const el = document.getElementById('prayerList');
    el.innerHTML = PRAYER_ORDER.map(k=>{
      const active = k===next;
      return `<div class="prayer-row ${active?'active':''}"><div class="name"><span class="dot"></span>${prayerLabel(k)}</div><div class="time mono">${fmtTime(pt[k])}</div></div>`;
    }).join('');
  }

  function todayKey(){
    const n = new Date();
    return `${n.getFullYear()}-${String(n.getMonth()+1).padStart(2,'0')}-${String(n.getDate()).padStart(2,'0')}`;
  }

  function updateCountdown(){
    const pt = state.prayerTimes; if(!pt) return;
    const next = getNextPrayer();
    document.getElementById('nextPrayerName').textContent = prayerLabel(next);
    const now = currentHourDecimal();
    let target = pt[next];
    let diff = target - now;
    if(diff <= 0) diff += 24;
    const totalSec = Math.round(diff*3600);
    const hh = Math.floor(totalSec/3600), mm = Math.floor((totalSec%3600)/60), ss = totalSec%60;
    document.getElementById('countdown').textContent = `${hh.toString().padStart(2,'0')}:${mm.toString().padStart(2,'0')}:${ss.toString().padStart(2,'0')}`;
    document.getElementById('countdownSub').textContent = `${t('untilNext')} · ${prayerLabel(next)}`;

    const nowDate = new Date();
    document.getElementById('liveClock').textContent = nowDate.toLocaleTimeString(undefined, {hour:'2-digit', minute:'2-digit', second:'2-digit'}) + ' · ' + (state.locName||'');

    // alert + 30-min-after prayer-check, once per minute
    const dKey = todayKey();
    for(const k of ['fajr','dhuhr','asr','maghrib','isha']){
      const kt = pt[k];
      const nowMin = Math.round(now*60), ktMin = Math.round(kt*60);
      if(state.alertsOn && nowMin === ktMin){
        const key = `${dKey}-${k}`;
        if(state.lastAlertMinute !== key){
          state.lastAlertMinute = key;
          fireAlert(prayerLabel(k));
        }
      }
      // 30 minutes after prayer start: ask if it was prayed
      const promptMin = ktMin + 30;
      if(nowMin === promptMin){
        const sessionKey = `${dKey}-${k}`;
        const already = state.prayerLog[dKey] && state.prayerLog[dKey][k];
        if(!state.promptedThisSession.has(sessionKey) && !already){
          state.promptedThisSession.add(sessionKey);
          showPrayerPrompt(k, dKey);
        }
      }
    }
  }

  function fireAlert(name){
    try{
      if(Notification && Notification.permission === 'granted'){
        new Notification(`${name} time`, { body: `It's time for ${name} prayer.` });
      }
    }catch(e){}
    playChime();
  }
  function playChime(){
    // A melodic tone sequence stands in for a real Adhan recitation — we can't embed an
    // actual reciter's audio here for rights reasons, so this is a gentle synthesized call instead.
    try{
      const ctx = new (window.AudioContext||window.webkitAudioContext)();
      const notes = [660, 780, 660, 550, 660, 440];
      notes.forEach((freq,i)=>{
        const o = ctx.createOscillator(), g = ctx.createGain();
        o.frequency.value = freq; o.type='sine';
        o.connect(g); g.connect(ctx.destination);
        const start = ctx.currentTime + i*0.42;
        g.gain.setValueAtTime(0, start);
        g.gain.linearRampToValueAtTime(0.16, start+0.06);
        g.gain.exponentialRampToValueAtTime(0.001, start+0.75);
        o.start(start); o.stop(start+0.8);
      });
    }catch(e){}
  }

  /* ---- prayer-check prompt (asks 30 min after a prayer starts) ---- */
  function showPrayerPrompt(prayerKey, dKey){
    state.pendingPrompt = { prayer: prayerKey, date: dKey };
    document.getElementById('promptTitle').textContent = `${t('didYouPray')} ${prayerLabel(prayerKey)}?`;
    document.getElementById('promptModal').classList.add('open');
    try{
      if(Notification && Notification.permission === 'granted'){
        new Notification(`${prayerLabel(prayerKey)}?`, { body: `${t('didYouPray')} ${prayerLabel(prayerKey)}?` });
      }
    }catch(e){}
  }
  function answerPrompt(answer){
    const p = state.pendingPrompt; if(!p) return;
    if(!state.prayerLog[p.date]) state.prayerLog[p.date] = {};
    state.prayerLog[p.date][p.prayer] = answer;
    savePrayerLog();
    document.getElementById('promptModal').classList.remove('open');
    state.pendingPrompt = null;
    renderTrackChecklist(); renderMonthStats();
  }
  document.getElementById('promptYes').addEventListener('click', ()=> answerPrompt('yes'));
  document.getElementById('promptNo').addEventListener('click', ()=> answerPrompt('no'));

  async function savePrayerLog(){
    try{ await window.storage.set('deen-prayer-log', JSON.stringify(state.prayerLog)); }catch(e){}
  }
  async function loadPrayerLog(){
    try{
      const r = await window.storage.get('deen-prayer-log');
      if(r && r.value) state.prayerLog = JSON.parse(r.value);
    }catch(e){}
  }

  function renderTrackChecklist(){
    const dKey = todayKey();
    const dayLog = state.prayerLog[dKey] || {};
    const el = document.getElementById('trackChecklist');
    if(!el) return;
    el.innerHTML = ['fajr','dhuhr','asr','maghrib','isha'].map(k=>{
      const val = dayLog[k] || null;
      return `<div class="track-row"><div class="track-name">${prayerLabel(k)}</div>
        <div class="yn-btns">
          <button class="yn-btn no ${val==='no'?'active':''}" data-k="${k}" data-v="no">${t('notYet')}</button>
          <button class="yn-btn yes ${val==='yes'?'active':''}" data-k="${k}" data-v="yes">${t('prayed')}</button>
        </div></div>`;
    }).join('');
    el.querySelectorAll('.yn-btn').forEach(btn=>{
      btn.addEventListener('click', ()=>{
        if(!state.prayerLog[dKey]) state.prayerLog[dKey] = {};
        state.prayerLog[dKey][btn.dataset.k] = btn.dataset.v;
        savePrayerLog();
        renderTrackChecklist();
        renderMonthStats();
      });
    });
  }
  function renderMonthStats(){
    const now = new Date();
    const prefix = `${now.getFullYear()}-${String(now.getMonth()+1).padStart(2,'0')}`;
    let possible = 0, prayed = 0;
    for(let d=1; d<=now.getDate(); d++){
      const key = `${prefix}-${String(d).padStart(2,'0')}`;
      const dayLog = state.prayerLog[key] || {};
      for(const k of ['fajr','dhuhr','asr','maghrib','isha']){
        possible += 1;
        if(dayLog[k]==='yes') prayed += 1;
      }
    }
    const pct = possible ? Math.round((prayed/possible)*100) : 0;
    const label = document.getElementById('monthStatLabel');
    const fill = document.getElementById('monthFill');
    if(label) label.textContent = `${prayed}/${possible} ${t('monthProgress')} (${pct}%)`;
    if(fill) fill.style.width = pct+'%';
  }

  function renderHeaderDate(){
    const now = new Date();
    const jdn = gregorianToJDN(now.getFullYear(), now.getMonth()+1, now.getDate());
    const h = jdnToHijri(jdn);
    document.getElementById('hijriDate').textContent = `${h.day} ${HIJRI_MONTHS[h.month-1]} ${h.year} AH`;
  }


  function renderDayArc(){
    const pt = state.prayerTimes; if(!pt) return;
    const w=440, hgt=150, pad=26;
    const start = pt.fajr, end = pt.isha;
    let span = end - start; if(span<=0) span += 24;
    function xFor(hourVal){
      let rel = hourVal - start; if(rel<0) rel+=24;
      const frac = Math.min(Math.max(rel/span,0),1);
      return pad + frac*(w-2*pad);
    }
    function yFor(x){
      const frac = (x-pad)/(w-2*pad);
      return hgt-30 - Math.sin(frac*Math.PI)*70;
    }
    const points = ['fajr','dhuhr','asr','maghrib','isha'];
    const next = getNextPrayer();
    let path = `M ${pad} ${hgt-30}`;
    for(let x=pad; x<=w-pad; x+=8){ path += ` L ${x.toFixed(1)} ${yFor(x).toFixed(1)}`; }

    const nowX = xFor(currentHourDecimal());
    const nowY = yFor(nowX);

    let dots = points.map(k=>{
      const x = xFor(pt[k]); const y = yFor(x);
      const active = k===next;
      return `<circle cx="${x.toFixed(1)}" cy="${y.toFixed(1)}" r="${active?6:4}" fill="${active?'var(--accent)':'#B9C2BC'}" stroke="var(--bg)" stroke-width="2"/>
              <text x="${x.toFixed(1)}" y="${(hgt-6).toFixed(1)}" text-anchor="middle" class="arc-label ${active?'arc-label-active':''}">${prayerLabel(k)}</text>`;
    }).join('');

    document.getElementById('dayArc').innerHTML = `
      <svg viewBox="0 0 ${w} ${hgt}" xmlns="http://www.w3.org/2000/svg">
        <path d="${path}" fill="none" stroke="#DDE3DC" stroke-width="2"/>
        <circle cx="${nowX.toFixed(1)}" cy="${nowY.toFixed(1)}" r="7" fill="#14342B"/>
        <circle cx="${nowX.toFixed(1)}" cy="${nowY.toFixed(1)}" r="11" fill="#14342B" opacity="0.15"/>
        ${dots}
      </svg>`;
  }

  /* ===================== QIBLA ===================== */
  const KAABA = { lat: 21.4225, lng: 39.8262 };
  function qiblaBearing(lat,lng){
    const phiK=dtr(KAABA.lat), lambdaK=dtr(KAABA.lng), phi=dtr(lat), lambda=dtr(lng);
    const y = Math.sin(lambdaK-lambda);
    const x = Math.cos(phi)*Math.tan(phiK) - Math.sin(phi)*Math.cos(lambdaK-lambda);
    let brng = rtd(Math.atan2(y,x));
    return (brng+360)%360;
  }
  function haversineKm(lat1,lng1,lat2,lng2){
    const R=6371, dLat=dtr(lat2-lat1), dLng=dtr(lng2-lng1);
    const a = Math.sin(dLat/2)**2 + Math.cos(dtr(lat1))*Math.cos(dtr(lat2))*Math.sin(dLng/2)**2;
    return R*2*Math.atan2(Math.sqrt(a), Math.sqrt(1-a));
  }
  let deviceHeading = null;
  function updateQibla(){
    const bearing = qiblaBearing(state.lat, state.lng);
    const dist = haversineKm(state.lat, state.lng, KAABA.lat, KAABA.lng);
    document.getElementById('qiblaDist').textContent = `${Math.round(dist).toLocaleString()} km ${t('toMecca')}`;
    const needleRotation = deviceHeading===null ? bearing : (bearing - deviceHeading + 360)%360;
    document.getElementById('qiblaDeg').textContent = `${Math.round(bearing)}°`;
    drawCompass(needleRotation, deviceHeading!==null);
  }
  function drawCompass(rot, live){
    const svg = document.getElementById('compassSvg');
    svg.innerHTML = `
      <circle cx="130" cy="130" r="118" fill="var(--surface)" stroke="var(--border)" stroke-width="1.5"/>
      <circle cx="130" cy="130" r="96" fill="none" stroke="var(--border)" stroke-width="1"/>
      <text x="130" y="24" text-anchor="middle" font-size="13" fill="var(--ink-soft)" font-family="Inter">N</text>
      <text x="130" y="246" text-anchor="middle" font-size="13" fill="var(--ink-soft)" font-family="Inter">S</text>
      <text x="16" y="135" text-anchor="middle" font-size="13" fill="var(--ink-soft)" font-family="Inter">W</text>
      <text x="244" y="135" text-anchor="middle" font-size="13" fill="var(--ink-soft)" font-family="Inter">E</text>
      <g transform="rotate(${rot} 130 130)">
        <path d="M 130 34 L 118 140 L 130 128 L 142 140 Z" fill="var(--accent)"/>
        <path d="M 130 226 L 122 150 L 130 158 L 138 150 Z" fill="#C7CFC9"/>
      </g>
      <circle cx="130" cy="130" r="5" fill="var(--ink)"/>
    `;
  }
  function initCompassPermission(){
    const btn = document.getElementById('compassPermBtn');
    if(typeof DeviceOrientationEvent !== 'undefined' && typeof DeviceOrientationEvent.requestPermission === 'function'){
      btn.style.display='block';
      btn.onclick = async ()=>{
        try{
          const res = await DeviceOrientationEvent.requestPermission();
          if(res==='granted'){ attachOrientation(); btn.style.display='none'; }
        }catch(e){}
      };
    } else if('ondeviceorientationabsolute' in window || 'ondeviceorientation' in window){
      attachOrientation();
      btn.style.display='none';
    } else {
      btn.style.display='none';
    }
  }
  function attachOrientation(){
    window.addEventListener('deviceorientationabsolute', handleOrientation, true);
    window.addEventListener('deviceorientation', handleOrientation, true);
  }
  function handleOrientation(e){
    let heading = e.webkitCompassHeading!==undefined ? e.webkitCompassHeading : (e.absolute ? 360 - e.alpha : null);
    if(heading===null || isNaN(heading)) return;
    deviceHeading = heading;
    updateQibla();
  }

  /* ===================== QURAN ===================== */
  let surahCache = null;
  async function loadSurahList(){
    const container = document.getElementById('surahListInner');
    try{
      const res = await fetch('https://api.alquran.cloud/v1/surah');
      const data = await res.json();
      surahCache = data.data;
      renderSurahList(surahCache);
    }catch(e){
      container.innerHTML = `<div class="empty-state">Couldn't load the surah list. Check your connection and reopen the Qur'an tab.</div>`;
    }
  }
  function renderSurahList(list){
    const container = document.getElementById('surahListInner');
    container.innerHTML = list.map(s=>`
      <div class="surah-row" data-num="${s.number}">
        <div class="surah-num">${s.number}</div>
        <div style="flex:1;">
          <div class="surah-en">${s.englishName}</div>
          <div class="surah-meta">${s.englishNameTranslation} · ${s.numberOfAyahs} verses</div>
        </div>
        <div class="surah-ar">${s.name}</div>
      </div>`).join('');
    container.querySelectorAll('.surah-row').forEach(row=>{
      row.addEventListener('click', ()=> openSurah(parseInt(row.dataset.num)));
    });
  }
  document.getElementById('surahSearch').addEventListener('input', (e)=>{
    if(!surahCache) return;
    const q = e.target.value.toLowerCase();
    renderSurahList(surahCache.filter(s=> s.englishName.toLowerCase().includes(q) || s.englishNameTranslation.toLowerCase().includes(q) || String(s.number)===q));
  });

  async function openSurah(num){
    document.getElementById('quranList').style.display='none';
    const reader = document.getElementById('quranReader');
    reader.style.display='block';
    reader.innerHTML = `<button class="back-btn" id="backToList">‹ ${t('allSurahs')}</button><div class="empty-state"><span class="loading-dot"></span><span class="loading-dot"></span><span class="loading-dot"></span></div>`;
    document.getElementById('backToList').onclick = ()=>{ reader.style.display='none'; document.getElementById('quranList').style.display='block'; };
    try{
      const res = await fetch(`https://api.alquran.cloud/v1/surah/${num}/editions/quran-uthmani,en.sahih`);
      const data = await res.json();
      const arabic = data.data[0].ayahs, translation = data.data[1].ayahs;
      const meta = data.data[0];
      let html = `<button class="back-btn" id="backToList2">‹ ${t('allSurahs')}</button>
        <h3 class="serif" style="font-size:20px; margin-bottom:2px;">${meta.englishName} <span style="color:var(--ink-soft); font-weight:400; font-size:14px;">· ${meta.englishNameTranslation}</span></h3>`;
      for(let i=0;i<arabic.length;i++){
        html += `<div class="ayah"><span class="num-chip">${arabic[i].numberInSurah}</span>
          <div class="arabic">${arabic[i].text}</div>
          <div class="translation">${translation[i].text}</div></div>`;
      }
      reader.innerHTML = html;
      document.getElementById('backToList2').onclick = ()=>{ reader.style.display='none'; document.getElementById('quranList').style.display='block'; };
    }catch(e){
      reader.innerHTML = `<button class="back-btn" id="backToList3">‹ ${t('allSurahs')}</button><div class="empty-state">Couldn't load this surah. Check your connection and try again.</div>`;
      document.getElementById('backToList3').onclick = ()=>{ reader.style.display='none'; document.getElementById('quranList').style.display='block'; };
    }
  }

  /* ===================== TASBIH ===================== */
  const DHIKR_LIST = ['SubhanAllah','Alhamdulillah','Allahu Akbar','La ilaha illallah','Astaghfirullah'];
  function renderDhikrChips(){
    const el = document.getElementById('dhikrChips');
    el.innerHTML = DHIKR_LIST.map(d=>`<button class="chip ${d===state.tasbihDhikr?'active':''}" data-d="${d}">${d}</button>`).join('');
    el.querySelectorAll('.chip').forEach(c=>{
      c.addEventListener('click', ()=>{ state.tasbihDhikr = c.dataset.d; renderDhikrChips(); renderTasbihCount(); });
    });
  }
  function renderTasbihCount(){
    const count = state.tasbihCounts[state.tasbihDhikr] || 0;
    document.getElementById('tasbihCount').textContent = count;
    document.getElementById('tasbihTarget').textContent = `target ${state.tasbihTarget}`;
  }
  document.getElementById('tasbihBtn').addEventListener('click', ()=>{
    const cur = (state.tasbihCounts[state.tasbihDhikr]||0) + 1;
    state.tasbihCounts[state.tasbihDhikr] = cur;
    renderTasbihCount();
    if(navigator.vibrate) navigator.vibrate(cur % state.tasbihTarget === 0 ? [30,40,30] : 12);
    saveTasbih();
  });
  document.getElementById('tasbihReset').addEventListener('click', ()=>{
    state.tasbihCounts[state.tasbihDhikr] = 0; renderTasbihCount(); saveTasbih();
  });
  document.getElementById('tasbihTargetBtn').addEventListener('click', ()=>{
    const options = [33,99,100];
    const idx = options.indexOf(state.tasbihTarget);
    state.tasbihTarget = options[(idx+1)%options.length];
    renderTasbihCount();
  });

  /* ===================== CALENDAR VIEW ===================== */
  function initCalendar(){
    const now = new Date();
    const jdn = gregorianToJDN(now.getFullYear(), now.getMonth()+1, now.getDate());
    const h = jdnToHijri(jdn);
    state.calYear = h.year; state.calMonth = h.month;
    document.getElementById('calTodayHijri').textContent = `${h.day} ${HIJRI_MONTHS[h.month-1]} ${h.year} AH`;
    document.getElementById('calTodayGreg').textContent = now.toLocaleDateString(undefined, {weekday:'long', year:'numeric', month:'long', day:'numeric'});
    renderCalendarMonth();
    renderTrackChecklist();
    renderMonthStats();
  }
  function renderCalendarMonth(){
    document.getElementById('calMonthTitle').textContent = `${HIJRI_MONTHS[state.calMonth-1]} ${state.calYear}`;
    const firstJdn = hijriToJDN(state.calYear, state.calMonth, 1);
    const daysInMonth = hijriToJDN(state.calMonth===12?state.calYear+1:state.calYear, state.calMonth===12?1:state.calMonth+1, 1) - firstJdn;
    const firstGreg = jdnToGregorian(firstJdn);
    const firstDow = new Date(firstGreg.year, firstGreg.month-1, firstGreg.day).getDay(); // 0=Sun

    const todayJdn = gregorianToJDN(new Date().getFullYear(), new Date().getMonth()+1, new Date().getDate());

    let html = ['S','M','T','W','T','F','S'].map(d=>`<div class="cal-dow">${d}</div>`).join('');
    for(let i=0;i<firstDow;i++) html += `<div class="cal-day empty"></div>`;
    for(let day=1; day<=daysInMonth; day++){
      const jdn = firstJdn + day - 1;
      const g = jdnToGregorian(jdn);
      const dow = new Date(g.year,g.month-1,g.day).getDay();
      const isToday = jdn===todayJdn;
      const isFriday = dow===5;
      html += `<div class="cal-day ${isToday?'today':''} ${isFriday?'friday':''}">
        <div>${day}</div><div class="g">${g.month}/${g.day}</div></div>`;
    }
    document.getElementById('calGrid').innerHTML = html;
  }
  document.getElementById('calPrev').addEventListener('click', ()=>{
    state.calMonth -= 1; if(state.calMonth<1){ state.calMonth=12; state.calYear-=1; }
    renderCalendarMonth();
  });
  document.getElementById('calNext').addEventListener('click', ()=>{
    state.calMonth += 1; if(state.calMonth>12){ state.calMonth=1; state.calYear+=1; }
    renderCalendarMonth();
  });

  /* ===================== NAV / TABS ===================== */
  document.querySelectorAll('.tab-btn').forEach(btn=>{
    btn.addEventListener('click', ()=>{
      document.querySelectorAll('.tab-btn').forEach(b=>b.classList.remove('active'));
      btn.classList.add('active');
      document.querySelectorAll('.view').forEach(v=>v.classList.remove('active'));
      document.getElementById('view-'+btn.dataset.view).classList.add('active');
      if(btn.dataset.view==='qibla') updateQibla();
    });
  });

  /* ===================== SETTINGS MODAL ===================== */
  const settingsModal = document.getElementById('settingsModal');
  document.getElementById('settingsBtn').addEventListener('click', ()=>{
    document.getElementById('alertToggle').checked = state.alertsOn;
    document.getElementById('calcMethod').value = state.calcMethod;
    document.getElementById('asrMethod').value = String(state.asrMethod);
    document.getElementById('profileInput').value = state.profileName || '';
    updateThemeLangButtons();
    settingsModal.classList.add('open');
  });
  document.getElementById('closeSettings').addEventListener('click', ()=> settingsModal.classList.remove('open'));
  settingsModal.addEventListener('click', (e)=>{ if(e.target===settingsModal) settingsModal.classList.remove('open'); });
  document.getElementById('alertToggle').addEventListener('change', async (e)=>{
    if(e.target.checked && 'Notification' in window && Notification.permission === 'default'){
      await Notification.requestPermission();
    }
    state.alertsOn = e.target.checked;
    savePersisted();
  });
  document.getElementById('calcMethod').addEventListener('change', (e)=>{
    state.calcMethod = e.target.value; savePersisted(); refreshPrayerTimes();
  });
  document.getElementById('asrMethod').addEventListener('change', (e)=>{
    state.asrMethod = parseInt(e.target.value); savePersisted(); refreshPrayerTimes();
  });
  document.getElementById('relocateBtn').addEventListener('click', ()=>{ locate(); settingsModal.classList.remove('open'); });

  /* ---- theme ---- */
  function updateThemeLangButtons(){
    document.getElementById('themeLightBtn').classList.toggle('active', state.theme==='light');
    document.getElementById('themeDarkBtn').classList.toggle('active', state.theme==='dark');
    document.getElementById('langEnBtn').classList.toggle('active', state.lang==='en');
    document.getElementById('langUrBtn').classList.toggle('active', state.lang==='ur');
  }
  function applyTheme(){
    document.documentElement.dataset.theme = state.theme;
  }
  document.getElementById('themeLightBtn').addEventListener('click', ()=>{ state.theme='light'; applyTheme(); updateThemeLangButtons(); savePersisted(); });
  document.getElementById('themeDarkBtn').addEventListener('click', ()=>{ state.theme='dark'; applyTheme(); updateThemeLangButtons(); savePersisted(); });

  /* ---- language ---- */
  function applyLanguage(){
    document.documentElement.lang = state.lang;
    document.documentElement.dir = state.lang==='ur' ? 'rtl' : 'ltr';
    document.body.classList.toggle('lang-ur', state.lang==='ur');
    document.querySelectorAll('[data-i18n]').forEach(el=>{ el.textContent = t(el.dataset.i18n); });
    document.querySelectorAll('[data-i18n-placeholder]').forEach(el=>{ el.placeholder = t(el.dataset.i18nPlaceholder); });
    renderPrayerList(); renderDayArc(); renderHeaderDate(); updateQibla();
    renderTrackChecklist(); renderMonthStats();
  }
  document.getElementById('langEnBtn').addEventListener('click', ()=>{ state.lang='en'; applyLanguage(); updateThemeLangButtons(); savePersisted(); });
  document.getElementById('langUrBtn').addEventListener('click', ()=>{ state.lang='ur'; applyLanguage(); updateThemeLangButtons(); savePersisted(); });

  /* ---- profile ---- */
  document.getElementById('profileInput').addEventListener('change', (e)=>{ state.profileName = e.target.value.trim(); savePersisted(); });

  /* ---- about ---- */
  const aboutModal = document.getElementById('aboutModal');
  document.getElementById('aboutBtn').addEventListener('click', ()=>{
    document.getElementById('aboutText').innerHTML = `<p>${t('aboutBody')}</p><div class="about-signature">— Muhammad Abdullah bin Farooq</div>`;
    document.getElementById('aboutText').classList.toggle('lang-ur', state.lang==='ur');
    aboutModal.classList.add('open');
  });
  document.getElementById('closeAbout').addEventListener('click', ()=> aboutModal.classList.remove('open'));
  aboutModal.addEventListener('click', (e)=>{ if(e.target===aboutModal) aboutModal.classList.remove('open'); });

  /* ===================== INIT ===================== */
  async function init(){
    await loadPersisted();
    await loadPrayerLog();
    applyTheme();
    applyLanguage();
    document.getElementById('locLabel').textContent = state.locName || t('locating');
    renderHeaderDate();
    refreshPrayerTimes();
    updateQibla();
    initCompassPermission();
    renderDhikrChips();
    renderTasbihCount();
    initCalendar();
    loadSurahList();
    locate(); // attempt live geolocation, overrides fallback on success

    setInterval(()=>{ updateCountdown(); }, 1000);
    setInterval(()=>{ refreshPrayerTimes(); }, 60000);
  }
  init();
})();
</script>
</body>
</html>
