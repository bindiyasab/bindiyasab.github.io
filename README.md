
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bindiya K — Data Analyst</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,400&family=Space+Mono:wght@400;700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --white:#ffffff;
    --paper:#faf9fc;
    --ink:#221c2e;
    --ink-dim:#5d5568;
    --purple:#5a2ea6;
    --purple-deep:#3b1d70;
    --lilac:#efe9fb;
    --lilac-2:#e2d7f5;
    --rule:#e6e0f0;
  }
  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--white);
    color:var(--ink);
    font-family:'Inter',sans-serif;
    font-size:16px;
    line-height:1.65;
    -webkit-font-smoothing:antialiased;
  }
  ::selection{background:var(--purple);color:var(--white);}

  .wrap{max-width:920px;margin:0 auto;padding:0 32px;}

  .eyebrow{
    font-family:'Space Mono',monospace;
    font-size:12.5px;
    letter-spacing:0.14em;
    text-transform:uppercase;
    color:var(--purple);
    display:flex;align-items:center;gap:10px;
    margin-bottom:18px;
  }
  .eyebrow::before{content:'';width:22px;height:1px;background:var(--purple);display:inline-block;}

  h1,h2,h3{font-family:'Fraunces',serif;font-weight:500;letter-spacing:-0.01em;color:var(--ink);}

  /* NAV */
  nav{
    position:sticky;top:0;z-index:10;
    background:rgba(255,255,255,0.9);
    backdrop-filter:blur(10px);
    border-bottom:1px solid var(--rule);
  }
  nav .wrap{display:flex;align-items:center;justify-content:space-between;padding:20px 32px;}
  .nav-mark{font-family:'Space Mono',monospace;font-size:14px;color:var(--ink);letter-spacing:0.05em;}
  .nav-mark span{color:var(--purple);}
  .nav-links{display:flex;gap:28px;list-style:none;font-family:'Space Mono',monospace;font-size:12.5px;letter-spacing:0.05em;}
  .nav-links a{color:var(--ink-dim);text-decoration:none;transition:color .2s;}
  .nav-links a:hover, .nav-links a:focus-visible{color:var(--purple);}

  /* HERO */
  .hero{padding:100px 0 70px;position:relative;overflow:hidden;}
  .hero::before{
    content:'';position:absolute;top:-180px;right:-160px;width:460px;height:460px;
    background:radial-gradient(circle, var(--lilac) 0%, rgba(239,233,251,0) 70%);
    z-index:0;pointer-events:none;
  }
  .hero-kicker{font-family:'Space Mono',monospace;font-size:13px;color:var(--purple);letter-spacing:0.12em;text-transform:uppercase;margin-bottom:22px;position:relative;}
  .hero h1{font-size:clamp(38px,6vw,66px);line-height:1.08;max-width:16ch;position:relative;}
  .hero h1 em{font-style:italic;color:var(--purple);}
  .hero-sub{margin-top:26px;max-width:58ch;color:var(--ink-dim);font-size:17.5px;position:relative;}

  /* KPI DASHBOARD STRIP */
  .kpi-strip{
    margin-top:56px;
    border:1px solid var(--rule);
    background:var(--white);
    border-radius:10px;
    overflow:hidden;
    box-shadow:0 20px 50px -30px rgba(90,46,166,0.35);
    position:relative;
  }
  .kpi-strip-head{
    display:flex;align-items:center;justify-content:space-between;
    padding:12px 20px;border-bottom:1px solid var(--rule);
    background:var(--lilac);
    font-family:'Space Mono',monospace;font-size:11.5px;color:var(--purple-deep);letter-spacing:0.08em;text-transform:uppercase;
  }
  .kpi-strip-head .dot{width:7px;height:7px;border-radius:50%;background:var(--purple);display:inline-block;margin-right:8px;box-shadow:0 0 0 3px rgba(90,46,166,0.15);}
  .kpi-grid{display:grid;grid-template-columns:repeat(4,1fr);}
  .kpi{padding:26px 20px;border-right:1px solid var(--rule);}
  .kpi:last-child{border-right:none;}
  .kpi-num{font-family:'Fraunces',serif;font-size:clamp(20px,2.8vw,28px);color:var(--ink);}
  .kpi-num .accent{color:var(--purple);}
  .kpi-label{margin-top:6px;font-family:'Space Mono',monospace;font-size:11px;color:var(--ink-dim);letter-spacing:0.05em;text-transform:uppercase;}

  @media (max-width:720px){
    .kpi-grid{grid-template-columns:repeat(2,1fr);}
    .kpi:nth-child(2){border-right:none;}
  }

  section{padding:88px 0;border-top:1px solid var(--rule);}
  .section-head{display:flex;align-items:baseline;justify-content:space-between;margin-bottom:44px;flex-wrap:wrap;gap:10px;}
  .section-head h2{font-size:clamp(26px,3.4vw,34px);}

  /* SUMMARY */
  .summary-block p{max-width:68ch;color:var(--ink-dim);font-size:17px;}
  .summary-block strong{color:var(--ink);font-weight:600;}

  /* SKILLS */
  .skills-table{border:1px solid var(--rule);border-radius:10px;overflow:hidden;}
  .skill-row{display:grid;grid-template-columns:210px 1fr;border-top:1px solid var(--rule);}
  .skill-row:first-child{border-top:none;}
  .skill-key{
    padding:20px 22px;font-family:'Space Mono',monospace;font-size:12.5px;color:var(--purple);
    letter-spacing:0.06em;text-transform:uppercase;border-right:1px solid var(--rule);
    display:flex;align-items:center;background:var(--paper);
  }
  .skill-val{padding:20px 22px;color:var(--ink-dim);font-size:15.5px;display:flex;flex-wrap:wrap;gap:8px 10px;align-items:center;}
  .chip{
    display:inline-block;padding:5px 11px;border:1px solid var(--lilac-2);background:var(--lilac);border-radius:100px;
    font-family:'Space Mono',monospace;font-size:12px;color:var(--purple-deep);white-space:nowrap;
  }
  @media (max-width:640px){
    .skill-row{grid-template-columns:1fr;}
    .skill-key{border-right:none;border-bottom:1px solid var(--rule);}
  }

  /* PROJECTS */
  .project{
    padding:34px 0;border-top:1px solid var(--rule);display:grid;grid-template-columns:180px 1fr;gap:28px;
  }
  .project:first-child{border-top:none;}
  .project-idx{font-family:'Fraunces',serif;font-style:italic;font-size:15px;color:var(--ink-dim);padding-top:4px;}
  .project h3{font-size:22px;color:var(--ink);margin-bottom:10px;}
  .project p{color:var(--ink-dim);font-size:15.5px;max-width:60ch;}
  .project ul{margin-top:14px;padding-left:0;list-style:none;}
  .project li{position:relative;padding-left:20px;color:var(--ink-dim);font-size:15px;margin-bottom:9px;max-width:62ch;}
  .project li::before{content:'∴';position:absolute;left:0;color:var(--purple);font-family:'Fraunces',serif;}
  .project-tags{margin-top:16px;display:flex;flex-wrap:wrap;gap:8px;align-items:center;}
  .view-link{
    margin-top:18px;display:inline-flex;align-items:center;gap:8px;
    font-family:'Space Mono',monospace;font-size:12.5px;letter-spacing:0.05em;text-transform:uppercase;
    color:var(--purple);text-decoration:none;padding:9px 16px;border:1px solid var(--purple);border-radius:100px;
    transition:background .2s, color .2s;
  }
  .view-link:hover, .view-link:focus-visible{background:var(--purple);color:var(--white);}
  .view-link svg{width:13px;height:13px;transition:transform .2s;}
  .view-link:hover svg{transform:translate(2px,-2px);}
  @media (max-width:640px){.project{grid-template-columns:1fr;gap:8px;}}

  /* EXPERIENCE */
  .xp-item{display:grid;grid-template-columns:1fr auto;gap:12px;padding:26px 0;border-top:1px solid var(--rule);align-items:baseline;}
  .xp-item:first-child{border-top:none;}
  .xp-role{font-family:'Fraunces',serif;font-size:20px;color:var(--ink);}
  .xp-org{color:var(--purple);font-family:'Space Mono',monospace;font-size:13px;margin-top:4px;}
  .xp-date{font-family:'Space Mono',monospace;font-size:12.5px;color:var(--ink-dim);white-space:nowrap;}
  .xp-list{grid-column:1 / -1;margin-top:14px;list-style:none;}
  .xp-list li{position:relative;padding-left:20px;color:var(--ink-dim);font-size:15px;margin-bottom:8px;max-width:62ch;}
  .xp-list li::before{content:'—';position:absolute;left:0;color:var(--ink-dim);}

  /* CREDENTIALS */
  .cred-grid{display:grid;grid-template-columns:1fr 1fr;gap:48px;}
  .cred-col h3{font-family:'Space Mono',monospace;font-size:12.5px;letter-spacing:0.1em;text-transform:uppercase;color:var(--purple);margin-bottom:22px;font-weight:400;}
  .cred-entry{padding:16px 0;border-top:1px solid var(--rule);}
  .cred-entry:first-of-type{border-top:none;}
  .cred-title{color:var(--ink);font-size:15.5px;font-family:'Fraunces',serif;}
  .cred-meta{color:var(--ink-dim);font-family:'Space Mono',monospace;font-size:12px;margin-top:5px;}
  .lang-row{display:flex;gap:10px;flex-wrap:wrap;margin-top:6px;}
  @media (max-width:640px){.cred-grid{grid-template-columns:1fr;gap:0;}.cred-col{margin-bottom:36px;}}

  /* CONTACT FORM (visitor -> Bindiya) */
  .contact-form{
    display:grid;grid-template-columns:1fr 1fr;gap:20px;
    background:var(--paper);border:1px solid var(--rule);border-radius:14px;padding:36px;
  }
  .field{display:flex;flex-direction:column;gap:8px;}
  .field.full{grid-column:1 / -1;}
  .field label{font-family:'Space Mono',monospace;font-size:11.5px;letter-spacing:0.08em;text-transform:uppercase;color:var(--ink-dim);}
  .field input, .field textarea{
    font-family:'Inter',sans-serif;font-size:15px;color:var(--ink);
    background:var(--white);border:1px solid var(--rule);border-radius:8px;padding:12px 14px;
    outline-offset:2px;transition:border-color .2s;
  }
  .field input:focus, .field textarea:focus{border-color:var(--purple);}
  .field textarea{resize:vertical;min-height:100px;}
  .submit-btn{
    grid-column:1 / -1;justify-self:start;
    font-family:'Space Mono',monospace;font-size:13px;letter-spacing:0.06em;text-transform:uppercase;
    background:var(--purple);color:var(--white);border:none;border-radius:100px;padding:13px 28px;
    cursor:pointer;transition:background .2s;
  }
  .submit-btn:hover{background:var(--purple-deep);}
  .form-note{margin-top:16px;font-family:'Space Mono',monospace;font-size:12px;color:var(--ink-dim);display:none;}
  .form-note.show{display:block;}
  @media (max-width:640px){.contact-form{grid-template-columns:1fr;padding:26px;}}

  /* FOOTER — Bindiya's own contact details, shown only here */
  footer{padding:90px 0 60px;border-top:1px solid var(--rule);background:var(--purple-deep);}
  footer .wrap{position:relative;}
  footer .eyebrow{color:var(--lilac-2);}
  footer .eyebrow::before{background:var(--lilac-2);}
  footer h2{color:var(--white);font-size:clamp(30px,5vw,46px);max-width:14ch;}
  .contact-links{margin-top:34px;display:flex;flex-direction:column;gap:14px;font-family:'Space Mono',monospace;font-size:15px;}
  .contact-links a{color:var(--white);text-decoration:none;border-bottom:1px solid rgba(255,255,255,0.35);width:fit-content;padding-bottom:2px;transition:border-color .2s, color .2s;}
  .contact-links a:hover{color:var(--lilac-2);border-color:var(--lilac-2);}
  .contact-links .plain{color:rgba(255,255,255,0.75);}
  .foot-note{margin-top:60px;color:rgba(255,255,255,0.55);font-family:'Space Mono',monospace;font-size:12px;letter-spacing:0.04em;}

  @media (prefers-reduced-motion:no-preference){
    .reveal{opacity:0;transform:translateY(16px);transition:opacity .7s ease, transform .7s ease;}
    .reveal.in{opacity:1;transform:translateY(0);}
  }
  a:focus-visible, button:focus-visible, input:focus-visible, textarea:focus-visible{outline:2px solid var(--purple);outline-offset:2px;}
