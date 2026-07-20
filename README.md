<!DOCTYPE html>
<html lang="ro">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mentor AI – Planuri de Abonament</title>
<style>
:root {
  /* === NOUA PALETĂ CROMATICĂ MENTOR AI === */
  /* Culoare primară: Albastru închis profesional */
  --primary-900: #0f172a;
  --primary-800: #1e293b;
  --primary-700: #334155;
  --primary-600: #475569;
  --primary-500: #64748b;
  --primary-400: #94a3b8;
  --primary-300: #cbd5e1;
  --primary-200: #e2e8f0;
  --primary-100: #f1f5f9;
  --primary-50:  #f8fafc;

  /* Culoare secundară: Portocaliu/Amber (opus albastru) */
  --accent-900: #78350f;
  --accent-800: #92400e;
  --accent-700: #b45309;
  --accent-600: #d97706;
  --accent-500: #f59e0b;
  --accent-400: #fbbf24;
  --accent-300: #fcd34d;
  --accent-200: #fde68a;
  --accent-100: #fef3c7;
  --accent-50:  #fffbeb;

  /* Culoare terțiară: Gri neutru (între alb și gri) */
  --neutral-900: #171717;
  --neutral-800: #262626;
  --neutral-700: #404040;
  --neutral-600: #525252;
  --neutral-500: #737373;
  --neutral-400: #a3a3a3;
  --neutral-300: #d4d4d4;
  --neutral-200: #e5e5e5;
  --neutral-100: #f5f5f5;
  --neutral-50:  #fafafa;

  /* Culori funcționale */
  --success: #059669;
  --success-light: #d1fae5;
  --danger: #dc2626;
  --danger-light: #fee2e2;
  --warning: #d97706;
  --warning-light: #fef3c7;

  /* Culori planuri */
  --plan-free: #dc2626;
  --plan-free-light: #fef2f2;
  --plan-free-bg: linear-gradient(135deg, #fef2f2 0%, #fee2e2 100%);

  --plan-premium: #d97706;
  --plan-premium-light: #fffbeb;
  --plan-premium-bg: linear-gradient(135deg, #fffbeb 0%, #fef3c7 100%);

  --plan-pro: #059669;
  --plan-pro-light: #ecfdf5;
  --plan-pro-bg: linear-gradient(135deg, #ecfdf5 0%, #d1fae5 100%);

  --plan-elite: #475569;
  --plan-elite-light: #f8fafc;
  --plan-elite-bg: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
  background: var(--primary-50);
  color: var(--primary-900);
  line-height: 1.6;
  min-height: 100vh;
}

/* ===== HEADER APLICAȚIE ===== */
.app-header {
  background: var(--primary-900);
  color: white;
  padding: 16px 32px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  box-shadow: 0 2px 8px rgba(15, 23, 42, 0.3);
}

.app-logo {
  display: flex;
  align-items: center;
  gap: 12px;
  font-size: 1.4rem;
  font-weight: 800;
}

.app-logo-icon {
  width: 40px;
  height: 40px;
  background: var(--accent-500);
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
}

.app-nav {
  display: flex;
  gap: 8px;
}

.nav-btn {
  padding: 8px 18px;
  border: none;
  border-radius: 8px;
  background: transparent;
  color: var(--primary-300);
  font-size: 0.9rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.2s;
}

.nav-btn:hover, .nav-btn.active {
  background: var(--primary-800);
  color: white;
}

.nav-btn.active {
  box-shadow: 0 0 0 2px var(--accent-500);
}

/* ===== HERO SECTION ===== */
.hero {
  background: var(--primary-900);
  color: white;
  padding: 60px 32px;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  top: -50%;
  right: -20%;
  width: 600px;
  height: 600px;
  background: var(--accent-500);
  opacity: 0.08;
  border-radius: 50%;
}

.hero::after {
  content: '';
  position: absolute;
  bottom: -30%;
  left: -10%;
  width: 400px;
  height: 400px;
  background: var(--accent-400);
  opacity: 0.05;
  border-radius: 50%;
}

.hero h1 {
  font-size: 2.8rem;
  font-weight: 800;
  margin-bottom: 12px;
  position: relative;
  z-index: 1;
}

.hero h1 span {
  color: var(--accent-400);
}

.hero p {
  font-size: 1.2rem;
  color: var(--primary-300);
  max-width: 600px;
  margin: 0 auto;
  position: relative;
  z-index: 1;
}

/* ===== PRICING CONTAINER ===== */
.pricing-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 48px 24px;
}

.section-header {
  text-align: center;
  margin-bottom: 48px;
}

.section-header h2 {
  font-size: 2rem;
  color: var(--primary-900);
  margin-bottom: 8px;
}

.section-header p {
  color: var(--primary-500);
  font-size: 1.05rem;
}

/* ===== PLANS GRID ===== */
.plans-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  margin-bottom: 48px;
}

.plan-card {
  border-radius: 20px;
  padding: 28px 20px;
  position: relative;
  transition: all 0.35s cubic-bezier(0.4, 0, 0.2, 1);
  border: 2px solid;
  display: flex;
  flex-direction: column;
  background: white;
}

.plan-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 40px rgba(15, 23, 42, 0.12);
}

