<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1"/>
<title>Veerbhan Singh Tomar — Senior .NET Developer</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;800;900&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet"/>
<style>
*{margin:0;padding:0;box-sizing:border-box}
:root{
  --white:#ffffff;
  --bg:#f7f5f0;
  --bg2:#efecea;
  --ink:#1a1814;
  --ink2:#4a4540;
  --ink3:#8a8580;
  --blue:#1e5fe8;
  --blue-light:#e8effd;
  --blue-mid:#c5d7fa;
  --violet:#6c3de8;
  --violet-light:#ede8fd;
  --teal:#0f9e75;
  --teal-light:#e0f5ed;
  --amber:#c47a15;
  --amber-light:#fdf0dc;
  --border:#e0ddd8;
  --border2:#ccc9c2;
}
body{
  background:var(--bg);
  color:var(--ink);
  font-family:'Plus Jakarta Sans',sans-serif;
  line-height:1.6;
}
a{text-decoration:none;color:inherit}
.page{max-width:940px;margin:0 auto;padding:0 28px 80px}

/* ── TOP NAV BAR ── */
.topbar{
  border-bottom:1px solid var(--border);
  background:var(--white);
  padding:0 28px;
  display:flex;align-items:center;justify-content:space-between;
  height:52px;
  position:sticky;top:0;z-index:10;
}
.topbar-logo{
  font-family:'Fira Code',monospace;
  font-size:13px;font-weight:500;
  color:var(--blue);
  letter-spacing:0.02em;
}
.topbar-nav{display:flex;gap:6px}
.topbar-link{
  font-size:12px;font-weight:500;
  color:var(--ink3);
  padding:5px 12px;
  border-radius:20px;
  border:1px solid transparent;
  transition:.15s;
}
.topbar-link:hover{background:var(--bg2);border-color:var(--border);color:var(--ink)}

