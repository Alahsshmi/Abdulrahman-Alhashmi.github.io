<!doctype html>
<html lang="en" data-theme="auto">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>MSc AI E-Portfolio | Abdul Rahman Husain Alhashmi</title>
<meta name="description" content="E-portfolio of Abdul Rahman Husain Alhashmi — MSc Artificial Intelligence student with an electrical engineering background.">
<meta name="theme-color" content="#0f172a" media="(prefers-color-scheme: dark)">
<meta name="theme-color" content="#ffffff" media="(prefers-color-scheme: light)">
<style>
/* ===== Tokens ============================================================ */
:root{
  --bg: #ffffff; --surface:#f8fafc; --card:#ffffff; --text:#0f172a; --muted:#475569;
  --border:#e2e8f0; --accent:#2563eb; --accent-2:#16a34a; --ring:#93c5fd; --shadow:0 8px 24px rgba(2,6,23,.08);
}
@media (prefers-color-scheme: dark){
  :root{
    --bg:#0b1020; --surface:#0f172a; --card:#0f172a; --text:#e5e7eb; --muted:#94a3b8;
    --border:#1f2937; --accent:#60a5fa; --accent-2:#22c55e; --ring:#2563eb; --shadow:0 10px 30px rgba(0,0,0,.45);
  }
}
:root[data-theme="light"]{
  --bg:#ffffff; --surface:#f8fafc; --card:#ffffff; --text:#0f172a; --muted:#475569;
  --border:#e2e8f0; --accent:#2563eb; --accent-2:#16a34a; --ring:#93c5fd; --shadow:0 8px 24px rgba(2,6,23,.08);
}
:root[data-theme="dark"]{
  --bg:#0b1020; --surface:#0f172a; --card:#0f172a; --text:#e5e7eb; --muted:#94a3b8;
  --border:#1f2937; --accent:#60a5fa; --accent-2:#22c55e; --ring:#2563eb; --shadow:0 10px 30px rgba(0,0,0,.45);
}

/* ===== Base ============================================================= */
*{box-sizing:border-box}
html,body{margin:0;background:var(--bg);color:var(--text);font-family:system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,Cantarell,"Helvetica Neue",Arial;scroll-behavior:smooth}
img{max-width:100%;height:auto}
a{color:var(--accent);text-decoration:none}
a:hover{text-decoration:underline}
:focus-visible{outline:2px solid var(--ring);outline-offset:3px}

/* ===== Layout =========================================================== */
.container{max-width:1100px;margin-inline:auto;padding:1rem}
header{position:sticky;top:0;background:color-mix(in oklab, var(--bg) 85%, transparent);backdrop-filter:saturate(160%) blur(6px);border-bottom:1px solid var(--border);z-index:20}
.nav{display:flex;align-items:center;justify-content:space-between;gap:1rem;padding:.7rem 0}
.brand{font-weight:700;letter-spacing:.2px}
.menu{display:flex;gap:1rem;list-style:none;margin:0;padding:0}
.menu a{display:block;padding:.45rem .6rem;border-radius:.5rem}
.menu a:hover{background:color-mix(in oklab, var(--accent) 14%, transparent);text-decoration:none}
.menu a.is-active{background:color-mix(in oklab, var(--accent) 18%, transparent)}
#nav-toggle{display:none}
.menu-btn{display:none;cursor:pointer}
.menu-btn span,.menu-btn span::before,.menu-btn span::after{content:"";display:block;height:2px;width:22px;border-radius:10px;background:var(--text)}
.menu-btn span::before{transform:translateY(-6px)}
.menu-btn span::after{transform:translateY(4px)}
@media (max-width:820px){
  .menu-btn{display:block}
  .menu{position:absolute;right:1rem;top:60px;flex-direction:column;background:var(--card);border:1px solid var(--border);border-radius:.6rem;padding:.6rem;display:none;box-shadow:var(--shadow)}
  #nav-toggle:checked + label + ul{display:flex}
}

