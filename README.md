<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Proposta Comercial — Solution Licitações</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=DM+Sans:wght@300;400;500;600&display=swap');

  :root {
    --navy: #0D1B3E;
    --gold: #C9A84C;
    --gold-light: #E8C97B;
    --teal: #1B7A78;
    --teal-light: #2AA8A5;
    --cream: #F9F6F0;
    --white: #FFFFFF;
    --text-dark: #1A1A2E;
    --text-muted: #5A6275;
    --plan1: #1B4F72;
    --plan2: #1B7A78;
    --plan3: #7D3C98;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--text-dark);
    overflow-x: clip;
  }

  /* ── HERO ── */
  .hero {
    background: var(--navy);
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;
    overflow: hidden;
    padding: 60px 40px;
    text-align: center;
  }

  .hero::before {
    content: '';
    position: absolute;
    width: 700px; height: 700px;
    background: radial-gradient(circle, rgba(201,168,76,0.15) 0%, transparent 70%);
    top: -200px; right: -200px;
    border-radius: 50%;
  }
  .hero::after {
    content: '';
    position: absolute;
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(27,122,120,0.2) 0%, transparent 70%);
    bottom: -150px; left: -100px;
    border-radius: 50%;
  }

  .hero-badge {
    display: inline-block;
    background: rgba(201,168,76,0.15);
    border: 1px solid rgba(201,168,76,0.4);
    color: var(--gold-light);
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 3px;
    text-transform: uppercase;
    padding: 8px 24px;
    border-radius: 100px;
    margin-bottom: 32px;
    animation: fadeDown 0.8s ease both;
  }

  .hero-logo {
    font-family: 'Playfair Display', serif;
    font-size: clamp(36px, 6vw, 64px);
    font-weight: 900;
    color: var(--white);
    line-height: 1.1;
    margin-bottom: 12px;
    animation: fadeDown 0.9s ease 0.1s both;
  }

  .hero-logo span { color: var(--gold); }

  .hero-sub {
    font-size: clamp(13px, 2vw, 16px);
    color: rgba(255,255,255,0.55);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 48px;
    animation: fadeDown 1s ease 0.2s both;
  }

  .hero-headline {
    font-family: 'Playfair Display', serif;
    font-size: clamp(28px, 5vw, 56px);
    font-weight: 700;
    color: var(--white);
    max-width: 780px;
    line-height: 1.2;
    margin-bottom: 24px;
    animation: fadeDown 1s ease 0.3s both;
  }

  .hero-desc {
    font-size: clamp(15px, 2vw, 18px);
    color: rgba(255,255,255,0.7);
    max-width: 600px;
    line-height: 1.7;
    margin-bottom: 52px;
    animation: fadeDown 1s ease 0.4s both;
  }

  .hero-cta {
    display: inline-block;
    background: linear-gradient(135deg, var(--gold), var(--gold-light));
    color: var(--navy);
    font-weight: 700;
    font-size: 15px;
    padding: 16px 44px;
    border-radius: 100px;
    text-decoration: none;
    letter-spacing: 0.5px;
    animation: fadeDown 1s ease 0.5s both;
    transition: transform 0.2s, box-shadow 0.2s;
    box-shadow: 0 8px 32px rgba(201,168,76,0.35);
  }
  .hero-cta:hover { transform: translateY(-2px); box-shadow: 0 14px 40px rgba(201,168,76,0.45); }

  .scroll-hint {
    position: absolute;
    bottom: 36px;
    left: 50%;
    transform: translateX(-50%);
    color: rgba(255,255,255,0.3);
    font-size: 12px;
    letter-spacing: 2px;
    text-transform: uppercase;
    animation: bounce 2s infinite;
  }
  .scroll-hint::after { content: ' ↓'; }

  /* ── SECTION WRAPPER ── */
  .section {
    padding: 100px 40px;
    max-width: 1200px;
    margin: 0 auto;
  }

  .section-tag {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 16px;
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(28px, 4vw, 46px);
    font-weight: 700;
    color: var(--navy);
    line-height: 1.2;
    margin-bottom: 20px;
  }

  .section-desc {
    font-size: 17px;
    color: var(--text-muted);
    line-height: 1.8;
    max-width: 700px;
    margin-bottom: 64px;
  }

  /* ── DIFERENCIAIS ── */
  .diff-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 28px;
  }

  .diff-card {
    background: var(--white);
    border-radius: 16px;
    padding: 36px 32px;
    border: 1px solid rgba(0,0,0,0.06);
    box-shadow: 0 4px 24px rgba(0,0,0,0.05);
    transition: transform 0.25s, box-shadow 0.25s;
  }
  .diff-card:hover { transform: translateY(-4px); box-shadow: 0 12px 40px rgba(0,0,0,0.1); }

  .diff-icon {
    width: 52px; height: 52px;
    border-radius: 14px;
    display: flex; align-items: center; justify-content: center;
    font-size: 22px;
    margin-bottom: 20px;
  }

  .diff-card h3 {
    font-weight: 700;
    font-size: 17px;
    margin-bottom: 10px;
    color: var(--navy);
  }
  .diff-card p { font-size: 14px; color: var(--text-muted); line-height: 1.7; }

  /* ── PLANOS ── */
  .plans-bg {
    background: var(--navy);
    padding: 100px 0;
  }

  .plans-inner {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 40px;
  }

  .plans-header { text-align: center; margin-bottom: 64px; }
  .plans-header .section-tag { color: var(--gold-light); }
  .plans-header .section-title { color: var(--white); }
  .plans-header .section-desc { color: rgba(255,255,255,0.6); margin: 0 auto 0; }

  .plans-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 28px;
    align-items: start;
  }

  .plan-card {
    border-radius: 20px;
    padding: 40px 32px;
    position: relative;
    overflow: hidden;
    transition: transform 0.25s;
  }
  .plan-card:hover { transform: translateY(-6px); }

  .plan-card.p1 { background: linear-gradient(145deg, #1B4F72, #154360); border: 1px solid rgba(255,255,255,0.1); }
  .plan-card.p2 { background: linear-gradient(145deg, #1B7A78, #0E6655); border: 2px solid var(--gold); transform: scale(1.02); }
  .plan-card.p3 { background: linear-gradient(145deg, #6C3483, #5B2C6F); border: 1px solid rgba(255,255,255,0.1); }
  .plan-card.p2:hover { transform: scale(1.02) translateY(-6px); }

  .plan-badge {
    position: absolute;
    top: 20px; right: 20px;
    background: var(--gold);
    color: var(--navy);
    font-size: 10px;
    font-weight: 800;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    padding: 5px 14px;
    border-radius: 100px;
  }

  .plan-num {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: rgba(255,255,255,0.45);
    margin-bottom: 10px;
  }

  .plan-name {
    font-family: 'Playfair Display', serif;
    font-size: 26px;
    font-weight: 700;
    color: var(--white);
    margin-bottom: 8px;
    line-height: 1.2;
  }

  .plan-tagline {
    font-size: 13px;
    color: rgba(255,255,255,0.55);
    margin-bottom: 32px;
    line-height: 1.5;
  }

  .plan-divider {
    height: 1px;
    background: rgba(255,255,255,0.12);
    margin-bottom: 28px;
  }

  .price-block { margin-bottom: 28px; }

  .price-label {
    font-size: 11px;
    text-transform: uppercase;
    letter-spacing: 2px;
    color: rgba(255,255,255,0.45);
    margin-bottom: 6px;
  }

  .price-value {
    font-family: 'Playfair Display', serif;
    font-size: 32px;
    font-weight: 700;
    color: var(--gold-light);
    line-height: 1;
  }

  .price-note {
    font-size: 12px;
    color: rgba(255,255,255,0.45);
    margin-top: 4px;
  }

  .plan-features { list-style: none; margin-bottom: 36px; }
  .plan-features li {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    font-size: 14px;
    color: rgba(255,255,255,0.8);
    margin-bottom: 12px;
    line-height: 1.5;
  }
  .plan-features li .ck {
    width: 18px; height: 18px;
    border-radius: 50%;
    background: rgba(201,168,76,0.25);
    display: flex; align-items: center; justify-content: center;
    font-size: 10px;
    flex-shrink: 0;
    margin-top: 1px;
  }

  .plan-profile {
    background: rgba(0,0,0,0.2);
    border-radius: 12px;
    padding: 16px 20px;
    margin-bottom: 28px;
  }
  .plan-profile-label {
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--gold-light);
    margin-bottom: 8px;
  }
  .plan-profile p { font-size: 13px; color: rgba(255,255,255,0.7); line-height: 1.6; }

  .plan-btn {
    display: block;
    text-align: center;
    padding: 14px;
    border-radius: 12px;
    font-weight: 700;
    font-size: 14px;
    text-decoration: none;
    letter-spacing: 0.3px;
    transition: opacity 0.2s, transform 0.2s;
  }
  .plan-btn:hover { opacity: 0.9; transform: scale(0.98); }
  .plan-btn.gold { background: linear-gradient(135deg, var(--gold), var(--gold-light)); color: var(--navy); }
  .plan-btn.outline { background: rgba(255,255,255,0.1); color: var(--white); border: 1px solid rgba(255,255,255,0.25); }

  /* ── AVISO PAGAMENTO ── */
  .payment-notice {
    background: rgba(201,168,76,0.1);
    border: 1px solid rgba(201,168,76,0.3);
    border-radius: 12px;
    padding: 20px 28px;
    margin-top: 48px;
    display: flex;
    align-items: center;
    gap: 16px;
    color: rgba(255,255,255,0.8);
    font-size: 14px;
    line-height: 1.6;
  }
  .payment-notice .icon { font-size: 28px; flex-shrink: 0; }

  /* ── PROCESSO ── */
  .process-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 0;
    position: relative;
  }

  .process-step {
    padding: 32px 24px;
    text-align: center;
    position: relative;
  }

  .step-num {
    width: 56px; height: 56px;
    border-radius: 50%;
    background: var(--navy);
    color: var(--gold);
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    font-weight: 700;
    display: flex; align-items: center; justify-content: center;
    margin: 0 auto 20px;
  }

  .process-step h3 { font-size: 16px; font-weight: 700; color: var(--navy); margin-bottom: 8px; }
  .process-step p { font-size: 13px; color: var(--text-muted); line-height: 1.6; }

  /* ── CONTACT ── */
  .contact-bg {
    background: linear-gradient(135deg, var(--navy) 0%, #0a1628 100%);
    padding: 100px 40px;
    text-align: center;
  }

  .contact-inner { max-width: 700px; margin: 0 auto; }

  .contact-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(28px, 4vw, 46px);
    font-weight: 700;
    color: var(--white);
    margin-bottom: 16px;
  }

  .contact-sub { font-size: 17px; color: rgba(255,255,255,0.6); margin-bottom: 48px; line-height: 1.7; }

  .contact-info {
    display: flex;
    gap: 28px;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 40px;
  }

  .contact-item {
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 14px;
    padding: 20px 28px;
    color: var(--white);
    min-width: 200px;
  }
  .contact-item .ci-label { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: var(--gold-light); margin-bottom: 8px; }
  .contact-item .ci-val { font-size: 16px; font-weight: 600; }

  .whatsapp-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: #25D366;
    color: var(--white);
    font-weight: 700;
    font-size: 15px;
    padding: 16px 40px;
    border-radius: 100px;
    text-decoration: none;
    box-shadow: 0 8px 32px rgba(37,211,102,0.35);
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .whatsapp-btn:hover { transform: translateY(-2px); box-shadow: 0 14px 40px rgba(37,211,102,0.45); }

  footer {
    background: #060D1F;
    padding: 28px 40px;
    text-align: center;
    color: rgba(255,255,255,0.3);
    font-size: 12px;
    line-height: 1.8;
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-20px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  @keyframes bounce {
    0%, 100% { transform: translateX(-50%) translateY(0); }
    50%       { transform: translateX(-50%) translateY(8px); }
  }

  .reveal {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.visible { opacity: 1; transform: translateY(0); }

  /* ── TABELA COMPARATIVA ── */
  .comp-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 14px;
    border-radius: 16px;
    overflow: hidden;
    box-shadow: 0 4px 32px rgba(0,0,0,0.07);
  }

  .comp-table thead tr th {
    padding: 20px 18px;
    font-weight: 700;
    font-family: 'Playfair Display', serif;
    font-size: 15px;
    text-align: center;
    line-height: 1.4;
  }
  .comp-table thead th span {
    display: block;
    font-family: 'DM Sans', sans-serif;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    opacity: 0.75;
    margin-top: 4px;
  }

  .ct-label { background: var(--navy); color: var(--white); text-align: left !important; width: 24%; }
  .ct-p1    { background: #1B4F72; color: var(--white); }
  .ct-p2    { background: var(--teal); color: var(--white); }
  .ct-p3    { background: #6C3483; color: var(--white); }

  .comp-table tbody tr td {
    padding: 16px 18px;
    text-align: center;
    color: var(--text-dark);
    border-bottom: 1px solid rgba(0,0,0,0.05);
    vertical-align: middle;
    line-height: 1.5;
  }

  .ct-row-label {
    text-align: left !important;
    font-weight: 600;
    color: var(--navy) !important;
    background: var(--white);
    font-size: 13px;
  }

  .comp-table tbody tr { background: var(--white); }
  .comp-table tbody tr.ct-alt { background: #F4F7FB; }
  .comp-table tbody tr.ct-alt .ct-row-label { background: #F4F7FB; }

  .ct-highlight {
    background: rgba(27,122,120,0.08) !important;
    color: var(--teal) !important;
    font-weight: 600;
  }

  .comp-table tbody tr:hover { background: #EEF4FF; }
  .comp-table tbody tr:hover .ct-row-label { background: #EEF4FF; }
  .comp-table tbody tr:last-child td { border-bottom: none; }

  .table-scroll-wrap { position: relative; }
  .table-scroll-hint {
    display: none;
    text-align: center;
    font-size: 11px;
    color: var(--text-muted);
    letter-spacing: 1px;
    margin-bottom: 10px;
    opacity: 0.7;
  }
  @media (max-width: 700px) {
    .table-scroll-hint { display: block; }
  }

  /* ════════════════════════════════════════
     RESPONSIVIDADE MOBILE
  ════════════════════════════════════════ */

  /* Tablet (≤ 900px) */
  @media (max-width: 900px) {
    .section { padding: 72px 24px; }
    .plans-bg { padding: 72px 0; }
    .plans-inner { padding: 0 24px; }
    .contact-bg { padding: 72px 24px; }
    footer { padding: 24px 24px; }

    .diff-grid {
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
    }

    .plans-grid {
      grid-template-columns: 1fr;
      max-width: 520px;
      margin: 0 auto;
    }

    /* Remove escala do card destaque em coluna única */
    .plan-card.p2 { transform: none; }
    .plan-card.p2:hover { transform: translateY(-6px); }

    .process-grid {
      grid-template-columns: repeat(3, 1fr);
    }

    .contact-info { gap: 16px; }
    .contact-item { min-width: 160px; padding: 16px 20px; }
  }

  /* Mobile (≤ 600px) */
  @media (max-width: 600px) {
    .hero { padding: 80px 20px 60px; min-height: auto; }
    .hero::before, .hero::after { display: none; }

    .scroll-hint { display: none; }

    .section { padding: 56px 20px; }
    .plans-bg { padding: 56px 0; }
    .plans-inner { padding: 0 20px; }
    .contact-bg { padding: 56px 20px; }
    footer { padding: 24px 20px; }

    .section-desc { font-size: 15px; margin-bottom: 40px; }

    /* Diferenciais: 1 coluna */
    .diff-grid {
      grid-template-columns: 1fr;
      gap: 16px;
    }
    .diff-card { padding: 28px 24px; }

    /* Planos: 1 coluna, sem escala */
    .plans-grid {
      grid-template-columns: 1fr;
      max-width: 100%;
      gap: 20px;
    }
    .plan-card { padding: 32px 24px; }
    .plan-card.p2 { transform: none; border-width: 2px; }
    .plan-card.p2:hover { transform: translateY(-4px); }

    /* Processo: 1 coluna */
    .process-grid {
      grid-template-columns: 1fr;
      gap: 0;
    }
    .process-step {
      padding: 20px 16px;
      display: flex;
      align-items: flex-start;
      text-align: left;
      gap: 20px;
      border-left: 2px solid rgba(13,27,62,0.1);
      margin-left: 28px;
    }
    .process-step:last-child { border-left: 2px solid transparent; }
    .step-num {
      width: 48px; height: 48px;
      font-size: 18px;
      flex-shrink: 0;
      margin: 0 0 0 -28px;
    }
    .process-step-text { flex: 1; }
    .process-step h3 { margin-bottom: 4px; }

    /* Payment notice: empilha */
    .payment-notice {
      flex-direction: column;
      align-items: flex-start;
      padding: 20px;
      gap: 10px;
    }

    /* Contato */
    .contact-info {
      flex-direction: column;
      align-items: stretch;
      gap: 12px;
    }
    .contact-item {
      min-width: unset;
      width: 100%;
      padding: 16px 20px;
    }
    .whatsapp-btn {
      padding: 16px 28px;
      font-size: 14px;
      width: 100%;
      justify-content: center;
    }

    /* Tabela comparativa: scroll horizontal */
    .comp-table {
      font-size: 12px;
      min-width: 540px;
    }
    .comp-table thead tr th { padding: 14px 10px; font-size: 12px; }
    .comp-table tbody tr td { padding: 12px 10px; }
  }

  /* Mobile pequeno (≤ 400px) */
  @media (max-width: 400px) {
    .hero-badge { font-size: 9px; padding: 6px 16px; letter-spacing: 2px; }
    .hero-cta { padding: 14px 28px; font-size: 14px; }
    .plan-card { padding: 28px 18px; }
    .price-value { font-size: 26px; }
    .comp-table { min-width: 480px; font-size: 11px; }
  }
</style>
</head>
<body>

<!-- ════════════ HERO ════════════ -->
<section class="hero">
  <span class="hero-badge">Proposta Comercial Exclusiva</span>
  <div class="hero-logo">Solution <span>Licitações</span></div>
  <div class="hero-sub">CNPJ 62.826.468/0001-97</div>
  <h1 class="hero-headline">Sua empresa vencendo licitações com segurança e expertise</h1>
  <p class="hero-desc">Assessoria completa em processos licitatórios — da análise do edital à representação jurídica — com planos flexíveis que se adaptam ao seu perfil e volume de negócios.</p>
  <a href="#planos" class="hero-cta">Conheça os Planos →</a>
  <div class="scroll-hint">Rolar para ver</div>
</section>

<!-- ════════════ DIFERENCIAIS ════════════ -->
<div class="section reveal">
  <div class="section-tag">Por que escolher a Solution</div>
  <h2 class="section-title">Expertise que gera resultados reais</h2>
  <p class="section-desc">Combinamos conhecimento jurídico especializado com domínio técnico dos processos licitatórios para maximizar suas chances de êxito em cada disputa.</p>

  <div class="diff-grid">
    <div class="diff-card reveal">
      <div class="diff-icon" style="background:#EAF2FB;">⚖️</div>
      <h3>Peças Jurídicas Incluídas</h3>
      <p>Recursos, impugnações e manifestações elaboradas por especialistas, incluídas nos planos sem custo adicional.</p>
    </div>
    <div class="diff-card reveal">
      <div class="diff-icon" style="background:#E9F7EF;">📋</div>
      <h3>Gestão Completa do Processo</h3>
      <p>Análise de edital, habilitação, proposta técnica e comercial, acompanhamento da sessão e pós-certame.</p>
    </div>
    <div class="diff-card reveal">
      <div class="diff-icon" style="background:#FEF9E7;">🏆</div>
      <h3>Modelo de Risco Compartilhado</h3>
      <p>Nossos planos alinham os nossos incentivos aos seus resultados — só ganhamos bem quando você ganha.</p>
    </div>
    <div class="diff-card reveal">
      <div class="diff-icon" style="background:#F9EBF8;">🔍</div>
      <h3>Monitoramento de Oportunidades</h3>
      <p>Identificamos e filtramos editais compatíveis com o perfil da sua empresa em todo o Brasil.</p>
    </div>
    <div class="diff-card reveal">
      <div class="diff-icon" style="background:#FDEBD0;">📊</div>
      <h3>Relatórios e Transparência</h3>
      <p>Acompanhe cada processo em tempo real com relatórios detalhados e comunicação direta com nossa equipe.</p>
    </div>
    <div class="diff-card reveal">
      <div class="diff-icon" style="background:#E8F8F5;">🤝</div>
      <h3>Pagamento só após O.S.</h3>
      <p>Os pagamentos são iniciados apenas após o recebimento da Ordem de Serviços pelo órgão contratante.</p>
    </div>
  </div>
</div>

<!-- ════════════ PLANOS ════════════ -->
<section class="plans-bg" id="planos">
  <div class="plans-inner">
    <div class="plans-header reveal">
      <div class="section-tag">Planos de Assessoria</div>
      <h2 class="section-title">Escolha o modelo ideal para seu negócio</h2>
      <p class="section-desc">Três estruturas pensadas para diferentes perfis e estratégias de negócio — escolha o modelo que melhor se encaixa na sua realidade.</p>
    </div>

    <div class="plans-grid">

      <!-- PLANO 01 -->
      <div class="plan-card p1 reveal">
        <div class="plan-num">Plano 01</div>
        <div class="plan-name">Risco<br>Compartilhado</div>
        <div class="plan-tagline">Invista com consciência — pagando pouco por cada tentativa e muito pouco pelo sucesso.</div>
        <div class="plan-divider"></div>

        <div class="price-block">
          <div class="price-label">Taxa por licitação não vencida</div>
          <div class="price-value">R$ 500<span style="font-size:18px">,00</span></div>
          <div class="price-note">Inclui peças jurídicas do processo</div>
        </div>

        <div class="price-block">
          <div class="price-label">Em caso de êxito</div>
          <div class="price-value">1,5%</div>
          <div class="price-note">do valor do contrato</div>
        </div>

        <ul class="plan-features">
          <li><span class="ck">✓</span> Representação completa no certame</li>
          <li><span class="ck">✓</span> Peças jurídicas inclusas (recursos, impugnações)</li>
          <li><span class="ck">✓</span> Pagamento iniciado após recebimento da O.S.</li>
        </ul>

        <div class="plan-profile">
          <div class="plan-profile-label">🎯 Perfil Ideal</div>
          <p>Para empresas que valorizam previsibilidade financeira: com uma taxa fixa por processo, é possível planejar o investimento em licitações sem surpresas no fluxo de caixa — independentemente do resultado de cada disputa. Ideal para quem quer manter o controle sobre os custos enquanto expande sua presença no mercado público.</p>
        </div>

        <a href="https://wa.me/5533984241654" class="plan-btn outline">Quero este plano →</a>
      </div>

      <!-- PLANO 02 -->
      <div class="plan-card p2 reveal">
        <div class="plan-badge">⭐ Mais escolhido</div>
        <div class="plan-num">Plano 02</div>
        <div class="plan-name">Risco<br>Zero</div>
        <div class="plan-tagline">Participe sem desembolso antecipado — você só paga quando vence.</div>
        <div class="plan-divider"></div>

        <div class="price-block">
          <div class="price-label">Taxa por licitação não vencida</div>
          <div class="price-value" style="color:#6EE7E7;">R$ 0,00</div>
          <div class="price-note">Sem cobrança em caso de insucesso</div>
        </div>

        <div class="price-block">
          <div class="price-label">Em caso de êxito</div>
          <div class="price-value">2%</div>
          <div class="price-note">do valor do contrato</div>
        </div>

        <ul class="plan-features">
          <li><span class="ck">✓</span> Zero investimento em processos não vencidos</li>
          <li><span class="ck">✓</span> Representação completa no certame</li>
          <li><span class="ck">✓</span> Peças jurídicas inclusas (recursos, impugnações)</li>
          <li><span class="ck">✓</span> Pagamento iniciado após recebimento da O.S.</li>
        </ul>

        <div class="plan-profile">
          <div class="plan-profile-label">🎯 Perfil Ideal</div>
          <p>Para empresas que priorizam fluxo de caixa positivo e crescimento sustentável. Sem desembolso por processos não vencidos, os recursos da empresa ficam intactos para o que realmente importa: operar, investir e crescer. O custo só aparece quando o resultado já está garantido.</p>
        </div>

        <a href="https://wa.me/5533984241654" class="plan-btn gold">Quero este plano →</a>
      </div>

      <!-- PLANO 03 -->
      <div class="plan-card p3 reveal">
        <div class="plan-num">Plano 03</div>
        <div class="plan-name">Parceria<br>Mensal</div>
        <div class="plan-tagline">Tenha um setor de licitação completo e externo pelo preço de um funcionário.</div>
        <div class="plan-divider"></div>

        <div class="price-block">
          <div class="price-label">Mensalidade fixa</div>
          <div class="price-value">R$ 4.000<span style="font-size:18px">,00</span></div>
          <div class="price-note">Gestão integral de todos os processos</div>
        </div>

        <div class="price-block">
          <div class="price-label">Bônus por licitação vencida</div>
          <div class="price-value">+ R$ 1.000</div>
          <div class="price-note">por contrato ganho</div>
        </div>

        <ul class="plan-features">
          <li><span class="ck">✓</span> Setor licitatório externo dedicado</li>
          <li><span class="ck">✓</span> Gerenciamento de todos os processos</li>
          <li><span class="ck">✓</span> Até 2 peças jurídicas por mês incluídas</li>
          <li><span class="ck">✓</span> Pagamento iniciado após recebimento da O.S.</li>
          <li><span class="ck">✓</span> Monitoramento contínuo de editais</li>
        </ul>

        <div class="plan-profile">
          <div class="plan-profile-label">🎯 Perfil Ideal</div>
          <p>Empresas com operação consolidada e volume significativo de licitações, que desejam terceirizar completamente o setor sem contratar uma equipe interna. Perfeito para quem quer previsibilidade de custo e foco total na execução dos contratos.</p>
        </div>

        <a href="https://wa.me/5533984241654" class="plan-btn outline">Quero este plano →</a>
      </div>

    </div>

    <div class="payment-notice reveal">
      <span class="icon">🔒</span>
      <div><strong style="color:var(--gold-light)">Condições de pagamento:</strong> As taxas fixas por processo são acertadas mensalmente. A porcentagem sobre o valor do contrato é paga somente após a emissão da Ordem de Serviços pelo órgão contratante — quando o resultado já está garantido.</div>
    </div>
  </div>
</section>

<!-- ════════════ TABELA COMPARATIVA ════════════ -->
<div class="section reveal">
  <div class="section-tag">Comparativo de Planos</div>
  <h2 class="section-title">Tudo lado a lado para facilitar sua decisão</h2>
  <p class="section-desc">Veja as principais características de cada plano em uma visão consolidada.</p>

  <div class="table-scroll-wrap">
    <div class="table-scroll-hint">← deslize para ver →</div>
    <div style="overflow-x:auto; -webkit-overflow-scrolling:touch; border-radius:16px;">
    <table class="comp-table">
      <thead>
        <tr>
          <th class="ct-label">Característica</th>
          <th class="ct-p1">Plano 01<br><span>Risco Compartilhado</span></th>
          <th class="ct-p2">Plano 02<br><span>Risco Zero ⭐</span></th>
          <th class="ct-p3">Plano 03<br><span>Parceria Mensal</span></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td class="ct-row-label">Custo por processo não vencido</td>
          <td>R$ 500,00</td>
          <td class="ct-highlight">R$ 0,00 ✓</td>
          <td>Incluso na mensalidade</td>
        </tr>
        <tr class="ct-alt">
          <td class="ct-row-label">Taxa de êxito</td>
          <td>1,5% do contrato</td>
          <td>2% do contrato</td>
          <td>+ R$ 1.000 por vitória</td>
        </tr>
        <tr class="ct-alt">
          <td class="ct-row-label">Mensalidade fixa</td>
          <td style="color:var(--text-muted)">Não</td>
          <td style="color:var(--text-muted)">Não</td>
          <td><strong>R$ 4.000,00/mês</strong></td>
        </tr>
        <tr>
          <td class="ct-row-label">Peças jurídicas inclusas</td>
          <td style="color:var(--teal)">✓ Sim</td>
          <td style="color:var(--teal)" class="ct-highlight">✓ Sim</td>
          <td style="color:var(--teal)">✓ Até 2/mês</td>
        </tr>
        <tr class="ct-alt">
          <td class="ct-row-label">Acerto das taxas fixas</td>
          <td>Mensal</td>
          <td>—</td>
          <td>Mensal</td>
        </tr>
        <tr>
          <td class="ct-row-label">Pagamento da porcentagem</td>
          <td>Após emissão da O.S.</td>
          <td class="ct-highlight">Após emissão da O.S.</td>
          <td>Após emissão da O.S.</td>
        </tr>
        <tr class="ct-alt">
          <td class="ct-row-label">Ideal para</td>
          <td>Custo previsível por processo</td>
          <td class="ct-highlight">Fluxo de caixa positivo</td>
          <td>Operação de alto volume</td>
        </tr>
      </tbody>
    </table>
    </div>
  </div>
</div>

<!-- ════════════ PROCESSO ════════════ -->
<div class="section reveal">
  <div class="section-tag">Como funciona</div>
  <h2 class="section-title">Do primeiro contato ao contrato assinado</h2>
  <p class="section-desc">Um processo simples, transparente e orientado a resultados.</p>

  <div class="process-grid">
    <div class="process-step reveal">
      <div class="step-num">1</div>
      <div class="process-step-text">
      <h3>Diagnóstico</h3>
      <p>Avaliamos o perfil da sua empresa, documentação e aptidões para mapear os melhores editais.</p>
      </div>
    </div>
    <div class="process-step reveal">
      <div class="step-num">2</div>
      <div class="process-step-text">
      <h3>Seleção de Licitações</h3>
      <p>Monitoramos os portais e selecionamos licitações alinhadas ao seu negócio e capacidade de entrega.</p>
      </div>
    </div>
    <div class="process-step reveal">
      <div class="step-num">3</div>
      <div class="process-step-text">
      <h3>Habilitação & Proposta</h3>
      <p>Preparamos toda a documentação de habilitação e elaboramos a proposta técnica e comercial mais competitiva.</p>
      </div>
    </div>
    <div class="process-step reveal">
      <div class="step-num">4</div>
      <div class="process-step-text">
      <h3>Representação</h3>
      <p>Acompanhamos o certame, respondemos às diligências, elaboramos recursos e peças jurídicas quando necessário.</p>
      </div>
    </div>
    <div class="process-step reveal">
      <div class="step-num">5</div>
      <div class="process-step-text">
      <h3>Êxito & Contrato</h3>
      <p>Com a vitória, auxiliamos na assinatura e emissão da Ordem de Serviços para início da execução.</p>
      </div>
    </div>
  </div>
</div>

<!-- ════════════ CONTATO ════════════ -->
<section class="contact-bg">
  <div class="contact-inner reveal">
    <h2 class="contact-title">Pronto para vencer sua próxima licitação?</h2>
    <p class="contact-sub">Fale com nossa equipe agora e descubra qual plano se adapta melhor ao perfil da sua empresa. A consulta inicial é gratuita.</p>

    <div class="contact-info">
      <div class="contact-item">
        <div class="ci-label">Razão Social</div>
        <div class="ci-val">Solution Licitações LTDA</div>
      </div>
      <div class="contact-item">
        <div class="ci-label">CNPJ</div>
        <div class="ci-val">62.826.468/0001-97</div>
      </div>
      <div class="contact-item">
        <div class="ci-label">Telefone / WhatsApp</div>
        <div class="ci-val">(33) 98424-1654</div>
      </div>
    </div>

    <a href="https://wa.me/5533984241654?text=Olá!%20Tenho%20interesse%20nos%20planos%20de%20assessoria%20em%20licitações.%20Gostaria%20de%20saber%20mais." class="whatsapp-btn">
      💬 Falar pelo WhatsApp
    </a>
  </div>
</section>

<footer>
  <strong style="color:rgba(255,255,255,0.6)">Solution Licitações LTDA</strong> · CNPJ 62.826.468/0001-97<br>
  Assessoria e Representação em Processos Licitatórios · (33) 98424-1654
</footer>

<script>
  // Reveal on scroll
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((e, i) => {
      if (e.isIntersecting) {
        setTimeout(() => e.target.classList.add('visible'), i * 80);
        observer.unobserve(e.target);
      }
    });
  }, { threshold: 0.1 });
  reveals.forEach(r => observer.observe(r));
</script>
</body>
</html>