/* ── HERO ── */
.hero{
  padding:64px 0 56px;
  display:grid;
  grid-template-columns:1fr 220px;
  gap:48px;
  align-items:center;
}
.hero-eyebrow{
  display:inline-flex;align-items:center;gap:8px;
  font-family:'Fira Code',monospace;font-size:12px;
  color:var(--teal);font-weight:500;letter-spacing:0.04em;
  padding:5px 14px 5px 10px;
  background:var(--teal-light);
  border:1px solid #b2e8d6;
  border-radius:20px;
  margin-bottom:20px;
}
.pulse{
  width:7px;height:7px;border-radius:50%;
  background:var(--teal);
  animation:blink 2s ease-in-out infinite;
}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.3}}
.hero h1{
  font-family:'Playfair Display',serif;
  font-size:clamp(38px,5.5vw,64px);
  font-weight:900;
  line-height:1.02;
  letter-spacing:-0.025em;
  color:var(--ink);
  margin-bottom:6px;
}
.hero h1 em{
  font-style:normal;
  color:var(--blue);
}
.hero-role{
  font-family:'Fira Code',monospace;font-size:13px;
  color:var(--ink3);letter-spacing:0.02em;
  margin-bottom:18px;
}
.hero-role b{color:var(--violet);font-weight:500}
.hero-bio{
  font-size:15px;color:var(--ink2);line-height:1.75;
  max-width:500px;margin-bottom:30px;
}
.hero-bio strong{color:var(--ink);font-weight:600}
.cta-row{display:flex;gap:10px;flex-wrap:wrap}
.cta-primary{
  display:inline-flex;align-items:center;gap:8px;
  padding:11px 22px;
  background:var(--blue);color:#fff;
  font-family:'Plus Jakarta Sans',sans-serif;
  font-weight:600;font-size:13px;letter-spacing:0.02em;
  border-radius:8px;transition:.2s;
}
.cta-primary:hover{background:#1650cc;transform:translateY(-1px)}
.cta-secondary{
  display:inline-flex;align-items:center;gap:8px;
  padding:11px 22px;
  background:var(--white);color:var(--ink);
  font-family:'Plus Jakarta Sans',sans-serif;
  font-weight:600;font-size:13px;
  border:1.5px solid var(--border2);
  border-radius:8px;transition:.2s;
}
.cta-secondary:hover{border-color:var(--blue);color:var(--blue);background:var(--blue-light)}

/* Avatar */
.avatar-wrap{display:flex;flex-direction:column;align-items:center;gap:14px}
.avatar-ring{
  width:168px;height:168px;border-radius:50%;
  background:var(--white);
  border:3px solid var(--blue-mid);
  display:flex;align-items:center;justify-content:center;
  position:relative;
}
.avatar-circle{
  width:152px;height:152px;border-radius:50%;
  background:linear-gradient(135deg,#dbeaff 0%,#e8e0fd 100%);
  display:flex;align-items:center;justify-content:center;
  font-family:'Playfair Display',serif;
  font-size:52px;font-weight:900;color:var(--blue);
  letter-spacing:-0.02em;
}
.avatar-badge{
  background:var(--white);
  border:1.5px solid var(--blue-mid);
  border-radius:20px;padding:5px 14px;
  font-family:'Fira Code',monospace;font-size:11px;
  color:var(--blue);font-weight:500;
  text-align:center;white-space:nowrap;
}
.view-badge{
  display:inline-flex;align-items:center;gap:6px;
  font-family:'Fira Code',monospace;font-size:11px;
  color:var(--ink3);
}

/* ── STAT STRIP ── */
.stats{
  display:grid;grid-template-columns:repeat(4,1fr);
  background:var(--white);
  border:1px solid var(--border);
  border-radius:14px;
  overflow:hidden;
  margin-bottom:60px;
}
.stat{
  padding:22px 16px;text-align:center;
  border-right:1px solid var(--border);
}
.stat:last-child{border-right:none}
.stat-val{
  font-family:'Playfair Display',serif;
  font-size:34px;font-weight:900;
  color:var(--ink);display:block;margin-bottom:3px;
}
.stat-val .hi{color:var(--blue)}
.stat-lbl{
  font-family:'Fira Code',monospace;
  font-size:10px;letter-spacing:0.1em;text-transform:uppercase;
  color:var(--ink3);
}

/* ── SECTION HEADER ── */
.sec{margin-bottom:56px}
.sec-hd{
  display:flex;align-items:center;gap:12px;margin-bottom:24px;
}
.sec-num{
  font-family:'Fira Code',monospace;font-size:11px;
  color:var(--blue);background:var(--blue-light);
  border:1px solid var(--blue-mid);
  border-radius:6px;padding:3px 9px;font-weight:500;letter-spacing:0.06em;
}
.sec-title{
  font-family:'Playfair Display',serif;
  font-size:22px;font-weight:800;color:var(--ink);
}
.sec-line{flex:1;height:1px;background:var(--border)}

/* ── ABOUT ── */
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.about-item{
  display:flex;align-items:flex-start;gap:10px;
  padding:13px 16px;
  background:var(--white);
  border:1px solid var(--border);border-radius:10px;
  font-size:14px;color:var(--ink2);
  transition:.15s;
}
.about-item:hover{border-color:var(--blue-mid);background:var(--blue-light)}
.about-item .ck{
  color:var(--teal);font-size:15px;flex-shrink:0;margin-top:1px;
  font-weight:700;
}
.about-item strong{color:var(--ink);font-weight:600}

/* ── BUILD GRID ── */
.build-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
.build-card{
  background:var(--white);
  border:1px solid var(--border);
  border-radius:12px;
  padding:20px 18px;
  transition:.2s;
  cursor:default;
}
.build-card:hover{border-color:var(--blue-mid);transform:translateY(-2px)}
.build-card:hover .build-num{color:var(--blue)}
.build-num{
  font-family:'Fira Code',monospace;font-size:11px;
  color:var(--ink3);letter-spacing:0.06em;margin-bottom:10px;display:block;
  transition:.2s;
}
.build-icon{
  font-size:22px;margin-bottom:10px;display:block;
  font-family:'Plus Jakarta Sans',sans-serif;
}
.build-name{
  font-family:'Plus Jakarta Sans',sans-serif;
  font-size:14px;font-weight:700;color:var(--ink);margin-bottom:5px;
}
.build-desc{font-size:12px;color:var(--ink3);line-height:1.55}

/* ── STACK ── */
.stack-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px}
.stack-card{
  background:var(--white);
  border:1px solid var(--border);
  border-radius:12px;
  padding:20px 20px 16px;
  transition:.15s;
}
.stack-card:hover{border-color:var(--blue-mid)}
.stack-hd{
  display:flex;align-items:center;gap:10px;margin-bottom:14px;
  padding-bottom:12px;border-bottom:1px solid var(--border);
}
.stack-ico{
  width:34px;height:34px;border-radius:8px;
  display:flex;align-items:center;justify-content:center;
  font-size:15px;flex-shrink:0;
}
.ico-blue{background:var(--blue-light);border:1px solid var(--blue-mid);color:var(--blue)}
.ico-violet{background:var(--violet-light);border:1px solid #c9baf7;color:var(--violet)}
.ico-teal{background:var(--teal-light);border:1px solid #b2e8d6;color:var(--teal)}
.ico-amber{background:var(--amber-light);border:1px solid #f5d8a0;color:var(--amber)}
.stack-cat{
  font-family:'Plus Jakarta Sans',sans-serif;
  font-size:14px;font-weight:700;color:var(--ink);
}
.pills{display:flex;flex-wrap:wrap;gap:7px}
.pill{
  font-family:'Fira Code',monospace;font-size:11px;font-weight:400;
  padding:4px 10px;border-radius:6px;
  background:var(--bg);border:1px solid var(--border);
  color:var(--ink2);transition:.15s;cursor:default;
}
.pill:hover{background:var(--blue-light);border-color:var(--blue-mid);color:var(--blue)}
.pill.hot{background:var(--blue-light);border-color:var(--blue-mid);color:var(--blue);font-weight:500}

/* ── GITHUB STATS ── */
.gh-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-bottom:14px}
.gh-img{
  width:100%;display:block;border-radius:10px;
  border:1px solid var(--border);background:var(--white);
}
.gh-wide{
  width:100%;display:block;border-radius:10px;
  border:1px solid var(--border);background:var(--white);
  margin-bottom:14px;
}
.gh-trophy{
  width:100%;display:block;border-radius:10px;
  border:1px solid var(--border);background:var(--white);
}

/* ── CONNECT ── */
.connect-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.conn-card{
  display:flex;align-items:center;gap:14px;
  padding:16px 18px;
  background:var(--white);
  border:1px solid var(--border);
  border-radius:12px;
  text-decoration:none;transition:.2s;
  position:relative;overflow:hidden;
}
.conn-card::after{
  content:'↗';
  position:absolute;right:16px;top:50%;transform:translateY(-50%);
  font-size:15px;font-weight:700;
  opacity:0;transition:.2s;
}
.conn-card:hover{transform:translateY(-1px)}
.conn-card.li:hover{border-color:#0077b5;background:#f0f7ff}
.conn-card.li:hover::after{color:#0077b5;opacity:1}
.conn-card.tw:hover{border-color:#1da1f2;background:#f0f9ff}
.conn-card.tw:hover::after{color:#1da1f2;opacity:1}
.conn-card.yt:hover{border-color:#ff0000;background:#fff5f5}
.conn-card.yt:hover::after{color:#ff0000;opacity:1}
.conn-card.em:hover{border-color:var(--blue);background:var(--blue-light)}
.conn-card.em:hover::after{color:var(--blue);opacity:1}
.conn-ico{
  width:42px;height:42px;border-radius:10px;flex-shrink:0;
  display:flex;align-items:center;justify-content:center;
}
.conn-ico svg{width:20px;height:20px}
.conn-ico.li{background:#e8f4fc;border:1px solid #c5dff5}
.conn-ico.tw{background:#e8f6fd;border:1px solid #b8e3f8}
.conn-ico.yt{background:#fdeaea;border:1px solid #f7c0c0}
.conn-ico.em{background:var(--blue-light);border:1px solid var(--blue-mid)}
.conn-name{font-weight:700;font-size:14px;color:var(--ink);margin-bottom:2px}
.conn-handle{font-family:'Fira Code',monospace;font-size:11px;color:var(--ink3)}

/* ── FOOTER ── */
.footer{
  margin-top:20px;
  padding-top:32px;border-top:1px solid var(--border);
  display:flex;align-items:center;justify-content:space-between;
  flex-wrap:wrap;gap:10px;
}
.footer-l{font-size:13px;color:var(--ink2)}
.footer-l span{color:var(--amber);font-size:16px}
.footer-r{
  font-family:'Fira Code',monospace;font-size:11px;color:var(--ink3);
}

/* ── ANIMATIONS ── */
@keyframes up{from{opacity:0;transform:translateY(16px)}to{opacity:1;transform:translateY(0)}}
.a1{animation:up .5s ease both}
.a2{animation:up .5s .1s ease both}
.a3{animation:up .5s .2s ease both}
.a4{animation:up .5s .3s ease both}
.a5{animation:up .5s .4s ease both}
</style>
</head>
<body>

<!-- TOP BAR -->
<nav class="topbar">
  <span class="topbar-logo">veerbhan.dev</span>
  <div class="topbar-nav">
    <a class="topbar-link" href="https://www.linkedin.com/in/veerbhansinghtomar/">LinkedIn</a>
    <a class="topbar-link" href="https://twitter.com/TomarVeerbhan">Twitter</a>
    <a class="topbar-link" href="https://www.youtube.com/c/WingTech">YouTube</a>
    <a class="topbar-link" href="mailto:your-email@gmail.com">Email</a>
  </div>
</nav>

<div class="page">

  <!-- HERO -->
  <div class="hero a1">
    <div>
      <div class="hero-eyebrow">
        <span class="pulse"></span>
        Available for senior roles &amp; freelance
      </div>
      <h1>Veerbhan<br/><em>Singh Tomar</em></h1>
      <p class="hero-role">// Senior <b>.NET Full Stack Developer</b> · 8+ Years</p>
      <p class="hero-bio">
        Building <strong>enterprise-grade web applications</strong>, high-performance REST APIs, and scalable systems with
        <strong>ASP.NET Core, C#, SQL Server</strong> &amp; Azure.
        Passionate about clean architecture and mentoring developers.
      </p>
      <div class="cta-row">
        <a class="cta-primary" href="https://www.linkedin.com/in/veerbhansinghtomar/">↗ Connect on LinkedIn</a>
        <a class="cta-secondary" href="https://www.youtube.com/c/WingTech">▶ WingTech on YouTube</a>
      </div>
    </div>
    <div class="avatar-wrap">
      <div class="avatar-ring">
        <div class="avatar-circle">VST</div>
      </div>
      <div class="avatar-badge">⬡ 8+ Years Experience</div>
      <div class="view-badge">
        <img src="https://komarev.com/ghpvc/?username=veerbhansinghtomar&label=&color=1e5fe8&style=flat-square" alt="views" style="height:18px"/>
        <span>profile views</span>
      </div>
    </div>
  </div>

  <!-- STATS -->
  <div class="stats a2">
    <div class="stat">
      <span class="stat-val"><span class="hi">8</span>+</span>
      <span class="stat-lbl">Years of Exp.</span>
    </div>
    <div class="stat">
      <span class="stat-val">50<span class="hi">+</span></span>
      <span class="stat-lbl">Projects Shipped</span>
    </div>
    <div class="stat">
      <span class="stat-val"><span class="hi">∞</span></span>
      <span class="stat-lbl">Lines of C#</span>
    </div>
    <div class="stat">
      <span class="stat-val">1<span class="hi">k+</span></span>
      <span class="stat-lbl">Git Commits</span>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="sec a2">
    <div class="sec-hd">
      <span class="sec-num">01 · about</span>
      <span class="sec-title">About Me</span>
      <div class="sec-line"></div>
    </div>
    <div class="about-grid">
      <div class="about-item"><span class="ck">✓</span><span>Senior <strong>Full Stack .NET Developer</strong></span></div>
      <div class="about-item"><span class="ck">✓</span><span>Expert in <strong>N-Tier Architecture</strong></span></div>
      <div class="about-item"><span class="ck">✓</span><span><strong>8+ Years</strong> in Enterprise Web Dev</span></div>
      <div class="about-item"><span class="ck">✓</span><span>Passionate about <strong>Clean Code</strong></span></div>
      <div class="about-item"><span class="ck">✓</span><span>Deep expertise in <strong>ASP.NET Core &amp; Web API</strong></span></div>
      <div class="about-item"><span class="ck">✓</span><span>Mentoring &amp; <strong>Technical Leadership</strong></span></div>
    </div>
  </div>

  <!-- WHAT I BUILD -->
  <div class="sec a3">
    <div class="sec-hd">
      <span class="sec-num">02 · builds</span>
      <span class="sec-title">What I Build</span>
      <div class="sec-line"></div>
    </div>
    <div class="build-grid">
      <div class="build-card">
        <span class="build-num">// 001</span>
        <span class="build-icon">🏢</span>
        <div class="build-name">Enterprise Web Apps</div>
        <div class="build-desc">Scalable, maintainable apps for real business needs with solid architecture.</div>
      </div>
      <div class="build-card">
        <span class="build-num">// 002</span>
        <span class="build-icon">⚡</span>
        <div class="build-name">REST APIs</div>
        <div class="build-desc">High-performance APIs with ASP.NET Core — secure, documented &amp; tested.</div>
      </div>
      <div class="build-card">
        <span class="build-num">// 003</span>
        <span class="build-icon">☁️</span>
        <div class="build-name">Cloud Backend Systems</div>
        <div class="build-desc">Distributed, Azure-ready backend services built for scale.</div>
      </div>
      <div class="build-card">
        <span class="build-num">// 004</span>
        <span class="build-icon">🗄️</span>
        <div class="build-name">Database Solutions</div>
        <div class="build-desc">Optimized SQL Server schemas, procedures &amp; data models.</div>
      </div>
      <div class="build-card">
        <span class="build-num">// 005</span>
        <span class="build-icon">🔍</span>
        <div class="build-name">SEO-Optimized Sites</div>
        <div class="build-desc">Fast, crawlable web apps with server-side rendering &amp; structured data.</div>
      </div>
      <div class="build-card">
        <span class="build-num">// 006</span>
        <span class="build-icon">🎓</span>
        <div class="build-name">Technical Mentoring</div>
        <div class="build-desc">Code reviews, architecture sessions, and team upskilling on WingTech.</div>
      </div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="sec a3">
    <div class="sec-hd">
      <span class="sec-num">03 · stack</span>
      <span class="sec-title">Tech Stack</span>
      <div class="sec-line"></div>
    </div>
    <div class="stack-grid">
      <div class="stack-card">
        <div class="stack-hd">
          <div class="stack-ico ico-blue">⬡</div>
          <span class="stack-cat">Backend</span>
        </div>
        <div class="pills">
          <span class="pill hot">ASP.NET Core</span>
          <span class="pill hot">.NET MVC</span>
          <span class="pill hot">Web API</span>
          <span class="pill hot">C#</span>
          <span class="pill">Entity Framework</span>
          <span class="pill">LINQ</span>
          <span class="pill">SignalR</span>
          <span class="pill">Dapper</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-hd">
          <div class="stack-ico ico-violet">◈</div>
          <span class="stack-cat">Frontend</span>
        </div>
        <div class="pills">
          <span class="pill">HTML5</span>
          <span class="pill">CSS3</span>
          <span class="pill">JavaScript</span>
          <span class="pill">Angular</span>
          <span class="pill">Bootstrap</span>
          <span class="pill">jQuery</span>
          <span class="pill">React</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-hd">
          <div class="stack-ico ico-teal">◫</div>
          <span class="stack-cat">Database</span>
        </div>
        <div class="pills">
          <span class="pill hot">SQL Server</span>
          <span class="pill">MySQL</span>
          <span class="pill">T-SQL</span>
          <span class="pill">Stored Procedures</span>
          <span class="pill">SSRS</span>
          <span class="pill">SSIS</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-hd">
          <div class="stack-ico ico-amber">◆</div>
          <span class="stack-cat">Cloud &amp; Tools</span>
        </div>
        <div class="pills">
          <span class="pill">Azure</span>
          <span class="pill">Git</span>
          <span class="pill">GitHub</span>
          <span class="pill">Visual Studio</span>
          <span class="pill">VS Code</span>
          <span class="pill">Postman</span>
          <span class="pill">Docker</span>
        </div>
      </div>
    </div>
  </div>

  <!-- SKILL ICONS -->
  <div class="sec a3">
    <div class="sec-hd">
      <span class="sec-num">04 · tools</span>
      <span class="sec-title">Languages &amp; Tools</span>
      <div class="sec-line"></div>
    </div>
    <div style="background:var(--white);border:1px solid var(--border);border-radius:12px;padding:24px;text-align:center">
      <img src="https://skillicons.dev/icons?i=dotnet,cs,js,html,css,bootstrap,angular,react,mysql,git,github,vscode,azure&theme=light" alt="Tech Skills" style="max-width:100%;border-radius:6px"/>
    </div>
  </div>

  <!-- GITHUB STATS -->
  <div class="sec a4">
    <div class="sec-hd">
      <span class="sec-num">05 · github</span>
      <span class="sec-title">GitHub Stats</span>
      <div class="sec-line"></div>
    </div>
    <div class="gh-grid">
      <img class="gh-img"
        src="https://github-readme-stats.vercel.app/api?username=veerbhansinghtomar&show_icons=true&theme=default&hide_border=true&bg_color=ffffff&title_color=1e5fe8&icon_color=6c3de8&text_color=4a4540&border_radius=10"
        alt="GitHub Stats"/>
      <img class="gh-img"
        src="https://github-readme-streak-stats.herokuapp.com/?user=veerbhansinghtomar&theme=default&hide_border=true&background=ffffff&ring=1e5fe8&fire=6c3de8&currStreakLabel=1e5fe8&border_radius=10"
        alt="GitHub Streak"/>
    </div>
    <img class="gh-wide"
      src="https://github-readme-stats.vercel.app/api/top-langs/?username=veerbhansinghtomar&layout=compact&theme=default&hide_border=true&bg_color=ffffff&title_color=1e5fe8&text_color=4a4540&border_radius=10"
      alt="Top Languages"/>
    <img class="gh-trophy"
      src="https://github-profile-trophy.vercel.app/?username=veerbhansinghtomar&theme=flat&no-frame=true&no-bg=true&column=7"
      alt="GitHub Trophies"/>
  </div>

  <!-- CONNECT -->
  <div class="sec a5">
    <div class="sec-hd">
      <span class="sec-num">06 · connect</span>
      <span class="sec-title">Connect With Me</span>
      <div class="sec-line"></div>
    </div>
    <div class="connect-grid">
      <a class="conn-card li" href="https://www.linkedin.com/in/veerbhansinghtomar/">
        <div class="conn-ico li">
          <svg viewBox="0 0 24 24" fill="none" stroke="#0077b5" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
            <path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/>
          </svg>
        </div>
        <div><div class="conn-name">LinkedIn</div><div class="conn-handle">veerbhansinghtomar</div></div>
      </a>
      <a class="conn-card tw" href="https://twitter.com/TomarVeerbhan">
        <div class="conn-ico tw">
          <svg viewBox="0 0 24 24" fill="none" stroke="#1da1f2" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
            <path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"/>
          </svg>
        </div>
        <div><div class="conn-name">Twitter / X</div><div class="conn-handle">@TomarVeerbhan</div></div>
      </a>
      <a class="conn-card yt" href="https://www.youtube.com/c/WingTech">
        <div class="conn-ico yt">
          <svg viewBox="0 0 24 24" fill="none" stroke="#ff0000" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
            <path d="M22.54 6.42a2.78 2.78 0 00-1.94-1.96C18.88 4 12 4 12 4s-6.88 0-8.6.46a2.78 2.78 0 00-1.94 1.96A29 29 0 001 12a29 29 0 00.46 5.58A2.78 2.78 0 003.4 19.54C5.12 20 12 20 12 20s6.88 0 8.6-.46a2.78 2.78 0 001.94-1.96A29 29 0 0023 12a29 29 0 00-.46-5.58z"/><polygon points="9.75 15.02 15.5 12 9.75 8.98 9.75 15.02" fill="#ff0000" stroke="none"/>
          </svg>
        </div>
        <div><div class="conn-name">YouTube</div><div class="conn-handle">WingTech Channel</div></div>
      </a>
      <a class="conn-card em" href="mailto:veerbhansingh2705@gmail.com">
        <div class="conn-ico em">
          <svg viewBox="0 0 24 24" fill="none" stroke="#1e5fe8" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
            <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/>
          </svg>
        </div>
        <div><div class="conn-name">Email</div><div class="conn-handle">veerbhansingh2705@gmail.com</div></div>
      </a>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer a5">
    <span class="footer-l"><span>⭐</span> If my work helps you — please star my repositories. It motivates me to build more!</span>
    <span class="footer-r">// Crafted with C# &amp; coffee ☕</span>
  </div>

</div>
</body>
</html>