/* Plan Gratuit – Roșu */
.plan-card.free {
  border-color: var(--plan-free);
  background: var(--plan-free-bg);
}

.plan-card.free .plan-badge {
  background: var(--plan-free);
}

.plan-card.free .price {
  color: var(--plan-free);
}

.plan-card.free .btn {
  background: var(--plan-free);
}

/* Plan Premium – Portocaliu/Amber */
.plan-card.premium {
  border-color: var(--plan-premium);
  background: var(--plan-premium-bg);
}

.plan-card.premium .plan-badge {
  background: var(--plan-premium);
}

.plan-card.premium .price {
  color: var(--accent-800);
}

.plan-card.premium .btn {
  background: var(--plan-premium);
}

/* Plan Pro – Verde */
.plan-card.pro {
  border-color: var(--plan-pro);
  background: var(--plan-pro-bg);
  transform: scale(1.04);
  box-shadow: 0 12px 32px rgba(5, 150, 105, 0.15);
  z-index: 2;
}

.plan-card.pro .plan-badge {
  background: var(--plan-pro);
}

.plan-card.pro .price {
  color: var(--plan-pro);
}

.plan-card.pro .btn {
  background: var(--plan-pro);
}

/* Plan Elite – Gri/Ardezie */
.plan-card.elite {
  border-color: var(--plan-elite);
  background: var(--plan-elite-bg);
  position: relative;
}

.plan-card.elite::before {
  content: '';
  position: absolute;
  inset: -3px;
  border-radius: 22px;
  background: linear-gradient(135deg, var(--primary-400), var(--accent-400), var(--primary-500));
  z-index: -1;
  opacity: 0.4;
}

.plan-card.elite .plan-badge {
  background: linear-gradient(135deg, var(--primary-700), var(--primary-500));
}

.plan-card.elite .price {
  color: var(--primary-800);
}

.plan-card.elite .btn {
  background: linear-gradient(135deg, var(--primary-700), var(--primary-500));
}

/* Badge-uri */
.plan-badge {
  position: absolute;
  top: -12px;
  right: 16px;
  padding: 6px 14px;
  border-radius: 20px;
  font-size: 0.7rem;
  font-weight: 800;
  text-transform: uppercase;
  letter-spacing: 0.8px;
  color: white;
  box-shadow: 0 2px 8px rgba(0,0,0,0.15);
}

.plan-card h3 {
  font-size: 1.4rem;
  margin-bottom: 4px;
  color: var(--primary-900);
}

.plan-subtitle {
  font-size: 0.85rem;
  color: var(--primary-500);
  margin-bottom: 16px;
}

.price {
  font-size: 2.2rem;
  font-weight: 800;
  margin-bottom: 4px;
}