</style>
</head>
<body>

<nav>
  <div class="wrap">
    <div class="nav-mark">BINDIYA<span>·</span>K</div>
    <ul class="nav-links">
      <li><a href="#work">Projects</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#credentials">Credentials</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>
</nav>

<main class="wrap">

  <section class="hero" style="border-top:none;padding-top:80px;">
    <h1>Bindiya K</h1>
    <div class="hero-kicker" style="margin-top:16px;">Data Analyst · Mathematics Graduate</div>
    <p class="hero-sub" style="font-family:'Fraunces',serif;font-style:italic;font-size:clamp(20px,2.6vw,26px);color:var(--purple);margin-top:14px;">Turning raw data into clear business insight.</p>
    <p class="hero-sub">I clean messy datasets, build the logic that makes sense of them, and design dashboards that drive decisions — grounded in SQL, Python, Excel, Power BI, and Tableau, with a mathematician's instinct for structure.</p>
  </section>

  <section id="about">
    <div class="eyebrow">Summary</div>
    <div class="summary-block reveal">
      <p><strong>Data Analyst</strong> passionate about turning raw data into clear business insights. Skilled in <strong>SQL, Python, Excel, Power BI, and Tableau</strong>, with hands-on experience in data cleaning, dashboards, and reporting through academic projects and internships. Strong foundation in statistics and problem-solving — looking to leverage analytical skills to help companies make data-driven decisions and drive growth.</p>
    </div>
  </section>

  <section id="skills">
    <div class="section-head">
      <div>
        <div class="eyebrow">Truth Table</div>
        <h2>Technical skills</h2>
      </div>
    </div>
    <div class="skills-table reveal">
      <div class="skill-row">
        <div class="skill-key">Programming &amp; Analysis</div>
        <div class="skill-val">
          <span class="chip">Python</span><span class="chip">Pandas</span><span class="chip">NumPy</span><span class="chip">Matplotlib</span><span class="chip">Seaborn</span><span class="chip">SQL</span><span class="chip">Statistics</span>
        </div>
      </div>
      <div class="skill-row">
        <div class="skill-key">Visualization &amp; BI</div>
        <div class="skill-val"><span class="chip">Power BI</span><span class="chip">Tableau</span><span class="chip">Excel — VLOOKUP</span><span class="chip">HLOOKUP</span><span class="chip">Pivot Tables</span><span class="chip">SUMIFS / AVERAGEIFS</span></div>
      </div>
      <div class="skill-row">
        <div class="skill-key">Core Competencies</div>
        <div class="skill-val"><span class="chip">Data Cleaning</span><span class="chip">Data Interpretation</span><span class="chip">Market Research</span><span class="chip">Dashboard Development</span><span class="chip">MS Office</span></div>
      </div>
      <div class="skill-row">
        <div class="skill-key">Soft Skills</div>
        <div class="skill-val"><span class="chip">Problem Solving</span><span class="chip">Analytical Thinking</span><span class="chip">Communication</span><span class="chip">Team Management</span><span class="chip">Strategic Planning</span><span class="chip">Adaptability</span></div>
      </div>
    </div>
  </section>

  <section id="work">
    <div class="section-head">
      <div>
        <div class="eyebrow">Selected Work</div>
        <h2>Projects</h2>
      </div>
    </div>

    <div class="project reveal">
      <div class="project-idx">01 —<br>dashboard</div>
      <div>
        <h3>Retail Sales Performance Dashboard</h3>
        <p>Built an end-to-end analytics project covering 1,800+ retail orders: raw data ingestion, data cleaning, calculated fields, pivot summaries, and interactive dashboard design.</p>
        <ul>
          <li>Cleaned and standardized raw sales data (removed duplicates, fixed blanks, standardized text) and engineered calculated fields including Revenue, Cost, Profit, and Margin %.</li>
          <li>Built dynamic summaries using SUMIFS/AVERAGEIFS to analyze sales by Region, Month, and Top 10 Products, auto-recalculating as source data changed.</li>
        </ul>
        <div class="project-tags"><span class="chip">Excel</span><span class="chip">SUMIFS</span><span class="chip">Pivot Tables</span><span class="chip">KPI Design</span></div>
        <a href="#" class="view-link">View project
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M7 17L17 7M17 7H7M17 7V17"/></svg>
        </a>
      </div>
    </div>

    <div class="project reveal">
      <div class="project-idx">02 —<br>logic</div>
      <div>
        <h3>Boolean Algebra &amp; Logical Reasoning Analysis</h3>
        <p>Applied Boolean algebra and computational logic to mathematical problem-solving, strengthening the analytical and logical reasoning skills used in data analysis.</p>
        <div class="project-tags"><span class="chip">Logical Operators</span><span class="chip">Truth Tables</span><span class="chip">Conditional Logic</span></div>
        <a href="#" class="view-link">View project
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M7 17L17 7M17 7H7M17 7V17"/></svg>
        </a>
      </div>
    </div>
    
    <div class="project reveal">
      <div class="project-idx">03 —<br>EDA</div>
      <div>
        <h3>Zomato Restaurant Data Analysis</h3>
        <p>Performed EDA on Zomato dataset with 5,000+ restaurant records using Python. Analyzed the impact of restaurant type, online ordering, cost, and ratings on customer votes.</p>
        <ul>
          <li>Built 8 visualizations including countplots, boxplots, and heatmaps to uncover trends in restaurant popularity and service models.</li>
        </ul>
        <div class="project-tags"><span class="chip">Python</span><span class="chip">Pandas</span><span class="chip">Seaborn</span><span class="chip">Matplotlib</span><span class="chip">EDA</span></div>
        <a href="https://github.com/bindiyasab/DATA-ANALYSIS-" class="view-link" target="_blank" rel="noopener">View project
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M7 17L17 7M17 7H7M17 7V17"/></svg>
        </a>
      </div>
    </div>
    <div class="section-head">
      <div>
        <div class="eyebrow">Track Record</div>
        <h2>Experience</h2>
      </div>
    </div>
    <div class="xp-item reveal">
      <div>
        <div class="xp-role">Academic Counselor</div>
        <div class="xp-org">Stock Market Kerala, Calicut, Kerala</div>
      </div>
      <div class="xp-date">Oct 2024 — Mar 2025</div>
      <ul class="xp-list">
        <li>Assisted students in developing academic plans, selecting courses, and navigating the educational system.</li>
      </ul>
    </div>
    <div class="xp-item reveal">
      <div>
        <div class="xp-role">Relationship Officer</div>
        <div class="xp-org">Jaytrade Group of Companies, Calicut</div>
      </div>
      <div class="xp-date">Sep 2023 — Jan 2024</div>
      <ul class="xp-list">
        <li>Built and preserved strong relationships with clients, achieving sales targets.</li>
      </ul>
    </div>
  

  <section id="credentials">
    <div class="section-head">
      <div>
        <div class="eyebrow">Foundation</div>
        <h2>Credentials</h2>
      </div>
    </div>
    <div class="cred-grid">
      <div class="cred-col reveal">
        <h3>Education</h3>
        <div class="cred-entry">
          <div class="cred-title">Bachelor's Degree in Mathematics</div>
          <div class="cred-meta">College of Applied Science, Calicut, Kerala — 2025</div>
        </div>
        <div class="cred-entry">
          <div class="cred-title">Higher Secondary, Bio Maths</div>
          <div class="cred-meta">BEM Girls Higher Secondary School, Calicut, Kerala — 2018</div>
        </div>
        <div class="cred-entry">
          <div class="cred-title">Secondary Education, Maths &amp; Science</div>
          <div class="cred-meta">BEM Girls Higher Secondary School, Calicut, Kerala — 2016</div>
        </div>
      </div>
      <div class="cred-col reveal">
        <h3>Certifications</h3>
        <div class="cred-entry">
          <div class="cred-title">Foundations of Data Analysis</div>
          <div class="cred-meta">Coursera — data cleaning, visualization, spreadsheets, SQL basics, data-driven decision-making</div>
        </div>
        <h3 style="margin-top:36px;">Languages</h3>
        <div class="lang-row">
          <span class="chip">English</span><span class="chip">Malayalam</span><span class="chip">Hindi</span><span class="chip">Tamil</span>
        </div>
      </div>
    </div>
  </section>
  
  <section id="experience">
    <div class="section-head">
      <div>
        <div class="eyebrow">Track Record</div>
        <h2>Experience</h2>
      </div>
    </div>
    <div class="xp-item reveal">
      <div>
        <div class="xp-role">Academic Counselor</div>
        <div class="xp-org">Stock Market Kerala, Calicut, Kerala</div>
      </div>
      <div class="xp-date">Oct 2024 — Mar 2025</div>
      <ul class="xp-list">
        <li>Assisted students in developing academic plans, selecting courses, and navigating the educational system.</li>
      </ul>
    </div>
    <div class="xp-item reveal">
      <div>
        <div class="xp-role">Relationship Officer</div>
        <div class="xp-org">Jaytrade Group of Companies, Calicut</div>
      </div>
      <div class="xp-date">Sep 2023 — Jan 2024</div>
      <ul class="xp-list">
        <li>Built and preserved strong relationships with clients, achieving sales targets.</li>
      </ul>
    </div>
  </section>

  <section id="credentials">
    <div class="section-head">
      <div>
        <div class="eyebrow">Foundation</div>
        <h2>Credentials</h2>
      </div>
    </div>
    <div class="cred-grid">
      <div class="cred-col reveal">
        <h3>Education</h3>
        <div class="cred-entry">
          <div class="cred-title">Bachelor's Degree in Mathematics</div>
          <div class="cred-meta">College of Applied Science, Calicut, Kerala — 2025</div>
        </div>
        <div class="cred-entry">
          <div class="cred-title">Higher Secondary, Bio Maths</div>
          <div class="cred-meta">BEM Girls Higher Secondary School, Calicut, Kerala — 2018</div>
        </div>
        <div class="cred-entry">
          <div class="cred-title">Secondary Education, Maths &amp; Science</div>
          <div class="cred-meta">BEM Girls Higher Secondary School, Calicut, Kerala — 2016</div>
        </div>
      </div>
      <div class="cred-col reveal">
        <h3>Certifications</h3>
        <div class="cred-entry">
          <div class="cred-title">Foundations of Data Analysis</div>
          <div class="cred-meta">Coursera — data cleaning, visualization, spreadsheets, SQL basics, data-driven decision-making</div>
        </div>
        <h3 style="margin-top:36px;">Languages</h3>
        <div class="lang-row">
          <span class="chip">English</span><span class="chip">Malayalam</span><span class="chip">Hindi</span><span class="chip">Tamil</span>
        </div>
      </div>
    </div>
  </section>

 
  <section id="contact-form-section">
    <div class="section-head">
      <div>
        <div class="eyebrow">Reach Out</div>
        <h2>Send a message</h2>
      </div>
    </div>
    <form class="contact-form reveal" id="reachForm">
      <div class="field">
        <label for="visitorName">Your name</label>
        <input type="text" id="visitorName" name="visitorName" placeholder="Jane Doe" required>
      </div>
      <div class="field">
        <label for="visitorEmail">Your email</label>
        <input type="email" id="visitorEmail" name="visitorEmail" placeholder="jane@company.com" required>
      </div>
      <div class="field">
        <label for="visitorPhone">Your number</label>
        <input type="tel" id="visitorPhone" name="visitorPhone" placeholder="+91 XXXXX XXXXX">
      </div>
      <div class="field">
        <label for="visitorSubject">Subject</label>
        <input type="text" id="visitorSubject" 
        name="visitorSubject" placeholder="Job opportunity, project inquiry...">
      </div>
      <div class="field full">
        <label for="visitorMessage">Message</label>
        <textarea id="visitorMessage" name="visitorMessage" placeholder="Tell me a bit about what you have in mind..."></textarea>
      </div>
      <button type="submit" class="submit-btn">Send message</button>
      <div class="form-note" id="formNote">Thanks — this opens your email app with the message pre-filled to Bindiya.</div>
    </form>
  </section>

  <footer id="contact">
    <div class="wrap">
      <div class="eyebrow">Get in touch</div>
      <h2>Let's talk about your data.</h2>
      <div class="contact-links">
        <a href="mailto:bindiyasab1516@gmail.com">bindiyasab1516@gmail.com</a>
        <a href="tel:8590629313">8590629313</a>
        <a href="https://linkedin.com/in/bindiya-k-34842621a" target="_blank" rel="noopener">linkedin.com/in/bindiya-k-34842621a</a>
        <span class="plain">Beypore, Calicut, Kerala</span>
      </div>
      <div class="foot-note">© 2026 Bindiya K. Built with data-driven precision.</div>
    </div>
  </footer>



<script>
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target);} });
  },{threshold:0.15});
  document.querySelectorAll('.reveal').forEach(el=>io.observe(el));

  const form = document.getElementById('reachForm');
  const note = document.getElementById('formNote');
  form.addEventListener('submit', function(e){
    e.preventDefault();
    const name = document.getElementById('visitorName').value;
    const email = document.getElementById('visitorEmail').value;
    const phone = document.getElementById('visitorPhone').value;
    const subject = document.getElementById('visitorSubject').value || 'Portfolio inquiry';
    const message = document.getElementById('visitorMessage').value;
    const body = `Name: ${name}\nEmail: ${email}\nPhone: ${phone}\n\n${message}`;
    window.location.href = `mailto:bindiyasab1516@gmail.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
    note.classList.add('show');
  });
</script>


</section>  <!-- closes Experience section -->

</main>
</body>
</html>













        
                
