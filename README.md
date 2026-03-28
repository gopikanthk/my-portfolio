<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gopi Kanth | Senior Application Architect</title>
  <meta name="description" content="Portfolio of Gopi Kanth — Senior Application Architect specializing in cloud-native platforms, microservices, Azure, security, and GenAI solutions." />
  <style>
    :root {
      --bg: #0b1020;
      --bg-soft: #121936;
      --card: rgba(18, 25, 54, 0.72);
      --card-strong: rgba(20, 29, 61, 0.92);
      --text: #eef2ff;
      --muted: #b8c2e0;
      --line: rgba(255, 255, 255, 0.1);
      --accent: #7dd3fc;
      --accent-2: #a78bfa;
      --success: #86efac;
      --shadow: 0 25px 50px rgba(0, 0, 0, 0.28);
      --radius: 24px;
      --max: 1180px;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      color: var(--text);
      background:
        radial-gradient(circle at top left, rgba(125, 211, 252, 0.18), transparent 30%),
        radial-gradient(circle at top right, rgba(167, 139, 250, 0.18), transparent 26%),
        linear-gradient(180deg, #060914 0%, #0b1020 45%, #0d1327 100%);
      line-height: 1.6;
    }

    a { color: inherit; text-decoration: none; }
    img { max-width: 100%; display: block; }

    .container {
      width: min(var(--max), calc(100% - 32px));
      margin: 0 auto;
    }

    .nav {
      position: sticky;
      top: 0;
      z-index: 20;
      backdrop-filter: blur(18px);
      background: rgba(6, 9, 20, 0.65);
      border-bottom: 1px solid var(--line);
    }

    .nav-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
      padding: 16px 0;
    }

    .brand {
      font-weight: 800;
      letter-spacing: 0.2px;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .brand-dot {
      width: 12px;
      height: 12px;
      border-radius: 999px;
      background: linear-gradient(135deg, var(--accent), var(--accent-2));
      box-shadow: 0 0 24px rgba(125, 211, 252, 0.7);
    }

    .nav-links {
      display: flex;
      gap: 18px;
      flex-wrap: wrap;
      color: var(--muted);
      font-size: 0.95rem;
    }

    .nav-links a:hover { color: var(--text); }

    .hero {
      padding: 84px 0 44px;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.3fr 0.9fr;
      gap: 28px;
      align-items: stretch;
    }

    .hero-card,
    .panel,
    .timeline-item,
    .project,
    .contact-card {
      background: var(--card);
      border: 1px solid var(--line);
      box-shadow: var(--shadow);
      border-radius: var(--radius);
      backdrop-filter: blur(16px);
    }

    .hero-card {
      padding: 42px;
      position: relative;
      overflow: hidden;
    }

    .hero-card::before {
      content: "";
      position: absolute;
      inset: auto -10% -30% auto;
      width: 260px;
      height: 260px;
      background: radial-gradient(circle, rgba(125, 211, 252, 0.24), transparent 60%);
      pointer-events: none;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 8px 14px;
      border: 1px solid rgba(125, 211, 252, 0.25);
      border-radius: 999px;
      color: var(--accent);
      background: rgba(125, 211, 252, 0.08);
      font-size: 0.88rem;
      margin-bottom: 18px;
    }

    h1, h2, h3 {
      margin: 0 0 12px;
      line-height: 1.15;
    }

    h1 {
      font-size: clamp(2.5rem, 5vw, 4.5rem);
      letter-spacing: -0.04em;
      max-width: 10ch;
    }

    .subtitle {
      font-size: 1.08rem;
      color: var(--muted);
      max-width: 60ch;
      margin-top: 16px;
    }

    .hero-actions {
      display: flex;
      gap: 14px;
      margin-top: 28px;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      padding: 14px 18px;
      border-radius: 14px;
      font-weight: 700;
      border: 1px solid var(--line);
      transition: transform 0.18s ease, border-color 0.18s ease, background 0.18s ease;
    }

    .btn:hover {
      transform: translateY(-2px);
      border-color: rgba(255,255,255,0.22);
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--accent), var(--accent-2));
      color: #09101f;
      border: none;
    }

    .btn-secondary {
      background: rgba(255,255,255,0.04);
      color: var(--text);
    }

    .hero-side {
      display: grid;
      gap: 18px;
    }

    .panel {
      padding: 24px;
    }

    .stat-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 16px;
      margin-top: 12px;
    }

    .stat {
      padding: 18px;
      border-radius: 18px;
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.06);
    }

    .stat strong {
      display: block;
      font-size: 1.8rem;
      margin-bottom: 6px;
    }

    .label {
      color: var(--muted);
      font-size: 0.92rem;
    }

    section {
      padding: 28px 0;
    }

    .section-head {
      display: flex;
      justify-content: space-between;
      align-items: end;
      gap: 20px;
      margin-bottom: 22px;
    }

    .section-head p {
      color: var(--muted);
      max-width: 62ch;
      margin: 0;
    }

    .grid-2 {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 22px;
    }

    .about-list,
    .skill-list,
    .highlights,
    .project ul,
    .timeline-item ul {
      margin: 14px 0 0;
      padding-left: 18px;
    }

    .about-list li,
    .skill-list li,
    .highlights li,
    .project li,
    .timeline-item li {
      margin-bottom: 10px;
      color: var(--muted);
    }

    .badge-wrap {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 18px;
    }

    .badge {
      padding: 10px 12px;
      border-radius: 999px;
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.08);
      color: #dbe6ff;
      font-size: 0.92rem;
    }

    .timeline {
      display: grid;
      gap: 18px;
    }

    .timeline-item {
      padding: 24px;
      position: relative;
    }

    .role-meta {
      color: var(--muted);
      margin-bottom: 12px;
      font-size: 0.95rem;
    }

    .project-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 18px;
    }

    .project {
      padding: 24px;
    }

    .project-tag {
      display: inline-block;
      margin-bottom: 10px;
      color: var(--success);
      font-size: 0.88rem;
      font-weight: 700;
      letter-spacing: 0.02em;
    }

    .contact-card {
      padding: 28px;
      display: grid;
      grid-template-columns: 1.2fr 1fr;
      gap: 24px;
      margin: 30px 0 60px;
    }

    .contact-links {
      display: grid;
      gap: 12px;
    }

    .contact-link {
      display: flex;
      justify-content: space-between;
      gap: 16px;
      padding: 15px 16px;
      border-radius: 16px;
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.07);
      color: var(--muted);
    }

    .contact-link strong { color: var(--text); }

    footer {
      padding: 0 0 44px;
      color: var(--muted);
      text-align: center;
      font-size: 0.94rem;
    }

    @media (max-width: 980px) {
      .hero-grid,
      .grid-2,
      .contact-card,
      .project-grid {
        grid-template-columns: 1fr;
      }

      .hero-card { padding: 30px; }
      .contact-card { padding: 22px; }
    }

    @media (max-width: 640px) {
      .nav-inner { align-items: flex-start; }
      .nav-links { gap: 12px; font-size: 0.9rem; }
      .hero { padding-top: 52px; }
      .hero-card { padding: 24px; }
      .panel, .project, .timeline-item { padding: 20px; }
      .stat-grid { grid-template-columns: 1fr; }
      h1 { max-width: 100%; }
    }
  </style>
