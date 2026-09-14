[index.html](https://github.com/user-attachments/files/32188862/index.html)
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>陈佳佳 · 游戏社区运营个人主页</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Noto+Serif+SC:wght@300;400;500;700;900&family=Noto+Sans+SC:wght@300;400;500;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #fbfbf9;
    --card: #ffffff;
    --text: #1a1a1a;
    --soft: #4b4b4b;
    --muted: #8a8a8a;
    --line: #e8e4dc;
    --line-soft: #f2efe8;
    --accent: #b8860b;
    --highlight: #fff8e7;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    font-family: "Noto Sans SC", sans-serif;
    color: var(--text);
    background: var(--bg);
    line-height: 1.75;
  }
  .topbar {
    position: sticky;
    top: 0;
    z-index: 20;
    background: rgba(251, 251, 249, 0.95);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--line);
  }
  .topbar-inner, .wrap { max-width: 1100px; margin: 0 auto; padding: 0 36px; }
  .topbar-inner {
    min-height: 66px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .brand {
    font-family: "Playfair Display", serif;
    font-size: 22px;
    font-weight: 700;
    letter-spacing: 1px;
  }
  .brand span { color: var(--accent); font-style: italic; }
  .nav { list-style: none; display: flex; gap: 24px; }
  .nav a {
    text-decoration: none;
    color: var(--soft);
    font-size: 13px;
    font-family: "JetBrains Mono", monospace;
    letter-spacing: 1px;
  }
  .hero {
    border-bottom: 1px solid var(--line);
    padding: 78px 0 62px;
  }
  .hero-mark {
    font-family: "JetBrains Mono", monospace;
    font-size: 11px;
    letter-spacing: 3px;
    color: var(--muted);
    margin-bottom: 22px;
  }
  .hero h1 {
    font-family: "Noto Serif SC", serif;
    font-size: 82px;
    line-height: 1;
    letter-spacing: -2px;
    margin-bottom: 8px;
  }
  .hero h1 em {
    font-family: "Playfair Display", serif;
    font-style: italic;
    font-weight: 400;
    color: var(--accent);
  }
  .hero-sub {
    font-family: "Playfair Display", serif;
    font-size: 27px;
    color: var(--muted);
    margin-bottom: 20px;
    font-style: italic;
  }
  .hero-intro {
    max-width: 760px;
    color: var(--soft);
    font-size: 16px;
  }
  .hero-intro strong { background: var(--highlight); font-weight: 500; color: var(--text); }
  .hero-meta {
    margin-top: 26px;
    display: flex;
    flex-wrap: wrap;
    gap: 8px 18px;
    font-size: 14px;
    color: var(--soft);
  }
  .section {
    border-bottom: 1px solid var(--line);
    padding: 74px 0;
  }
  .section-header {
    display: flex;
    align-items: baseline;
    gap: 18px;
    border-bottom: 1px solid var(--line-soft);
    padding-bottom: 14px;
    margin-bottom: 30px;
  }
  .section-num {
    color: var(--accent);
    font-family: "Playfair Display", serif;
    font-style: italic;
    font-size: 14px;
    letter-spacing: 2px;
  }
  .section-title {
    font-family: "Noto Serif SC", serif;
    font-size: 40px;
    font-weight: 900;
    letter-spacing: -1px;
  }
  .section-en {
    margin-left: auto;
    color: var(--muted);
    font-size: 10px;
    letter-spacing: 3px;
    font-family: "JetBrains Mono", monospace;
  }
  .games-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 18px;
  }
  .game-card {
    background: var(--card);
    border: 1px solid var(--line);
    padding: 24px;
    display: flex;
    gap: 16px;
    transition: all .2s ease;
  }
  .game-card:hover { border-color: var(--accent); transform: translateY(-2px); }
  .game-card img {
    width: 68px;
    height: 68px;
    border-radius: 16px;
    object-fit: cover;
    flex-shrink: 0;
    border: 1px solid #efefef;
  }
  .game-card h3 {
    font-family: "Noto Serif SC", serif;
    font-size: 24px;
    margin-bottom: 4px;
  }
  .game-card .meta {
    font-family: "JetBrains Mono", monospace;
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 1px;
    margin-bottom: 7px;
  }
  .game-card p { font-size: 14px; color: var(--soft); }
  /* —— 项目经历（产品运营向排版） —— */
  .exp-lead {
    max-width: 720px;
    font-size: 14.5px;
    line-height: 1.85;
    color: var(--soft);
    margin: -12px 0 28px;
    padding: 16px 20px;
    background: var(--highlight);
    border-left: 3px solid var(--accent);
    border-radius: 0 10px 10px 0;
  }
  .exp-lead strong { font-weight: 600; color: var(--text); }
  .exp-track {
    display: flex;
    flex-direction: column;
    gap: 22px;
  }
  .exp-card {
    display: grid;
    grid-template-columns: 168px 1fr;
    background: var(--card);
    border: 1px solid var(--line);
    border-radius: 14px;
    overflow: hidden;
    transition: border-color 0.22s ease, box-shadow 0.22s ease;
  }
  .exp-card:hover {
    border-color: rgba(184, 134, 11, 0.38);
    box-shadow: 0 14px 42px rgba(26, 26, 26, 0.06);
  }
  .exp-card__meta {
    padding: 22px 18px;
    background: linear-gradient(165deg, var(--line-soft) 0%, rgba(251, 251, 249, 0.9) 100%);
    border-right: 1px solid var(--line);
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
  .exp-date {
    font-family: "JetBrains Mono", monospace;
    font-size: 11px;
    letter-spacing: 0.5px;
    color: var(--muted);
    line-height: 1.55;
  }
  .exp-skills {
    list-style: none;
    margin: 20px 0 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    gap: 7px;
    width: 100%;
  }
  .exp-skills li {
    font-family: "JetBrains Mono", monospace;
    font-size: 9px;
    letter-spacing: 0.8px;
    text-transform: uppercase;
    color: var(--soft);
    border: 1px solid var(--line);
    padding: 5px 9px;
    border-radius: 6px;
    background: rgba(255, 255, 255, 0.85);
    line-height: 1.3;
  }
  .exp-card__main {
    padding: 22px 26px 26px;
    min-width: 0;
  }
  .exp-card h4 {
    font-family: "Noto Serif SC", serif;
    font-size: 21px;
    font-weight: 900;
    margin-bottom: 6px;
    letter-spacing: -0.3px;
    color: var(--text);
  }
  .exp-role {
    font-size: 12px;
    color: var(--accent);
    font-family: "JetBrains Mono", monospace;
    letter-spacing: 1px;
    margin-bottom: 18px;
    padding-bottom: 14px;
    border-bottom: 1px dashed var(--line);
  }
  .exp-role span {
    font-family: "Playfair Display", serif;
    font-style: italic;
    letter-spacing: 0;
    margin-left: 8px;
    color: var(--muted);
  }
  .quest-blocks {
    margin: 0;
    display: grid;
    gap: 12px;
  }
  @media (min-width: 900px) {
    .quest-blocks {
      grid-template-columns: repeat(3, 1fr);
      gap: 14px;
    }
  }
  .quest-block {
    padding: 14px 14px 14px 16px;
    background: var(--bg);
    border: 1px solid var(--line-soft);
    border-radius: 10px;
    border-left: 3px solid var(--accent);
    min-height: 100%;
  }
  .quest-block .quest-sub {
    font-family: "Noto Sans SC", sans-serif;
    font-size: 13px;
    font-weight: 600;
    color: var(--text);
    margin-bottom: 8px;
    letter-spacing: 0.03em;
    line-height: 1.35;
  }
  .quest-block .quest-txt {
    margin: 0;
    font-size: 13.5px;
    color: var(--soft);
    line-height: 1.72;
  }
  /* —— 实习经历 强调卡 —— */
  .exp-card--featured {
    border-color: rgba(184, 134, 11, 0.42);
    box-shadow: 0 10px 34px rgba(184, 134, 11, 0.07);
  }
  .exp-card--featured .exp-card__meta {
    background: linear-gradient(165deg, #fdf6e6 0%, rgba(251, 251, 249, 0.92) 100%);
  }
  .exp-badge {
    display: inline-block;
    font-family: "JetBrains Mono", monospace;
    font-size: 9px;
    letter-spacing: 1.4px;
    text-transform: uppercase;
    color: #8a6508;
    background: var(--highlight);
    border: 1px solid rgba(184, 134, 11, 0.32);
    border-radius: 5px;
    padding: 4px 8px;
    margin-bottom: 12px;
  }
  .exp-metrics {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 10px;
    margin: 0 0 18px;
  }
  .metric {
    background: var(--highlight);
    border: 1px solid rgba(184, 134, 11, 0.2);
    border-radius: 9px;
    padding: 11px 12px;
  }
  .metric b {
    display: block;
    font-family: "Playfair Display", serif;
    font-size: 21px;
    line-height: 1.15;
    color: #8a6508;
    letter-spacing: -0.4px;
  }
  .metric span {
    display: block;
    margin-top: 3px;
    font-size: 10.5px;
    line-height: 1.45;
    color: var(--soft);
    letter-spacing: 0.02em;
  }
  .exp-note {
    margin: 16px 0 0;
    padding-top: 13px;
    border-top: 1px dashed var(--line);
    font-size: 12.5px;
    line-height: 1.7;
    color: var(--muted);
  }
  .exp-note strong { color: var(--soft); font-weight: 600; }
  .works-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 20px;
  }
  .work {
    display: flex;
    flex-direction: column;
  }
  .work p { flex: 1; }
  .resume-dl {
    margin-top: 34px;
  }
  .resume-btn {
    display: inline-flex;
    align-items: center;
    gap: 14px;
    padding: 16px 26px;
    background: var(--text);
    color: #fff;
    text-decoration: none;
    border: 1px solid var(--text);
    transition: background .2s ease, transform .2s ease, box-shadow .2s ease;
  }
  .resume-btn:hover {
    background: var(--accent);
    border-color: var(--accent);
    transform: translateY(-2px);
    box-shadow: 0 10px 26px rgba(184, 134, 11, 0.26);
  }
  .resume-btn__ico {
    font-size: 20px;
    line-height: 1;
    width: 34px;
    height: 34px;
    display: flex;
    align-items: center;
    justify-content: center;
    border: 1px solid rgba(255, 255, 255, 0.35);
    border-radius: 50%;
    flex-shrink: 0;
  }
  .resume-btn b {
    display: block;
    font-family: "Noto Serif SC", serif;
    font-size: 15px;
    font-weight: 700;
    letter-spacing: 1px;
  }
  .resume-btn em {
    display: block;
    margin-top: 3px;
    font-family: "JetBrains Mono", monospace;
    font-style: normal;
    font-size: 10px;
    letter-spacing: 1.4px;
    opacity: 0.72;
  }
  @media (max-width: 640px) {
    .resume-btn { width: 100%; justify-content: center; padding: 15px 18px; }
  }
  .exp-title-with-icon {
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .exp-game-icon {
    width: 40px;
    height: 40px;
    border-radius: 10px;
    border: 1px solid var(--line);
    box-shadow: 0 2px 8px rgba(26, 26, 26, 0.08);
    flex-shrink: 0;
  }
  @media (max-width: 640px) {
    .exp-game-icon { width: 32px; height: 32px; }
  }
  .work-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-bottom: 14px;
  }
  .work-tag {
    font-family: "JetBrains Mono", monospace;
    font-size: 10px;
    letter-spacing: 0.6px;
    color: #8a6508;
    background: var(--highlight);
    border: 1px solid rgba(184, 134, 11, 0.28);
    border-radius: 999px;
    padding: 4px 10px;
  }
  .work a:hover {
    border-color: var(--accent);
    color: var(--accent);
  }
  .work {
    border: 1px solid var(--line);
    background: var(--card);
    padding: 24px;
  }
  .work-num {
    color: var(--accent);
    font-family: "Playfair Display", serif;
    font-size: 46px;
    line-height: 1;
    margin-bottom: 10px;
    font-style: italic;
  }
  .work h4 {
    font-family: "Noto Serif SC", serif;
    font-size: 20px;
    margin-bottom: 9px;
  }
  .work p { color: var(--soft); font-size: 14px; margin-bottom: 15px; }
  .work-icons {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 14px;
  }
  .work-icons img {
    width: 44px;
    height: 44px;
    border-radius: 12px;
    object-fit: cover;
    border: 1px solid var(--line);
  }
  .work a {
    display: inline-block;
    text-decoration: none;
    color: var(--text);
    border: 1px solid var(--line);
    padding: 6px 12px;
    font-size: 12px;
    font-family: "JetBrains Mono", monospace;
    letter-spacing: 1px;
  }
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 16px;
  }
  .skill-card {
    background: var(--card);
    border: 1px solid var(--line);
    border-radius: 12px;
    padding: 22px 20px 20px;
    min-height: 100%;
    transition: border-color 0.2s ease, box-shadow 0.2s ease, transform 0.2s ease;
  }
  .skill-card:hover {
    border-color: rgba(184, 134, 11, 0.45);
    box-shadow: 0 10px 32px rgba(26, 26, 26, 0.06);
    transform: translateY(-2px);
  }
  .skill-card h3 {
    font-family: "Noto Serif SC", serif;
    font-size: 17px;
    font-weight: 700;
    margin: 0 0 14px;
    padding-bottom: 12px;
    border-bottom: 1px solid var(--line-soft);
    color: var(--text);
    letter-spacing: 0.02em;
  }
  .skill-card ul {
    list-style: none;
    margin: 0;
    padding: 0;
  }
  .skill-card li {
    position: relative;
    font-size: 13.5px;
    color: var(--soft);
    line-height: 1.65;
    padding: 5px 0 5px 14px;
  }
  .skill-card li::before {
    content: "";
    position: absolute;
    left: 0;
    top: 0.72em;
    width: 5px;
    height: 5px;
    border-radius: 50%;
    background: var(--accent);
    opacity: 0.85;
  }
  .contact {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    border: 1px solid var(--line);
    background: var(--card);
  }
  .contact-item {
    padding: 20px;
    text-align: center;
    border-right: 1px solid var(--line);
  }
  .contact-item:last-child { border-right: none; }
  .contact-label {
    font-family: "JetBrains Mono", monospace;
    color: var(--muted);
    font-size: 10px;
    letter-spacing: 2px;
    margin-bottom: 6px;
  }
  .foot {
    text-align: center;
    padding: 36px 0 52px;
    color: var(--muted);
    font-size: 12px;
    letter-spacing: 2px;
    font-family: "JetBrains Mono", monospace;
  }
  @media (max-width: 850px) {
    .topbar-inner, .wrap { padding: 0 22px; }
    .nav { display: none; }
    .hero h1 { font-size: 54px; }
    .hero-sub { font-size: 20px; }
    .games-grid, .works-grid, .skills-grid, .contact { grid-template-columns: 1fr; }
    .exp-card { grid-template-columns: 1fr; }
    .exp-card__meta {
      border-right: none;
      border-bottom: 1px solid var(--line);
      flex-direction: row;
      flex-wrap: wrap;
      align-items: center;
      gap: 12px 16px;
    }
    .exp-skills {
      flex-direction: row;
      flex-wrap: wrap;
      margin: 0;
      width: auto;
      gap: 6px;
    }
    .quest-blocks { grid-template-columns: 1fr; }
    .exp-metrics { grid-template-columns: repeat(2, minmax(0, 1fr)); }
    .contact-item { border-right: none; border-bottom: 1px solid var(--line); }
    .contact-item:last-child { border-bottom: none; }
    .section-title { font-size: 29px; }
  }
  @media (max-width: 900px) and (min-width: 851px) {
    .skills-grid { grid-template-columns: repeat(2, minmax(0, 1fr)); }
  }
