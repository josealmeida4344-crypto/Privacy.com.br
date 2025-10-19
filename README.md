# Privacy
<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>SeuNome • Cartões Virtuais</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header class="site-header">
    <div class="container">
      <a class="logo" href="#">SeuNome</a>
      <nav class="nav">
        <a href="#features">Recursos</a>
        <a href="#how">Como funciona</a>
        <a href="privacy.html">Privacidade</a>
        <button id="signupBtn" class="btn primary">Criar conta</button>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="container hero-inner">
        <div class="hero-copy">
          <h1>Cartões virtuais para pagar online com segurança</h1>
          <p>Crie cartões únicos, defina limites, pause e feche instantaneamente — mantenha seu cartão real protegido.</p>
          <div class="hero-ctas">
            <button id="ctaSignup" class="btn primary">Começar grátis</button>
            <a class="btn ghost" href="#how">Como funciona</a>
          </div>
        </div>
        <div class="hero-mock">
          <div class="mock-card">
            <div class="card-top">VIRTUAL • **** **** **** 1234</div>
            <div class="card-bottom">
              <div class="left">EXP 12/28</div>
              <div class="right">CVV •••</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="features" class="features">
      <div class="container">
        <h2>Recursos</h2>
        <div class="grid">
          <div class="feature">
            <h3>Cartões únicos</h3>
            <p>Gere cartões para cada loja — se um vazamento ocorrer, isole o dano.</p>
          </div>
          <div class="feature">
            <h3>Limites e bloqueios</h3>
            <p>Defina limite de gastos e bloqueie por comerciante em segundos.</p>
          </div>
          <div class="feature">
            <h3>Pausar ou fechar</h3>
            <p>Pausar automaticamente pagamentos recorrentes ou fechar o cartão com um clique.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="how" class="how">
      <div class="container">
        <h2>Como funciona</h2>
        <ol>
          <li>Crie uma conta gratuita.</li>
          <li>Vincule sua conta bancária (mock neste template).</li>
          <li>Gere um cartão virtual e use normalmente online.</li>
        </ol>
      </div>
    </section>

    <section class="cards-demo">
      <div class="container">
        <h2>Seu painel</h2>
        <p>Exemplo interativo — crie cartões fictícios abaixo (apenas frontend).</p>

        <div class="card-actions">
          <input id="merchant" placeholder="Nome do comerciante (ex: Netflix)" />
          <input id="limit" placeholder="Limite (R$)" type="number" />
          <button id="createCard" class="btn primary">Gerar cartão</button>
        </div>

        <div id="cardsList" class="cards-list">
          <!-- cartões serão inseridos via JS -->
        </div>
      </div>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container">
      <div>© <span id="year"></span> SeuNome — Protegendo seus pagamentos</div>
      <div><a href="privacy.html">Política de Privacidade</a></div>
    </div>
  </footer>

  <!-- modal de signup (simples) -->
  <div id="modal" class="modal hidden">
    <div class="modal-panel">
      <button id="closeModal" class="modal-close">×</button>
      <h3>Criar conta</h3>
      <p>Este é um formulário mock — para transformar em real, integre um back-end.</p>
      <form id="signupForm">
        <input name="email" type="email" placeholder="Seu e-mail" required />
        <input name="password" type="password" placeholder="Senha" required />
        <button class="btn primary" type="submit">Criar conta</button>
      </form>
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
:root{
  --bg:#0f1724;
  --card:#0b1220;
  --accent:#4f46e5;
  --muted:#94a3b8;
  --white:#ffffff;
  --glass: rgba(255,255,255,0.04);
  font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
}
*{box-sizing:border-box}
body{margin:0;background:linear-gradient(180deg,#071025 0%, #071126 100%);color:var(--white);-webkit-font-smoothing:antialiased}
.container{max-width:1100px;margin:0 auto;padding:28px}
.site-header{padding:18px 0;background:transparent;position:sticky;top:0;z-index:40}
.site-header .container{display:flex;align-items:center;justify-content:space-between}
.logo{font-weight:700;color:var(--white);text-decoration:none;font-size:20px}
.nav a{color:var(--muted);margin-right:18px;text-decoration:none}
.btn{padding:10px 14px;border-radius:8px;border:0;cursor:pointer;font-weight:600}
.btn.primary{background:linear-gradient(90deg,var(--accent),#7c3aed);color:white}
.btn.ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--white)}
.hero{padding:60px 0}
.hero-inner{display:flex;gap:28px;align-items:center}
.hero-copy{flex:1}
.hero-copy h1{font-size:36px;margin:0 0 12px}
.hero-copy p{color:var(--muted);margin:0 0 18px}
.hero-mock{width:320px;display:flex;justify-content:center}
.mock-card{width:320px;height:190px;border-radius:14px;padding:18px;background:linear-gradient(180deg,#0b1220, #0b1326);box-shadow:0 8px 30px rgba(0,0,0,0.6);border:1px solid rgba(255,255,255,0.03);color:var(--muted)}
.mock-card .card-top{font-weight:700;color:var(--white);font-size:18px;margin-bottom:36px}
.mock-card .card-bottom{display:flex;justify-content:space-between;color:var(--muted)}
.features{padding:40px 0}
.features h2{margin-bottom:18px}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:18px}
.feature{background:var(--glass);padding:18px;border-radius:10px;color:var(--muted)}
.how{padding:32px 0;background:rgba(255,255,255,0.02);border-top:1px solid rgba(255,255,255,0.02)}
.cards-demo{padding:36px 0}
.card-actions{display:flex;gap:8px;margin-bottom:18px}
.card-actions input{padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.06);background:transparent;color:var(--white)}
.cards-list{display:flex;flex-wrap:wrap;gap:12px}
.card-item{width:220px;background:linear-gradient(180deg,#0b1220,#071126);padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.03)}
.card-item .meta{color:var(--muted);font-size:13px;margin-top:8px}
.site-footer{padding:18px 0;border-top:1px solid rgba(255,255,255,0.03);margin-top:40px}
.modal{position:fixed;inset:0;display:flex;align-items:center;justify-content:center;background:rgba(2,6,23,0.6)}
.hidden{display:none}
.modal-panel{background:#071029;padding:20px;border-radius:12px;width:360px;position:relative;border:1px solid rgba(255,255,255,0.03)}
.modal-close{position:absolute;right:10px;top:6px;background:transparent;color:var(--muted);font-size:22px;border:0}
input, button{font-family:inherit}
@media (max-width:820px){
  .hero-inner{flex-direction:column}
  .hero-mock{width:100%}
}