/* ===== Hero ============================================================= */
.hero{padding:3.2rem 0;background:
  radial-gradient(1200px 400px at 20% -10%, color-mix(in oklab,var(--accent) 14%,transparent), transparent),
  radial-gradient(1200px 400px at 120% 10%, color-mix(in oklab,var(--accent-2) 16%,transparent), transparent);
}
.hero-grid{display:grid;grid-template-columns:1.1fr .9fr;gap:2rem;align-items:center}
@media (max-width:880px){.hero-grid{grid-template-columns:1fr}}
.kicker{letter-spacing:.08em;color:var(--accent-2);font-weight:700;text-transform:uppercase;font-size:.8rem}
.hero h1{margin:.2rem 0 1rem}
.hero p{color:var(--muted);line-height:1.7}
.btn{display:inline-block;background:var(--accent);color:#fff;padding:.7rem 1rem;border-radius:.55rem;font-weight:600;border:1px solid color-mix(in oklab, var(--accent) 70%, black 5%)}
.btn:hover{text-decoration:none;filter:brightness(1.05)}
.btn.ghost{background:transparent;color:var(--text);border:1px solid var(--border)}
.badge{display:inline-block;background:color-mix(in oklab,var(--accent) 12%, transparent);border:1px solid var(--border);padding:.15rem .45rem;border-radius:.4rem;color:var(--text);font-size:.8rem}

/* ===== Cards & sections ================================================ */
.section{padding:1.2rem 0}
.grid{display:grid;gap:1rem}
.grid-3{grid-template-columns:repeat(3,1fr)}
@media (max-width:980px){.grid-3{grid-template-columns:repeat(2,1fr)}}
@media (max-width:640px){.grid-3{grid-template-columns:1fr}}
.card{background:var(--card);border:1px solid var(--border);border-radius:.9rem;padding:1rem;box-shadow:var(--shadow)}
.card h3{margin:.2rem 0 .4rem}
.card:hover{transform:translateY(-1px)}
hr.rule{border:0;border-top:1px solid var(--border);margin:1.6rem 0}

/* ===== Tables & forms =================================================== */
.table{width:100%;border-collapse:collapse;margin:1rem 0}
.table th,.table td{border:1px solid var(--border);padding:.6rem;text-align:left}
.table th{background:var(--surface)}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:1rem}
@media (max-width:720px){.form-row{grid-template-columns:1fr}}
input,textarea{width:100%;padding:.65rem;border-radius:.5rem;border:1px solid var(--border);background:var(--card);color:var(--text)}
button.theme{background:transparent;border:1px solid var(--border);padding:.45rem .6rem;border-radius:.5rem;cursor:pointer}
button.theme:hover{background:var(--surface)}

/* ===== Utilities ======================================================== */
.small{font-size:.92rem;color:var(--muted)}
.figure{background:var(--surface);border:1px dashed var(--border);border-radius:.8rem;padding:.6rem;display:flex;align-items:center;justify-content:center;min-height:140px}
footer{border-top:1px solid var(--border);margin-top:2rem}
.sr-only{position:absolute;width:1px;height:1px;padding:0;margin:-1px;overflow:hidden;clip:rect(0,0,0,0);white-space:nowrap;border:0}
</style>
</head>
<body>
<header>
  <div class="container nav" role="navigation" aria-label="Primary">
    <div class="brand">Abdul Rahman Husain Alhashmi</div>
    <div style="display:flex;align-items:center;gap:.6rem">
      <button id="themeBtn" class="theme" type="button" aria-pressed="false" aria-label="Toggle theme">Theme</button>
      <input id="nav-toggle" type="checkbox" aria-label="Toggle menu">
      <label for="nav-toggle" class="menu-btn" aria-hidden="true"><span></span></label>
      <ul class="menu">
        <li><a href="#home" class="is-active">Home</a></li>
        <li><a href="#modules">Modules</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#ml">Machine Learning</a></li>
        <li><a href="#agents">Intelligent Agents</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>
  </div>
