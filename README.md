[index (1).html](https://github.com/user-attachments/files/29508530/index.1.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Alberto Hilario — Data &amp; Customer Experience</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=Source+Serif+4:opsz,wght@8..60,400;8..60,600;8..60,700&display=swap');

  :root{
    --bg:#0B0F14;
    --panel:#121822;
    --panel-2:#161E2B;
    --line:#222C3C;
    --text:#E7ECF3;
    --muted:#8A97AC;
    --amber:#E8A33D;
    --cyan:#6FD6C7;
    --rose:#E0707A;
    --mono: 'JetBrains Mono', ui-monospace, SFMono-Regular, Menlo, monospace;
    --serif: 'Source Serif 4', Georgia, serif;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--bg);
    color:var(--text);
    font-family:var(--mono);
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  a{color:inherit;}
  ::selection{background:var(--amber); color:#0B0F14;}

  .wrap{max-width:880px; margin:0 auto; padding:0 24px;}

  /* ---------- NAV ---------- */
  nav{
    position:sticky; top:0; z-index:20;
    background:rgba(11,15,20,0.88);
    backdrop-filter: blur(8px);
    border-bottom:1px solid var(--line);
  }
  nav .wrap{display:flex; align-items:center; justify-content:space-between; padding:14px 24px;}
  .brand{font-weight:700; letter-spacing:0.02em; font-size:14px; color:var(--text); text-decoration:none;}
  .brand span{color:var(--amber);}
  .navlinks{display:flex; gap:22px; font-size:13px; color:var(--muted);}
  .navlinks a{text-decoration:none; transition:color .15s;}
  .navlinks a:hover{color:var(--cyan);}

  /* ---------- HERO ---------- */
  header.hero{padding:64px 0 40px; border-bottom:1px solid var(--line);}
  .query-block{
    background:var(--panel);
    border:1px solid var(--line);
    border-radius:8px;
    padding:22px 24px;
    font-size:13px;
    overflow-x:auto;
  }
  .q-kw{color:var(--rose);}
  .q-str{color:var(--cyan);}
  .q-com{color:var(--muted);}
  .q-num{color:var(--amber);}
  .cursor{display:inline-block; width:7px; height:14px; background:var(--amber); margin-left:2px; animation:blink 1s steps(1) infinite; vertical-align:-2px;}
  @keyframes blink{50%{opacity:0;}}

  .hero-name{
    font-family:var(--serif);
    font-size:clamp(34px, 6vw, 54px);
    font-weight:700;
    margin:28px 0 6px;
    letter-spacing:-0.01em;
  }
  .hero-role{color:var(--cyan); font-size:15px; margin-bottom:18px;}
  .hero-sub{color:var(--muted); font-size:14.5px; max-width:600px; margin-bottom:26px;}
  .hero-links{display:flex; flex-wrap:wrap; gap:10px;}
  .pill{
    display:inline-flex; align-items:center; gap:6px;
    border:1px solid var(--line); border-radius:999px;
    padding:8px 16px; font-size:12.5px; text-decoration:none; color:var(--text);
    transition:border-color .15s, color .15s, background .15s;
  }
  .pill:hover{border-color:var(--amber); color:var(--amber); background:rgba(232,163,61,0.06);}
  .pill.solid{background:var(--amber); color:#0B0F14; border-color:var(--amber); font-weight:700;}
  .pill.solid:hover{background:#f0b250; color:#0B0F14;}

  /* ---------- SECTION SHELL ---------- */
  section{padding:54px 0; border-bottom:1px solid var(--line);}
  .eyebrow{
    font-size:11px; letter-spacing:0.12em; text-transform:uppercase;
    color:var(--muted); margin-bottom:6px;
  }
  .eyebrow span{color:var(--amber);}
  h2.sec-title{
    font-family:var(--serif); font-size:26px; font-weight:600; margin:0 0 26px;
  }

  /* ---------- ABOUT ---------- */
  .about-grid{display:grid; grid-template-columns: 1.3fr 1fr; gap:36px;}
  .about-grid p{color:#C7CEDA; font-size:14.5px; margin:0 0 14px;}
  .stat-card{
    background:var(--panel); border:1px solid var(--line); border-radius:8px;
    padding:16px 18px; margin-bottom:12px;
  }
  .stat-num{font-family:var(--serif); color:var(--amber); font-size:22px; font-weight:700;}
  .stat-label{color:var(--muted); font-size:12px; margin-top:2px;}

  @media (max-width:720px){ .about-grid{grid-template-columns:1fr;} }

  /* ---------- SKILLS ---------- */
  .skill-row{display:flex; flex-wrap:wrap; gap:8px;}
  .tag{
    border:1px solid var(--line); border-radius:6px; padding:6px 12px;
    font-size:12.5px; color:var(--cyan); background:var(--panel);
  }

  /* ---------- PROJECTS ---------- */
  .proj{
    display:grid; grid-template-columns: 90px 1fr; gap:18px;
    padding:20px 0; border-top:1px solid var(--line);
  }
  .proj:first-of-type{border-top:none;}
  .proj-idx{color:var(--muted); font-size:12px; padding-top:3px;}
  .proj-title{font-family:var(--serif); font-size:18px; font-weight:600; margin:0 0 6px;}
  .proj-title a{text-decoration:none; border-bottom:1px solid transparent;}
  .proj-title a:hover{color:var(--amber); border-color:var(--amber);}
  .proj-desc{color:var(--muted); font-size:13.5px; margin:0 0 10px;}
  .proj-tags{display:flex; gap:6px; flex-wrap:wrap;}
  .proj-tags span{font-size:11px; color:var(--muted); border:1px solid var(--line); border-radius:4px; padding:3px 8px;}

  /* ---------- EXPERIENCE ---------- */
  .job{display:grid; grid-template-columns: 150px 1fr; gap:18px; padding:18px 0; border-top:1px solid var(--line);}
  .job:first-of-type{border-top:none;}
  .job-date{color:var(--muted); font-size:12px; padding-top:2px;}
  .job-title{font-weight:700; font-size:14px; margin:0 0 2px;}
  .job-org{color:var(--cyan); font-size:13px; margin-bottom:8px;}
  .job ul{margin:0; padding-left:18px; color:#C7CEDA; font-size:13px;}
  .job li{margin-bottom:5px;}

  @media (max-width:600px){
    .job{grid-template-columns:1fr;}
    .proj{grid-template-columns:1fr;}
  }

  /* ---------- FOOTER ---------- */
  footer{padding:40px 0; text-align:center;}
  footer .wrap{display:flex; flex-direction:column; align-items:center; gap:14px;}
  .footer-links{display:flex; gap:18px; font-size:13px;}
  .footer-links a{text-decoration:none; color:var(--muted);}
  .footer-links a:hover{color:var(--amber);}
  .footer-note{color:var(--muted); font-size:11.5px;}

  @media (prefers-reduced-motion: reduce){
    .cursor{animation:none;}
    html{scroll-behavior:auto;}
  }
</style>
</head>
<body>

<nav>
  <div class="wrap">
    <a class="brand" href="#top">bert<span>toe</span>.io</a>
    <div class="navlinks">
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#experience">Experience</a>
      <a href="#contact">Contact</a>
    </div>
  </div>
</nav>

<header class="hero" id="top">
  <div class="wrap">
    <div class="query-block">
<span class="q-kw">SELECT</span> name, role, location
<span class="q-kw">FROM</span> profile
<span class="q-kw">WHERE</span> focus <span class="q-kw">IN</span> (<span class="q-str">'data analytics'</span>, <span class="q-str">'customer experience'</span>)
<span class="q-com">-- 1 row returned</span><span class="cursor"></span>
    </div>

    <h1 class="hero-name">Alberto Hilario</h1>
    <div class="hero-role">Data Analytics &amp; Customer Experience — Brooklyn, NY</div>
    <p class="hero-sub">
      I turn high-volume customer environments into structured, measurable systems — and structured data
      into decisions. Google Data Analytics Certified, with six years across retail operations, CRM-driven
      sales, and guest services.
    </p>
    <div class="hero-links">
      <a class="pill solid" href="mailto:albertohilario101@gmail.com">Email me</a>
      <a class="pill" href="https://github.com/BertToe" target="_blank" rel="noopener">GitHub ↗</a>
      <a class="pill" href="https://www.linkedin.com/in/alberto-hilario-2106b2255" target="_blank" rel="noopener">LinkedIn ↗</a>
    </div>
  </div>
</header>

<section id="about">
  <div class="wrap">
    <div class="eyebrow"><span>01</span> — About</div>
    <h2 class="sec-title">From the floor to the dataset</h2>
    <div class="about-grid">
      <div>
        <p>
          Most of my analytics instinct comes from the floor, not the classroom: tracking lead drop-off at
          Toyota's Business Development Center, reading shrink patterns at Petco, watching 300+ guests move
          through the American Museum of Natural History on a Saturday. The Google Data Analytics
          Certificate gave me the SQL, cleaning, and visualization vocabulary to formalize what I was
          already doing by instinct.
        </p>
        <p>
          I'm currently looking for remote or hybrid data analyst and customer experience analyst roles —
          somewhere that values both the rigor of a clean query and the judgment that comes from talking to
          a real customer 200 times a day.
        </p>
      </div>
      <div>
        <div class="stat-card"><div class="stat-num">25+</div><div class="stat-label">employees led, Petco</div></div>
        <div class="stat-card"><div class="stat-num">4</div><div class="stat-label">end-to-end SQL analytics projects</div></div>
        <div class="stat-card"><div class="stat-num">6 yrs</div><div class="stat-label">across retail, CRM, and guest services</div></div>
      </div>
    </div>
  </div>
</section>

<section id="skills">
  <div class="wrap">
    <div class="eyebrow"><span>02</span> — Tools</div>
    <h2 class="sec-title">Stack</h2>
    <div class="skill-row">
      <span class="tag">SQL</span>
      <span class="tag">Data Cleaning</span>
      <span class="tag">Tableau</span>
      <span class="tag">Excel / Sheets</span>
      <span class="tag">CRM Systems</span>
      <span class="tag">Data Visualization</span>
      <span class="tag">Git / GitHub</span>
      <span class="tag">Inventory &amp; Ops Analysis</span>
    </div>
  </div>
</section>

<section id="projects">
  <div class="wrap">
    <div class="eyebrow"><span>03</span> — Projects</div>
    <h2 class="sec-title">SQL analytics work</h2>

    <div class="proj">
      <div class="proj-idx">01</div>
      <div>
        <h3 class="proj-title"><a href="https://github.com/BertToe/cyclistic-bike-share-analysis" target="_blank" rel="noopener">Cyclistic Bike-Share Analysis</a></h3>
        <p class="proj-desc">Google Data Analytics Certificate capstone — SQL analysis of rider behavior to identify casual-to-member conversion opportunities.</p>
        <div class="proj-tags"><span>SQL</span><span>Capstone</span><span>Customer Segmentation</span></div>
      </div>
    </div>

    <div class="proj">
      <div class="proj-idx">02</div>
      <div>
        <h3 class="proj-title"><a href="https://github.com/BertToe/nyc-taxi-analysis" target="_blank" rel="noopener">NYC Taxi Analysis</a></h3>
        <p class="proj-desc">SQL-driven look at demand patterns across NYC taxi trip data, with an interactive dashboard for exploring peak windows.</p>
        <div class="proj-tags"><span>SQL</span><span>Dashboard</span><span>Demand Patterns</span></div>
      </div>
    </div>

    <div class="proj">
      <div class="proj-idx">03</div>
      <div>
        <h3 class="proj-title"><a href="https://github.com/BertToe/Retail-sales-analysis" target="_blank" rel="noopener">Retail Sales Analysis</a></h3>
        <p class="proj-desc">Trend analysis on retail sales data — identifying seasonality and category performance using SQL queries.</p>
        <div class="proj-tags"><span>SQL</span><span>Retail</span><span>Trend Analysis</span></div>
      </div>
    </div>

    <div class="proj">
      <div class="proj-idx">04</div>
      <div>
        <h3 class="proj-title"><a href="https://github.com/BertToe/crm-segmentation-analysis" target="_blank" rel="noopener">CRM Segmentation Analysis</a></h3>
        <p class="proj-desc">Customer behavior segmentation built on CRM data — directly informed by hands-on lead-management experience at Toyota.</p>
        <div class="proj-tags"><span>SQL</span><span>CRM</span><span>Segmentation</span></div>
      </div>
    </div>
  </div>
</section>

<section id="experience">
  <div class="wrap">
    <div class="eyebrow"><span>04</span> — Experience</div>
    <h2 class="sec-title">Work history</h2>

    <div class="job">
      <div class="job-date">2026 – Present</div>
      <div>
        <div class="job-title">Store Manager</div>
        <div class="job-org">Petco</div>
        <ul>
          <li>Own business performance for a high-volume location, accountable for revenue, operational execution, and customer satisfaction</li>
          <li>Leverage sales and operational data to identify trends, optimize inventory, and implement strategies that increase profitability</li>
          <li>Lead, coach, and develop a team of 25+ employees, consistently exceeding performance targets</li>
        </ul>
      </div>
    </div>

    <div class="job">
      <div class="job-date">Jun 2024 – Oct 2025</div>
      <div>
        <div class="job-title">Independent Contractor</div>
        <div class="job-org">Uber Eats</div>
        <ul>
          <li>Analyzed peak demand windows and optimized delivery routing to increase daily volume</li>
          <li>Self-managed scheduling and workload planning against platform performance benchmarks</li>
        </ul>
      </div>
    </div>

    <div class="job">
      <div class="job-date">Feb 2024 – Mar 2025</div>
      <div>
        <div class="job-title">Guest Services Representative</div>
        <div class="job-org">American Museum of Natural History</div>
        <ul>
          <li>Assisted 300+ guests daily across a high-traffic museum floor</li>
          <li>Coordinated with team members to manage crowd flow during peak visitation</li>
        </ul>
      </div>
    </div>

    <div class="job">
      <div class="job-date">Mar 2022 – Nov 2023</div>
      <div>
        <div class="job-title">Bartender / Waiter</div>
        <div class="job-org">Wolf and Warrior Brewing Company</div>
        <ul>
          <li>Built repeat customer relationships through personalized service and recommendations</li>
          <li>Improved table turnover 15–25% through proactive guest and seating management</li>
        </ul>
      </div>
    </div>

    <div class="job">
      <div class="job-date">Feb 2019 – Jul 2020</div>
      <div>
        <div class="job-title">Business Development Consultant</div>
        <div class="job-org">Toyota</div>
        <ul>
          <li>Managed 90+ daily leads, prioritizing by intent and conversion likelihood</li>
          <li>Ran multi-touch CRM follow-up across 200+ leads weekly, improving pipeline retention</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<footer id="contact">
  <div class="wrap">
    <div class="eyebrow"><span>05</span> — Get in touch</div>
    <div class="footer-links">
      <a href="mailto:albertohilario101@gmail.com">albertohilario101@gmail.com</a>
      <a href="https://github.com/BertToe" target="_blank" rel="noopener">GitHub</a>
      <a href="https://www.linkedin.com/in/alberto-hilario-2106b2255" target="_blank" rel="noopener">LinkedIn</a>
    </div>
    <div class="footer-note">Brooklyn, NY — open to remote / hybrid roles</div>
  </div>
</footer>

</body>
</html>