</style>
</head>
<body>
  <header class="topbar">
    <div class="topbar-inner">
      <div class="brand">Chen <span>Jiajia</span></div>
      <nav>
        <ul class="nav">
          <li><a href="#about">ABOUT</a></li>
          <li><a href="#games">GAMES</a></li>
          <li><a href="#internship">INTERNSHIP</a></li>
          <li><a href="#experience">EXPERIENCE</a></li>
          <li><a href="#works">WORKS</a></li>
          <li><a href="#skills">SKILLS</a></li>
          <li><a href="#contact">CONTACT</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <section class="hero" id="about">
    <div class="wrap">
      <div class="hero-mark">PERSONAL PORTFOLIO · 2026</div>
      <h1>陈<em>佳佳</em></h1>
      <div class="hero-sub">A player. A community operator.</div>
      <p class="hero-intro">
        深圳大学工商管理本科在读，曾于深圳冰川网络《我要当老祖》项目组担任社区运营实习生，
        完整经历产品<strong>内测末期 — 公测上线 — 暑期大版本</strong>的运营周期。
        具备多平台内容运营、活动策划落地、玩家社区氛围建设与跨团队协同能力；
        以玩家身份长期深度体验放置类与 MMORPG 产品，习惯用<strong>“用户问题-运营动作-结果反馈”</strong>进行拆解和记录。
      </p>
      <div class="hero-meta">
        <span>📞 19200420107</span>
        <span>📧 13826118669@163.com</span>
        <span>💬 a1048955336</span>
        <span>📍 深圳</span>
      </div>
    </div>
  </section>

  <section class="section" id="games">
    <div class="wrap">
      <div class="section-header">
        <div class="section-num">Chapter 01</div>
        <div class="section-title">游戏档案</div>
        <div class="section-en">GAME PROFILE</div>
      </div>
      <div class="games-grid">
        <article class="game-card">
          <img src="./assets/icons/zhangjianchuanshuo.png" alt="杖剑传说图标">
          <div>
            <h3>杖剑传说</h3>
            <div class="meta">MMORPG · 放置成长 · 7个月深度体验</div>
            <p>内测+公测持续跟进，关注职业平衡、赛季节奏、用户情绪与社区讨论变化。</p>
          </div>
        </article>
        <article class="game-card">
          <img src="./assets/icons/valorant.png" alt="无畏契约图标">
          <div>
            <h3>无畏契约</h3>
            <div class="meta">FPS · 竞技体系 · 2年</div>
            <p>长期体验排位生态，关注版本平衡对局内行为与玩家反馈节奏的影响。</p>
          </div>
        </article>
        <article class="game-card">
          <img src="./assets/icons/lol.png" alt="英雄联盟图标">
          <div>
            <h3>英雄联盟</h3>
            <div class="meta">MOBA · 长线运营 · 3年</div>
            <p>关注活动节点、通行证设计、英雄强度调整对留存与活跃的拉动方式。</p>
          </div>
        </article>
        <article class="game-card">
          <img src="./assets/icons/tower-of-fantasy.png" alt="幻塔图标">
          <div>
            <h3>幻塔</h3>
            <div class="meta">开放世界 · MMO社交 · 2年</div>
            <p>关注大版本更新、跨系统内容投放和长线付费体验的一致性。</p>
          </div>
        </article>
      </div>
    </div>
  </section>

  <section class="section" id="internship">
    <div class="wrap">
      <div class="section-header">
        <div class="section-num">Chapter 02</div>
        <div class="section-title">实习经历</div>
        <div class="section-en">INTERNSHIP</div>
      </div>
      <p class="exp-lead">在<strong>放置类修仙手游《我要当老祖》</strong>项目组，完整经历<strong>内测末期 → 公测上线 → 暑期大版本</strong>的运营周期：从多平台内容供给、活动策划落地，到以官方人格与玩家日常对话、跨部门对齐版本释放节奏，形成一套<strong>可复用的社区运营打法</strong>。</p>
      <div class="exp-track">
        <article class="exp-card exp-card--featured">
          <div class="exp-card__meta">
            <div class="exp-badge">Internship</div>
            <div class="exp-date">2026.05 —<br>2026.08</div>
            <ul class="exp-skills" aria-label="相关能力">
              <li>多平台内容</li>
              <li>活动运营</li>
              <li>玩家沟通</li>
              <li>跨部门协同</li>
              <li>AI 提效</li>
            </ul>
          </div>
          <div class="exp-card__main">
            <h4 class="exp-title-with-icon">
              <img class="exp-game-icon" src="./assets/work04/icon-wdlz.png" alt="" width="40" height="40">
              <span>深圳冰川网络《我要当老祖》项目组</span>
            </h4>
            <div class="exp-role">COMMUNITY OPS INTERN <span>· 社区运营实习生 · 放置类修仙手游</span></div>
            <div class="exp-metrics" aria-label="关键结果">
              <div class="metric"><b>24.8万</b><span>公众号累计阅读人数<br>单篇峰值 1.6 万+</span></div>
              <div class="metric"><b>1.4万</b><span>爆款活动帖浏览<br>留言 2000+</span></div>
              <div class="metric"><b>49万+</b><span>TapTap 社区关注<br>累计发帖 6000+</span></div>
              <div class="metric"><b>前 0.28%</b><span>微信游戏圈访问用户数<br>全平台排名 271/95242</span></div>
            </div>
            <div class="quest-blocks">
              <div class="quest-block">
                <div class="quest-sub">多平台内容运营</div>
                <p class="quest-txt">统筹 TapTap、微信游戏圈、微信公众号、抖音、好游快爆等平台的内容策划与发布，保持<strong>日更 1-2 篇</strong>的稳定供给；主导限定角色长图 SOP、公测内容一览图、暑期活动长图节奏释放等系列内容，形成各平台差异化的内容表达。</p>
              </div>
              <div class="quest-block">
                <div class="quest-sub">活动策划与用户互动</div>
                <p class="quest-txt">主导节日、抽奖等主题活动帖的策划与落地，单帖稳定实现<strong>浏览 5000+、留言 400+</strong>；通过话题设计与互动机制优化持续放大参与度，其中爆款活动帖达成<strong>浏览 1.4 万、留言 2000+</strong> 的社区互动峰值。</p>
              </div>
              <div class="quest-block">
                <div class="quest-sub">官方人格化运营</div>
                <p class="quest-txt">以「<strong>南猫猫</strong>」官方运营身份活跃于各社区平台与玩家社群，主导日常互动与氛围维护；在一线对话中捕捉玩家真实诉求并快速响应传达，让官方形象保有<strong>“真人味”</strong>的同时保持响应效率。</p>
              </div>
              <div class="quest-block">
                <div class="quest-sub">跨部门协同与节奏统筹</div>
                <p class="quest-txt">对接 <strong>GS、客服、美术、研发</strong>等多部门核对新版本释放内容，统筹策划内容的释放节奏与社区侧落地排期，保障版本信息<strong>准确、按节奏、及时</strong>触达玩家。</p>
              </div>
              <div class="quest-block">
                <div class="quest-sub">社区生态与板块搭建</div>
                <p class="quest-txt">参与 TapTap、微信游戏圈、好游快爆、抖音小游戏及游戏自建社区「<strong>论道阁</strong>」的板块搭建与内容体系建设，熟练使用各平台运营功能；期间微信游戏圈粉丝达 <strong>3.7 万+</strong>，<strong>日新增 664 / 退圈仅 15</strong>，沉淀高粘性的玩家社区氛围。</p>
              </div>
              <div class="quest-block">
                <div class="quest-sub">AI 工具提效</div>
                <p class="quest-txt">运用 AI 工具辅助 TapTap 买量素材设计与社区内容生产，参与投放创意迭代，投放实现<strong>点击率 4.74%、详情页转化率 7.54%</strong>；并将 AI 能力嵌入选题策划与长图生产流程，沉淀可复用的内容生产 SOP。</p>
              </div>
            </div>
            <p class="exp-note"><strong>周期覆盖：</strong>内测末期切入 → 公测上线爆发期 → 暑期大版本活动期，完整参与一款长线放置类产品从冷启动到版本运营的社区侧全流程。</p>
          </div>
        </article>
      </div>
    </div>
  </section>

  <section class="section" id="experience">
    <div class="wrap">
      <div class="section-header">
        <div class="section-num">Chapter 03</div>
        <div class="section-title">项目经历</div>
        <div class="section-en">EXPERIENCE</div>
      </div>
      <p class="exp-lead">以下经历按<strong>产品运营</strong>常用能力组织表述：从用户/场景需求拆解目标，用<strong>里程碑与数据</strong>推进迭代，在<strong>跨职能协作</strong>中保障交付，并把可复用流程沉淀为资产——与版本节奏、活动运营、用户触达等岗位场景同构。</p>
      <div class="exp-track">
        <article class="exp-card">
          <div class="exp-card__meta">
            <div class="exp-date">2024.05 —<br>2024.06</div>
            <ul class="exp-skills" aria-label="相关能力">
              <li>0-1 交付</li>
              <li>需求拆解</li>
              <li>用户触达</li>
            </ul>
          </div>
          <div class="exp-card__main">
            <h4>开普勒星人分享会（沙龙）</h4>
            <div class="exp-role">PROJECT OWNER <span>· 策划负责人 · 活动全链路</span></div>
            <div class="quest-blocks">
              <div class="quest-block">
                <div class="quest-sub">需求定义与范围管理</div>
                <p class="quest-txt">识别校内对<strong>互联网行业实习与就业</strong>的路径、岗位与准备节奏等信息需求，以及报名与咨询仍分散在多个触点的现状，将「认知—报名—到场—反馈」收敛为一条可交付链路。在约 <strong>2 个月</strong>内牵头 <strong>6 人</strong>跨小组，对齐方案、嘉宾与物料、宣发节奏、现场流程与复盘文档的<strong>范围与优先级</strong>。</p>
              </div>
              <div class="quest-block">
                <div class="quest-sub">执行推进与风险处置</div>
                <p class="quest-txt">按里程碑拆解任务并同步干系人；将咨询侧沉淀为<strong>50+ 人</strong>社群运营，对高频问题做分类与话术迭代，相当于轻量用户运营与 FAQ 维护。现场突发时快速调整环节顺序，控制风险对<strong>核心体验路径</strong>的影响。</p>
              </div>
              <div class="quest-block">
                <div class="quest-sub">复盘与流程资产</div>
                <p class="quest-txt">交付书面复盘与问题清单，将可重复环节固化为后续同类活动的<strong>流程说明与 FAQ 素材</strong>——对应产品中「文档化 + 降低下次交付成本」的做事方式。</p>
              </div>
            </div>
          </div>
        </article>
        <article class="exp-card">
          <div class="exp-card__meta">
            <div class="exp-date">2024.03 —<br>2024.07</div>
            <ul class="exp-skills" aria-label="相关能力">
              <li>指标意识</li>
              <li>内容迭代</li>
              <li>增长触达</li>
            </ul>
          </div>
          <div class="exp-card__main">
            <h4>深圳大学学生会公众号</h4>
            <div class="exp-role">CONTENT OPS <span>· 内容运营 · 增长向触达</span></div>
            <div class="quest-blocks">
              <div class="quest-block">
                <div class="quest-sub">用户场景与北极星指标</div>
                <p class="quest-txt">校招季信息过载，目标用户更需要<strong>可追更、结构清晰</strong>的就业指导内容。在 <strong>5 个月</strong>内对就业向栏目负责，将<strong>阅读与互动</strong>作为核心观测指标，用推送节奏与选题规划承接「拉新—留存—转化注意力」的运营逻辑。</p>
              </div>
              <div class="quest-block">
                <div class="quest-sub">假设验证与快速迭代</div>
                <p class="quest-txt">从 0 搭建「就业宝典」「job馆」等栏目，把每一次推送当作一次<strong>小版本</strong>：结合阅读与「在看」等数据做标题与信息结构的 A/B 式优化；用秀米统一版式，固化「策划—撰写—发布—数据复盘—改版」闭环，贴近版本迭代中的<strong>数据反馈—调优</strong>习惯。</p>
              </div>
              <div class="quest-block">
                <div class="quest-sub">结果与可复用方法论</div>
                <p class="quest-txt">系列推文累计阅读 <strong>5000+</strong>；沉淀复盘模板与版式规范，便于<strong>新成员按同一标准续写栏目</strong>，与运营侧「SOP + 轻量知识库」的沉淀思路一致。</p>
              </div>
            </div>
          </div>
        </article>
        <article class="exp-card">
          <div class="exp-card__meta">
            <div class="exp-date">2023.09 —<br>2024.12</div>
            <ul class="exp-skills" aria-label="相关能力">
              <li>多项目</li>
              <li>资源协调</li>
              <li>里程碑</li>
            </ul>
          </div>
          <div class="exp-card__main">
            <h4>深圳大学（丽湖）学生会实践部</h4>
            <div class="exp-role">TEAM LEAD <span>· 部门负责人 · 资源与节奏</span></div>
            <div class="quest-blocks">
              <div class="quest-block">
                <div class="quest-sub">复杂场景下的优先级</div>
                <p class="quest-txt">就业季并行分享会、就业电台、春秋招、沙龙等多条「产品线」，宣传、场置与现场执行<strong>资源竞争</strong>明显。在 <strong>约 16 个月</strong>内以负责人身份做分工与排期，让单场活动从预告到撤场的<strong>关键路径可追踪</strong>，类似多版本并行时的节奏管理。</p>
              </div>
              <div class="quest-block">
                <div class="quest-sub">跨职能落地与关键场次</div>
                <p class="quest-txt">将物料、人力与时间节点<strong>清单化</strong>，对齐设计、宣传与现场多方交付物，推进宣发与现场执行无缝衔接，保障重点场次<strong>峰值体验</strong>可控。</p>
              </div>
              <div class="quest-block">
                <div class="quest-sub">交付质量与协作机制</div>
                <p class="quest-txt">在多项目重叠下保持<strong>节点按期交付</strong>；通过固定对齐节奏降低跨组信息差与重复劳动，使协作方式可复用到下一届活动——对应产运中「稳定交付 + 降低沟通税」。</p>
              </div>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>

  <section class="section" id="works">
    <div class="wrap">
      <div class="section-header">
        <div class="section-num">Chapter 04</div>
        <div class="section-title">作品集</div>
        <div class="section-en">WORKS</div>
      </div>
      <div class="works-grid">
        <article class="work">
          <div class="work-num">01</div>
          <h4>《杖剑传说》玩家反馈分析</h4>
          <p>围绕玩家讨论高频问题，提炼情绪焦点与可执行优化建议，展示“反馈-判断-动作”能力。</p>
          <a href="./work-01-player-feedback.html">OPEN PAGE</a>
        </article>
        <article class="work">
          <div class="work-num">02</div>
          <h4>放置类竞品横评</h4>
          <div class="work-icons" aria-hidden="true">
            <img src="./assets/work02/icon-xdds.png" alt="" width="44" height="44">
            <img src="./assets/work02/icon-zjcs.png" alt="" width="44" height="44">
            <img src="./assets/work02/icon-xyzw.png" alt="" width="44" height="44">
          </div>
          <div class="work-tags">
            <span class="work-tag">竞品分析</span>
            <span class="work-tag">商业化</span>
            <span class="work-tag">留存路径</span>
          </div>
          <p>对比三款头部产品的题材、玩法、商业化与留存路径，提炼可迁移的运营启示。</p>
          <a href="./work-02-idle-competitors.html">OPEN PAGE</a>
        </article>
        <article class="work">
          <div class="work-num">03</div>
          <h4>《我的勇者》七周年<br>TapTap 社区运营节奏分析</h4>
          <div class="work-icons" aria-hidden="true">
            <img src="./assets/work03/icon-wdyz.png" alt="" width="44" height="44">
          </div>
          <div class="work-tags">
            <span class="work-tag">节奏拆解</span>
            <span class="work-tag">UGC 引导</span>
            <span class="work-tag">危机响应</span>
          </div>
          <p>完整跟踪官方号 16 天、五阶段共 17 条发帖节奏，拆解互动设计、话题标签、礼包码与 UGC 引导策略，总结六条可复用的社区运营手法。</p>
          <a href="./work-03-community-rhythm.html">OPEN PAGE</a>
        </article>
        <article class="work">
          <div class="work-num">04</div>
          <h4>《我要当老祖》<br>社区运营内容作品集</h4>
          <div class="work-icons" aria-hidden="true">
            <img src="./assets/work04/icon-wdlz.png" alt="" width="44" height="44">
          </div>
          <div class="work-tags">
            <span class="work-tag">买量图</span>
            <span class="work-tag">长图</span>
            <span class="work-tag">社区内容图</span>
            <span class="work-tag">表情包</span>
          </div>
          <p>实习期间产出的社区视觉内容合集，涵盖 TapTap 买量素材、版本长图、社区内容配图与官方表情包设计。</p>
          <a href="./work-04-visual-works.html">OPEN PAGE</a>
        </article>
      </div>
    </div>
  </section>

  <section class="section" id="skills">
    <div class="wrap">
      <div class="section-header">
        <div class="section-num">Chapter 05</div>
        <div class="section-title">能力与工具</div>
        <div class="section-en">CAPABILITIES & TOOLS</div>
      </div>
      <div class="skills-grid">
        <article class="skill-card">
          <h3>游戏洞察与产品思维</h3>
          <ul>
            <li>主玩放置类与 MMORPG，习惯主动拆解游戏设计意图与运营逻辑</li>
            <li>深度参与放置类修仙产品从内测末期到公测、暑期大版本的完整运营周期</li>
            <li>独立产出玩家反馈分析与放置类竞品横评报告</li>
            <li>能将玩家体验转化为可执行的产品与运营洞察</li>
          </ul>
        </article>
        <article class="skill-card">
          <h3>内容策划与数据运营</h3>
          <ul>
            <li>限定角色长图 SOP、版本内容一览图、活动长图节奏释放等系列内容策划</li>
            <li>覆盖 TapTap、微信游戏圈、公众号、抖音、好游快爆等多平台分发</li>
            <li>持续追踪传播数据并迭代选题方向</li>
            <li>形成“策划—发布—数据复盘—调优”的完整运营闭环</li>
          </ul>
        </article>
        <article class="skill-card">
          <h3>跨团队协作与用户运营</h3>
          <ul>
            <li>与 GS、客服、美术、研发等多部门协同沟通</li>
            <li>核对新版本释放内容并统筹内容释放节奏</li>
            <li>以官方运营人格活跃于社区，捕捉并传达真实玩家需求</li>
            <li>在保持官方响应效率的同时保有“真人味”的运营形象</li>
          </ul>
        </article>
        <article class="skill-card">
          <h3>活动执行与落地能力</h3>
          <ul>
            <li>节日、抽奖等主题社区活动全流程策划与落地</li>
            <li>通过话题设计与互动机制激发玩家参与</li>
            <li>带领团队完成线下沙龙方案制定与执行</li>
            <li>搭建用户运营群并基于反馈持续优化活动体验</li>
          </ul>
        </article>
        <article class="skill-card">
          <h3>AI 工具应用与自驱学习</h3>
          <ul>
            <li>Claude · Seedance · GPT Image 等 AI 工具应用</li>
            <li>辅助买量素材设计、社区内容生产与竞品分析</li>
            <li>能将 AI 能力落地为可交付产出与可复用 SOP</li>
            <li>学习能力强、适应性高，能在高压环境下保持效率</li>
          </ul>
        </article>
        <article class="skill-card">
          <h3>设计与办公工具</h3>
          <ul>
            <li>Photoshop · 剪映</li>
            <li>飞书 · Word · Excel · PPT</li>
            <li>TapTap / 微信游戏圈 / 公众号等各平台创作者后台</li>
            <li>活动主视觉、长图版式与数据材料产出</li>
          </ul>
        </article>
      </div>
    </div>
  </section>

  <section class="section" id="contact" style="border-bottom:none;">
    <div class="wrap">
      <div class="section-header">
        <div class="section-num">Chapter 06</div>
        <div class="section-title">联系方式</div>
        <div class="section-en">OPEN TO OPPORTUNITIES</div>
      </div>
      <div class="contact">
        <div class="contact-item">
          <div class="contact-label">PHONE</div>
          <div>19200420107</div>
        </div>
        <div class="contact-item">
          <div class="contact-label">EMAIL</div>
          <div>13826118669@163.com</div>
        </div>
        <div class="contact-item">
          <div class="contact-label">WECHAT</div>
          <div>a1048955336</div>
        </div>
      </div>
      <div class="resume-dl">
        <a class="resume-btn" href="./resume.pdf" target="_blank" rel="noopener">
          <span class="resume-btn__ico" aria-hidden="true">&#8595;</span>
          <span>
            <b>下载完整简历</b>
            <em>PDF · 陈佳佳 · 游戏社区运营</em>
          </span>
        </a>
      </div>
    </div>
  </section>

  <footer class="foot">CHEN JIAJIA · GAME COMMUNITY OPERATIONS PORTFOLIO · 2026</footer>
</body>
</html>