</header>

<!-- HERO (updated) -->
<section id="home" class="hero">
  <div class="container hero-grid">
    <div>
      <div class="kicker">MSc Artificial Intelligence E-Portfolio</div>
      <h1>MSc Artificial Intelligence E-Portfolio</h1>
      <p>This e-portfolio reflects both my engineering foundation and my progression into AI, showcasing academic projects, technical skills, and my vision for integrating intelligent systems into practical, high-impact applications.</p>
      <p class="small">Last updated: 13 August 2025</p>
      <p>
        <a class="btn" href="#projects">View projects</a>
        <a class="btn ghost" href="#modules">Module sections</a>
        <a class="btn" href="cv/Abdulrahman-CV.pdf">Download CV</a>
      </p>
      <p class="small">Links:
        <a href="https://github.com/Alahsshmi" rel="noopener">GitHub</a> ·
        <a href="https://www.linkedin.com/in/abdul-rahman-alhashmi-b659541b0?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app" rel="noopener">LinkedIn</a>
      </p>
    </div>
    <div class="figure" aria-hidden="true">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 240 160" role="img" aria-label="Profile graphic">
        <defs><linearGradient id="g" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="#2563eb"/><stop offset="100%" stop-color="#16a34a"/></linearGradient></defs>
        <rect width="240" height="160" rx="10" fill="var(--card)"/>
        <circle cx="120" cy="60" r="34" fill="url(#g)"/>
        <rect x="55" y="100" width="130" height="38" rx="16" fill="var(--surface)"/>
      </svg>
    </div>
  </div>
</section>

<!-- Modules overview -->
<section id="modules" class="section">
  <div class="container">
    <h2>Modules overview</h2>
    <div class="grid grid-3">
      <article class="card">
        <h3>Machine Learning</h3>
        <p class="small"><span class="badge">20 CREDITS</span></p>
        <p>Supervised and unsupervised learning on tabular data; model evaluation and limits.</p>
        <p class="small">Tools: Python, scikit-learn, Pandas</p>
      </article>
      <article class="card">
        <h3>Research Methods & Professional Practice</h3>
        <p class="small"><span class="badge">20 CREDITS</span></p>
        <p>Evidence-based writing, ethics, references, and reflective practice for engineering contexts.</p>
      </article>
      <article class="card">
        <h3>Intelligent Agents</h3>
        <p class="small"><span class="badge">20 CREDITS</span></p>
        <p>Agent architectures and safeguards; human-in-the-loop and deployment patterns.</p>
      </article>
    </div>
  </div>
</section>

<!-- About Me (new) -->
<section id="about" class="section">
  <div class="container">
    <h2>About Me</h2>
    <p>I am a postgraduate MSc Artificial Intelligence student with over 14 years of experience as an electrical engineer. My background includes designing, implementing, and managing complex electrical systems, where I developed strong problem-solving skills and the ability to deliver under pressure.</p>
    <p>Driven by a passion for technology, I am now expanding my expertise into AI, gaining practical experience in Python, machine learning, computer vision, and AI model development. My goal is to combine my engineering knowledge with intelligent systems to create practical, scalable, and impactful solutions.</p>
  </div>
</section>

