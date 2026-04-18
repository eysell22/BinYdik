# BinYdik<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BinYdik 🛡️ — Application de sécurité pour femmes</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@700;800&family=DM+Sans:wght@300;400;500;600&family=Noto+Sans+Arabic:wght@400;600&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
:root{
  --bg:#08010f;
  --surface:#110720;
  --card:#160a28;
  --border:rgba(167,139,250,.15);
  --border2:rgba(167,139,250,.3);
  --purple:#7c3aed;
  --violet:#a78bfa;
  --lilac:#c4b5fd;
  --rose:#f43f5e;
  --green:#22c55e;
  --white:#fff;
  --muted:rgba(196,181,253,.65);
  --sans:'DM Sans',sans-serif;
  --title:'Syne',sans-serif;
  --arabic:'Noto Sans Arabic',sans-serif;
}
html{scroll-behavior:smooth;}
body{font-family:var(--sans);background:var(--bg);color:var(--white);overflow-x:hidden;min-height:100vh;}

/* NAV */
nav{position:fixed;top:0;left:0;right:0;z-index:200;display:flex;align-items:center;justify-content:space-between;padding:1rem 5%;background:rgba(8,1,15,.9);backdrop-filter:blur(20px);border-bottom:1px solid var(--border);}
.logo{font-family:var(--title);font-size:1.4rem;color:var(--white);text-decoration:none;display:flex;align-items:center;gap:.4rem;}
.logo span{color:var(--lilac);}
.nav-links{display:flex;gap:1.8rem;list-style:none;}
.nav-links a{color:var(--muted);text-decoration:none;font-size:.88rem;transition:color .2s;}
.nav-links a:hover{color:var(--white);}
.nav-btn{background:linear-gradient(135deg,var(--purple),var(--rose));color:white;border:none;padding:.55rem 1.3rem;border-radius:6px;font-family:var(--sans);font-size:.85rem;font-weight:600;cursor:pointer;text-decoration:none;transition:opacity .2s;}
.nav-btn:hover{opacity:.85;}

/* LAYOUT */
.page{padding-top:72px;}
.container{max-width:1100px;margin:0 auto;padding:0 5%;}

