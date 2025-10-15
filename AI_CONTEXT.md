# AI_CONTEXT — Projeto SEO Linhas de Metrô Brasil

## Objetivo
- Ranquear no Google (SEO) para termos relacionados às linhas de metrô das capitais brasileiras.
- **Somente** HTML + CSS + JavaScript vanilla. Sem frameworks, sem bundlers, sem SSR.
- Páginas **mobile-first**, rápidas, acessíveis e sem dependências externas desnecessárias.
- Foco em informações práticas: horários, estações, mapas, integrações, tarifas e dicas de uso.

## 🎯 Estrutura de Arquivos (OBRIGATÓRIO)
- **TODAS as páginas devem ter CSS e JavaScript INLINE** no mesmo arquivo HTML
- **NÃO criar** arquivos separados de CSS ou JS
- **NÃO usar** pastas `/assets/css/` ou `/assets/js/`
- **Estrutura ideal**: apenas arquivos HTML na raiz + `img/` quando necessário
- **Vantagens**: Zero requisições HTTP, deploy instantâneo, performance máxima

## Regras Gerais (obrigatórias)
1. **Tecnologia**: apenas HTML, CSS e JS puros. Nada de frameworks, bibliotecas externas, nem imports de CDNs (salvo fontes/svgs estritamente necessárias).
2. **Performance**: 
   - Lighthouse alvo: Performance ≥ 90, SEO ≥ 95, Acessibilidade ≥ 90.
   - TTFB baixo (usar HTML estático), **TODO CSS inline** no `<head>`.
   - **TODO JavaScript inline** no final do `<body>` com `defer`.
   - Imagens responsivas (`<img srcset>`), formatos modernos quando possível (webp/avif), `width/height` definidos.
3. **SEO On-Page**:
   - Uma **palavra-chave foco** por página (definir no topo do arquivo ao criar).
   - **Title** único (≤ 60 caracteres) e **meta description** (120–160).
   - **URL** curta, descritiva, com hífens: `minha-pagina-exemplo.html`.
   - **Heading único H1** contendo a palavra-chave foco; hierarquia correta de H2/H3.
   - **Conteúdo original** e útil; inserir sinônimos e LSI naturalmente.
   - **Links internos** contextuais e breadcrumbs.
   - **Canonical** sempre presente.
   - **Dados estruturados JSON-LD** apropriados (ex: `WebPage`, `Article`, `FAQPage`, `BreadcrumbList`).
   - **Open Graph/Twitter** para compartilhamento.
4. **Mobile-first & UX**:
   - `meta viewport` correto.
   - Layout fluido; tipografia legível; touch targets adequados (mín. 44x44px).
   - Evitar modais intrusivos; respeitar **CLS** (evitar layout shift).
5. **Acessibilidade**:
   - Semântica correta; `alt` em imagens; contrastes AA; foco visível; navegação por teclado.
   - `aria-` somente quando necessário (não substitui semântica).
6. **Privacidade/Tracking**:
   - Adiar qualquer script de analytics (se usado) com `defer` e eventuais consentimentos.
   - Não carregar tags que não sejam essenciais.
7. **Conteúdo e Tom**:
   - Clareza, utilidade e profundidade; responda intenção de busca (informacional/transacional/navegacional).
   - Use FAQs quando fizer sentido para *featured snippets*.
8. **Google Tag Manager (OBRIGATÓRIO)**:
   - **SEMPRE** incluir o snippet do GTM em TODAS as páginas criadas.
   - **Código no `<head>`**: antes do `</head>`, logo após as meta tags.
   - **Código após `<body>`**: logo após a abertura da tag `<body>`.
   - **ID do container**: usar `GTM-N7Q7XMDD` (será rotacionado por segurança).
   - **Posicionamento**: GTM deve ser o primeiro script no head e o primeiro elemento no body.
   - **Fallback**: incluir sempre o código noscript para usuários sem JavaScript.

## Checklist para **nova página**
- [ ] Definir **palavra-chave foco** e intenção de busca.
- [ ] Redigir **Title** e **meta description**.
- [ ] Esqueleto HTML semântico, **H1 único** com a keyword.
- [ ] Conteúdo original e escaneável (sumário, H2/H3, listas, imagens com `alt`).
- [ ] Links internos (incluir 2–4 para páginas relevantes).
- [ ] JSON-LD adequado (WebPage/Article + BreadcrumbList; FAQ se houver).
- [ ] **TODO CSS inline** no `<head>` (não criar arquivos separados).
- [ ] **TODO JavaScript inline** no final do `<body>` com `defer`.
- [ ] **GOOGLE TAG MANAGER** incluído no head e body (OBRIGATÓRIO).
- [ ] Teste mobile (quebra de layout, tipografia, CLS).
- [ ] Verificar Lighthouse (Perf/SEO/A11y).
- [ ] Adicionar à `sitemap.xml` (e link no `robots.txt`).
- [ ] Revisar ortografia e consistência de tom.