<!-- Machine Learning Units 1–12 -->
<section id="ml" class="section">
  <div class="container">
    <h2>Machine Learning</h2>
    <p class="small">Applied modelling on tabular data with clear splits, honest metrics, and reproducible workflows.</p>

    <div class="small" style="display:flex;gap:.5rem;flex-wrap:wrap;margin:.5rem 0 1rem">
      <button class="theme" type="button" data-scope="#ml" data-expand>Expand all</button>
      <button class="theme" type="button" data-scope="#ml" data-collapse>Collapse all</button>
    </div>

    <details class="card"><summary><strong>Unit 1:</strong> Induction & tools</summary>
      <ul>
        <li>Outcomes: Python setup, repo, environment, style guide.</li>
        <li>Work: “hello dataset” notebook, smoke tests, Git commits.</li>
        <li>Evidence: <a href="#" title="Add link">Repo</a> · <a href="#" title="Add link">Notebook</a></li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 2:</strong> EDA & data quality</summary>
      <ul>
        <li>Outcomes: profiling, missingness, target distribution, leakage checks.</li>
        <li>Work: EDA plots, data dictionary, data quality log.</li>
        <li>Evidence: <a href="#" title="Add link">EDA notebook</a> · <a href="#" title="Add link">Report</a></li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 3:</strong> Cleaning & feature engineering</summary>
      <ul>
        <li>Outcomes: encodings, scaling, winsorising, date/geo features.</li>
        <li>Work: pipeline fragments; train/test split policy.</li>
        <li>Evidence: <a href="#" title="Add link">Features notebook</a> · <a href="#" title="Add link">Pipeline code</a></li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 4:</strong> Baselines & split strategy</summary>
      <ul>
        <li>Outcomes: baseline MAE/RMSE, CV choice (KFold/Stratified/Group).</li>
        <li>Work: constant/median baseline; proper CV.</li>
        <li>Evidence: <a href="#" title="Add link">Results table</a> · <a href="#" title="Add link">CV policy</a></li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 5:</strong> Linear models</summary>
      <ul>
        <li>Outcomes: OLS/Ridge/Lasso; interpret coefficients.</li>
        <li>Work: log(price) target; regularisation path.</li>
        <li>Evidence: <a href="#" title="Add link">Metrics</a> · <a href="#" title="Add link">Coefficients</a></li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 6:</strong> Trees & ensembles</summary>
      <ul>
        <li>Outcomes: RF/GB basics; variance control.</li>
        <li>Work: RF with light tuning; feature importance caveats.</li>
        <li>Evidence: <a href="#" title="Add link">MAE/RMSE</a> · <a href="#" title="Add link">Top signals</a></li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 7:</strong> Model evaluation</summary>
      <ul>
        <li>Outcomes: CV diagnostics, error analysis, residuals.</li>
        <li>Work: learning curves; error by segment (room type, borough).</li>
        <li>Evidence: <a href="#" title="Add link">Plots</a> · <a href="#" title="Add link">Segment errors</a></li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 8:</strong> Regularisation & robustness</summary>
      <ul>
        <li>Outcomes: bias–variance, overfitting handling.</li>
        <li>Work: dropout rows, noise tests, outlier sensitivity checks.</li>
        <li>Evidence: <a href="#" title="Add link">Stress tests</a> · <a href="#" title="Add link">Delta metrics</a></li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 9:</strong> Unsupervised learning</summary>
      <ul>
        <li>Outcomes: clustering for segments; K-means vs DBSCAN notes.</li>
        <li>Work: simple customer segments; silhouette check.</li>
        <li>Evidence: <a href="#" title="Add link">Clusters summary</a> · <a href="#" title="Add link">Notebook</a></li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 10:</strong> Interpretability</summary>
      <ul>
        <li>Outcomes: permutation importance; PDP/ICE basics.</li>
        <li>Work: explain key features (room type, neighbourhood).</li>
        <li>Evidence: <a href="#" title="Add link">PDP/ICE</a> · <a href="#" title="Add link">Narrative</a></li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 11:</strong> Pipelines & reproducibility</summary>
      <ul>
        <li>Outcomes: sklearn Pipeline; random seeds; run logs.</li>
        <li>Work: single script/notebook end-to-end.</li>
        <li>Evidence: <a href="#" title="Add link">Repo link</a> · <a href="#" title="Add link">versions.txt</a></li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 12:</strong> Final synthesis & reflection</summary>
      <ul>
        <li>Outcomes: concise case study using STAR.</li>
        <li>Work: results table; limits; next steps.</li>
        <li>Evidence: <a href="#" title="Add link">Final notebook</a> · <a href="#" title="Add link">Report PDF</a></li>
      </ul>
    </details>
  </div>
