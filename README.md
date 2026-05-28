<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Vaishnavi Thridandapani — Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;700;800&family=JetBrains+Mono:wght@400;700&family=Manrope:wght@300;400;600;700&display=swap" rel="stylesheet"/>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body { font-family: 'Manrope', sans-serif; background: #020b18; color: #e8f4ff; min-height: 100vh; }

  .orb1 { position: fixed; width: 400px; height: 400px; border-radius: 50%; background: #0ea5e9; opacity: 0.08; top: -100px; right: -80px; pointer-events: none; z-index: 0; }
  .orb2 { position: fixed; width: 300px; height: 300px; border-radius: 50%; background: #06b6d4; opacity: 0.07; top: 40%; left: -100px; pointer-events: none; z-index: 0; }
  .orb3 { position: fixed; width: 250px; height: 250px; border-radius: 50%; background: #38bdf8; opacity: 0.06; bottom: 80px; right: 80px; pointer-events: none; z-index: 0; }

  .wrapper { max-width: 900px; margin: 0 auto; padding: 2.5rem 1.5rem 4rem; position: relative; z-index: 1; }

  /* HERO */
  .hero { padding: 2.5rem 2rem 2rem; background: rgba(14,165,233,0.06); border: 1px solid rgba(56,189,248,0.15); border-radius: 20px; margin-bottom: 1.5rem; position: relative; overflow: hidden; }
  .hero-badge-row { display: flex; gap: 8px; flex-wrap: wrap; margin-bottom: 1.2rem; }
  .hbadge { font-family: 'JetBrains Mono', monospace; font-size: 10px; padding: 4px 12px; border-radius: 100px; letter-spacing: 0.08em; font-weight: 700; }
  .hb1 { background: rgba(6,182,212,0.15); color: #67e8f9; border: 1px solid rgba(6,182,212,0.3); }
  .hb2 { background: rgba(14,165,233,0.12); color: #7dd3fc; border: 1px solid rgba(14,165,233,0.25); }
  .hb3 { background: rgba(56,189,248,0.1); color: #93c5fd; border: 1px solid rgba(56,189,248,0.2); }
  .hero-row { display: flex; align-items: flex-start; justify-content: space-between; flex-wrap: wrap; gap: 1rem; }
  .hname { font-family: 'Syne', sans-serif; font-size: 52px; font-weight: 800; line-height: 1; letter-spacing: -1.5px; margin-bottom: 8px; }
  .hname span { color: #38bdf8; }
  .hsub { font-family: 'JetBrains Mono', monospace; font-size: 12px; color: #4a7fa5; margin-bottom: 1.5rem; }
  .hlinks { display: flex; gap: 8px; flex-wrap: wrap; }
  .hlink { font-family: 'JetBrains Mono', monospace; font-size: 11px; padding: 8px 16px; border-radius: 8px; background: rgba(14,165,233,0.08); border: 1px solid rgba(56,189,248,0.18); color: #7dd3fc; text-decoration: none; display: inline-flex; align-items: center; gap: 6px; transition: all 0.2s; }
  .hlink:hover { background: rgba(14,165,233,0.18); border-color: rgba(56,189,248,0.4); }
  .cgpa-box { text-align: right; }
  .cgpa-num { font-family: 'Syne', sans-serif; font-size: 48px; font-weight: 800; color: #38bdf8; line-height: 1; }
  .cgpa-lbl { font-family: 'JetBrains Mono', monospace; font-size: 10px; color: #4a7fa5; }

  /* STATS */
  .stats4 { display: grid; grid-template-columns: repeat(4, 1fr); gap: 10px; margin-bottom: 1.5rem; }
  .sc { background: rgba(14,165,233,0.07); border: 1px solid rgba(56,189,248,0.13); border-radius: 12px; padding: 1rem; text-align: center; }
  .sc-n { font-family: 'Syne', sans-serif; font-size: 26px; font-weight: 800; color: #38bdf8; line-height: 1; margin-bottom: 4px; }
  .sc-l { font-size: 11px; color: #4a7fa5; }

  /* SECTION LABEL */
  .sl { font-family: 'JetBrains Mono', monospace; font-size: 10px; color: #0ea5e9; letter-spacing: 0.15em; text-transform: uppercase; margin: 2.2rem 0 1rem; display: flex; align-items: center; gap: 8px; }
  .sl::after { content: ''; flex: 1; height: 1px; background: rgba(56,189,248,0.12); }

  /* ABOUT */
  .about-p { font-size: 15px; line-height: 1.9; color: #7aa8c7; font-weight: 300; }
  .about-p b { color: #e8f4ff; font-weight: 700; }

  /* PROJECTS */
  .pgrid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 12px; }
  .pc { background: rgba(14,165,233,0.06); border: 1px solid rgba(56,189,248,0.14); border-radius: 14px; padding: 1.25rem; cursor: pointer; transition: all 0.2s; text-decoration: none; display: block; color: inherit; }
  .pc:hover { background: rgba(14,165,233,0.12); border-color: rgba(56,189,248,0.35); }
  .pc-top { display: flex; align-items: center; justify-content: space-between; margin-bottom: 10px; }
  .pc-ico { width: 38px; height: 38px; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 18px; background: rgba(6,182,212,0.15); border: 1px solid rgba(6,182,212,0.2); }
  .pc-arr { font-size: 16px; color: rgba(56,189,248,0.3); transition: color 0.2s; }
  .pc:hover .pc-arr { color: #38bdf8; }
  .pc-name { font-family: 'Syne', sans-serif; font-size: 17px; font-weight: 700; margin-bottom: 5px; color: #e8f4ff; }
  .pc-desc { font-size: 12px; color: #4a7fa5; line-height: 1.6; margin-bottom: 12px; }
  .pc-tags { display: flex; flex-wrap: wrap; gap: 6px; }
  .pt { font-family: 'JetBrains Mono', monospace; font-size: 10px; padding: 3px 8px; border-radius: 4px; background: rgba(14,165,233,0.1); color: #67e8f9; border: 1px solid rgba(6,182,212,0.2); }

  /* TIMELINE */
  .tl { position: relative; padding-left: 18px; }
  .tl::before { content: ''; position: absolute; left: 0; top: 8px; bottom: 8px; width: 1px; background: rgba(56,189,248,0.15); }
  .tli { position: relative; padding-left: 24px; margin-bottom: 1.75rem; }
  .tli:last-child { margin-bottom: 0; }
  .tl-dot { position: absolute; left: -25px; top: 5px; width: 10px; height: 10px; border-radius: 50%; background: #0ea5e9; border: 2px solid #38bdf8; box-shadow: 0 0 10px rgba(56,189,248,0.5); }
  .tl-date { font-family: 'JetBrains Mono', monospace; font-size: 10px; color: #0ea5e9; margin-bottom: 3px; }
  .tl-role { font-family: 'Syne', sans-serif; font-size: 18px; font-weight: 700; margin-bottom: 2px; color: #e8f4ff; }
  .tl-co { font-family: 'JetBrains Mono', monospace; font-size: 11px; color: #4a7fa5; margin-bottom: 8px; }
  .tl-pts { padding-left: 1rem; }
  .tl-pts li { font-size: 13px; color: #7aa8c7; line-height: 1.7; margin-bottom: 3px; }

  /* SKILLS */
  .sw { display: flex; flex-wrap: wrap; gap: 8px; }
  .sk { font-family: 'JetBrains Mono', monospace; font-size: 11px; padding: 6px 13px; border-radius: 8px; background: rgba(14,165,233,0.07); border: 1px solid rgba(56,189,248,0.13); color: #7dd3fc; display: inline-flex; align-items: center; gap: 6px; transition: all 0.2s; }
  .sk:hover { background: rgba(14,165,233,0.15); border-color: rgba(56,189,248,0.3); }
  .sk i { font-size: 14px; }

  /* ACHIEVEMENTS */
  .ach-g { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 8px; }
  .ach-c { background: rgba(14,165,233,0.06); border: 1px solid rgba(56,189,248,0.12); border-radius: 10px; padding: 0.875rem 1rem; display: flex; align-items: flex-start; gap: 10px; }
  .ach-ic { font-size: 16px; flex-shrink: 0; color: #38bdf8; margin-top: 1px; }
  .ach-tx { font-size: 12px; color: #7aa8c7; line-height: 1.5; }

  /* EXPLORING */
  .exp-wrap { display: flex; flex-wrap: wrap; gap: 8px; }
  .ep { font-family: 'JetBrains Mono', monospace; font-size: 11px; padding: 6px 14px; border-radius: 100px; background: rgba(14,165,233,0.07); color: #7dd3fc; border: 1px solid rgba(56,189,248,0.15); }
  .ep:nth-child(1) { border-color: rgba(56,189,248,0.35); color: #67e8f9; }
  .ep:nth-child(2) { border-color: rgba(6,182,212,0.3); color: #5DCAA5; }
  .ep:nth-child(3) { border-color: rgba(56,189,248,0.2); }
  .ep:nth-child(4) { border-color: rgba(14,165,233,0.2); }

  /* CTA */
  .cta { margin-top: 2rem; background: rgba(14,165,233,0.08); border: 1px solid rgba(56,189,248,0.2); border-radius: 16px; padding: 2rem; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 1rem; }
  .cta-t { font-family: 'Syne', sans-serif; font-size: 22px; font-weight: 700; color: #e8f4ff; }
  .cta-t span { color: #38bdf8; }
  .cta-bs { display: flex; gap: 8px; flex-wrap: wrap; }
  .cb { font-family: 'JetBrains Mono', monospace; font-size: 11px; padding: 9px 18px; border-radius: 8px; text-decoration: none; display: inline-flex; align-items: center; gap: 6px; border: 1px solid rgba(56,189,248,0.25); background: rgba(14,165,233,0.1); color: #7dd3fc; transition: all 0.2s; }
  .cb.primary { background: #0ea5e9; color: #fff; border-color: #0ea5e9; }
  .cb:hover { border-color: #38bdf8; background: rgba(14,165,233,0.2); }
  .cb.primary:hover { background: #38bdf8; }

  @media (max-width: 600px) {
    .hname { font-size: 36px; }
    .stats4 { grid-template-columns: repeat(2, 1fr); }
    .cgpa-num { font-size: 36px; }
    .cta { flex-direction: column; }
  }
</style>
</head>
<body>
<div class="orb1"></div>
<div class="orb2"></div>
<div class="orb3"></div>

<div class="wrapper">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-badge-row">
      <span class="hbadge hb1">● OPEN TO WORK</span>
      <span class="hbadge hb2">FULL-STACK</span>
      <span class="hbadge hb3">AI DEVELOPER</span>
    </div>
    <div class="hero-row">
      <div>
        <h1 class="hname">Vaishnavi<br><span>Thridandapani</span></h1>
        <p class="hsub">// software_engineer · hyderabad · b.tech_cs</p>
        <div class="hlinks">
          <a class="hlink" href="https://github.com/Vaishnavi-Thridandapani" target="_blank"><i class="ti ti-brand-github"></i> GitHub</a>
          <a class="hlink" href="https://www.linkedin.com/in/vaishnavi-thridandapani/" target="_blank"><i class="ti ti-brand-linkedin"></i> LinkedIn</a>
          <a class="hlink" href="mailto:thridandapani.vaishnavi26@gmail.com"><i class="ti ti-mail"></i> Email</a>
        </div>
      </div>
      <div class="cgpa-box">
        <div class="cgpa-num">8.43</div>
        <div class="cgpa-lbl">CGPA</div>
      </div>
    </div>
  </div>

  <!-- STATS -->
  <div class="stats4">
    <div class="sc"><div class="sc-n">4</div><div class="sc-l">projects</div></div>
    <div class="sc"><div class="sc-n">2</div><div class="sc-l">internships</div></div>
    <div class="sc"><div class="sc-n">5+</div><div class="sc-l">certs</div></div>
    <div class="sc"><div class="sc-n">🥈</div><div class="sc-l">hackathon</div></div>
  </div>

  <!-- ABOUT -->
  <div class="sl">about</div>
  <p class="about-p">CS graduate passionate about building <b>scalable full-stack apps</b>, <b>AI-powered workflows</b>, and modern products that solve real problems. I care about clean code, accessibility-first design, and systems that hold up at scale.</p>

  <!-- PROJECTS -->
  <div class="sl">projects</div>
  <div class="pgrid">
    <a class="pc" href="https://github.com/Vaishnavi-Thridandapani" target="_blank">
      <div class="pc-top"><div class="pc-ico">🤝</div><i class="ti ti-arrow-up-right pc-arr"></i></div>
      <p class="pc-name">Bridgy App</p>
      <p class="pc-desc">Real-time service exchange with virtual coin economy, push notifications & admin dashboard.</p>
      <div class="pc-tags"><span class="pt">Flutter</span><span class="pt">Firebase</span><span class="pt">Firestore</span></div>
    </a>
    <a class="pc" href="https://github.com/Vaishnavi-Thridandapani" target="_blank">
      <div class="pc-top"><div class="pc-ico">🤖</div><i class="ti ti-arrow-up-right pc-arr"></i></div>
      <p class="pc-name">ServeX AI</p>
      <p class="pc-desc">AI skill exchange platform with recommendation engine, Maps integration & multilingual support.</p>
      <div class="pc-tags"><span class="pt">Python</span><span class="pt">Node.js</span><span class="pt">Firebase</span></div>
    </a>
    <a class="pc" href="https://github.com/Vaishnavi-Thridandapani" target="_blank">
      <div class="pc-top"><div class="pc-ico">🧠</div><i class="ti ti-arrow-up-right pc-arr"></i></div>
      <p class="pc-name">MelloMind</p>
      <p class="pc-desc">Accessibility-first sensory platform for child engagement with interactive modules & animations.</p>
      <div class="pc-tags"><span class="pt">Python</span><span class="pt">Streamlit</span></div>
    </a>
    <a class="pc" href="https://github.com/Vaishnavi-Thridandapani" target="_blank">
      <div class="pc-top"><div class="pc-ico">🗳️</div><i class="ti ti-arrow-up-right pc-arr"></i></div>
      <p class="pc-name">DigitalDemocracy</p>
      <p class="pc-desc">Secure civic-tech voting platform with database-backed elections and structured participation.</p>
      <div class="pc-tags"><span class="pt">JavaScript</span><span class="pt">SQL</span></div>
    </a>
  </div>

  <!-- EXPERIENCE -->
  <div class="sl">experience</div>
  <div class="tl">
    <div class="tli">
      <div class="tl-dot"></div>
      <p class="tl-date">MAY 2026 – JUN 2026</p>
      <p class="tl-role">Software Developer Intern</p>
      <p class="tl-co">YUVAINTERN</p>
      <ul class="tl-pts">
        <li>End-to-end SDLC documentation and testing workflows</li>
        <li>Agile sprints, QA testing, risk analysis, and code reviews</li>
        <li>Cross-functional team collaboration on project delivery</li>
      </ul>
    </div>
    <div class="tli">
      <div class="tl-dot"></div>
      <p class="tl-date">FEB 2024 – MAR 2024</p>
      <p class="tl-role">Gen AI Intern</p>
      <p class="tl-co">IBM SKILLSBUILD</p>
      <ul class="tl-pts">
        <li>NLP projects with Python and NLTK</li>
        <li>Prompt engineering, AI text generation and summarization</li>
      </ul>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="sl">tech stack</div>
  <div class="sw">
    <span class="sk"><i class="ti ti-brand-python"></i> Python</span>
    <span class="sk"><i class="ti ti-brand-javascript"></i> JavaScript</span>
    <span class="sk"><i class="ti ti-brand-nodejs"></i> Node.js</span>
    <span class="sk"><i class="ti ti-device-mobile"></i> Flutter</span>
    <span class="sk"><i class="ti ti-flame"></i> Firebase</span>
    <span class="sk"><i class="ti ti-database"></i> MongoDB</span>
    <span class="sk"><i class="ti ti-database"></i> SQL</span>
    <span class="sk"><i class="ti ti-brand-aws"></i> AWS</span>
    <span class="sk"><i class="ti ti-api"></i> REST APIs</span>
    <span class="sk"><i class="ti ti-brand-git"></i> Git</span>
    <span class="sk"><i class="ti ti-brain"></i> NLP / AI</span>
    <span class="sk"><i class="ti ti-accessible"></i> Accessibility</span>
  </div>

  <!-- EXPLORING -->
  <div class="sl">currently exploring</div>
  <div class="exp-wrap">
    <span class="ep">Backend Architecture</span>
    <span class="ep">AI Product Workflows</span>
    <span class="ep">DevOps & CI/CD</span>
    <span class="ep">Enterprise App Design</span>
    <span class="ep">Scalable Full-Stack</span>
  </div>

  <!-- ACHIEVEMENTS -->
  <div class="sl">recognition</div>
  <div class="ach-g">
    <div class="ach-c"><i class="ti ti-star ach-ic"></i><span class="ach-tx">Second Prize — Data Analytics Hackathon</span></div>
    <div class="ach-c"><i class="ti ti-award ach-ic"></i><span class="ach-tx">Merit Scholarship Recipient</span></div>
    <div class="ach-c"><i class="ti ti-certificate ach-ic"></i><span class="ach-tx">Python Essentials — Cisco Networking Academy</span></div>
    <div class="ach-c"><i class="ti ti-certificate ach-ic"></i><span class="ach-tx">Joy of Computing Using Python — NPTEL</span></div>
    <div class="ach-c"><i class="ti ti-certificate ach-ic"></i><span class="ach-tx">DevOps on AWS — Simplilearn</span></div>
  </div>

  <!-- CTA -->
  <div class="cta">
    <div class="cta-t">Let's build something <span>great.</span></div>
    <div class="cta-bs">
      <a class="cb primary" href="mailto:thridandapani.vaishnavi26@gmail.com"><i class="ti ti-send"></i> Hire me</a>
      <a class="cb" href="https://www.linkedin.com/in/vaishnavi-thridandapani/" target="_blank"><i class="ti ti-brand-linkedin"></i> LinkedIn</a>
      <a class="cb" href="https://github.com/Vaishnavi-Thridandapani" target="_blank"><i class="ti ti-brand-github"></i> GitHub</a>
    </div>
  </div>

</div>
</body>
</html>