## Convenções de Arquivos
- **Páginas na raiz** com nomes descritivos: `metro-sao-paulo.html`, `metro-rio-de-janeiro.html`, `metro-brasilia.html`.
- **Estrutura ultra-simplificada**: apenas arquivos HTML na raiz.
- **CSS e JS inline**: cada página contém seu próprio CSS e JavaScript.
- **Imagens**: pasta `img/` na raiz para mapas, estações e diagramas.
- **Vantagens**: Zero requisições HTTP, deploy instantâneo, performance máxima.

## Estrutura de Conteúdo por Página
- **Página principal**: `index.html` - visão geral do metrô no Brasil
- **Por capital**: `metro-[cidade].html` - informações específicas de cada metrô
- **Por linha**: `linha-[cor]-[cidade].html` - detalhes de linhas específicas
- **Tópicos específicos**: `horarios-metro.html`, `tarifas-metro.html`, `mapas-metro.html`

## Palavras-chave Principais (SEO)
### Por Cidade
- **São Paulo**: "metrô são paulo", "linhas metrô sp", "estações metrô são paulo", "horário metrô sp"
- **Rio de Janeiro**: "metrô rio de janeiro", "metro rio", "linhas metrô rj", "estações metrô rio"
- **Brasília**: "metrô brasília", "metro df", "linhas metrô brasília", "estações metrô df"
- **Belo Horizonte**: "metrô belo horizonte", "metro mg", "linhas metrô bh"
- **Recife**: "metrô recife", "metro pe", "linhas metrô recife"
- **Salvador**: "metrô salvador", "metro ba", "linhas metrô salvador"
- **Fortaleza**: "metrô fortaleza", "metro ce", "linhas metrô fortaleza"

### Por Linha (São Paulo)
- **Linha Azul**: "linha azul metrô sp", "linha 1 azul", "estações linha azul"
- **Linha Verde**: "linha verde metrô sp", "linha 2 verde", "estações linha verde"
- **Linha Vermelha**: "linha vermelha metrô sp", "linha 3 vermelha", "estações linha vermelha"
- **Linha Amarela**: "linha amarela metrô sp", "linha 4 amarela", "estações linha amarela"
- **Linha Lilás**: "linha lilás metrô sp", "linha 5 lilás", "estações linha lilás"

### Informações Práticas
- "horário metrô", "funcionamento metrô", "frequência metrô"
- "tarifa metrô", "preço metrô", "bilhete metrô", "integração metrô"
- "mapa metrô", "estações metrô", "rotas metrô"
- "metrô 24 horas", "metrô domingo", "metrô feriado"