</section>

<!-- Intelligent Agents Units 1–12 (from your module document) -->
<section id="agents" class="section">
  <div class="container">
    <h2>Intelligent Agents</h2>
    <p class="small">Module content summarised from your course guide: topics, outcomes, and key activities per unit.</p>

    <div class="small" style="display:flex;gap:.5rem;flex-wrap:wrap;margin:.5rem 0 1rem">
      <button class="theme" type="button" data-scope="#agents" data-expand>Expand all</button>
      <button class="theme" type="button" data-scope="#agents" data-collapse>Collapse all</button>
    </div>

    <details class="card"><summary><strong>Unit 1:</strong> Introduction to Agent-Based Computing</summary>
      <ul>
        <li><strong>Topics:</strong> trends driving agent-based computing; autonomy; agent–environment interaction; real-world examples.</li>
        <li><strong>Learning outcomes:</strong> explain core concepts; recognise enabling trends; compare types of agent-based systems.</li>
        <li><strong>Activities:</strong> lecturecast (1 h); set up e-portfolio section; Module Wiki entry; first discussion post; seminar prep.</li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 2:</strong> Introducing First-Order Logic</summary>
      <ul>
        <li><strong>Topics:</strong> symbols and syntax; mapping between natural language and logic; quantifiers.</li>
        <li><strong>Learning outcomes:</strong> understand FOL elements; begin creating and reasoning over statements.</li>
        <li><strong>Activities:</strong> reading (4 h); follow-up discussion replies; e-portfolio updates; seminar on FOL.</li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 3:</strong> Agent Architectures</summary>
      <ul>
        <li><strong>Topics:</strong> history and development; symbolic reasoning agents; agents with state; reactive approaches.</li>
        <li><strong>Learning outcomes:</strong> evaluate architectures; select appropriate designs; distinguish intentions vs desires.</li>
        <li><strong>Activities:</strong> lecturecast (1 h); reading (4 h); summary discussion post; e-portfolio notes; seminar prep.</li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 4:</strong> Hybrid Agent Architectures</summary>
      <ul>
        <li><strong>Topics:</strong> combining reactive and deliberative behaviours; case study of a deployed hybrid system.</li>
        <li><strong>Learning outcomes:</strong> critically assess architectures; justify selections for a given problem.</li>
        <li><strong>Activities:</strong> reading (4 h); Module Wiki post; e-portfolio updates; seminar on hybrid designs.</li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 5:</strong> Agent Communication</summary>
      <ul>
        <li><strong>Topics:</strong> speech acts; KQML; role of ontologies in communication.</li>
        <li><strong>Learning outcomes:</strong> build ontologies; create inter-agent messages with suitable languages.</li>
        <li><strong>Activities:</strong> lecturecast (1 h); reading (4 h); start Discussion 2; e-portfolio updates.</li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 6:</strong> Working Together</summary>
      <ul>
        <li><strong>Topics:</strong> designing dialogues with KQML/KIF; strengths and limits of agent communication.</li>
        <li><strong>Learning outcomes:</strong> author dialogues; use ontologies for knowledge sharing.</li>
        <li><strong>Activities:</strong> “Creating Agent Dialogues” e-portfolio task; seminar on real KQML dialogues.</li>
        <li><strong>Assessment:</strong> Team Project report, 1,000 words, 20% (with peer review).</li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 7:</strong> Natural Language Processing (NLP)</summary>
      <ul>
        <li><strong>Topics:</strong> why NLP is challenging; common techniques; Word2Vec focus.</li>
        <li><strong>Learning outcomes:</strong> evaluate NLP difficulties; understand core principles and techniques.</li>
        <li><strong>Activities:</strong> lecturecast (1 h); reading (4 h); summary post; e-portfolio updates.</li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 8:</strong> Understanding NLP</summary>
      <ul>
        <li><strong>Topics:</strong> Word2Vec hands-on demo; constituency parse trees.</li>
        <li><strong>Learning outcomes:</strong> explain NLP model elements; build parse trees from examples.</li>
        <li><strong>Activities:</strong> “Creating Parse Trees” e-portfolio task; seminar with demo; reading (4 h).</li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 9:</strong> Introduction to Adaptive Algorithms</summary>
      <ul>
        <li><strong>Topics:</strong> artificial neural networks; deep learning; opportunities and limitations.</li>
        <li><strong>Learning outcomes:</strong> understand ANN concepts; appraise strengths of adaptive techniques.</li>
        <li><strong>Activities:</strong> lecturecast (1 h); reading (4 h); start Discussion 3; e-portfolio updates.</li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 10:</strong> Deep Learning in Action</summary>
      <ul>
        <li><strong>Topics:</strong> emerging applications; social and ethical issues; role of data.</li>
        <li><strong>Learning outcomes:</strong> assess product limits and impacts; explain data’s importance.</li>
        <li><strong>Activities:</strong> seminar on applications; “Deep Learning in Action” e-portfolio task; reading (4 h).</li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 11:</strong> Intelligent Agents in Action</summary>
      <ul>
        <li><strong>Topics:</strong> Industry 4.0 and smart manufacturing; smart shop floor; agent-based modelling in FinTech.</li>
        <li><strong>Learning outcomes:</strong> apply course concepts to sectors; gauge efficiency gains; evaluate approaches in context.</li>
        <li><strong>Activities:</strong> lecturecast (1 h); reading (4 h); summary post; e-portfolio updates.</li>
        <li><strong>Assessment:</strong> Individual presentation, 20 minutes, 40%.</li>
      </ul>
    </details>

    <details class="card"><summary><strong>Unit 12:</strong> The Future of Intelligent Agents</summary>
      <ul>
        <li><strong>Topics:</strong> future directions of deep learning and intelligent tech; societal implications.</li>
        <li><strong>Learning outcomes:</strong> appraise current tech; assess likely evolution; consider ethical and social factors.</li>
        <li><strong>Activities:</strong> seminar on future tech; reading (4 h).</li>
        <li><strong>Assessment:</strong> Individual e-Portfolio submission, 2,500 words total, 40%.</li>
      </ul>
    </details>

  </div>
