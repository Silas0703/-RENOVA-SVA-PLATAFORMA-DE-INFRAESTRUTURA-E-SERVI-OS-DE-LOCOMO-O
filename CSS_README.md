/* ==========================================
   RENOVA SVA - ESTILOS COMPLETOS
   Plataforma de Infraestrutura e Locomoção
   ========================================== */

/* ------------------------------------------
   VARIÁVEIS DE CORES
   ------------------------------------------ */
:root {
  /* Cores Principais */
  --verde-escuro: #166534;
  --verde-medio: #22c55e;
  --verde-claro: #dcfce7;
  --verde-fundo: #f0fdf4;
 
  /* Cores Neutras */
  --branco: #ffffff;
  --cinza-100: #f1f5f9;
  --cinza-200: #e2e8f0;
  --cinza-300: #cbd5e1;
  --cinza-400: #94a3b8;
  --cinza-500: #64748b;
  --cinza-600: #475569;
  --cinza-700: #334155;
  --preto: #1e293b;
 
  /* Cores de Estado */
  --vermelho: #ef4444;
  --vermelho-claro: #fee2e2;
  --amarelo: #eab308;
  --amarelo-claro: #fef9c3;
  --azul: #3b82f6;
  --azul-claro: #dbeafe;
 
  /* Sombras */
  --sombra-sm: 0 1px 2px rgba(0, 0, 0, 0.05);
  --sombra-md: 0 4px 6px rgba(0, 0, 0, 0.1);
  --sombra-lg: 0 10px 15px rgba(0, 0, 0, 0.1);
  --sombra-xl: 0 20px 25px rgba(0, 0, 0, 0.15);
 
  /* Border Radius */
  --raio-sm: 4px;
  --raio-md: 8px;
  --raio-lg: 12px;
  --raio-xl: 16px;
  --raio-full: 9999px;
 
  /* Transições */
  --transicao: all 0.3s ease;
}

/* ------------------------------------------
   RESET BÁSICO
   ------------------------------------------ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-size: 16px;
  scroll-behavior: smooth;
}

body {
  font-family: 'Segoe UI', -apple-system, BlinkMacSystemFont, 'Roboto',
               'Helvetica Neue', Arial, sans-serif;
  background-color: var(--cinza-100);
  color: var(--preto);
  line-height: 1.6;
  min-height: 100vh;
}

/* ------------------------------------------
   ESTRUTURA PRINCIPAL
   ------------------------------------------ */
