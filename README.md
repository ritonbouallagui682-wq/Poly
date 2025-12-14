<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Orion · Mobile Commerce App</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<meta name="description" content="Orion — modular mobile shopping application focused on clarity, performance and predictable commerce workflows.">

<style>
:root{
  --bg:#0b0c0f;
  --panel:#12131a;
  --border:#22232d;
  --text:#f4f5f7;
  --muted:#9aa0ad;
  --accent:#6ee7b7;
  --accent-soft:rgba(110,231,183,.15);
  --radius:16px;
}

*{box-sizing:border-box}

body{
  margin:0;
  background:
    radial-gradient(700px 400px at 15% -10%, #16201a 0%, transparent 60%),
    var(--bg);
  color:var(--text);
  font-family:-apple-system, BlinkMacSystemFont, "Segoe UI", system-ui, sans-serif;
}

.container{
  max-width:1080px;
  margin:0 auto;
  padding:84px 24px 96px;
}

/* ---------- HEADER ---------- */

header{
  margin-bottom:64px;
}

header h1{
  margin:0;
  font-size:48px;
  font-weight:600;
  letter-spacing:-0.04em;
}

header p{
  margin-top:14px;
  max-width:540px;
  font-size:15px;
  color:var(--muted);
}

.tags{
  margin-top:22px;
  display:flex;
  gap:10px;
  flex-wrap:wrap;
}

.tag{
  padding:8px 14px;
  font-size:12px;
  border-radius:999px;
  background:var(--accent-soft);
  border:1px solid rgba(110,231,183,.25);
  color:#d1fae5;
}

/* ---------- GRID ---------- */

.grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:26px;
}

@media(max-width:860px){
  .grid{grid-template-columns:1fr}
}

/* ---------- CARD ---------- */

.card{
  background:linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.015));
  border:1px solid var(--border);
  border-radius:var(--radius);
  padding:24px;
}

.card h2{
  margin:0 0 12px;
  font-size:14px;
  letter-spacing:.04em;
  text-transform:uppercase;
}

.card p{
  margin:0 0 12px;
  font-size:14px;
  color:var(--muted);
}

.card ul{
  margin:0;
  padding-left:18px;
  font-size:14px;
  color:var(--muted);
}

.card li{margin:6px 0}

/* ---------- CODE ---------- */

pre{
  margin:0;
  padding:18px;
  background:#0e1016;
  border:1px solid var(--border);
  border-radius:12px;
  font-family:ui-monospace, SFMono-Regular, Menlo, Consolas, monospace;
  font-size:12.5px;
  overflow:auto;
}

/* ---------- FOOTER ---------- */

footer{
  margin-top:72px;
  padding-top:24px;
  border-top:1px solid var(--border);
  display:flex;
  justify-content:space-between;
  flex-wrap:wrap;
  gap:10px;
  font-size:12px;
  color:var(--muted);
}
</style>
</head>

<body>
<div class="container">

<header>
  <h1>Orion</h1>
  <p>
    Modular mobile shopping application built for clean UX,
    predictable business logic and long-term scalability.
  </p>

  <div class="tags">
    <div class="tag">Mobile App</div>
    <div class="tag">Commerce Core</div>
    <div class="tag">Clean Architecture</div>
    <div class="tag">Scalable</div>
  </div>
</header>

<section class="grid">

  <div class="card">
    <h2>What Orion solves</h2>
    <ul>
      <li>Complex product catalogs</li>
      <li>Stable cart and checkout flow</li>
      <li>Transparent pricing logic</li>
      <li>Order tracking lifecycle</li>
      <li>User-centric experience</li>
    </ul>
  </div>

  <div class="card">
    <h2>Architecture</h2>
    <ul>
      <li>UI separated from business logic</li>
      <li>Domain-driven entities</li>
      <li>Explicit data ownership</li>
      <li>Composable services</li>
    </ul>
  </div>

  <div class="card">
    <h2>Project structure</h2>
<pre><code>src/
  app/
    screens/
    navigation/
    ui/
  domain/
    models/
    usecases/
  infrastructure/
    api/
    storage/
  shared/
    utils/
    constants/
</code></pre>
  </div>

  <div class="card">
    <h2>Commerce features</h2>
    <ul>
      <li>Product discovery</li>
      <li>Cart state management</li>
      <li>Checkout orchestration</li>
      <li>Order history</li>
      <li>Future payment integrations</li>
    </ul>
  </div>

  <div class="card">
    <h2>Getting started</h2>
<pre><code>git clone https://github.com/&lt;org&gt;/orion.git
cd orion

# install dependencies
# run on emulator or device
</code></pre>
  </div>

  <div class="card">
    <h2>Roadmap</h2>
    <ul>
      <li>User accounts & profiles</li>
      <li>Saved carts</li>
      <li>Analytics layer</li>
      <li>Performance benchmarks</li>
    </ul>
  </div>

</section>

<footer>
  <span>Orion · Mobile Commerce Platform</span>
  <span>Designed for clarity and evolution</span>
</footer>

</div>
</body>
</html>