</section>

<!-- Projects -->
<section id="projects" class="section">
  <div class="container">
    <h2>Projects</h2>
    <div class="grid grid-3">
      <article class="card" id="airbnb">
        <h3>Airbnb price prediction (NYC 2019)</h3>
        <p><strong>Aim:</strong> predict listing price from structured features and compare linear vs tree-based methods.</p>
        <ul>
          <li>Data: AB_NYC_2019.csv (neighbourhood group, room type, min nights, reviews, availability)</li>
          <li>Models: linear regression on log(price); random forest regressor (light tuning)</li>
          <li>Metrics: MAE and RMSE on held-out data</li>
          <li>Signals: room type, neighbourhood group, availability</li>
        </ul>
        <p class="small">Add your notebook link here when ready.</p>
      </article>

      <article class="card" id="wannacry">
        <h3>NHS cyber incident study (WannaCry, 2017)</h3>
        <p><strong>Focus:</strong> causes, operational impact, and practical steps to reduce risk for future events.</p>
        <ul>
          <li>Patch management with ownership and testing windows</li>
          <li>Network zoning and least-privilege design</li>
          <li>Regular staff refreshers on phishing and device care</li>
          <li>Tested, offline backups</li>
        </ul>
      </article>

      <article class="card" id="agents-quick">
        <h3>Agent-based systems — safeguards and use</h3>
        <p><strong>Focus:</strong> where agents add value and how to keep decisions safe.</p>
        <ul>
          <li>Distributed control for local, low-latency decisions</li>
          <li>Data validation and anomaly alerts</li>
          <li>Pilots and sandboxes before live rollout</li>
          <li>Regular review and retraining</li>
        </ul>
      </article>
    </div>
  </div>