.price span {
  font-size: 0.9rem;
  font-weight: 400;
  color: var(--primary-400);
}

.price-period {
  font-size: 0.85rem;
  color: var(--primary-400);
  margin-bottom: 20px;
}

.trial-badge {
  background: var(--primary-800);
  color: var(--accent-300);
  padding: 6px 12px;
  border-radius: 8px;
  font-size: 0.8rem;
  font-weight: 700;
  margin-bottom: 16px;
  display: inline-flex;
  align-items: center;
  gap: 6px;
  width: fit-content;
}

/* Features list */
.features {
  list-style: none;
  padding: 0;
  margin: 0 0 24px 0;
  flex-grow: 1;
}

.features li {
  padding: 10px 0;
  border-bottom: 1px solid rgba(0,0,0,0.04);
  font-size: 0.9rem;
  display: flex;
  align-items: center;
  gap: 10px;
  color: var(--primary-700);
}

.features li:last-child {
  border-bottom: none;
}

.features li .icon-yes {
  color: var(--success);
  font-weight: 700;
  min-width: 20px;
}

.features li .icon-no {
  color: var(--neutral-300);
  min-width: 20px;
}

.features li .limit {
  font-weight: 700;
  color: var(--primary-900);
}

.features li.limited {
  color: var(--accent-800);
}

.features li.no {
  color: var(--neutral-400);
  text-decoration: line-through;
}

.features li.highlight {
  background: var(--accent-50);
  margin: 0 -8px;
  padding: 10px 8px;
  border-radius: 8px;
  border-bottom: none;
}

/* Butoane */
.btn {
  width: 100%;
  padding: 14px;
  border: none;
  border-radius: 12px;
  font-size: 1rem;
  font-weight: 700;
  cursor: pointer;
  transition: all 0.2s;
  color: white;
  margin-top: auto;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(0,0,0,0.15);
}

.btn:active {
  transform: translateY(0);
}

/* ===== PARENTS SECTION ===== */
.parents-section {
  background: white;
  border: 2px solid var(--primary-200);
  border-radius: 20px;
  padding: 32px;
  margin-bottom: 48px;
  box-shadow: 0 4px 16px rgba(15, 23, 42, 0.06);
}

.parents-section h3 {
  color: var(--primary-900);
  font-size: 1.3rem;
  margin-bottom: 8px;
  display: flex;
  align-items: center;
  gap: 10px;
}

.parents-section .section-desc {
  color: var(--primary-500);
  font-size: 0.95rem;
  margin-bottom: 24px;
}

.parents-form {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}

.form-group {
  display: flex;
  flex-direction: column;
}

.form-group.full {
  grid-column: 1 / -1;
}

.form-group label {
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--primary-700);
  margin-bottom: 8px;
  display: flex;
  align-items: center;
  gap: 6px;
}

.form-group input {
  padding: 12px 16px;
  border: 2px solid var(--primary-200);
  border-radius: 10px;
  font-size: 1rem;
  transition: all 0.2s;
  background: var(--primary-50);
  color: var(--primary-900);
}

.form-group input:focus {
  outline: none;
  border-color: var(--accent-500);
  background: white;
  box-shadow: 0 0 0 3px var(--accent-100);
}

.form-group input::placeholder {
  color: var(--primary-400);
}

.checkbox-group {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 12px;
  margin-top: 8px;
}

.checkbox-group label {
  display: flex;
  align-items: center;
  gap: 10px;
  font-weight: 500;
  cursor: pointer;
  padding: 10px 14px;
  border-radius: 8px;
  transition: background 0.2s;
  color: var(--primary-700);
}

.checkbox-group label:hover {
  background: var(--primary-50);
}

.checkbox-group input[type="checkbox"] {
  width: 20px;
  height: 20px;
  accent-color: var(--accent-600);
  cursor: pointer;
}

