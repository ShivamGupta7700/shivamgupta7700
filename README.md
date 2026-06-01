<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shivam — GitHub Profile</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0d1117;
    --surface: #161b22;
    --border: #21262d;
    --text: #e6edf3;
    --muted: #7d8590;
    --accent: #58a6ff;
    --green: #3fb950;
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Syne', sans-serif;
    min-height: 100vh;
    display: flex;
    align-items: flex-start;
    justify-content: center;
    padding: 48px 24px;
  }

  .card {
    width: 100%;
    max-width: 680px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 40px 44px;
    position: relative;
    overflow: hidden;
  }

  .card::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 260px; height: 260px;
    background: radial-gradient(circle, rgba(88,166,255,0.07) 0%, transparent 70%);
    pointer-events: none;
  }

  /* Typewriter section */
  .typewriter-section {
    text-align: center;
    margin-bottom: 32px;
    padding-bottom: 28px;
    border-bottom: 1px solid var(--border);
  }

  .typewriter-line {
    font-family: 'JetBrains Mono', monospace;
    font-size: 22px;
    font-weight: 500;
    color: #36bcf7;
    min-height: 34px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 2px;
  }

  .cursor {
    display: inline-block;
    width: 2px;
    height: 1.2em;
    background: #36bcf7;
    margin-left: 2px;
    animation: blink 0.75s step-end infinite;
  }

  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }

  /* Header */
  .header { display: flex; align-items: center; gap: 18px; margin-bottom: 28px; }

  .avatar {
    width: 56px; height: 56px; border-radius: 50%;
    background: linear-gradient(135deg, #1f6feb 0%, #58a6ff 100%);
    display: flex; align-items: center; justify-content: center;
    font-size: 22px; font-weight: 800; color: #fff;
    flex-shrink: 0;
    border: 2px solid var(--border);
  }

  .header-text h1 {
    font-size: 22px; font-weight: 700;
    color: var(--text); line-height: 1.2;
  }

  .header-text p {
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px; color: var(--accent);
    margin-top: 4px;
    display: flex; align-items: center; gap: 6px;
  }

  .header-text p::before {
    content: '';
    display: inline-block;
    width: 8px; height: 8px; border-radius: 50%;
    background: var(--green);
    box-shadow: 0 0 6px var(--green);
    animation: pulse 2s ease-in-out infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.5; }
  }

  .divider {
    height: 1px; background: var(--border);
    margin: 0 -44px 28px;
  }

  .about {
    font-size: 15px; color: var(--muted);
    line-height: 1.7; margin-bottom: 32px;
  }

  .about strong { color: var(--text); font-weight: 600; }

  .section-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px; font-weight: 500;
    color: var(--muted);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 14px;
  }

  .chips { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 32px; }

  .chip {
    display: flex; align-items: center; gap: 7px;
    background: var(--bg);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 7px 14px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px; font-weight: 500;
    color: var(--text);
    transition: border-color 0.2s, color 0.2s;
  }

  .chip:hover { border-color: var(--accent); color: var(--accent); }

  .chip .dot {
    width: 7px; height: 7px; border-radius: 50%;
    flex-shrink: 0;
  }

  .stats { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; }

  .stat {
    background: var(--bg);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 14px 16px;
    text-align: center;
  }

  .stat-val {
    font-size: 18px; font-weight: 700;
    color: var(--text); margin-bottom: 4px;
  }

  .stat-label {
    font-size: 11px; color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
  }

  .footer-note {
    margin-top: 24px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px; color: var(--muted);
    text-align: center;
  }

  .footer-note span { color: var(--accent); }
</style>
</head>
<body>
<div class="card">

  <!-- Typewriter -->
  <div class="typewriter-section">
    <div class="typewriter-line">
      <span id="typed-text"></span><span class="cursor"></span>
    </div>
  </div>

  <div class="header">
    <div class="avatar">S</div>
    <div class="header-text">
      <h1>Shivam</h1>
      <p>JEE 2026 Aspirant</p>
    </div>
  </div>

  <div class="divider"></div>

  <p class="about">
    Exploring <strong>machine learning & automation</strong> — understanding how algorithms learn and make decisions, alongside JEE prep. Building skills in AI/ML to create real products someday.
  </p>

  <div class="section-label">Tech I use</div>
  <div class="chips">
    <div class="chip"><span class="dot" style="background:#3776ab;"></span>Python</div>
    <div class="chip"><span class="dot" style="background:#f34b7d;"></span>C++</div>
    <div class="chip"><span class="dot" style="background:#ff9f43;"></span>Machine Learning</div>
    <div class="chip"><span class="dot" style="background:#58a6ff;"></span>DSA</div>
  </div>

  <div class="section-label">Currently</div>
  <div class="stats">
    <div class="stat">
      <div class="stat-val">📚</div>
      <div class="stat-label">JEE Prep</div>
    </div>
    <div class="stat">
      <div class="stat-val">🤖</div>
      <div class="stat-label">Learning ML</div>
    </div>
    <div class="stat">
      <div class="stat-val">⚡</div>
      <div class="stat-label">Building</div>
    </div>
  </div>

  <div class="footer-note">
    // <span>open to learn</span> · <span>open to build</span>
  </div>

</div>

<script>
  const lines = [
    "Hello, World!",
    "I am Shivam.",
    "JEE 2026 Aspirant.",
    "Future Software Engineer.",
    "Building A Brain. 🧠"
  ];

  let lineIndex = 0;
  let charIndex = 0;
  let deleting = false;
  const el = document.getElementById('typed-text');
  const typeSpeed = 70;
  const deleteSpeed = 40;
  const pauseAfterType = 1800;
  const pauseAfterDelete = 400;

  function type() {
    const current = lines[lineIndex];
    if (!deleting) {
      el.textContent = current.slice(0, charIndex + 1);
      charIndex++;
      if (charIndex === current.length) {
        setTimeout(() => { deleting = true; type(); }, pauseAfterType);
        return;
      }
      setTimeout(type, typeSpeed);
    } else {
      el.textContent = current.slice(0, charIndex - 1);
      charIndex--;
      if (charIndex === 0) {
        deleting = false;
        lineIndex = (lineIndex + 1) % lines.length;
        setTimeout(type, pauseAfterDelete);
        return;
      }
      setTimeout(type, deleteSpeed);
    }
  }

  type();
</script>
</body>
</html>
