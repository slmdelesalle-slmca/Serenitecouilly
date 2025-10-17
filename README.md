<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sérénité Couilly – Accompagnement seniors</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
<style>
body { font-family: "Segoe UI", Arial, sans-serif; margin:0; padding:0; color:#2c3e50; background:#f0f6f5; font-size:18px; line-height:1.6; }
header { background:#7fc4b5; padding:25px; text-align:center; color:white; }
header h1 { margin:0; font-size:2.5em; }
nav { background:#66b2a5; padding:12px; text-align:center; }
nav a { color:white; text-decoration:none; margin:0 15px; font-weight:bold; font-size:1.1em; }
nav a:hover { text-decoration:underline; }
section { padding:50px 20px; max-width:1100px; margin:auto; }
h2 { color:#3a7d6e; margin-bottom:25px; text-align:center; font-size:2em; }
.services, .packs { display:flex; flex-wrap:wrap; gap:25px; justify-content:center; }
.card { background:white; padding:25px; border-radius:15px; box-shadow:0 3px 8px rgba(0,0,0,0.12); flex:1 1 300px; position:relative; transition: transform 0.3s, box-shadow 0.3s; }
.card:hover { transform: translateY(-5px); box-shadow:0 10px 20px rgba(0,0,0,0.2); }
.card h3 { margin-top:0; color:#3a7d6e; font-size:1.5em; }
.card p { margin:12px 0; font-size:1.1em; }
.icon { font-size:2.2em; color:#7fc4b5; margin-bottom:12px; }
.btn { display:inline-block; padding:14px 25px; margin-top:15px; background:#7fc4b5; color:white; text-decoration:none; border-radius:12px; font-weight:bold; cursor:pointer; font-size:1.2em; text-align:center; width:100%; }
.btn:hover { background:#66b2a5; }
form { display:flex; flex-direction:column; gap:18px; }
input, textarea, button { padding:14px; font-size:1.1em; border:1px solid #ccc; border-radius:12px; }
button { background:#7fc4b5; color:white; border:none; cursor:pointer; font-weight:bold; font-size:1.2em; }
button:hover { background:#66b2a5; }
footer { text-align:center; padding:25px; background:#66b2a5; color:white; margin-top:40px; font-size:1.1em; }
#map { width:100%; height:350px; border-radius:15px; margin-top:20px; }
/* Slider témoignages */
.testimonial-container { position: relative; overflow: hidden; max-width:100%; height:160px; margin:auto; }
.testimonial-slide { display:flex; transition: transform 0.5s ease; }
.testimonial { min-width:100%; padding:20px; box-sizing:border-box; text-align:center; font-style:italic; font-size:1.1em; }
.slider-btn { position:absolute; top:50%; transform:translateY(-50%); background:rgba(0,0,0,0.35); color:white; border:none; padding:10px; cursor:pointer; border-radius:50%; font-size:1.2em; }
.prev { left:12px; }
.next { right:12px; }
/* Pop-up form */
.modal { display:none; position:fixed; z-index:1000; left:0; top:0; width:100%; height:100%; background:rgba(0,0,0,0.65); justify-content:center; align-items:center; }
.modal-content { background:white; padding:35px; border-radius:15px; max-width:450px; width:90%; position:relative; }
.close { position:absolute; top:12px; right:18px; font-size:22px; font-weight:bold; cursor:pointer; }
@media (max-width:768px) { .services, .packs { flex-direction:column; } }
</style>
</head>
<body>

<header>
  <h1>Sérénité Couilly</h1>
  <p>Accompagnement et compagnie pour seniors à Couilly-Pont-aux-Dames et environs</p>
</header>

<nav>
  <a href="#services">Services</a>
  <a href="#packs">Packs</a>
  <a href="#about">À propos</a>
  <a href="#testimonials">Témoignages</a>
  <a href="#contact">Contact</a>
</nav>

<section id="services">
<h2>Nos services</h2>
<div class="services">
  <div class="card"><div class="icon"><i class="fas fa-users"></i></div><h3>Visite de compagnie</h3><p>Moments conviviaux, discussion et promenades courtes.</p></div>
  <div class="card"><div class="icon"><i class="fas fa-car-side"></i></div><h3>Accompagnement RDV / sorties</h3><p>Présence sécurisée pour rendez-vous médicaux ou sorties.</p></div>
  <div class="card"><div class="icon"><i class="fas fa-file-alt"></i></div><h3>Aide administrative / numérique</h3><p>Tri courrier, formulaires et démarches en ligne simples.</p></div>
  <div class="card"><div class="icon"><i class="fas fa-brain"></i></div><h3>Ateliers mémoire / bien-être</h3><p>Stimulation cognitive, jeux et activités douces.</p></div>
</div>
</section>

<section id="packs">
<h2>Nos packs et tarifs</h2>
<div class="packs">

  <!-- Standard 4 visites -->
  <div class="card">
    <h3>Standard 4 visites</h3>
    <p>4 visites / mois, compagnie et aide simple</p>
    <p><strong>90 € / mois</strong></p>
    <div class="btn" onclick="openModal('Standard 4 visites')">Réserver ce pack</div>
    <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
      <input type="hidden" name="cmd" value="_xclick">
      <input type="hidden" name="business" value="ton-email-paypal@example.com">
      <input type="hidden" name="item_name" value="Standard 4 visites">
      <input type="hidden" name="amount" value="90.00">
      <input type="hidden" name="currency_code" value="EUR">
      <input type="submit" value="Payer maintenant" class="btn">
    </form>
  </div>

  <!-- Présence & Confort -->
  <div class="card">
    <h3>Présence & Confort</h3>
    <p>6 visites / mois, compagnie et aide administrative</p>
    <p><strong>110 € / mois</strong></p>
    <div class="btn" onclick="openModal('Présence & Confort')">Réserver ce pack</div>
    <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
      <input type="hidden" name="cmd" value="_xclick">
      <input type="hidden" name="business" value="ton-email-paypal@example.com">
      <input type="hidden" name="item_name" value="Présence & Confort">
      <input type="hidden" name="amount" value="110.00">
      <input type="hidden" name="currency_code" value="EUR">
      <input type="submit" value="Payer maintenant" class="btn">
    </form>
  </div>

  <!-- Premium Bien-Être -->
  <div class="card">
    <h3>Premium Bien-Être</h3>
    <p>4 visites + 2 ateliers</p>
    <p><strong>130 € / mois</strong></p>
    <div class="btn" onclick="openModal('Premium Bien-Être')">Réserver ce pack</div>
    <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
      <input type="hidden" name="cmd" value="_xclick">
      <input type="hidden" name="business" value="ton-email-paypal@example.com">
      <input type="hidden" name="item_name" value="Premium Bien-Être">
      <input type="hidden" name="amount" value="130.00">
      <input type="hidden" name="currency_code" value="EUR">
      <input type="submit" value="Payer maintenant" class="btn">
    </form>
  </div>

  <!-- Accompagnement complet -->
  <div class="card">
    <h3>Accompagnement complet</h3>
    <p>8 visites / mois, accompagnement complet</p>
    <p><strong>210 € / mois</strong></p>
    <div class="btn" onclick="openModal('Accompagnement complet')">Réserver ce pack</div>
    <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
      <input type="hidden" name="cmd" value="_xclick">
      <input type="hidden" name="business" value="ton-email-paypal@example.com">
      <input type="hidden" name="item_name" value="Accompagnement complet">
      <input type="hidden" name="amount" value="210.00">
      <input type="hidden" name="currency_code" value="EUR">
      <input type="submit" value="Payer maintenant" class="btn">
    </form>
  </div>

  <!-- Répits pour aidants -->
  <div class="card">
    <h3>Répits pour aidants</h3>
    <p>4 h / mois à domicile</p>
    <p><strong>85 € / mois</strong></p>
    <div class="btn" onclick="openModal('Répits pour aidants')">Réserver ce pack</div>
    <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
      <input type="hidden" name="cmd" value="_xclick">
      <input type="hidden" name="business" value="ton-email-paypal@example.com">
      <input type="hidden" name="item_name" value="Répits pour aidants">
      <input type="hidden" name="amount" value="85.00">
      <input type="hidden" name="currency_code" value="EUR">
      <input type="submit" value="
