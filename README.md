<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fanfan Wang · fresh dev profile</title>
  <!-- Font & minimal styling -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #f9fafc;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
      padding: 2rem 1.5rem;
      color: #1e293b;
    }

    .card {
      max-width: 1000px;
      width: 100%;
      background: #ffffff;
      border-radius: 40px;
      padding: 3rem 3rem 2.8rem;
      box-shadow: 0 20px 60px -12px rgba(0, 0, 0, 0.06), 0 8px 24px -6px rgba(0, 0, 0, 0.02);
      transition: all 0.2s ease;
      border: 1px solid rgba(255, 255, 255, 0.5);
      backdrop-filter: blur(2px);
    }

    /* TYPOGRAPHY – fresh, airy */
    .greeting {
      text-align: center;
      margin-bottom: 2.2rem;
    }

    .greeting-svg {
      max-width: 100%;
      height: auto;
    }

    .greeting-svg img {
      width: 100%;
      height: auto;
      display: block;
    }

    .divider {
      border: 0;
      height: 1px;
      background: linear-gradient(to right, transparent, #e2e8f0, transparent);
      margin: 2rem 0 2.2rem;
    }

    .section-title {
      font-weight: 600;
      font-size: 0.85rem;
      letter-spacing: 0.03em;
      text-transform: uppercase;
      color: #94a3b8;
      margin-bottom: 1.2rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .section-title span {
      background: #f1f5f9;
      padding: 0.2rem 0.8rem;
      border-radius: 40px;
      font-size: 0.7rem;
      color: #475569;
      letter-spacing: 0;
    }

    /* tech badges – clean, rounded, subtle */
    .badge-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.6rem 0.7rem;
      margin: 0.4rem 0 0.2rem;
    }

    .badge {
      background: #f1f5f9;
      color: #1e293b;
      padding: 0.45rem 1rem;
      border-radius: 40px;
      font-size: 0.8rem;
      font-weight: 500;
      letter-spacing: -0.01em;
      transition: all 0.15s ease;
      border: 1px solid #e9edf2;
      box-shadow: 0 1px 2px rgba(0,0,0,0.02);
      display: inline-flex;
      align-items: center;
      gap: 6px;
    }

    .badge:hover {
      background: #eef2f7;
      border-color: #cbd5e1;
      transform: translateY(-1px);
      box-shadow: 0 6px 14px -8px rgba(0,0,0,0.08);
    }

    .badge i {
      font-style: normal;
      font-weight: 400;
      opacity: 0.7;
    }

    /* project table – minimal */
    .project-grid {
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
      margin-top: 0.2rem;
    }

    .project-row {
      display: grid;
      grid-template-columns: 1.1fr 2.2fr 1.3fr;
      gap: 1rem;
      align-items: start;
      background: #fafcff;
      padding: 1rem 1.2rem;
      border-radius: 20px;
      border: 1px solid #f0f3f8;
      transition: background 0.15s;
    }

    .project-row:hover {
      background: #f6f9ff;
      border-color: #e2eaf5;
    }

    .project-name {
      font-weight: 600;
      font-size: 0.95rem;
      color: #0b1e33;
      letter-spacing: -0.01em;
      display: flex;
      align-items: center;
      gap: 4px;
    }

    .project-name a {
      color: #1e4b7a;
      text-decoration: none;
      border-bottom: 1px dotted rgba(30, 75, 122, 0.2);
    }

    .project-name a:hover {
      border-bottom: 1px solid #1e4b7a;
      color: #0b2c4a;
    }

    .project-desc {
      font-size: 0.9rem;
      line-height: 1.5;
      color: #334155;
      font-weight: 400;
    }

    .project-tech {
      font-size: 0.75rem;
      font-weight: 500;
      color: #64748b;
      background: #f1f5f9;
      padding: 0.3rem 0.9rem;
      border-radius: 30px;
      display: inline-block;
      border: 1px solid #e9edf2;
      letter-spacing: -0.01em;
      white-space: nowrap;
    }

    .project-tech-wrap {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      align-items: center;
    }

    /* what i'm doing – clean list */
    .doing-list {
      display: flex;
      flex-direction: column;
      gap: 0.8rem;
      margin-top: 0.2rem;
    }

    .doing-item {
      display: flex;
      align-items: baseline;
      gap: 0.6rem;
      font-size: 0.95rem;
      line-height: 1.5;
      color: #1e293b;
      padding: 0.2rem 0;
      border-bottom: 1px solid #f1f5f9;
    }

    .doing-item strong {
      font-weight: 600;
      color: #0b1e33;
      min-width: 80px;
    }

    .doing-item .light {
      color: #64748b;
      font-weight: 400;
    }

    .doing-item .tag {
      background: #eef2f6;
      padding: 0.15rem 0.7rem;
      border-radius: 30px;
      font-size: 0.75rem;
      font-weight: 500;
      color: #2c3e5c;
      margin-left: 0.2rem;
    }

    .contact-row {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1.2rem 2.2rem;
      margin-top: 0.8rem;
    }

    .contact-item {
      font-size: 0.9rem;
      color: #1e293b;
      display: flex;
      align-items: center;
      gap: 0.3rem;
    }

    .contact-item a {
      color: #1e4b7a;
      text-decoration: none;
      font-weight: 500;
      border-bottom: 1px solid transparent;
      transition: 0.1s;
    }

    .contact-item a:hover {
      border-bottom-color: #1e4b7a;
    }

    .tag-cloud {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.5rem 0.7rem;
      margin: 0.6rem 0 0.2rem;
    }

    .tag-pill {
      background: #eef2f6;
      padding: 0.2rem 1rem;
      border-radius: 30px;
      font-size: 0.75rem;
      font-weight: 500;
      color: #2c3e5c;
      letter-spacing: -0.01em;
      border: 1px solid #e2e8f0;
    }

    .footer-meta {
      text-align: center;
      font-size: 0.75rem;
      color: #94a3b8;
      margin-top: 2.2rem;
      letter-spacing: 0.01em;
    }

    /* responsive */
    @media (max-width: 700px) {
      .card { padding: 2rem 1.5rem; }
      .project-row {
        grid-template-columns: 1fr;
        gap: 0.5rem;
        padding: 1rem;
      }
      .project-name { font-size: 1rem; }
      .project-tech-wrap { margin-top: 0.2rem; }
      .doing-item { flex-wrap: wrap; }
      .doing-item strong { min-width: 60px; }
    }

    @media (max-width: 480px) {
      .badge-grid { gap: 0.3rem; }
      .badge { font-size: 0.7rem; padding: 0.3rem 0.7rem; }
    }

    /* remove default link styles */
    a { text-decoration: none; }
  </style>
</head>
<body>
  <div class="card">

    <!-- greeting / typing SVG (clean, no extra) -->
    <div class="greeting">
      <img 
        src="https://readme-typing-svg.demolab.com?font=Inter&weight=500&size=26&duration=2800&pause=1000&color=2563EB&center=true&vCenter=true&width=600&lines=Hey+%F0%9F%91%8B%2C+I'm+Fanfan+Wang;AI+%26+Full-Stack+Developer;Knowledge+Graph+%26+LLM+Researcher;Building+AI+Agents+%26+Learning+Platforms" 
        alt="Typing SVG – Fanfan Wang"
        style="max-width: 100%; height: auto;"
      />
    </div>

    <hr class="divider" />

    <!-- Tech stack -->
    <div class="section-title">
      ⚙️ tech stack <span>toolkit</span>
    </div>
    <div class="badge-grid">
      <span class="badge">🐍 Python</span>
      <span class="badge">🟦 TypeScript</span>
      <span class="badge">☕ Java</span>
      <span class="badge">🌱 Spring Boot</span>
      <span class="badge">⚛️ React</span>
      <span class="badge">🟩 Vue</span>
      <span class="badge">🟢 Node.js</span>
      <span class="badge">🔷 Neo4j</span>
      <span class="badge">🔥 PyTorch</span>
      <span class="badge">🧠 LangGraph</span>
      <span class="badge">🐘 PostgreSQL</span>
      <span class="badge">📬 Kafka</span>
      <span class="badge">🐳 Docker</span>
    </div>

    <hr class="divider" />

    <!-- Featured projects -->
    <div class="section-title">
      📌 featured projects <span>picks</span>
    </div>
    <div class="project-grid">
      <!-- SpeakMate -->
      <div class="project-row">
        <div class="project-name">
          <a href="https://github.com/wangff0329/SpeakMate">SpeakMate</a>
        </div>
        <div class="project-desc">
          AI English speaking & listening coach — digital human, RAG, pronunciation feedback, learning loop.
        </div>
        <div class="project-tech-wrap">
          <span class="project-tech">TypeScript · Bun</span>
          <span class="project-tech">LangGraph</span>
          <span class="project-tech">PostgreSQL</span>
          <span class="project-tech">vLLM · RAG</span>
        </div>
      </div>

      <!-- 3-Agent KG audit -->
      <div class="project-row">
        <div class="project-name">
          <a href="https://github.com/wangff0329/知识图谱审计">3‑Agent KG Audit</a>
        </div>
        <div class="project-desc">
          Collaborative audit framework for oil & gas geology KG extraction — weighted voting, conflict resolution, GraphRAG.
        </div>
        <div class="project-tech-wrap">
          <span class="project-tech">Python · LangGraph</span>
          <span class="project-tech">Neo4j</span>
          <span class="project-tech">PyTorch</span>
        </div>
      </div>

      <!-- SpeakMate digital human -->
      <div class="project-row">
        <div class="project-name">
          <a href="#">SpeakMate · Digital Human</a>
        </div>
        <div class="project-desc">
          User profiling, character‑driven dialogues, read‑along training, full loop from role → conversation → evaluation.
        </div>
        <div class="project-tech-wrap">
          <span class="project-tech">TypeScript</span>
          <span class="project-tech">WebSocket</span>
          <span class="project-tech">TTS · STT</span>
        </div>
      </div>
    </div>

    <hr class="divider" />

    <!-- What I'm doing -->
    <div class="section-title">
      🎯 currently <span>focus</span>
    </div>
    <div class="doing-list">
      <div class="doing-item"><strong>🔭 building</strong> SpeakMate — AI English coach (full‑stack, 0→1)</div>
      <div class="doing-item"><strong>🌱 researching</strong> KG quality evaluation · GraphRAG scheduling · multi‑agent coordination</div>
      <div class="doing-item"><strong>🤝 industry</strong> KG extraction for oil & gas geology <span class="light">(with IGGCAS)</span></div>
      <div class="doing-item"><strong>💬 happy to chat</strong> LLM apps · RAG / GraphRAG · multi‑agent · full‑stack</div>
      <div class="doing-item"><strong>📫 reach me</strong> <a href="mailto:sailffan@163.com" style="color:#1e4b7a; font-weight:500;">sailffan@163.com</a></div>
    </div>

    <hr class="divider" />

    <!-- Tags / labels -->
    <div class="section-title">
      🏷️ labels <span>topics</span>
    </div>
    <div class="tag-cloud">
      <span class="tag-pill">#AI</span>
      <span class="tag-pill">#LLM</span>
      <span class="tag-pill">#KnowledgeGraph</span>
      <span class="tag-pill">#GraphRAG</span>
      <span class="tag-pill">#MultiAgent</span>
      <span class="tag-pill">#FullStack</span>
      <span class="tag-pill">#RAG</span>
      <span class="tag-pill">#LangGraph</span>
      <span class="tag-pill">#NLP</span>
      <span class="tag-pill">#Neo4j</span>
      <span class="tag-pill">#PyTorch</span>
      <span class="tag-pill">#React</span>
      <span class="tag-pill">#TypeScript</span>
    </div>

    <div class="footer-meta">
      ✦ built with fresh air · always building ✦
    </div>
  </div>
</body>
</html>