</section>

<!-- Contact -->
<section id="contact" class="section">
  <div class="container">
    <h2>Contact</h2>
    <div class="grid" style="gap:1.2rem">
      <div class="card">
        <h3>Send a message</h3>
        <form action="mailto:Alhashmi-ad@outlook.com" method="post" enctype="text/plain">
          <div class="form-row">
            <div><label for="name">Name</label><input id="name" name="name" required></div>
            <div><label for="email">Email</label><input id="email" name="email" type="email" required></div>
          </div>
          <label for="message">Message</label>
          <textarea id="message" name="message" rows="6" required></textarea>
          <p><button class="btn" type="submit">Send</button></p>
          <p class="small">The button opens your mail client. Replace the address above if you prefer another inbox.</p>
        </form>
      </div>
      <div class="card">
        <h3>Details</h3>
        <p>Phone: <a href="tel:+971503280002">+971 50 328 0002</a></p>
        <p>Email: <a href="mailto:Alhashmi-ad@outlook.com">Alhashmi-ad@outlook.com</a></p>
        <p>GitHub: <a href="https://github.com/Alahsshmi" rel="noopener">github.com/Alahsshmi</a></p>
        <p>LinkedIn: <a href="https://www.linkedin.com/in/abdul-rahman-alhashmi-b659541b0?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app" rel="noopener">Profile</a></p>
        <p><a class="btn ghost" href="cv/Abdulrahman-CV.pdf">Download CV</a></p>
        <p class="small">Location: United Arab Emirates</p>
      </div>
    </div>
  </div>
</section>

<footer>
  <div class="container">
    <p>© 2025 — Edited by Abdul Rahman Husain Alhashmi</p>
  </div>
</footer>

<script>
/* Theme toggle with persistence */
(function(){
  const root = document.documentElement;
  const btn = document.getElementById('themeBtn');
  const saved = localStorage.getItem('theme'); // 'light' | 'dark' | null
  if(saved){ root.setAttribute('data-theme', saved); }
  function current(){ return root.getAttribute('data-theme') || 'auto'; }
  function cycle(){
    const now = current();
    const next = now === 'light' ? 'dark' : now === 'dark' ? 'auto' : 'light';
    root.setAttribute('data-theme', next);
    localStorage.setItem('theme', next);
    btn.setAttribute('aria-pressed', next === 'dark');
  }
  btn.addEventListener('click', cycle);
})();

/* Active link highlighting on scroll */
(function(){
  const links = [...document.querySelectorAll('.menu a')];
  const map = new Map(links.map(a => [a.getAttribute('href'), a]));
  const opts = {rootMargin:'-55% 0px -40% 0px', threshold: [0,1]};
  const obs = new IntersectionObserver(entries=>{
    entries.forEach(e=>{
      const id = '#'+e.target.id;
      const link = map.get(id);
      if(!link) return;
      if(e.isIntersecting){
        links.forEach(l=>l.classList.remove('is-active'));
        link.classList.add('is-active');
      }
    });
  }, opts);
  ['home','modules','about','ml','agents','projects','contact']
    .forEach(id=>{const el=document.getElementById(id); if(el) obs.observe(el);});
})();

/* Expand/Collapse all for sections */
document.querySelectorAll('button[data-expand],button[data-collapse]').forEach(btn=>{
  const scopeSel = btn.getAttribute('data-scope');
  const scope = scopeSel ? document.querySelector(scopeSel) : null;
  if(!scope) return;
  const open = btn.hasAttribute('data-expand');
  btn.addEventListener('click', () => {
    scope.querySelectorAll('details.card').forEach(d => d.open = open);
  });
});

/* Respect reduced motion */
if (window.matchMedia('(prefers-reduced-motion: reduce)').matches) {
  document.documentElement.style.scrollBehavior = 'auto';
}
</script>
</body>
</html>