.App {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

/* ------------------------------------------
   CABEÇALHO (HEADER)
   ------------------------------------------ */
.App-header {
  background: linear-gradient(135deg, var(--verde-escuro) 0%, #15803d 50%, #166534 100%);
  color: var(--branco);
  padding: 30px 20px;
  box-shadow: var(--sombra-xl);
  position: relative;
  overflow: hidden;
}

.App-header::before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
  animation: pulse 4s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% { transform: scale(1); opacity: 0.5; }
  50% { transform: scale(1.1); opacity: 0.3; }
}

.logo-area {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
  position: relative;
  z-index: 1;
}

.logo-icon {
  font-size: 4rem;
  filter: drop-shadow(2px 2px 4px rgba(0,0,0,0.3));
  animation: bounce 2s ease-in-out infinite;
}

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

.logo-text {
  text-align: left;
}

.logo-text h1 {
  font-size: 2.5rem;
  font-weight: 800;
  letter-spacing: -1px;
  margin-bottom: 5px;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
}

.logo-text p {
  font-size: 1rem;
  opacity: 0.9;
  font-weight: 400;
}

/* ------------------------------------------
   BARRA DE NAVEGAÇÃO (TABS)
   ------------------------------------------ */
.nav-tabs {
  display: flex;
  justify-content: center;
  gap: 10px;
  background: var(--branco);
  padding: 15px 20px;
  box-shadow: var(--sombra-md);
  position: sticky;
  top: 0;
  z-index: 100;
}

.nav-tabs button {
  padding: 12px 24px;
  border: none;
  background: transparent;
  color: var(--cinza-600);
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  border-radius: var(--raio-lg);
  transition: var(--transicao);
  display: flex;
  align-items: center;
  gap: 8px;
}

.nav-tabs button:hover {
  background: var(--verde-claro);
  color: var(--verde-escuro);
}

.nav-tabs button.active {
  background: var(--verde-escuro);
  color: var(--branco);
  box-shadow: var(--sombra-md);
}

/* ------------------------------------------
   MENSAGENS (ALERTS)
   ------------------------------------------ */
.mensagem {
  max-width: 800px;
  margin: 20px auto;
  padding: 15px 20px;
  border-radius: var(--raio-lg);
  text-align: center;
  font-weight: 600;
  animation: slideDown 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
}

@keyframes slideDown {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.mensagem.sucesso {
  background: var(--verde-claro);
  color: var(--verde-escuro);
  border: 2px solid var(--verde-medio);
}

.mensagem.erro {
  background: var(--vermelho-claro);
  color: #991b1b;
  border: 2px solid var(--vermelho);
}

.mensagem.processando {
  background: var(--amarelo-claro);
  color: #854d0e;
  border: 2px solid var(--amarelo);
}

/* ------------------------------------------
   CONTAINER PRINCIPAL
   ------------------------------------------ */
.container {
  flex: 1;
  padding: 40px 20px;
  max-width: 1200px;
  margin: 0 auto;
  width: 100%;
}

/* ------------------------------------------
   TÍTULOS DE SEÇÃO
   ------------------------------------------ */
.section-title {
  text-align: center;
  margin-bottom: 40px;
}

.section-title h2 {
  font-size: 2rem;
  color: var(--verde-escuro);
  margin-bottom: 10px;
}

.section-title p {
  color: var(--cinza-500);
  font-size: 1.1rem;
}

/* -------------------------------- ----------
   LOADING (SPINNER)
   ------------------------------------------ */
.loading {
  text-align: center;
  padding: 80px 20px;
}

.spinner {
  width: 60px;
  height: 60px;
  margin: 0 auto 20px;
  border: 4px solid var(--cinza-200);
  border-top-color: var(--verde-medio);
  border-radius: 50%;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

/* ------------------------------------------
   GRID DE CARDS
   ------------------------------------------ */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 30px;
}

/* ------------------------------------------
   CARD DE VEÍCULO
   ------------------------------------------ */
.card {
  background: var(--branco);
  border-radius: var(--raio-xl);
  overflow: hidden;
  box-shadow: var(--sombra-md);
  transition: var(--transicao);
  display: flex;
  flex-direction: column;
}

.card:hover {
  transform: translateY(-8px);
  box-shadow: var(--sombra-xl);
}

.card.indisponivel {
  opacity: 0.7;
  background: var(--cinza-100);
}

.card-image {
  background: linear-gradient(135deg, var(--verde-claro) 0%, var(--verde-fundo) 100%);
  padding: 40px;
  text-align: center;
  position: relative;
}

.card-image::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 50px;
  background: linear-gradient(to top, var(--branco), transparent);
}

.card-image img {
  width: 100px;
  height: 100px;
  object-fit: contain;
  transition: var(--transicao);
}

.card:hover .card-image img {
  transform: scale(1.1);
}

.card-content {
  padding: 25px;
  flex: 1;
}

.card-content h3 {
  font-size: 1.4rem;
  color: var(--preto);
  margin-bottom: 10px;
  font-weight: 700;
}

.badge-tipo {
  display: inline-block;
  background: var(--verde-claro);
  color: var(--verde-escuro);
  padding: 5px 12px;
  border-radius: var(--raio-full);
  font-size: 0.85rem;
  font-weight: 600;
  margin-right: 8px;
}

.badge-categoria {
  display: inline-block;
  padding: 5px 12px;
  border-radius: var(--raio-full);
  font-size: 0.85rem;
  font-weight: 600;
}

.badge-categoria.Premium {
  background: #fef9c3;
  color: #854d0e;
}

.badge-categoria.Padrão {
  background: #dbeafe;
  color: #1e40af;
}

.badge-categoria.Básico {
  background: var(--cinza-100);
  color: var(--cinza-600);
}

.card-details {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.detail-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 15px;
  background: var(--cinza-100);
  border-radius: var(--raio-md);
}

.detail-item span:first-child {
  color: var(--cinza-600);
  font-size: 0.95rem;
}

.detail-item span:last-child {
  color: var(--preto);
  font-weight: 700;
  font-size: 1rem;
}

/* ------------------------------------------
   CARD DE ESTAÇÃO
   ------------------------------------------ */
.card.estacion {
  border-left: 4px solid var(--amarelo);
}

.card.estacion .card-image {
  background: linear-gradient(135deg, #fef9c3 0%, #fefce8 100%);
}

.card.estacion .endereco {
  color: var(--cinza-600);
  margin-top: 8px;
  font-size: 0.95rem;
}

/* ------------------------------------------
   BOTÕES
   ------------------------------------------ */
.card-actions {
  padding: 0 25px 25px;
}

.btn-alugar {
  width: 100%;
  padding: 14px 24px;
  border: none;
  border-radius: var(--raio-lg);
  font-size: 1rem;
  font-weight: 700;
  cursor: pointer;
  transition: var(--transicao);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  background: linear-gradient(135deg, var(--verde-medio) 0%, #16a34a 100%);
  color: var(--branco);
  box-shadow: var(--sombra-md);
}

.btn-alugar:hover {
  background: linear-gradient(135deg, #16a34a 0%, #15803d 100%);
  transform: scale(1.02);
  box-shadow: var(--sombra-lg);
}

.btn-alugar:active {
  transform: scale(0.98);
}

.btn-indisponivel {
  width: 100%;
  padding: 14px 24px;
  border: none;
  border-radius: var(--raio-lg);
  font-size: 1rem;
  font-weight: 600;
  cursor: not-allowed;
  background: var(--cinza-300);
  color: var(--branco);
}

/* ------------------------------------------
   DASHBOARD
   ------------------------------------------ */
.dashboard-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  margin-bottom: 40px;
}

.dashboard-card {
  background: var(--branco);
  padding: 30px;
  border-radius: var(--raio-xl);
  box-shadow: var(--sombra-md);
  text-align: center;
  transition: var(--transicao);
}

.dashboard-card:hover {
  transform: translateY(-5px);
  box-shadow: var(--sombra-lg);
}

.dashboard-card .icon {
  font-size: 3rem;
  margin-bottom: 15px;
}

.dashboard-card .value {
  font-size: 2.5rem;
  font-weight: 800;
  color: var(--verde-escuro);
  margin-bottom: 5px;
}

.dashboard-card .label {
  font-size: 1rem;
  color: var(--cinza-500);
  font-weight: 600;
}

/* ------------------------------------------
   RODAPÉ (FOOTER)
   ------------------------------------------ */
.App-footer {
  background: var(--preto);
  color: var(--branco);
  text-align: center;
  padding: 30px 20px;
  margin-top: auto;
}

.App-footer p {
  margin: 5px 0;
  opacity: 0.8;
  font-size: 0.95rem;
}

.App-footer .social {
  margin-top: 15px;
}

.App-footer .social a {
  color: var(--branco);
  margin: 0 10px;
  font-size: 1.5rem;
  text-decoration: none;
}

/* ------------------------------------------
   RESPONSIVIDADE
   ------------------------------------------ */
@media (max-width: 768px) {
  .logo-area {
    flex-direction: column;
    text-align: center;
  }
 
  .logo-text {
    text-align: center;
  }
 
  .logo-text h1 {
    font-size: 2rem;
  }
 
  .nav-tabs {
    flex-wrap: wrap;
  }
 
  .nav-tabs button {
    flex: 1;
    min-width: 100px;
  }
 
  .grid {
    grid-template-columns: 1fr;
  }
 
  .dashboard-grid {
    grid-template-columns: 1fr 1fr;
  }
}

@media (max-width: 480px) {
  .App-header {
    padding: 20px 15px;
  }
 
  .logo-icon {
    font-size: 3rem;
  }
 
  .logo-text h1 {
    font-size: 1.75rem;
  }
 
  .container {
    padding: 20px 15px;
  }
 
  .nav-tabs button {
    padding: 10px 15px;
    font-size: 0.9rem;
  }
 
  .dashboard-grid {
    grid-template-columns: 1fr;
  }
 
  .dashboard-card {
    padding: 20px;
  }
 
  .dashboard-card .value {
    font-size: 2rem;
  }
}

/* ------------------------------------------
   ANIMAÇÕES ADICIONAIS
   ------------------------------------------ */
.fade-in {
  animation: fadeIn 0.5s ease;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.slide-up {
  animation: slideUp 0.5s ease;
}

@keyframes slideUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ------------------------------------------
   SCROLLBAR PERSONALIZADA
   ------------------------------------------ */
::-webkit-scrollbar {
  width: 10px;
}

::-webkit-scrollbar-track {
  background: var(--cinza-100);
}

::-webkit-scrollbar-thumb {
  background: var(--cinza-300);
  border-radius: var(--raio-full);
}

::-webkit-scrollbar-thumb:hover {
  background: var(--cinza-400);
}

/* ------------------------------------------
   SELEÇÃO DE TEXTO
   ------------------------------------------ */
::selection {
  background: var(--verde-medio);
  color: var(--branco);
}