</head>
<body>
  <nav class="nav">
    <div class="container nav-inner">
      <a href="#top" class="brand"><span class="brand-dot"></span> Gopi Kanth</a>
      <div class="nav-links">
        <a href="#about">About</a>
        <a href="#experience">Experience</a>
        <a href="#projects">Projects</a>
        <a href="#skills">Skills</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
  </nav>

  <header class="hero" id="top">
    <div class="container hero-grid">
      <div class="hero-card">
        <div class="eyebrow">Senior Application Architect • Cloud-native Platforms • GenAI</div>
        <h1>Designing resilient software for scale, security, and real-world impact.</h1>
        <p class="subtitle">
          I’m Gopi Kanth, a Senior Application Architect with 17+ years of experience building enterprise applications across insurance, healthcare, and supply chain. I focus on cloud-native platforms, multi-tenant SaaS, architecture governance, and AI-enabled product experiences.
        </p>
        <div class="hero-actions">
          <a class="btn btn-primary" href="#contact">Let’s Connect</a>
          <a class="btn btn-secondary" href="#projects">View Key Projects</a>
        </div>
      </div>

      <div class="hero-side">
        <div class="panel">
          <h3>Impact Snapshot</h3>
          <div class="stat-grid">
            <div class="stat">
              <strong>17+</strong>
              <span class="label">Years in enterprise engineering and architecture</span>
            </div>
            <div class="stat">
              <strong>100+</strong>
              <span class="label">Cloud customers supported through SaaS architecture</span>
            </div>
            <div class="stat">
              <strong>100M+</strong>
              <span class="label">Records processed in high-volume distributed workloads</span>
            </div>
            <div class="stat">
              <strong>99%</strong>
              <span class="label">SLA-aligned solution design and operational focus</span>
            </div>
          </div>
        </div>

        <div class="panel">
          <h3>Core Strengths</h3>
          <div class="badge-wrap">
            <span class="badge">Azure / AKS</span>
            <span class="badge">Microservices</span>
            <span class="badge">Multi-tenant SaaS</span>
            <span class="badge">Security by Design</span>
            <span class="badge">Architecture Governance</span>
            <span class="badge">GenAI Applications</span>
          </div>
        </div>
      </div>
    </div>
  </header>

  <main>
    <section id="about">
      <div class="container">
        <div class="section-head">
          <div>
            <h2>About</h2>
            <p>Architecture leadership backed by hands-on delivery. I work at the intersection of platform engineering, product scalability, security, and pragmatic execution.</p>
          </div>
        </div>
        <div class="grid-2">
          <div class="panel">
            <h3>What I focus on</h3>
            <ul class="about-list">
              <li>Cloud-native architecture on Azure, Kubernetes, and modern CI/CD foundations.</li>
              <li>Multi-tenant SaaS design with scalability, tenant isolation, and cost efficiency built in.</li>
              <li>Architecture governance through reference patterns, design reviews, and ADR-driven decision making.</li>
              <li>Secure, resilient systems with SSO, authorization, DR strategy, auditability, and operational readiness.</li>
              <li>GenAI-powered conversational solutions integrated with rules-driven application workflows.</li>
            </ul>
          </div>
          <div class="panel">
            <h3>Domain experience</h3>
            <ul class="highlights">
              <li><strong>Insurance:</strong> next-generation solutions and GenAI-assisted underwriting experiences.</li>
              <li><strong>Supply Chain:</strong> high-volume distributed processing and product architecture for large-scale fulfillment workloads.</li>
              <li><strong>Healthcare:</strong> SaaS workflows supporting patient estimation and EDI-driven automation.</li>
            </ul>
            <div class="badge-wrap">
              <span class="badge">Insurance</span>
              <span class="badge">Supply Chain</span>
              <span class="badge">Healthcare</span>
              <span class="badge">Enterprise Platforms</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="experience">
      <div class="container">
        <div class="section-head">
          <div>
            <h2>Experience</h2>
            <p>Key roles across architecture, technical leadership, and platform engineering.</p>
          </div>
        </div>
        <div class="timeline">
          <article class="timeline-item">
            <h3>Swiss Re — Senior Application Architect (Vice President)</h3>
            <div class="role-meta">Aug 2023 – Present • Hyderabad, India</div>
            <ul>
              <li>Architected enterprise-grade cloud-native services on Azure and AKS for scalability, maintainability, and cost efficiency.</li>
              <li>Designed multi-tenant SaaS microservices including tenancy isolation, configuration patterns, and deployment standards.</li>
              <li>Defined security architecture with Okta, Azure AD, authorization strategy, and governance guardrails.</li>
              <li>Built resiliency foundations including DR, backup and restore, audit logging, and operational readiness.</li>
              <li>Designed a GenAI-based solution for interactive, rules-driven underwriting interviews via chat experience.</li>
            </ul>
          </article>

          <article class="timeline-item">
            <h3>Blue Yonder (JDA) — Technical Architect</h3>
            <div class="role-meta">May 2019 – Aug 2023</div>
            <ul>
              <li>Owned architecture for fulfillment capabilities serving large warehouse and distribution workloads.</li>
              <li>Designed cloud migration target architecture and rollout approach for production delivery.</li>
              <li>Improved performance and reliability for workloads processing roughly 100M records.</li>
              <li>Built POCs that validated feasibility and cost for roadmap-shaping product decisions.</li>
            </ul>
          </article>

          <article class="timeline-item">
            <h3>Optum — Tech Lead</h3>
            <div class="role-meta">Apr 2015 – May 2019</div>
            <ul>
              <li>Led development of patient estimation and EDI workflows in a healthcare SaaS platform.</li>
              <li>Supported architecture decisions across services, integrations, security, and delivery workflows.</li>
              <li>Improved execution quality through code reviews, design reviews, and CI/CD practices.</li>
            </ul>
          </article>

          <article class="timeline-item">
            <h3>Oracle — Senior Software Engineer</h3>
            <div class="role-meta">Jun 2012 – Apr 2015</div>
            <ul>
              <li>Built presales customization tools and reusable frameworks for Oracle Fusion demos.</li>
              <li>Enabled rapid prototyping and faster presales turnaround for large enterprise opportunities.</li>
            </ul>
          </article>
        </div>
      </div>
    </section>

    <section id="projects">
      <div class="container">
        <div class="section-head">
          <div>
            <h2>Selected Work</h2>
            <p>Representative initiatives that show architecture depth, product thinking, and system design maturity.</p>
          </div>
        </div>
        <div class="project-grid">
          <article class="project">
            <div class="project-tag">GenAI / Insurance</div>
            <h3>Rules-driven Underwriting Chat Platform</h3>
            <ul>
              <li>Designed a conversational underwriting experience backed by rule-based interview logic.</li>
              <li>Integrated LLM-based interaction with architecture governance and safety controls.</li>
              <li>Focused on maintainability, response consistency, and enterprise-grade design standards.</li>
            </ul>
          </article>

          <article class="project">
            <div class="project-tag">Cloud Platform</div>
            <h3>Multi-tenant SaaS Architecture</h3>
            <ul>
              <li>Created a scalable architecture model supporting single-tenant and multi-tenant deployment patterns.</li>
              <li>Defined tenant isolation, configuration strategy, and platform deployment standards.</li>
              <li>Balanced scale, security, and cost efficiency for broad customer adoption.</li>
            </ul>
          </article>

          <article class="project">
            <div class="project-tag">Distributed Data</div>
            <h3>High-volume Processing System</h3>
            <ul>
              <li>Improved distributed processing performance for supply chain workloads using Spark-based patterns.</li>
              <li>Supported large-scale execution across 100+ customers and 100M+ records.</li>
              <li>Strengthened reliability through tuning, architecture changes, and design review leadership.</li>
            </ul>
          </article>

          <article class="project">
            <div class="project-tag">Security / Governance</div>
            <h3>Enterprise Security-by-Design Framework</h3>
            <ul>
              <li>Implemented secure authentication and authorization architecture using Okta and Azure AD.</li>
              <li>Strengthened vulnerability management, OSS compliance, audit logging, and privacy alignment.</li>
              <li>Embedded security and governance into platform standards and architecture reviews.</li>
            </ul>
          </article>
        </div>
      </div>
    </section>

    <section id="skills">
      <div class="container">
        <div class="section-head">
          <div>
            <h2>Skills</h2>
            <p>A focused stack built around enterprise architecture, cloud delivery, platform security, and AI-driven product evolution.</p>
          </div>
        </div>
        <div class="grid-2">
          <div class="panel">
            <h3>Architecture & Platform</h3>
            <ul class="skill-list">
              <li>Microservices, distributed systems, event-driven design, API-first architecture</li>
              <li>Architecture governance, design reviews, ADRs, NFRs, DR/BCP</li>
              <li>Multi-tenant SaaS, resiliency, operational readiness, observability</li>
            </ul>
          </div>
          <div class="panel">
            <h3>Cloud & DevOps</h3>
            <ul class="skill-list">
              <li>Azure, AKS, Docker, Terraform, CI/CD, automated deployments</li>
              <li>Cloud migration, API management, deployment standardization</li>
              <li>Platform reliability, backup and restore, release governance</li>
            </ul>
          </div>
          <div class="panel">
            <h3>Backend & Data</h3>
            <ul class="skill-list">
              <li>Java, J2EE, Spring Boot, Hibernate, REST APIs, WebSockets, Spring Batch</li>
              <li>RabbitMQ, MS SQL, Oracle, Apache Spark, Apache Ignite</li>
              <li>High-throughput processing and enterprise integration patterns</li>
            </ul>
          </div>
          <div class="panel">
            <h3>Security & GenAI</h3>
            <ul class="skill-list">
              <li>Okta, Azure AD, RBAC, secure coding, vulnerability management</li>
              <li>OSS and license compliance, data privacy alignment</li>
              <li>LLM integration and chat-based application development</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section id="contact">
      <div class="container">
        <div class="contact-card">
          <div>
            <h2>Contact</h2>
            <p class="subtitle">Interested in architecture leadership, principal engineering, or AI platform roles. Reach out for opportunities, collaboration, or technical discussions.</p>
          </div>
          <div class="contact-links">
            <div class="contact-link"><strong>Email</strong><span>k.g.kanth@gmail.com</span></div>
            <div class="contact-link"><strong>Location</strong><span>Hyderabad, India</span></div>
            <div class="contact-link"><strong>Open to</strong><span>Senior Architect • Principal Engineer • AI Platform Architect</span></div>
            <div class="contact-link"><strong>GitHub / LinkedIn</strong><span>Add your profile links here</span></div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">© <span id="year"></span> Gopi Kanth. Built for GitHub Pages.</div>
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