/* ===== COMPARISON TABLE ===== */
.comparison-section {
  background: white;
  border-radius: 20px;
  padding: 32px;
  box-shadow: 0 4px 16px rgba(15, 23, 42, 0.06);
}

.comparison-section h3 {
  color: var(--primary-900);
  font-size: 1.3rem;
  margin-bottom: 24px;
  display: flex;
  align-items: center;
  gap: 10px;
}

.table-wrapper {
  overflow-x: auto;
  border-radius: 12px;
  border: 1px solid var(--primary-200);
}

.comparison-table {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.92rem;
}

.comparison-table thead th {
  padding: 16px 14px;
  text-align: left;
  font-weight: 700;
  background: var(--primary-50);
  color: var(--primary-700);
  border-bottom: 2px solid var(--primary-200);
  white-space: nowrap;
}

.comparison-table thead th:first-child {
  border-radius: 12px 0 0 0;
}

.comparison-table thead th:last-child {
  border-radius: 0 12px 0 0;
}

.comparison-table td {
  padding: 14px;
  border-bottom: 1px solid var(--primary-100);
  color: var(--primary-700);
}

.comparison-table tr:hover td {
  background: var(--primary-50);
}

.comparison-table tr:last-child td:first-child {
  border-radius: 0 0 0 12px;
}

.comparison-table tr:last-child td:last-child {
  border-radius: 0 0 12px 0;
}

.col-feature {
  font-weight: 600;
  color: var(--primary-900);
  min-width: 220px;
}

.col-free { 
  text-align: center; 
  color: var(--plan-free);
  font-weight: 600;
  background: var(--plan-free-light);
}

.col-premium { 
  text-align: center; 
  color: var(--accent-800);
  font-weight: 600;
  background: var(--plan-premium-light);
}

.col-pro { 
  text-align: center; 
  color: var(--plan-pro);
  font-weight: 700;
  background: var(--plan-pro-light);
}

.col-elite { 
  text-align: center; 
  color: var(--primary-800);
  font-weight: 700;
  background: var(--plan-elite-light);
}

.check-yes {
  color: var(--success);
  font-weight: 700;
  font-size: 1.1rem;
}

.check-no {
  color: var(--neutral-300);
  font-size: 1.1rem;
}

/* ===== FOOTER ===== */
.app-footer {
  background: var(--primary-900);
  color: var(--primary-300);
  padding: 40px 32px;
  text-align: center;
  margin-top: 48px;
}

.app-footer p {
  font-size: 0.9rem;
}

/* ===== RESPONSIVE ===== */
@media (max-width: 1100px) {
  .plans-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  .plan-card.pro {
    transform: scale(1.02);
  }
}

@media (max-width: 640px) {
  .plans-grid {
    grid-template-columns: 1fr;
  }
  .plan-card.pro {
    transform: none;
  }
  .hero h1 {
    font-size: 2rem;
  }
  .parents-form {
    grid-template-columns: 1fr;
  }
  .checkbox-group {
    grid-template-columns: 1fr;
  }
  .app-header {
    flex-direction: column;
    gap: 12px;
    padding: 16px;
  }
  .app-nav {
    flex-wrap: wrap;
    justify-content: center;
  }
}
</style>
<base target="_blank">
</head>
<body>

<!-- HEADER APLICAȚIE -->
<header class="app-header">
  <div class="app-logo">
    <div class="app-logo-icon">🎓</div>
    <span>Mentor AI</span>
  </div>
  <nav class="app-nav">
    <button class="nav-btn">Dashboard</button>
    <button class="nav-btn">Profesor AI</button>
    <button class="nav-btn">Teste</button>
    <button class="nav-btn">Flashcard-uri</button>
    <button class="nav-btn active">Abonament</button>
    <button class="nav-btn">Setări</button>
  </nav>
</header>

<!-- HERO -->
<section class="hero">
  <h1>Alege planul <span>perfect</span> pentru educație</h1>
  <p>De la învățare de bază la experiențe educaționale complete pentru întreaga familie</p>
</section>