## Template HTML Base (SEO + Mobile + GTM)
```html
<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />

  <!-- Google Tag Manager -->
  <script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
  new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
  j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
  'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
  })(window,document,'script','dataLayer','GTM-N7Q7XMDD');</script>
  <!-- End Google Tag Manager -->

  <title><!-- 55–60c: Título com keyword foco sobre metrô --></title>
  <meta name="description" content="<!-- 120–160c: descrição atraente com keyword sobre metrô -->" />

  <link rel="canonical" href="https://www.metrobrasil.com.br/slug-da-pagina/" />

  <!-- Open Graph -->
  <meta property="og:type" content="website" />
  <meta property="og:title" content="<!-- mesmo do title ou variante -->" />
  <meta property="og:description" content="<!-- igual/variante da description -->" />
  <meta property="og:url" content="https://www.metrobrasil.com.br/slug-da-pagina/" />
  <meta property="og:image" content="https://www.metrobrasil.com.br/img/og-metro.jpg" />

  <!-- Twitter -->
  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="<!-- título -->" />
  <meta name="twitter:description" content="<!-- descrição -->" />
  <meta name="twitter:image" content="https://www.metrobrasil.com.br/img/og-metro.jpg" />

  <!-- CSS COMPLETO inline (não usar arquivos externos) -->
  <style>
    /* Reset e base */
    *,*::before,*::after{box-sizing:border-box}html{line-height:1.15;-webkit-text-size-adjust:100%}body{margin:0;font-family:system-ui,-apple-system,'Segoe UI',Roboto,Arial,sans-serif;line-height:1.6;color:#1f2937;background:#fff}h1,h2,h3,h4,h5,h6{margin:0;font-weight:600;line-height:1.2}p{margin:0 0 1rem 0}a{color:#2563eb;text-decoration:none;transition:color 0.2s}a:hover{color:#1e40af;text-decoration:underline}img{max-width:100%;height:auto;display:block}ul,ol{margin:0;padding:0}li{list-style:none}button,input,select,textarea{font-family:inherit;font-size:inherit;line-height:inherit;margin:0}button{cursor:pointer;border:none;background:none}table{border-collapse:collapse;border-spacing:0}
    
    /* Variáveis CSS */
    :root{--primary:#2563eb;--primary-dark:#1e40af;--accent:#3b82f6;--text:#1f2937;--text-light:#6b7280;--bg-light:#f9fafb;--border:#e5e7eb;--success:#059669;--white:#fff;--shadow:0 2px 8px rgba(0,0,0,0.1);--shadow-lg:0 4px 12px rgba(0,0,0,0.15);--radius:8px;--radius-lg:12px;--transition:all 0.2s ease}
    
    /* Layout */
    .container{width:min(1200px,95%);margin:0 auto;padding:0 1rem}.grid{display:grid;gap:2rem}.grid-2{grid-template-columns:repeat(auto-fit,minmax(300px,1fr))}.grid-3{grid-template-columns:repeat(auto-fit,minmax(250px,1fr))}.grid-4{grid-template-columns:repeat(auto-fit,minmax(200px,1fr))}
    
    /* Componentes */
    .btn{display:inline-block;padding:1rem 2rem;background:var(--primary);color:var(--white);border-radius:var(--radius);font-weight:600;text-decoration:none;transition:var(--transition);border:1px solid var(--primary)}.btn:hover{background:var(--primary-dark);transform:translateY(-2px);box-shadow:var(--shadow-lg);text-decoration:none}
    
    .card{background:var(--white);padding:2rem;border-radius:var(--radius-lg);box-shadow:var(--shadow);border:1px solid var(--border);transition:var(--transition)}.card:hover{transform:translateY(-2px);box-shadow:0 4px 16px rgba(0,0,0,0.15)}.card h3{color:var(--primary);margin:0 0 1rem 0;font-size:1.25rem}.card p{margin:0;color:var(--text-light)}
    
    .hero{background:linear-gradient(135deg,var(--primary) 0%,var(--primary-dark) 100%);color:var(--white);padding:3rem 0;text-align:center}.hero h1{font-size:clamp(2rem,4vw,3rem);margin:0 0 1rem 0;font-weight:700}.hero p{font-size:1.2rem;margin:0 0 2rem 0;opacity:0.9}
    
    .section{padding:3rem 0}.section:nth-child(even){background:var(--bg-light)}
    
    /* Responsive */
    @media (max-width:768px){.container{padding:0 0.5rem}.hero{padding:2rem 0}.section{padding:2rem 0}.grid-2,.grid-3,.grid-4{grid-template-columns:1fr}.card{padding:1.5rem}}
    @media (max-width:480px){.btn{padding:0.75rem 1.5rem;font-size:0.9rem}.card{padding:1rem}}
    
    /* Acessibilidade */
    .btn:focus-visible,a:focus-visible{outline:2px solid var(--primary);outline-offset:2px}
    @media (prefers-reduced-motion:reduce){*,*::before,*::after{animation-duration:0.01ms!important;animation-iteration-count:1!important;transition-duration:0.01ms!important}.btn:hover{transform:none}.card:hover{transform:none}}
  </style>

  <!-- JSON-LD (ajuste conforme o tipo de página) -->
  <script type="application/ld+json">
  {
    "@context":"https://schema.org",
    "@type":"WebPage",
    "name":"<!-- título -->",
    "url":"https://www.metrobrasil.com.br/slug-da-pagina/",
    "description":"<!-- description -->",
    "breadcrumb":{
      "@type":"BreadcrumbList",
      "itemListElement":[
        {"@type":"ListItem","position":1,"name":"Início","item":"https://www.metrobrasil.com.br/"},
        {"@type":"ListItem","position":2,"name":"<!-- Cidade/Seção -->","item":"https://www.metrobrasil.com.br/secao/"},
        {"@type":"ListItem","position":3,"name":"<!-- Página -->","item":"https://www.metrobrasil.com.br/slug-da-pagina/"}
      ]
    }
  }
  </script>

  <!-- CSS está 100% inline acima - não usar arquivos externos -->
</head>
<body>
  <!-- Google Tag Manager (noscript) -->
  <noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-N7Q7XMDD"
  height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
  <!-- End Google Tag Manager (noscript) -->

  <header class="container" role="banner" aria-label="Topo do site">
    <nav aria-label="Breadcrumb">
      <ol>
        <li><a href="/">Início</a></li>
        <li><a href="/metro-sao-paulo.html">Metrô São Paulo</a></li>
        <li aria-current="page">Linha Azul</li>
      </ol>
    </nav>
    <h1><!-- H1 único com keyword foco sobre metrô --></h1>
  </header>

  <main class="container" role="main">
    <p><!-- Intro que responde a intenção de busca sobre metrô em 1–2 frases. --></p>

    <h2><!-- Horários de funcionamento --></h2>
    <p><!-- Horários, frequência, dias de funcionamento --></p>

    <h2><!-- Estações e integrações --></h2>
    <p><!-- Lista de estações, conexões com ônibus, trem, BRT --></p>

    <h2><!-- Tarifas e bilhetagem --></h2>
    <p><!-- Valores, tipos de bilhete, formas de pagamento --></p>

    <!-- FAQ opcional (ótimo para snippets) -->
    <section aria-labelledby="faq-title">
      <h2 id="faq-title">Perguntas frequentes sobre o metrô</h2>
      <dl>
        <dt><!-- Qual o horário de funcionamento do metrô? --></dt>
        <dd><!-- Resposta sobre horários e frequência --></dd>
        <dt><!-- Como funciona a integração com ônibus? --></dt>
        <dd><!-- Resposta sobre integração tarifária --></dd>
        <dt><!-- Quais são os tipos de bilhete disponíveis? --></dt>
        <dd><!-- Resposta sobre bilhetagem --></dd>
      </dl>
      <script type="application/ld+json">
      {
        "@context":"https://schema.org",
        "@type":"FAQPage",
        "mainEntity":[
          {"@type":"Question","name":"Qual o horário de funcionamento do metrô?","acceptedAnswer":{"@type":"Answer","text":"O metrô funciona de segunda a sexta das 4h40 às 24h, sábados das 4h40 às 1h e domingos das 4h40 às 24h."}},
          {"@type":"Question","name":"Como funciona a integração com ônibus?","acceptedAnswer":{"@type":"Answer","text":"A integração permite usar o mesmo bilhete para metrô e ônibus dentro do período de 3 horas."}},
          {"@type":"Question","name":"Quais são os tipos de bilhete disponíveis?","acceptedAnswer":{"@type":"Answer","text":"Estão disponíveis bilhete unitário, bilhete duplo, bilhete de 10 viagens e cartão de transporte."}}
        ]
      }
      </script>
    </section>

    <!-- Imagem exemplo com dimensões para evitar CLS -->
    <figure>
      <img src="/img/mapa-metro-sao-paulo.webp" width="1200" height="675" alt="Mapa das linhas de metrô de São Paulo" />
      <figcaption>Mapa completo das linhas de metrô da capital paulista.</figcaption>
    </figure>
  </main>

  <footer class="container" role="contentinfo">
    <nav aria-label="Links de rodapé">
      <a class="btn" href="/metro-sao-paulo.html">Metrô SP</a>
      <a class="btn" href="/metro-rio-de-janeiro.html">Metrô RJ</a>
      <a class="btn" href="/metro-brasilia.html">Metrô DF</a>
      <a class="btn" href="/horarios-metro.html">Horários</a>
    </nav>
    <p>&copy; <span id="year"></span> MetroBrasil - Informações sobre metrô no Brasil.</p>
  </footer>

  <script defer>
    // JavaScript COMPLETO inline (não usar arquivos externos)
    (function() {
        'use strict';
        
        // Utilitários
        const utils = {
            debounce: function(func, wait) {
                let timeout;
                return function executedFunction(...args) {
                    const later = () => {
                        clearTimeout(timeout);
                        func(...args);
                    };
                    clearTimeout(timeout);
                    timeout = setTimeout(later, wait);
                };
            },
            throttle: function(func, limit) {
                let inThrottle;
                return function() {
                    const args = arguments;
                    const context = this;
                    if (!inThrottle) {
                        func.apply(context, args);
                        inThrottle = true;
                        setTimeout(() => inThrottle = false, limit);
                    }
                };
            }
        };

        // Smooth scroll para links internos
        function initSmoothScroll() {
            const links = document.querySelectorAll('a[href^="#"]');
            links.forEach(link => {
                link.addEventListener('click', function(e) {
                    const href = this.getAttribute('href');
                    if (href === '#') return;
                    e.preventDefault();
                    const target = document.querySelector(href);
                    if (target) {
                        const headerHeight = document.querySelector('header')?.offsetHeight || 0;
                        const targetPosition = target.offsetTop - headerHeight - 20;
                        window.scrollTo({
                            top: targetPosition,
                            behavior: 'smooth'
                        });
                        target.focus();
                    }
                });
            });
        }

        // Inicialização
        function init() {
            if (document.readyState === 'loading') {
                document.addEventListener('DOMContentLoaded', init);
                return;
            }
            
            initSmoothScroll();
            
            // Atualizar ano no footer
            const yearElement = document.getElementById('year');
            if (yearElement) {
                yearElement.textContent = new Date().getFullYear();
            }
            
            console.log('Página carregada com JavaScript inline');
        }

        init();
    })();
  </script>
</body>
</html>