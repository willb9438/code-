# code-
<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Mon Site HTML — Exemple</title>
  <meta name="description" content="Exemple de site en une seule page HTML, responsive et prêt à personnaliser." />
  <style>
    :root{--bg:#0f1724;--card:#0b1220;--accent:#06b6d4;--muted:#94a3b8;--glass: rgba(255,255,255,0.04)}
    *{box-sizing:border-box}
    body{margin:0;font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;line-height:1.5;background:linear-gradient(180deg,#061223 0%, #071428 60%);color:#e6eef6}
    .container{max-width:1100px;margin:0 auto;padding:28px}
    header{display:flex;align-items:center;justify-content:space-between;padding:10px 0}
    .logo{display:flex;align-items:center;gap:12px}
    .logo .mark{width:42px;height:42px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#7c3aed);display:flex;align-items:center;justify-content:center;font-weight:700}
    nav a{color:var(--muted);text-decoration:none;margin-left:18px}
    nav a:hover{color:white}

    .hero{display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center;margin-top:28px}
    .card{background:var(--card);padding:22px;border-radius:14px;box-shadow:0 6px 30px rgba(2,6,23,0.6);backdrop-filter: blur(6px)}
    h1{font-size:clamp(28px,4vw,42px);margin:0 0 8px}
    p.lead{color:var(--muted);margin:0 0 18px}
    .btn{display:inline-block;padding:10px 16px;border-radius:10px;background:linear-gradient(90deg,var(--accent),#7c3aed);color:#042039;text-weight:700;text-decoration:none;font-weight:600}

    .features{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:20px}
    .feature{padding:14px;border-radius:10px;background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);border:1px solid rgba(255,255,255,0.03)}
    .feature h3{margin:0 0 8px;font-size:18px}
    .muted{color:var(--muted);font-size:14px}

    aside.right{position:relative}
    .mock{height:360px;border-radius:12px;background:linear-gradient(180deg,#031428,#05223b);display:flex;align-items:center;justify-content:center;color:var(--muted);font-weight:600}

    footer{margin-top:36px;padding:20px 0;border-top:1px solid rgba(255,255,255,0.03);color:var(--muted)}

    /* contact */
    form label{display:block;font-size:13px;margin-bottom:6px}
    form input, form textarea{width:100%;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.05);background:transparent;color:inherit}
    form .row{display:grid;grid-template-columns:1fr 1fr;gap:10px}

    @media (max-width:880px){
      .hero{grid-template-columns:1fr}
      .features{grid-template-columns:1fr}
      .mock{height:220px}
      nav a{margin-left:10px}
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="logo">
        <div class="mark">MS</div>
        <div>
          <div style="font-weight:700">MonSite</div>
          <div style="font-size:12px;color:var(--muted)">Exemple &amp; template</div>
        </div>
      </div>
      <nav>
        <a href="#features">Fonctionnalités</a>
        <a href="#contact">Contact</a>
        <a class="btn" href="#contact">Essayez</a>
      </nav>
    </header>

    <section class="hero">
      <div>
        <div class="card">
          <h1>Un site HTML simple, responsive et prêt à personnaliser</h1>
          <p class="lead">Ce modèle contient une structure claire — en-tête, zone "hero", features, contact — et un style moderne. Copiez-collez et modifiez comme vous le souhaitez.</p>
          <p>
            <a class="btn" href="#contact">Me contacter</a>
            <a style="margin-left:12px;color:var(--muted);text-decoration:none" href="#features">Voir les fonctionnalités →</a>
          </p>
        </div>

        <div id="features" class="features" style="margin-top:18px">
          <div class="feature card">
            <h3>Design responsive</h3>
            <div class="muted">S'adapte aux mobiles et tablettes.</div>
          </div>
          <div class="feature card">
            <h3>Facile à modifier</h3>
            <div class="muted">HTML + CSS clairs, pas de frameworks obligatoires.</div>
          </div>
          <div class="feature card">
            <h3>Formulaire de contact</h3>
            <div class="muted">Formulaire front-end prêt — connectez un back-end ou un service d'email.</div>
          </div>
        </div>
      </div>

      <aside class="right">
        <div class="mock card">
          Aperçu du site
        </div>
      </aside>
    </section>

    <section id="contact" style="margin-top:20px">
      <div class="card">
        <h2>Contact</h2>
        <p class="muted">Envoyez un message — ceci est uniquement la version front-end (pas d'envoi réel).</p>
        <form onsubmit="submitForm(event)">
          <div class="row" style="margin-top:12px">
            <div>
              <label for="name">Nom</label>
              <input id="name" placeholder="Votre nom" required />
            </div>
            <div>
              <label for="email">Email</label>
              <input id="email" type="email" placeholder="votre@exemple.com" required />
            </div>
          </div>
          <div style="margin-top:10px">
            <label for="message">Message</label>
            <textarea id="message" rows="5" placeholder="Votre message..."></textarea>
          </div>
          <p style="margin-top:12px">
            <button class="btn" type="submit">Envoyer</button>
          </p>
          <p id="status" class="muted" style="margin-top:8px"></p>
        </form>
      </div>
    </section>

    <footer>
      <div style="display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap">
        <div>© <strong>MonSite</strong> — Modèle simple</div>
        <div class="muted">Fait avec ❤️ — modifiez librement</div>
      </div>
    </footer>
  </div>

  <script>
    function submitForm(e){
      e.preventDefault();
      const status = document.getElementById('status');
      status.textContent = 'Simulation d\'envoi — intégration côté serveur requise pour envoyer réellement.';
      setTimeout(()=> status.textContent = 'Message prêt (pas envoyé). Vous pouvez connecter fetch() vers votre backend.',800);
    }
  </script>
</body>
</html>