<!-- PRICING -->
<div class="pricing-container">

  <div class="section-header">
    <h2>Planuri de Abonament</h2>
    <p>Flexibilitate maximă pentru fiecare etapă a învățării</p>
  </div>

  <div class="plans-grid">
    <!-- GRATUIT -->
    <div class="plan-card free">
      <div class="plan-badge">Gratuit</div>
      <h3>Free</h3>
      <p class="plan-subtitle">Începe călătoria</p>
      <div class="price">0 <span>RON</span></div>
      <p class="price-period">pe lună, pentru totdeauna</p>

      <ul class="features">
        <li class="limited">
          <span class="icon-yes">●</span>
          <span>Profesor AI: <span class="limit">5 mesaje</span> / zi</span>
        </li>
        <li class="limited">
          <span class="icon-yes">●</span>
          <span>Teste AI: <span class="limit">3 teste</span> / zi</span>
        </li>
        <li class="limited">
          <span class="icon-yes">●</span>
          <span>Flashcard-uri: <span class="limit">5</span> / zi</span>
        </li>
        <li class="no">
          <span class="icon-no">○</span>
          <span>Hărți mentale</span>
        </li>
        <li class="no">
          <span class="icon-no">○</span>
          <span>Predicții note</span>
        </li>
        <li class="no">
          <span class="icon-no">○</span>
          <span>Rapoarte progres</span>
        </li>
        <li class="no">
          <span class="icon-no">○</span>
          <span>Backup Cloud</span>
        </li>
        <li class="no">
          <span class="icon-no">○</span>
          <span>Email rapoarte părinți</span>
        </li>
        <li class="no">
          <span class="icon-no">○</span>
          <span>SMS notificări părinți</span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>1 copil</span>
        </li>
      </ul>
      <button class="btn">Începe Gratuit</button>
    </div>

    <!-- PREMIUM -->
    <div class="plan-card premium">
      <div class="plan-badge">Premium</div>
      <h3>Premium</h3>
      <p class="plan-subtitle">Pasul următor</p>
      <div class="price">50 <span>RON</span></div>
      <p class="price-period">pe lună</p>

      <ul class="features">
        <li>
          <span class="icon-yes">●</span>
          <span>Profesor AI: <span class="limit">7 mesaje</span> / zi</span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>Teste AI: <span class="limit">5 teste</span> / zi</span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>Flashcard-uri: <span class="limit">10</span> / zi</span>
        </li>
        <li class="no">
          <span class="icon-no">○</span>
          <span>Hărți mentale</span>
        </li>
        <li class="no">
          <span class="icon-no">○</span>
          <span>Predicții note</span>
        </li>
        <li class="no">
          <span class="icon-no">○</span>
          <span>Rapoarte progres</span>
        </li>
        <li class="no">
          <span class="icon-no">○</span>
          <span>Backup Cloud</span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>Email rapoarte părinți (1)</span>
        </li>
        <li class="no">
          <span class="icon-no">○</span>
          <span>SMS notificări părinți</span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>1 copil</span>
        </li>
      </ul>
      <button class="btn">Alege Premium</button>
    </div>

    <!-- PRO -->
    <div class="plan-card pro">
      <div class="plan-badge">PRO</div>
      <h3>Pro</h3>
      <p class="plan-subtitle">Cel mai popular</p>
      <div class="price">100 <span>RON</span></div>
      <p class="price-period">pe lună</p>

      <ul class="features">
        <li>
          <span class="icon-yes">●</span>
          <span>Profesor AI: <span class="limit">10 mesaje</span> / zi</span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>Teste AI: <span class="limit">10 teste</span> / zi</span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>Flashcard-uri: <span class="limit">15</span> / zi</span>
        </li>
        <li class="highlight">
          <span class="icon-yes">●</span>
          <span><strong>Hărți mentale</strong></span>
        </li>
        <li class="highlight">
          <span class="icon-yes">●</span>
          <span><strong>Predicții note</strong></span>
        </li>
        <li class="highlight">
          <span class="icon-yes">●</span>
          <span><strong>Rapoarte progres</strong></span>
        </li>
        <li class="highlight">
          <span class="icon-yes">●</span>
          <span><strong>Backup Cloud</strong></span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>Email rapoarte părinți (2)</span>
        </li>
        <li class="no">
          <span class="icon-no">○</span>
          <span>SMS notificări părinți</span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>1 copil</span>
        </li>
      </ul>
      <button class="btn">Alege Pro</button>
    </div>

    <!-- ELITE FAMILY PACK -->
    <div class="plan-card elite">
      <div class="plan-badge">ELITE</div>
      <h3>Elite Family Pack</h3>
      <p class="plan-subtitle">Pentru familie</p>
      <div class="price">150 <span>RON</span></div>
      <p class="price-period">pe lună</p>
      <div class="trial-badge">🎁 Trial 7 zile GRATUIT</div>

      <ul class="features">
        <li>
          <span class="icon-yes">●</span>
          <span>Profesor AI: <span class="limit">Nelimitat</span></span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>Teste AI: <span class="limit">Nelimitate</span></span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>Flashcard-uri: <span class="limit">Nelimitate</span></span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>Hărți mentale</span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>Predicții note avansate</span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>Rapoarte progres complete</span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>Backup Cloud</span>
        </li>
        <li>
          <span class="icon-yes">●</span>
          <span>Email rapoarte (2 părinți)</span>
        </li>
        <li class="highlight">
          <span class="icon-yes">●</span>
          <span><strong>SMS notificări (2 numere)</strong></span>
        </li>
        <li class="highlight">
          <span class="icon-yes">●</span>
          <span><strong>Până la 4 copii</strong></span>
        </li>
      </ul>
      <button class="btn">Alege Elite Family</button>
    </div>
  </div>

  <!-- PARENTS CONFIGURATION -->
  <div class="parents-section">
    <h3>👨‍👩‍👧 Configurare Notificări Părinți</h3>
    <p class="section-desc">Disponibil exclusiv în planul Elite Family Pack. Ambii părinți primesc rapoarte detaliate despre progresul copiilor.</p>

    <div class="parents-form">
      <div class="form-group">
        <label>📧 Email Părinte 1</label>
        <input type="email" placeholder="parinte1@email.com" />
      </div>
      <div class="form-group">
        <label>📧 Email Părinte 2</label>
        <input type="email" placeholder="parinte2@email.com" />
      </div>
      <div class="form-group">
        <label>📱 Telefon Părinte 1</label>
        <input type="tel" placeholder="+40 7xx xxx xxx" />
      </div>
      <div class="form-group">
        <label>📱 Telefon Părinte 2</label>
        <input type="tel" placeholder="+40 7xx xxx xxx" />
      </div>
      <div class="form-group full">
        <label>🔔 Tipuri de rapoarte și notificări trimise:</label>
        <div class="checkbox-group">
          <label><input type="checkbox" checked /> 📊 Raport săptămânal pe email</label>
          <label><input type="checkbox" checked /> ⚠️ Alertă notă scăzută (SMS)</label>
          <label><input type="checkbox" /> 📈 Predicție examen (SMS)</label>
          <label><input type="checkbox" checked /> 📋 Progres lunar detaliat (email)</label>
          <label><input type="checkbox" /> 🎯 Obiective atinse (SMS)</label>
          <label><input type="checkbox" /> 📚 Recomandări materiale (email)</label>
        </div>
      </div>
    </div>
  </div>

  <!-- COMPARISON TABLE -->
  <div class="comparison-section">
    <h3>📋 Tabel Comparativ Complet</h3>
    <div class="table-wrapper">
      <table class="comparison-table">
        <thead>
          <tr>
            <th>Funcționalitate</th>
            <th class="col-free">Free<br><small>0 RON</small></th>
            <th class="col-premium">Premium<br><small>50 RON</small></th>
            <th class="col-pro">Pro<br><small>100 RON</small></th>
            <th class="col-elite">Elite Family<br><small>150 RON</small></th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="col-feature">🤖 Profesor AI – Mesaje/zi</td>
            <td class="col-free">5</td>
            <td class="col-premium">7</td>
            <td class="col-pro">10</td>
            <td class="col-elite">Nelimitat</td>
          </tr>
          <tr>
            <td class="col-feature">📝 Teste AI – Teste/zi</td>
            <td class="col-free">3</td>
            <td class="col-premium">5</td>
            <td class="col-pro">10</td>
            <td class="col-elite">Nelimitat</td>
          </tr>
          <tr>
            <td class="col-feature">🗂️ Flashcard-uri – Bucăți/zi</td>
            <td class="col-free">5</td>
            <td class="col-premium">10</td>
            <td class="col-pro">15</td>
            <td class="col-elite">Nelimitat</td>
          </tr>
          <tr>
            <td class="col-feature">🧠 Hărți mentale</td>
            <td class="col-free"><span class="check-no">✕</span></td>
            <td class="col-premium"><span class="check-no">✕</span></td>
            <td class="col-pro"><span class="check-yes">✓</span></td>
            <td class="col-elite"><span class="check-yes">✓</span></td>
          </tr>
          <tr>
            <td class="col-feature">📊 Predicții note</td>
            <td class="col-free"><span class="check-no">✕</span></td>
            <td class="col-premium"><span class="check-no">✕</span></td>
            <td class="col-pro"><span class="check-yes">✓</span></td>
            <td class="col-elite"><span class="check-yes">✓</span> Avansat</td>
          </tr>
          <tr>
            <td class="col-feature">📈 Rapoarte progres</td>
            <td class="col-free"><span class="check-no">✕</span></td>
            <td class="col-premium"><span class="check-no">✕</span></td>
            <td class="col-pro"><span class="check-yes">✓</span></td>
            <td class="col-elite"><span class="check-yes">✓</span> Complet</td>
          </tr>
          <tr>
            <td class="col-feature">☁️ Backup Cloud</td>
            <td class="col-free"><span class="check-no">✕</span></td>
            <td class="col-premium"><span class="check-no">✕</span></td>
            <td class="col-pro"><span class="check-yes">✓</span></td>
            <td class="col-elite"><span class="check-yes">✓</span></td>
          </tr>
          <tr>
            <td class="col-feature">📧 Email rapoarte părinți</td>
            <td class="col-free"><span class="check-no">✕</span></td>
            <td class="col-premium"><span class="check-yes">✓</span> 1</td>
            <td class="col-pro"><span class="check-yes">✓</span> 2</td>
            <td class="col-elite"><span class="check-yes">✓</span> 2</td>
          </tr>
          <tr>
            <td class="col-feature">📱 SMS notificări părinți</td>
            <td class="col-free"><span class="check-no">✕</span></td>
            <td class="col-premium"><span class="check-no">✕</span></td>
            <td class="col-pro"><span class="check-no">✕</span></td>
            <td class="col-elite"><span class="check-yes">✓</span> 2 numere</td>
          </tr>
          <tr>
            <td class="col-feature">👨‍👩‍👧‍👦 Număr copii</td>
            <td class="col-free">1</td>
            <td class="col-premium">1</td>
            <td class="col-pro">1</td>
            <td class="col-elite">Până la 4</td>
          </tr>
          <tr>
            <td class="col-feature">🎁 Trial gratuit</td>
            <td class="col-free">–</td>
            <td class="col-premium">–</td>
            <td class="col-pro">–</td>
            <td class="col-elite"><strong>7 zile</strong></td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>

</div>

<!-- FOOTER -->
<footer class="app-footer">
  <p>© 2026 Mentor AI. Toate drepturile rezervate. | <span style="color: var(--accent-400);">🎓</span> Educație inteligentă pentru generația viitoare.</p>
</footer>

</body>
</html>