/* ── HERO ── */
.hero{min-height:calc(100vh - 72px);display:flex;align-items:center;justify-content:center;text-align:center;padding:4rem 5%;position:relative;overflow:hidden;}
.hero-glow{position:absolute;width:600px;height:600px;border-radius:50%;background:radial-gradient(circle,rgba(124,58,237,.3) 0%,transparent 70%);top:50%;left:50%;transform:translate(-50%,-55%);pointer-events:none;}
.hero-glow2{position:absolute;width:350px;height:350px;border-radius:50%;background:radial-gradient(circle,rgba(244,63,94,.15) 0%,transparent 70%);bottom:15%;right:10%;pointer-events:none;}
.hero-content{position:relative;z-index:1;max-width:720px;}
.hero-arabic{font-family:var(--arabic);font-size:1.1rem;color:var(--violet);margin-bottom:.4rem;letter-spacing:.05em;}
.hero-title{font-family:var(--title);font-size:clamp(3.5rem,8vw,6.5rem);font-weight:800;line-height:.95;background:linear-gradient(135deg,#fff 0%,var(--lilac) 50%,#f9a8d4 100%);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;margin-bottom:1.2rem;}
.hero-sub{font-size:1.05rem;color:var(--muted);line-height:1.75;max-width:520px;margin:0 auto 2.5rem;font-weight:300;}
.hero-btns{display:flex;gap:.8rem;justify-content:center;flex-wrap:wrap;}
.btn-main{background:linear-gradient(135deg,var(--purple),var(--rose));color:white;border:none;padding:.9rem 2rem;border-radius:8px;font-family:var(--sans);font-size:.95rem;font-weight:600;cursor:pointer;text-decoration:none;transition:transform .2s,box-shadow .2s;}
.btn-main:hover{transform:translateY(-2px);box-shadow:0 12px 35px rgba(124,58,237,.45);}
.btn-outline{background:transparent;color:var(--lilac);border:1px solid var(--border2);padding:.9rem 2rem;border-radius:8px;font-family:var(--sans);font-size:.95rem;font-weight:400;cursor:pointer;text-decoration:none;transition:all .2s;}
.btn-outline:hover{border-color:var(--violet);color:white;background:rgba(124,58,237,.1);}

/* ── APP SECTION ── */
.app-section{padding:4rem 0;}
.section-label{font-size:.7rem;font-weight:700;letter-spacing:.2em;text-transform:uppercase;color:var(--rose);margin-bottom:.8rem;display:block;}
.section-title{font-family:var(--title);font-size:clamp(1.8rem,3.5vw,2.6rem);font-weight:800;margin-bottom:.6rem;line-height:1.1;}
.section-sub{font-size:.95rem;color:var(--muted);line-height:1.7;margin-bottom:2.5rem;}

/* ── PHONE + DEMO ── */
.demo-layout{display:grid;grid-template-columns:280px 1fr;gap:4rem;align-items:start;}
.phone{background:#0d001f;border-radius:36px;border:2px solid var(--border2);padding:1.2rem 1rem;box-shadow:0 30px 80px rgba(0,0,0,.7),0 0 60px rgba(124,58,237,.25);position:sticky;top:90px;}
.phone-notch{width:70px;height:16px;background:#0d001f;border-radius:0 0 12px 12px;margin:-1.2rem auto .8rem;border:2px solid var(--border2);border-top:none;}
.phone-inner{display:flex;flex-direction:column;gap:.8rem;padding:.2rem 0;}

/* GPS bar */
.gps-bar{background:rgba(34,197,94,.08);border:1px solid rgba(34,197,94,.2);border-radius:8px;padding:.5rem .7rem;display:flex;align-items:center;gap:.5rem;font-size:.68rem;color:#4ade80;cursor:pointer;transition:background .2s;}
.gps-bar:hover{background:rgba(34,197,94,.15);}
.gps-dot{width:7px;height:7px;border-radius:50%;background:var(--green);box-shadow:0 0 8px var(--green);flex-shrink:0;animation:gpsPulse 2s ease infinite;}
@keyframes gpsPulse{0%,100%{opacity:1}50%{opacity:.4}}

/* SOS button */
.sos-wrap{display:flex;flex-direction:column;align-items:center;gap:.6rem;}
.sos-ring{position:relative;width:120px;height:120px;display:flex;align-items:center;justify-content:center;}
.sos-ring::before,.sos-ring::after{content:'';position:absolute;border-radius:50%;border:1.5px solid rgba(244,63,94,.3);animation:ring 2.5s ease infinite;}
.sos-ring::before{inset:-10px;}
.sos-ring::after{inset:-20px;animation-delay:.5s;}
@keyframes ring{0%{transform:scale(1);opacity:1}100%{transform:scale(1.15);opacity:0}}
.sos-btn{width:110px;height:110px;border-radius:50%;background:radial-gradient(circle at 38% 35%,#f43f5e,#9f1239);border:none;cursor:pointer;font-family:var(--title);font-size:1.5rem;font-weight:800;color:white;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:2px;position:relative;overflow:hidden;transition:transform .1s;user-select:none;-webkit-user-select:none;touch-action:none;}
.sos-btn:active{transform:scale(.94);}
.sos-btn .sos-sub{font-family:var(--sans);font-size:.55rem;font-weight:400;opacity:.8;}
.sos-progress{position:absolute;bottom:0;left:0;right:0;height:4px;background:rgba(255,255,255,.15);border-radius:0 0 50px 50px;overflow:hidden;}
.sos-fill{height:100%;background:#4ade80;width:0%;transition:none;}

/* Contacts in phone */
.phone-contacts{display:flex;flex-direction:column;gap:.4rem;}
.phone-contact-row{display:flex;align-items:center;gap:.5rem;background:rgba(167,139,250,.08);border:1px solid var(--border);border-radius:8px;padding:.45rem .6rem;}
.pc-avatar{width:28px;height:28px;border-radius:50%;background:linear-gradient(135deg,var(--purple),var(--rose));display:flex;align-items:center;justify-content:center;font-size:.75rem;flex-shrink:0;}
.pc-info{flex:1;min-width:0;}
.pc-name{font-size:.72rem;font-weight:600;color:white;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;}
.pc-phone{font-size:.62rem;color:var(--muted);}
.pc-remove{background:none;border:none;color:rgba(255,255,255,.25);cursor:pointer;font-size:.75rem;padding:0 2px;line-height:1;transition:color .2s;flex-shrink:0;}
.pc-remove:hover{color:var(--rose);}
.pc-status{width:6px;height:6px;border-radius:50%;background:var(--green);flex-shrink:0;}

/* ── CONTROLS PANEL ── */
.controls{display:flex;flex-direction:column;gap:1.2rem;}

/* Card */
.ctrl-card{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:1.4rem 1.6rem;transition:border-color .25s;}
.ctrl-card:hover{border-color:var(--border2);}
.ctrl-card-header{display:flex;align-items:center;gap:.8rem;margin-bottom:1rem;}
.ctrl-icon{width:38px;height:38px;border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:1.1rem;flex-shrink:0;}
.ctrl-title{font-weight:600;font-size:.95rem;}
.ctrl-sub{font-size:.8rem;color:var(--muted);margin-top:.1rem;}

/* Inputs */
.field{display:flex;flex-direction:column;gap:.35rem;margin-bottom:.9rem;}
.field label{font-size:.72rem;font-weight:600;letter-spacing:.1em;text-transform:uppercase;color:var(--lilac);}
.field input,.field select{background:rgba(255,255,255,.05);border:1px solid rgba(255,255,255,.12);border-radius:8px;padding:.65rem .9rem;color:white;font-size:.88rem;font-family:var(--sans);outline:none;transition:border-color .2s;width:100%;}
.field input:focus,.field select:focus{border-color:var(--violet);}
.field input::placeholder{color:rgba(255,255,255,.25);}
.field select option{background:#1a0f2e;color:white;}

/* Buttons */
.btn-action{width:100%;background:linear-gradient(135deg,var(--purple),var(--rose));border:none;color:white;padding:.75rem;border-radius:8px;font-family:var(--sans);font-size:.9rem;font-weight:600;cursor:pointer;transition:opacity .2s,transform .2s;}
.btn-action:hover{opacity:.88;transform:translateY(-1px);}
.btn-action:disabled{opacity:.4;cursor:not-allowed;transform:none;}
.btn-secondary{width:100%;background:transparent;border:1px solid var(--border2);color:var(--lilac);padding:.7rem;border-radius:8px;font-family:var(--sans);font-size:.88rem;cursor:pointer;transition:all .2s;margin-top:.5rem;}
.btn-secondary:hover{background:rgba(124,58,237,.15);border-color:var(--violet);}

/* Toggle */
.toggle-row{display:flex;align-items:center;justify-content:space-between;padding:.6rem 0;}
.toggle-label{font-size:.88rem;color:var(--white);}
.toggle-label small{display:block;font-size:.73rem;color:var(--muted);font-weight:300;}
.toggle{position:relative;width:44px;height:24px;flex-shrink:0;}
.toggle input{opacity:0;width:0;height:0;}
.toggle-slider{position:absolute;inset:0;background:rgba(255,255,255,.12);border-radius:12px;cursor:pointer;transition:.3s;}
.toggle-slider::before{content:'';position:absolute;width:18px;height:18px;border-radius:50%;background:white;left:3px;top:3px;transition:.3s;}
.toggle input:checked+.toggle-slider{background:var(--purple);}
.toggle input:checked+.toggle-slider::before{transform:translateX(20px);}

/* Badge */
.badge{font-size:.65rem;font-weight:700;padding:2px 7px;border-radius:10px;text-transform:uppercase;letter-spacing:.06em;}
.badge-free{background:rgba(34,197,94,.2);color:#4ade80;}
.badge-premium{background:rgba(251,191,36,.2);color:#fbbf24;}

/* Status chip */
.status-chip{display:inline-flex;align-items:center;gap:.35rem;font-size:.75rem;font-weight:500;padding:.3rem .7rem;border-radius:20px;margin-top:.6rem;}
.status-ok{background:rgba(34,197,94,.12);color:#4ade80;border:1px solid rgba(34,197,94,.25);}
.status-warn{background:rgba(251,191,36,.1);color:#fbbf24;border:1px solid rgba(251,191,36,.2);}
.status-err{background:rgba(244,63,94,.1);color:#fb7185;border:1px solid rgba(244,63,94,.2);}
.status-dot{width:6px;height:6px;border-radius:50%;background:currentColor;}

/* ── NOTIFICATIONS ── */
#notifStack{position:fixed;top:80px;right:1rem;z-index:9000;display:flex;flex-direction:column;gap:.6rem;pointer-events:none;max-width:300px;}
.notif{background:#150830;border-radius:14px;padding:.85rem 1rem;pointer-events:all;box-shadow:0 10px 40px rgba(0,0,0,.7);animation:slideIn .3s ease;max-width:300px;}
.notif-sos{border:1px solid rgba(244,63,94,.5);}
.notif-info{border:1px solid rgba(124,58,237,.4);}
.notif-ok{border:1px solid rgba(34,197,94,.4);}
.notif-head{display:flex;align-items:center;gap:.5rem;margin-bottom:.4rem;}
.notif-app-icon{width:26px;height:26px;border-radius:7px;display:flex;align-items:center;justify-content:center;font-size:.85rem;flex-shrink:0;}
.notif-app-name{font-size:.72rem;font-weight:600;color:white;flex:1;}
.notif-time{font-size:.65rem;color:rgba(255,255,255,.35);}
.notif-close{background:none;border:none;color:rgba(255,255,255,.3);cursor:pointer;font-size:.8rem;padding:0;line-height:1;}
.notif-contact{font-size:.73rem;font-weight:600;color:rgba(255,255,255,.85);margin-bottom:.2rem;}
.notif-msg{font-size:.73rem;color:rgba(255,255,255,.6);line-height:1.5;}
.notif-link{display:inline-block;margin-top:.4rem;font-size:.7rem;color:#93c5fd;text-decoration:none;background:rgba(59,130,246,.15);border:1px solid rgba(59,130,246,.25);padding:.2rem .6rem;border-radius:5px;}
@keyframes slideIn{from{opacity:0;transform:translateX(20px)}to{opacity:1;transform:translateX(0)}}

/* ── SOS ALERT MODAL ── */
.modal-bg{display:none;position:fixed;inset:0;background:rgba(0,0,0,.8);z-index:8000;align-items:center;justify-content:center;padding:1rem;}
.modal-box{background:#120728;border-radius:20px;padding:2rem;width:100%;max-width:460px;position:relative;text-align:center;}
.modal-close{position:absolute;top:1rem;right:1rem;background:rgba(255,255,255,.08);border:none;color:white;width:28px;height:28px;border-radius:50%;cursor:pointer;font-size:.8rem;}

/* ── SMS PHONE MOCKUP ── */
.sms-phone{background:#1a1a2e;border-radius:18px;overflow:hidden;border:1px solid rgba(255,255,255,.1);}
.sms-topbar{background:#252542;padding:.8rem 1rem;display:flex;align-items:center;gap:.6rem;}
.sms-avatar{width:32px;height:32px;border-radius:50%;background:linear-gradient(135deg,var(--rose),#9f1239);display:flex;align-items:center;justify-content:center;font-size:.9rem;}
.sms-from{font-size:.8rem;font-weight:600;color:white;}
.sms-time{font-size:.68rem;color:rgba(255,255,255,.35);margin-left:auto;}
.sms-body{padding:1rem;background:#0f0f20;}
.sms-bubble{background:#1e3a5f;border-radius:12px 12px 12px 4px;padding:.8rem 1rem;display:inline-block;max-width:90%;}
.sms-text{font-size:.8rem;color:white;line-height:1.6;white-space:pre-line;}
.sms-link{color:#60a5fa;text-decoration:underline;}

/* ── TRAJET ── */
.trajet-timer{font-family:var(--title);font-size:2rem;font-weight:800;color:var(--green);margin:.5rem 0;letter-spacing:.05em;}
.trajet-bar{height:6px;background:rgba(255,255,255,.08);border-radius:3px;overflow:hidden;margin:.6rem 0;}
.trajet-fill{height:100%;background:linear-gradient(90deg,var(--purple),var(--green));border-radius:3px;width:0%;transition:width 1s linear;}

/* ── FOOTER ── */
footer{border-top:1px solid var(--border);padding:2rem 5%;text-align:center;color:var(--muted);font-size:.8rem;margin-top:4rem;}
footer strong{color:var(--lilac);}

/* RESPONSIVE */
@media(max-width:800px){
  .nav-links{display:none;}
  .demo-layout{grid-template-columns:1fr;}
  .phone{position:static;max-width:280px;margin:0 auto;}
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="logo">🛡️ Bin<span>Ydik</span></a>
  <ul class="nav-links">
    <li><a href="#contacts-section">Contacts</a></li>
    <li><a href="#sos-section">SOS</a></li>
    <li><a href="#trajet-section">Trajet</a></li>
    <li><a href="#sms-section">SMS</a></li>
  </ul>
  <a href="#sos-section" class="nav-btn">🆘 SOS</a>
</nav>

<!-- NOTIFICATIONS -->
<div id="notifStack"></div>

<!-- HERO -->
<div class="page">
<section class="hero">
  <div class="hero-glow"></div>
  <div class="hero-glow2"></div>
  <div class="hero-content">
    <p class="hero-arabic">بين يديك — Entre tes mains</p>
    <h1 class="hero-title">BinYdik</h1>
    <p class="hero-sub">L'application de sécurité pour femmes. Ajoute tes contacts, active le GPS, et appuie sur SOS en cas de danger — tes proches sont alertés instantanément.</p>
    <div class="hero-btns">
      <a href="#contacts-section" class="btn-main">👥 Ajouter mes contacts</a>
      <a href="#sos-section" class="btn-outline">🆘 Tester le SOS</a>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════════════
     SECTION PRINCIPALE : APP
══════════════════════════════════════════ -->
<section class="app-section" id="contacts-section">
<div class="container">
  <div class="demo-layout">

    <!-- ── TÉLÉPHONE (sticky) ── -->
    <div class="phone" id="phoneDisplay">
      <div class="phone-notch"></div>
      <div class="phone-inner">

        <!-- GPS -->
        <div class="gps-bar" id="gpsBar" onclick="requestGPS()">
          <div class="gps-dot"></div>
          <span id="gpsText">Appuyer pour activer le GPS</span>
        </div>

        <!-- SOS -->
        <div class="sos-wrap" id="sos-section">
          <div class="sos-ring">
            <button class="sos-btn" id="sosBtn">
              SOS
              <span class="sos-sub" id="sosLabel">Maintenir 2s</span>
              <div class="sos-progress"><div class="sos-fill" id="sosFill"></div></div>
            </button>
          </div>
          <span style="font-size:.65rem;color:var(--muted);text-align:center;">Maintiens le bouton 2 secondes<br>pour déclencher l'alerte</span>
        </div>

        <!-- Contacts dans le téléphone -->
        <div style="font-size:.65rem;color:var(--muted);font-weight:600;text-transform:uppercase;letter-spacing:.1em;margin-top:.2rem;">Contacts d'urgence (<span id="phoneContactCount">0</span>)</div>
        <div class="phone-contacts" id="phoneContactList">
          <div style="font-size:.68rem;color:var(--muted);text-align:center;padding:.5rem;border:1px dashed var(--border);border-radius:8px;">Aucun contact →<br>ajoute-en ci-contre</div>
        </div>

      </div>
    </div>

    <!-- ── PANNEAU DE CONTRÔLE ── -->
    <div class="controls">

      <!-- CARTE 1: CONTACTS -->
      <div class="ctrl-card" id="contacts-card">
        <div class="ctrl-card-header">
          <div class="ctrl-icon" style="background:rgba(124,58,237,.2);">👥</div>
          <div>
            <div class="ctrl-title">Contacts d'urgence <span class="badge badge-free">Gratuit</span></div>
            <div class="ctrl-sub">Ces personnes recevront l'alerte SOS avec ta localisation</div>
          </div>
        </div>

        <div style="display:grid;grid-template-columns:1fr 1fr;gap:.7rem;">
          <div class="field">
            <label>Prénom</label>
            <input id="cName" type="text" placeholder="ex: Mama, Sara…">
          </div>
          <div class="field">
            <label>Numéro</label>
            <input id="cPhone" type="tel" placeholder="+216 XX XXX XXX">
          </div>
        </div>
        <div class="field">
          <label>Relation</label>
          <select id="cRel">
            <option>👩 Mère</option>
            <option>👨 Père</option>
            <option>👫 Amie</option>
            <option>🧑 Frère / Sœur</option>
            <option>❤️ Partenaire</option>
            <option>🏠 Autre famille</option>
          </select>
        </div>
        <button class="btn-action" onclick="addContact()">➕ Ajouter ce contact</button>

        <!-- Liste contacts -->
        <div id="contactListFull" style="margin-top:1rem;display:flex;flex-direction:column;gap:.5rem;"></div>
        <div id="noContactMsg" style="font-size:.8rem;color:var(--muted);text-align:center;padding:1rem;display:none;">Aucun contact pour l'instant.</div>
      </div>

      <!-- CARTE 2: GPS -->
      <div class="ctrl-card">
        <div class="ctrl-card-header">
          <div class="ctrl-icon" style="background:rgba(34,197,94,.15);">📍</div>
          <div>
            <div class="ctrl-title">Localisation GPS réelle <span class="badge badge-free">Gratuit</span></div>
            <div class="ctrl-sub">Ton lien Google Maps exact sera envoyé avec chaque alerte</div>
          </div>
        </div>
        <button class="btn-action" id="gpsBtn" onclick="requestGPS()" style="background:linear-gradient(135deg,#15803d,#16a34a);">📍 Activer ma localisation GPS</button>
        <div id="gpsResult" style="margin-top:.8rem;"></div>
      </div>

      <!-- CARTE 3: SOS DEMO -->
      <div class="ctrl-card" style="border-color:rgba(244,63,94,.3);">
        <div class="ctrl-card-header">
          <div class="ctrl-icon" style="background:rgba(244,63,94,.2);">🆘</div>
          <div>
            <div class="ctrl-title">Simuler une alerte SOS</div>
            <div class="ctrl-sub">Vois exactement ce que reçoivent tes contacts</div>
          </div>
        </div>
        <p style="font-size:.82rem;color:var(--muted);margin-bottom:1rem;line-height:1.6;">
          Utilise le <strong style="color:white;">bouton rouge sur le téléphone</strong> (maintenir 2s) — ou clique ci-dessous pour simuler directement.
        </p>
        <button class="btn-action" onclick="fireSOS()" style="background:linear-gradient(135deg,#9f1239,#f43f5e);">🚨 Déclencher l'alerte SOS</button>
        <button class="btn-secondary" onclick="showSMSPreview()">💬 Aperçu du SMS reçu</button>
      </div>

      <!-- CARTE 4: MODES -->
      <div class="ctrl-card" id="trajet-section">
        <div class="ctrl-card-header">
          <div class="ctrl-icon" style="background:rgba(251,191,36,.12);">⚙️</div>
          <div>
            <div class="ctrl-title">Paramètres & Modes</div>
            <div class="ctrl-sub">Personnalise ton expérience BinYdik</div>
          </div>
        </div>

        <div style="display:flex;flex-direction:column;gap:.2rem;">
          <div class="toggle-row">
            <div class="toggle-label">
              🤫 Mode discret
              <small>SOS silencieux — aucun son ni vibration</small>
            </div>
            <label class="toggle">
              <input type="checkbox" id="toggleDiscret" onchange="onToggleDiscret(this)">
              <span class="toggle-slider"></span>
            </label>
          </div>
          <div style="height:1px;background:var(--border);margin:.3rem 0;"></div>
          <div class="toggle-row">
            <div class="toggle-label">
              🎙️ Enregistrement audio
              <small>Enregistre le son lors de l'alerte SOS <span class="badge badge-premium">Premium</span></small>
            </div>
            <label class="toggle">
              <input type="checkbox" id="toggleAudio" onchange="onToggleAudio(this)">
              <span class="toggle-slider"></span>
            </label>
          </div>
          <div style="height:1px;background:var(--border);margin:.3rem 0;"></div>
          <div class="toggle-row">
            <div class="toggle-label">
              🔔 Alertes automatiques
              <small>Ping tes contacts toutes les 5 min si tu ne donnes pas signe de vie</small>
            </div>
            <label class="toggle">
              <input type="checkbox" id="togglePing" onchange="onTogglePing(this)">
              <span class="toggle-slider"></span>
            </label>
          </div>
        </div>
      </div>

      <!-- CARTE 5: PARTAGE TRAJET -->
      <div class="ctrl-card" id="sms-section">
        <div class="ctrl-card-header">
          <div class="ctrl-icon" style="background:rgba(96,165,250,.15);">🚶‍♀️</div>
          <div>
            <div class="ctrl-title">Partage de trajet en direct</div>
            <div class="ctrl-sub">Tes proches voient ta position en temps réel jusqu'à ton arrivée</div>
          </div>
        </div>
        <div class="field">
          <label>Destination</label>
          <input id="destName" type="text" placeholder="ex: Maison, Faculté, Boulot…">
        </div>
        <div id="trajetDisplay" style="display:none;">
          <div class="trajet-timer" id="trajetTimer">00:00</div>
          <div class="trajet-bar"><div class="trajet-fill" id="trajetFill"></div></div>
          <div style="font-size:.78rem;color:var(--muted);" id="trajetInfo">Trajet en cours…</div>
        </div>
        <button class="btn-action" id="trajetBtn" onclick="toggleTrajet()" style="background:linear-gradient(135deg,#1d4ed8,#2563eb);margin-top:.5rem;">🚶‍♀️ Démarrer le trajet</button>
        <div id="trajetStatus"></div>
      </div>

    </div>
  </div>
</div>
</section>

<!-- ── MODALS ── -->

<!-- SOS Modal -->
<div class="modal-bg" id="sosModal">
  <div class="modal-box">
    <button class="modal-close" onclick="closeModal('sosModal')">✕</button>
    <div id="sosModalContent"></div>
  </div>
</div>

<!-- SMS Preview Modal -->
<div class="modal-bg" id="smsModal">
  <div class="modal-box" style="text-align:left;">
    <button class="modal-close" onclick="closeModal('smsModal')">✕</button>
    <div style="margin-bottom:1rem;">
      <span class="section-label">Aperçu</span>
      <h3 style="font-family:var(--title);font-size:1.3rem;">Message reçu par tes contacts</h3>
      <p style="font-size:.82rem;color:var(--muted);margin-top:.3rem;">C'est exactement ce qu'ils verront sur leur téléphone.</p>
    </div>
    <div class="sms-phone">
      <div class="sms-topbar">
        <div class="sms-avatar">🛡️</div>
        <div>
          <div class="sms-from">BinYdik</div>
        </div>
        <div class="sms-time" id="smsTime"></div>
      </div>
      <div class="sms-body">
        <div class="sms-bubble">
          <div class="sms-text" id="smsBubble"></div>
        </div>
      </div>
    </div>
    <button class="btn-action" onclick="closeModal('smsModal')" style="margin-top:1rem;">Fermer</button>
  </div>
</div>

<!-- FOOTER -->
<footer>
  <p><strong>BinYdik 🛡️</strong> — Application de sécurité pour femmes</p>
  <p style="margin-top:.3rem;">Projet Entrepreneuriat · 2ème BI · FSEGT 2024-2025 · Dr. Samah Chemli Horchani</p>
</footer>
</div>

<!-- ══════════════════════════════════════════
     JAVASCRIPT — TOUT FONCTIONNEL
══════════════════════════════════════════ -->
<script>
// ── STATE ──
let contacts = JSON.parse(localStorage.getItem('by_contacts') || '[]');
let gpsLat = null, gpsLon = null;
let discreet = false, audioRec = false, pingActive = false;
let trajetActive = false, trajetSec = 0, trajetInterval = null;
let sosInterval = null, sosProgress = 0;

// ── INIT ──
window.addEventListener('DOMContentLoaded', () => {
  renderContacts();
  initSOS();
  // Try GPS silently on load
  if (navigator.geolocation) navigator.geolocation.getCurrentPosition(onGPSSuccess, () => {});
});

// ══════════════════════════
// GPS
// ══════════════════════════
function requestGPS() {
  const btn = document.getElementById('gpsBtn');
  btn.textContent = '⏳ Récupération GPS…';
  btn.disabled = true;
  if (!navigator.geolocation) {
    gpsLat = 36.8190; gpsLon = 10.1658;
    onGPSSuccess({ coords: { latitude: gpsLat, longitude: gpsLon } });
    return;
  }
  navigator.geolocation.getCurrentPosition(
    pos => onGPSSuccess(pos),
    err => {
      // Fallback Tunis
      gpsLat = 36.8190; gpsLon = 10.1658;
      onGPSSuccess({ coords: { latitude: gpsLat, longitude: gpsLon } });
    },
    { enableHighAccuracy: true, timeout: 8000 }
  );
}

function onGPSSuccess(pos) {
  gpsLat = pos.coords.latitude;
  gpsLon = pos.coords.longitude;
  const link = mapsLink();
  const shortCoords = `${gpsLat.toFixed(4)}, ${gpsLon.toFixed(4)}`;

  // Update phone GPS bar
  const gpsText = document.getElementById('gpsText');
  if (gpsText) gpsText.innerHTML = `GPS actif · <a href="${link}" target="_blank" style="color:#4ade80;">Voir Maps</a>`;

  // Update button
  const btn = document.getElementById('gpsBtn');
  if (btn) { btn.textContent = '✅ GPS actif — Cliquer pour rafraîchir'; btn.disabled = false; }

  // Show result
  const res = document.getElementById('gpsResult');
  if (res) res.innerHTML = `
    <div class="status-chip status-ok"><span class="status-dot"></span> Localisation obtenue</div>
    <div style="margin-top:.6rem;background:rgba(34,197,94,.06);border:1px solid rgba(34,197,94,.2);border-radius:8px;padding:.7rem .9rem;">
      <div style="font-size:.72rem;color:#4ade80;margin-bottom:.3rem;font-weight:600;">📍 Tes coordonnées GPS</div>
      <div style="font-size:.8rem;color:white;margin-bottom:.4rem;">${shortCoords}</div>
      <a href="${link}" target="_blank" style="font-size:.78rem;color:#60a5fa;text-decoration:underline;">Ouvrir dans Google Maps →</a>
    </div>
  `;
  notify('📍 GPS activé !', `Tes coordonnées sont prêtes à être partagées.`, 'ok');
}

function mapsLink() {
  return `https://maps.google.com/?q=${gpsLat},${gpsLon}`;
}

// ══════════════════════════
// CONTACTS
// ══════════════════════════
function addContact() {
  const name = document.getElementById('cName').value.trim();
  const phone = document.getElementById('cPhone').value.trim();
  const rel = document.getElementById('cRel').value;
  if (!name) { shake('cName'); return; }
  if (!phone) { shake('cPhone'); return; }
  const contact = { id: Date.now(), name, phone, rel };
  contacts.push(contact);
  save();
  renderContacts();
  document.getElementById('cName').value = '';
  document.getElementById('cPhone').value = '';
  notify(`✅ ${name} ajouté(e)`, `${rel} · ${phone} recevra tes alertes SOS.`, 'ok');
}

function removeContact(id) {
  contacts = contacts.filter(c => c.id !== id);
  save();
  renderContacts();
}

function renderContacts() {
  const phoneList = document.getElementById('phoneContactList');
  const fullList = document.getElementById('contactListFull');
  const count = document.getElementById('phoneContactCount');
  if (count) count.textContent = contacts.length;

  // Phone display
  if (phoneList) {
    if (contacts.length === 0) {
      phoneList.innerHTML = `<div style="font-size:.68rem;color:var(--muted);text-align:center;padding:.5rem;border:1px dashed var(--border);border-radius:8px;">Aucun contact →<br>ajoute-en ci-contre</div>`;
    } else {
      phoneList.innerHTML = contacts.map(c => `
        <div class="phone-contact-row">
          <div class="pc-status"></div>
          <div class="pc-avatar">${c.rel.split(' ')[0]}</div>
          <div class="pc-info">
            <div class="pc-name">${c.name}</div>
            <div class="pc-phone">${c.phone}</div>
          </div>
          <button class="pc-remove" onclick="removeContact(${c.id})">✕</button>
        </div>
      `).join('');
    }
  }

  // Full list panel
  if (fullList) {
    if (contacts.length === 0) {
      fullList.innerHTML = '';
      const msg = document.getElementById('noContactMsg');
      if (msg) msg.style.display = 'block';
    } else {
      const msg = document.getElementById('noContactMsg');
      if (msg) msg.style.display = 'none';
      fullList.innerHTML = contacts.map(c => `
        <div style="display:flex;align-items:center;gap:.7rem;background:rgba(167,139,250,.07);border:1px solid var(--border);border-radius:10px;padding:.7rem .9rem;">
          <div style="width:34px;height:34px;border-radius:50%;background:linear-gradient(135deg,var(--purple),var(--rose));display:flex;align-items:center;justify-content:center;font-size:.9rem;flex-shrink:0;">${c.rel.split(' ')[0]}</div>
          <div style="flex:1;min-width:0;">
            <div style="font-weight:600;font-size:.88rem;">${c.name} <span style="font-size:.72rem;color:var(--muted);font-weight:400;">${c.rel}</span></div>
            <div style="font-size:.78rem;color:var(--muted);">${c.phone}</div>
          </div>
          <button onclick="removeContact(${c.id})" style="background:rgba(244,63,94,.1);border:1px solid rgba(244,63,94,.2);color:var(--rose);border-radius:6px;padding:.3rem .6rem;cursor:pointer;font-size:.75rem;">Retirer</button>
        </div>
      `).join('');
    }
  }
}

// ══════════════════════════
// SOS BUTTON (hold 2s)
// ══════════════════════════
function initSOS() {
  const btn = document.getElementById('sosBtn');
  if (!btn) return;
  btn.addEventListener('mousedown', startHold);
  btn.addEventListener('mouseup', stopHold);
  btn.addEventListener('mouseleave', stopHold);
  btn.addEventListener('touchstart', e => { e.preventDefault(); startHold(); }, { passive: false });
  btn.addEventListener('touchend', stopHold);
}

function startHold() {
  sosProgress = 0;
  const fill = document.getElementById('sosFill');
  const label = document.getElementById('sosLabel');
  sosInterval = setInterval(() => {
    sosProgress += 2.5;
    if (fill) fill.style.width = sosProgress + '%';
    if (label) label.textContent = `${(sosProgress / 50).toFixed(1)}s / 2s`;
    if (sosProgress >= 100) {
      stopHold();
      fireSOS();
    }
  }, 50);
}

function stopHold() {
  if (sosInterval) { clearInterval(sosInterval); sosInterval = null; }
  const fill = document.getElementById('sosFill');
  const label = document.getElementById('sosLabel');
  if (fill) { fill.style.transition = 'width .3s ease'; fill.style.width = '0%'; setTimeout(() => fill.style.transition = 'none', 300); }
  if (label) label.textContent = 'Maintenir 2s';
}

// ══════════════════════════
// FIRE SOS
// ══════════════════════════
function fireSOS() {
  const btn = document.getElementById('sosBtn');
  const label = document.getElementById('sosLabel');
  if (btn) btn.style.background = 'radial-gradient(circle at 38% 35%,#16a34a,#15803d)';
  if (label) label.textContent = '✓ Envoyé !';
  setTimeout(() => {
    if (btn) btn.style.background = 'radial-gradient(circle at 38% 35%,#f43f5e,#9f1239)';
    if (label) label.textContent = 'Maintenir 2s';
  }, 3000);

  const link = gpsLat ? mapsLink() : 'https://maps.google.com/?q=36.8190,10.1658';
  const time = new Date().toLocaleTimeString('fr-TN', { hour: '2-digit', minute: '2-digit' });
  const msg = buildSOSMsg();

  // Show modal
  const modal = document.getElementById('sosModal');
  const content = document.getElementById('sosModalContent');
  content.innerHTML = `
    <div style="font-size:2.5rem;margin-bottom:.5rem;">🚨</div>
    <h2 style="font-family:var(--title);font-size:1.6rem;color:var(--rose);margin-bottom:.4rem;">Alerte SOS envoyée !</h2>
    <p style="font-size:.85rem;color:var(--muted);margin-bottom:1.5rem;">${time} · ${contacts.length} contact(s) alerté(s)</p>
    <div style="background:rgba(244,63,94,.08);border:1px solid rgba(244,63,94,.25);border-radius:12px;padding:1rem;margin-bottom:1.2rem;text-align:left;">
      <div style="font-size:.7rem;color:var(--rose);text-transform:uppercase;letter-spacing:.1em;margin-bottom:.5rem;">📩 Message envoyé :</div>
      <div style="font-size:.85rem;color:white;line-height:1.7;white-space:pre-line;">${msg}</div>
    </div>
    ${contacts.length > 0
      ? `<div style="display:flex;flex-wrap:wrap;gap:.4rem;justify-content:center;margin-bottom:1.2rem;">${contacts.map(c => `<div style="background:rgba(34,197,94,.12);border:1px solid rgba(34,197,94,.25);border-radius:20px;padding:.25rem .7rem;font-size:.75rem;color:#4ade80;">✓ ${c.name} (${c.phone})</div>`).join('')}</div>`
      : `<div style="background:rgba(244,63,94,.1);border:1px solid rgba(244,63,94,.2);border-radius:8px;padding:.7rem 1rem;margin-bottom:1rem;font-size:.82rem;color:#fb7185;">⚠️ Aucun contact enregistré — ajoute d'abord tes contacts !</div>`
    }
    <a href="${link}" target="_blank" class="btn-main" style="display:inline-block;margin-bottom:.8rem;text-decoration:none;">📍 Voir ma localisation sur Maps</a><br>
    <button onclick="closeModal('sosModal')" class="btn-outline" style="margin-top:.4rem;">Fermer</button>
  `;
  modal.style.display = 'flex';

  // Send notifications per contact
  if (contacts.length > 0) {
    contacts.forEach((c, i) => setTimeout(() => sendNotifToContact(c, link), i * 700));
  } else {
    notify('⚠️ Aucun contact', 'Ajoute des contacts pour recevoir les alertes !', 'sos');
  }
}

function buildSOSMsg() {
  const link = gpsLat ? mapsLink() : 'https://maps.google.com/?q=36.8190,10.1658';
  return `Hyeti BinYdik 🛡️ — SOS !\nAna m7taja mosa3da ! Taba3 ma localisation w ji bser3a ⚡\n\n📍 Ma position en temps réel :\n${link}`;
}

// ══════════════════════════
// NOTIFICATIONS
// ══════════════════════════
function sendNotifToContact(contact, link) {
  const time = new Date().toLocaleTimeString('fr-TN', { hour: '2-digit', minute: '2-digit' });
  const stack = document.getElementById('notifStack');
  const notif = document.createElement('div');
  notif.className = 'notif notif-sos';
  notif.innerHTML = `
    <div class="notif-head">
      <div class="notif-app-icon" style="background:linear-gradient(135deg,#9f1239,#f43f5e);">🛡️</div>
      <div class="notif-app-name">BinYdik · Messages</div>
      <div class="notif-time">${time}</div>
      <button class="notif-close" onclick="this.closest('.notif').remove()">✕</button>
    </div>
    <div class="notif-contact">📱 ${contact.name} (${contact.phone}) :</div>
    <div class="notif-msg">Hyeti BinYdik 🛡️ — SOS ! Ana m7taja mosa3da ! Taba3 ma localisation w ji bser3a ⚡</div>
    <a href="${link}" target="_blank" class="notif-link">📍 Voir la localisation →</a>
  `;
  stack.appendChild(notif);
  setTimeout(() => { notif.style.opacity = '0'; notif.style.transition = 'opacity .4s'; setTimeout(() => notif.remove(), 400); }, 8000);
}

function notify(title, body, type = 'info') {
  const stack = document.getElementById('notifStack');
  const cls = type === 'ok' ? 'notif-ok' : type === 'sos' ? 'notif-sos' : 'notif-info';
  const notif = document.createElement('div');
  notif.className = `notif ${cls}`;
  notif.innerHTML = `
    <div class="notif-head">
      <div class="notif-app-name">${title}</div>
      <button class="notif-close" onclick="this.closest('.notif').remove()">✕</button>
    </div>
    <div class="notif-msg">${body}</div>
  `;
  stack.appendChild(notif);
  setTimeout(() => { notif.style.opacity = '0'; notif.style.transition = 'opacity .4s'; setTimeout(() => notif.remove(), 400); }, 4000);
}

// ══════════════════════════
// SMS PREVIEW
// ══════════════════════════
function showSMSPreview() {
  const link = gpsLat ? mapsLink() : 'https://maps.google.com/?q=36.8190,10.1658';
  const msg = `Hyeti BinYdik 🛡️ — SOS !\nAna m7taja mosa3da ! Taba3 ma localisation w ji bser3a ⚡\n\n📍 Ma position en temps réel :\n${link}`;
  document.getElementById('smsTime').textContent = new Date().toLocaleTimeString('fr-TN', { hour: '2-digit', minute: '2-digit' });
  const bubble = document.getElementById('smsBubble');
  bubble.innerHTML = msg.replace(/\n/g, '<br>').replace(link, `<a href="${link}" target="_blank" class="sms-link">${link}</a>`);
  document.getElementById('smsModal').style.display = 'flex';
}

// ══════════════════════════
// TRAJET
// ══════════════════════════
function toggleTrajet() {
  if (!trajetActive) startTrajet(); else stopTrajet();
}

function startTrajet() {
  const dest = document.getElementById('destName').value.trim() || 'destination';
  trajetActive = true; trajetSec = 0;
  document.getElementById('trajetDisplay').style.display = 'block';
  document.getElementById('trajetBtn').textContent = '🛑 Terminer le trajet';
  document.getElementById('trajetBtn').style.background = 'linear-gradient(135deg,#9f1239,#f43f5e)';
  document.getElementById('trajetInfo').textContent = `Trajet vers ${dest} en cours…`;
  updateTrajetTimer();
  trajetInterval = setInterval(() => {
    trajetSec++;
    updateTrajetTimer();
    // Notify contacts every 60s
    if (trajetSec % 60 === 0 && contacts.length > 0) {
      const link = gpsLat ? mapsLink() : 'https://maps.google.com/?q=36.8190,10.1658';
      contacts.forEach(c => sendNotifToContact(c, link));
    }
  }, 1000);
  notify('🚶‍♀️ Trajet démarré', `Vers ${dest}. Tes contacts sont informés.`, 'info');
  if (contacts.length > 0) {
    const link = gpsLat ? mapsLink() : 'https://maps.google.com/?q=36.8190,10.1658';
    contacts.forEach((c, i) => setTimeout(() => sendNotifToContact(c, link), i * 600));
  }
}

function stopTrajet() {
  trajetActive = false;
  clearInterval(trajetInterval);
  document.getElementById('trajetBtn').textContent = '🚶‍♀️ Démarrer le trajet';
  document.getElementById('trajetBtn').style.background = 'linear-gradient(135deg,#1d4ed8,#2563eb)';
  document.getElementById('trajetInfo').textContent = 'Trajet terminé. Tes proches ont été notifiés.';
  document.getElementById('trajetFill').style.width = '100%';
  notify('🏁 Trajet terminé !', 'Tes contacts sont notifiés de ton arrivée.', 'ok');
}

function updateTrajetTimer() {
  const m = String(Math.floor(trajetSec / 60)).padStart(2, '0');
  const s = String(trajetSec % 60).padStart(2, '0');
  document.getElementById('trajetTimer').textContent = `${m}:${s}`;
  const pct = Math.min((trajetSec / 3600) * 100, 95);
  document.getElementById('trajetFill').style.width = pct + '%';
}

// ══════════════════════════
// TOGGLES
// ══════════════════════════
function onToggleDiscret(el) {
  discreet = el.checked;
  notify(discreet ? '🤫 Mode discret ON' : '🔔 Mode discret OFF',
    discreet ? 'L\'alerte SOS sera silencieuse.' : 'L\'alerte SOS émettra un son.', 'info');
}
function onToggleAudio(el) {
  audioRec = el.checked;
  if (audioRec && !el.dataset.warned) {
    el.dataset.warned = '1';
    notify('🎙️ Enregistrement audio', 'Fonctionnalité Premium — l\'audio sera enregistré lors du SOS.', 'info');
  }
}
function onTogglePing(el) {
  pingActive = el.checked;
  notify(pingActive ? '🔔 Alertes automatiques ON' : '🔕 Alertes automatiques OFF',
    pingActive ? 'Tes contacts recevront un ping toutes les 5 min.' : 'Alertes automatiques désactivées.', 'info');
}

// ══════════════════════════
// UTILS
// ══════════════════════════
function save() { localStorage.setItem('by_contacts', JSON.stringify(contacts)); }
function closeModal(id) { document.getElementById(id).style.display = 'none'; }
function shake(id) {
  const el = document.getElementById(id);
  el.style.borderColor = 'var(--rose)';
  el.animate([{transform:'translateX(-5px)'},{transform:'translateX(5px)'},{transform:'translateX(-4px)'},{transform:'translateX(0)'}], { duration: 350 });
  setTimeout(() => el.style.borderColor = '', 1000);
}

// Close modals on backdrop click
['sosModal','smsModal'].forEach(id => {
  document.getElementById(id).addEventListener('click', e => { if (e.target.id === id) closeModal(id); });
});
</script>
</body>
</html>

app de securité pour femmes[index.html.html](https://github.com/user-attachments/files/26848427/index.html.html)

