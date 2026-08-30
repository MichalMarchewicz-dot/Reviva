

<div class="section-background color-{{ section.settings.color_scheme }}"></div>
<div
  class="section section--{{ section.settings.section_width }} spacing-style {% if section.settings.color_scheme != blank %}color-{{ section.settings.color_scheme }}{% endif %}"
  style="{% render 'spacing-padding', settings: section.settings %}"
>
  {{ section.settings.custom_liquid }}
</div>

{% schema %}
{
  "name": "t:names.custom_liquid",
  "settings": [
    {
      "type": "liquid",
      "id": "custom_liquid",
      "label": "t:settings.custom_liquid",
      "info": "t:info.custom_liquid"
    },
    {
      "type": "color_scheme",
      "id": "color_scheme",
      "label": "t:settings.color_scheme",
      "default": "scheme-1"
    },
    {
      "type": "select",
      "id": "section_width",
      "label": "t:settings.width",
      "options": [
        {
          "value": "page-width",
          "label": "t:options.page"
        },
        {
          "value": "full-width",
          "label": "t:options.full"
        }
      ],
      "default": "page-width"
    },
    {
      "type": "header",
      "content": "t:content.padding"
    },
    {
      "type": "range",
      "id": "padding-block-start",
      "label": "t:settings.top",
      "min": 0,
      "max": 100,
      "step": 1,
      "unit": "px",
      "default": 0
    },
    {
      "type": "range",
      "id": "padding-block-end",
      "label": "t:settings.bottom",
      "min": 0,
      "max": 100,
      "step": 1,
      "unit": "px",
      "default": 0
    }
  ],
  "presets": [
    {
      "name": "t:names.custom_liquid",
      "category": "t:categories.layout"
    }
  ]
}
{% endschema %}




{% comment %} 
  Upewnij się, że w ustawieniach produktu w Shopify 
  URL handle to dokładnie: darmowy-ebook
{% endcomment %}
{% assign ebook_product = all_products['darmowy-ebook'] %}
{% assign ebook_variant_id = ebook_product.variants.first.id %}

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Unbounded:wght@700;900&family=Plus+Jakarta+Sans:wght@400;600;800&family=JetBrains+Mono:wght@500&display=swap" rel="stylesheet">

<div class="unified-landing">
    <div class="f-bg-layers">
        <div class="f-grid"></div>
        <div class="f-glow-static"></div>
    </div>

    <div class="action-container">
        <div class="action-header center-text">
            <div class="pulse-dot"></div>
            <span class="live-status">TWOJA SZANSA JEST TERAZ</span>
            <h2>Przestań planować.<br>Zacznij budować.</h2>
            <p class="section-subtitle">Ten kurs to paliwo, które odpali Twój biznes jeszcze dziś.</p>
        </div>

        <div class="transformation-card">
            <span class="live-status center-text" style="font-size:10px;">TWOJA TRANSFORMACJA</span>
            <h3 class="transformation-title">Zbuduj życie, w którym nie będziesz musiał brać urlopu.</h3>
            <p>Większość ludzi spędza życie budując czyjeś marzenia za stałą pensję. Ten system powstał po to, abyś w końcu przestał pytać o pozwolenie na wolność.</p>
            
            <div class="impact-row">
                <div class="impact-col">
                    <span class="impact-tag status-red">0% SZUMU</span>
                    <p class="impact-desc">Sama przejrzysta wiedza, gotowa do zastosowania.</p>
                </div>
                <div class="impact-col">
                    <span class="impact-tag status-green">100% KONTROLI</span>
                    <p class="impact-desc">Ty ustalasz reguły gry.</p>
                </div>
            </div>
        </div>

        <div class="cta-wrapper center-text">
            <a href="https://kursiify.myshopify.com/products/sklep-ktory-po-prostu-dziala-e-book?variant=52212676690262" class="massive-button main-cta-btn">ROZPOCZNIJ TRANSFORMACJĘ →</a>
            <p class="sub-cta-text">Dołącz do 2% ludzi, którzy biorą sprawy w swoje ręce.</p>
        </div>

        <div class="section-divider">
            <div class="divider-line"></div>
            <span class="divider-text">LUB ZACZNIJ ZA DARMO</span>
            <div class="divider-line"></div>
        </div>

        <div class="newsletter-integration horizontal-layout">
            <div class="ebook-split-container">
                <div class="k-visual-presentation">
                    <div class="k-floating-mockup">
                        <div class="promo-badge-green">ZA DARMO</div>
                        <div class="promo-badge-newsletter">NEWSLETTER</div>
                        
                        {% if ebook_product.featured_image != blank %}
                            <img src="{{ ebook_product.featured_image | img_url: '800x800', crop: 'center' }}" alt="{{ ebook_product.title }}" class="k-main-img">
                        {% else %}
                            <div class="k-no-img">
                                <div class="k-no-img-content">
                                    <span>KURSIFY</span>
                                    <strong>E-BOOK</strong>
                                </div>
                            </div>
                        {% endif %}
                        <div class="k-glow-effect"></div>
                    </div>
                </div>

                <div class="newsletter-content">
                    <div class="newsletter-header-left">
                        <span class="live-status">DARMOWY WARSZTAT</span>
                        <h2 class="mini-h2">Odbierz darmowy PDF</h2>
                        <p class="section-subtitle-small">Zacznij od konkretnych wskazówek, zanim wejdziesz na wyższy poziom. Praktyczna wiedza dostępna od ręki.</p>
                    </div>

                    <div class="form-row">
                        <a href="/checkout?updates[{{ ebook_variant_id | default: '52212676690262' }}]=1" class="massive-button ebook-btn-horizontal">
                            ODBIERZ E-BOOK ZA 0 ZŁ —
                        </a>
                    </div>
                    <p class="security-note">🔒 Odbierając e-book, dołączasz do newslettera Kursiify Digital Academy. </p>
                </div>
            </div>
        </div>
    </div>
</div>

<style>
    :root {
        --u-green: #2ecc71;
        --u-red: #ff4757;
        --u-black: #050505;
    }

    .center-text { text-align: center !important; margin-left: auto !important; margin-right: auto !important; }

    .unified-landing { 
        background-color: var(--u-black) !important; position: relative; color: #ffffff !important; 
        font-family: 'Plus Jakarta Sans', sans-serif !important; overflow: hidden; padding: 40px 0 80px 0; 
        width: 100%;
    }
    
    .unified-landing .f-bg-layers { position: absolute; inset: 0; pointer-events: none; z-index: 1; }
    .unified-landing .f-grid { 
        position: absolute; inset: 0; 
        background-image: linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px); 
        background-size: 60px 60px; mask-image: radial-gradient(circle at 50% 50%, black 10%, transparent 90%); 
    }
    .unified-landing .f-glow-static { 
        position: absolute; top: 40%; left: 50%; transform: translate(-50%, -50%); 
        width: 800px; height: 800px; background: var(--u-green); filter: blur(200px); opacity: 0.08; 
    }

    .unified-landing h2 { font-family: 'Unbounded', sans-serif !important; font-weight: 900 !important; font-size: clamp(2.2rem, 7vw, 3.8rem) !important; line-height: 1.1 !important; margin: 20px 0 !important; background: linear-gradient(to bottom, #ffffff 80%, #444444) !important; -webkit-background-clip: text !important; -webkit-text-fill-color: transparent !important; text-transform: uppercase; }

    .unified-landing .mini-h2 { font-family: 'Unbounded', sans-serif !important; font-weight: 700; font-size: clamp(1.6rem, 4.5vw, 2.1rem) !important; margin: 10px 0 !important; text-transform: uppercase; line-height: 1.2; color: #fff; }

    .unified-landing .section-subtitle { color: #888; font-size: 1.1rem; max-width: 600px; line-height: 1.6; margin: 0 auto; }
    .section-subtitle-small { color: #888; font-size: 0.95rem; line-height: 1.5; margin-bottom: 5px; }

    .unified-landing .transformation-card { 
        background: rgba(15, 15, 15, 0.8) !important; border: 1px solid rgba(255,255,255,0.1) !important; 
        border-radius: 40px; padding: 60px 40px; text-align: center; backdrop-filter: blur(20px); 
        max-width: 850px; width: calc(100% - 40px); margin: 40px auto; position: relative; z-index: 10; 
    }
    .transformation-title { font-family: 'Unbounded', sans-serif !important; font-weight: 700; text-transform: uppercase; font-size: clamp(1.1rem, 3.5vw, 1.5rem) !important; margin: 15px 0; }
    
    .impact-row { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 30px; border-top: 1px solid rgba(255,255,255,0.1); padding-top: 30px; }
    .impact-tag { font-family: 'Unbounded', sans-serif !important; font-weight: 800; font-size: 11px; display: block; margin-bottom: 8px; }
    .impact-desc { min-height: 50px; display: flex; align-items: center; justify-content: center; margin: 0; font-size: 14px; color: #aaa; }

    .status-red { color: var(--u-red) !important; text-shadow: 0 0 10px rgba(255, 71, 87, 0.3); }
    .status-green { color: var(--u-green) !important; text-shadow: 0 0 10px rgba(46, 204, 113, 0.3); }

    .massive-button { 
        display: inline-block; background: var(--u-green) !important; color: #000 !important; padding: 20px 35px; 
        font-family: 'Unbounded', sans-serif !important; font-weight: 900 !important; text-decoration: none !important; 
        border-radius: 12px; position: relative; transition: 0.3s; border: none; cursor: pointer; z-index: 10; text-transform: uppercase; font-size: 14px; 
    }
    .massive-button:hover { transform: translateY(-3px); box-shadow: 0 10px 30px rgba(46, 204, 113, 0.4); }
    
    .sub-cta-text { color: #666; font-size: 13px; margin-top: 15px; font-weight: 600; text-align: center; }

    .newsletter-integration.horizontal-layout {
        max-width: 900px; margin: 30px auto; padding: 40px; background: rgba(255,255,255,0.02); 
        border-radius: 30px; border: 1px solid rgba(255,255,255,0.05); position: relative; z-index: 10;
    }
    .ebook-split-container { display: flex; align-items: center; gap: 40px; text-align: left; }
    .newsletter-content { flex: 1; display: flex; flex-direction: column; align-items: flex-start; }

    .k-visual-presentation { flex: 0 0 220px; display: flex; justify-content: center; position: relative; }
    .k-floating-mockup { position: relative; width: 220px; height: 220px; animation: k-float-alt 5s ease-in-out infinite; }
    .k-main-img { width: 100%; height: 100%; object-fit: cover; border-radius: 12px; box-shadow: 15px 15px 40px rgba(0,0,0,0.6); border: 1px solid rgba(255,255,255,0.1); }

    /* NAKLEJKI */
    .promo-badge-green {
        position: absolute; top: -5px; right: -5px; background: var(--u-green); color: #000;
        font-family: 'Unbounded', sans-serif; font-weight: 900; font-size: 10px; padding: 8px 14px;
        border-radius: 50px; z-index: 30; transform: rotate(12deg); box-shadow: 0 5px 15px rgba(46, 204, 113, 0.4);
        text-transform: uppercase; letter-spacing: 1px; animation: badge-pulse 2s infinite ease-in-out;
    }

    .promo-badge-newsletter {
        position: absolute; bottom: -5px; left: -5px; background: #fff; color: #000;
        font-family: 'JetBrains Mono', monospace; font-weight: 800; font-size: 9px; padding: 6px 12px;
        border-radius: 4px; z-index: 30; transform: rotate(-8deg); box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        text-transform: uppercase; letter-spacing: 1px;
    }

    .section-divider { display: flex; align-items: center; justify-content: center; margin: 40px auto; max-width: 850px; opacity: 0.4; }
    .divider-line { flex: 1; height: 1px; background: #333; }
    .divider-text { padding: 0 20px; font-family: 'JetBrains Mono', monospace; font-size: 11px; color: var(--u-green); letter-spacing: 2px; }
    
    .live-status { font-family: 'JetBrains Mono', monospace !important; color: var(--u-green) !important; font-size: 11px; letter-spacing: 2px; text-transform: uppercase; display: block; margin-bottom: 8px; }
    
    /* KROPKA - POPRAWIONA NA ZIELONĄ */
    .pulse-dot { 
        width: 10px; height: 10px; 
        background-color: var(--u-green) !important; 
        border-radius: 50%; 
        margin: 0 auto 12px; 
        box-shadow: 0 0 15px var(--u-green) !important;
        animation: dot-pulse 2s infinite;
    }

    @keyframes dot-pulse {
        0% { transform: scale(0.95); box-shadow: 0 0 0 0 rgba(46, 204, 113, 0.7); }
        70% { transform: scale(1); box-shadow: 0 0 0 10px rgba(46, 204, 113, 0); }
        100% { transform: scale(0.95); box-shadow: 0 0 0 0 rgba(46, 204, 113, 0); }
    }

    .security-note { color: #555; font-size: 11px; margin-top: 12px; font-weight: 600; line-height: 1.4; }

    @keyframes k-float-alt { 0%, 100% { transform: translateY(0) rotate(-1deg); } 50% { transform: translateY(-8px) rotate(1deg); } }
    @keyframes badge-pulse { 0%, 100% { transform: rotate(12deg) scale(1); } 50% { transform: rotate(12deg) scale(1.1); } }

    @media (max-width: 768px) {
        .unified-landing { padding: 30px 0 60px 0; }
        .ebook-split-container { flex-direction: column; gap: 40px; text-align: center; }
        .newsletter-content { align-items: center; }
        .mini-h2, .section-subtitle-small, .security-note { text-align: center !important; }
        .ebook-btn-horizontal { width: 100%; }
        .k-floating-mockup { width: 180px; height: 180px; }
        .impact-row { grid-template-columns: 1fr; }
    }
</style>









<div class="blue-v2-full-wrapper multispectral-adjust">
  <div class="blue-v2-grid-overlay"></div>
  <div class="blue-v2-neon-glow"></div>

  <div class="system-why-container">
    <div class="system-header">
      <div class="header-content">
        <span class="system-code-blue">ID: KURSIIFY_CORE_V1.3</span>
        <h2 class="system-title-blue">PROTOKÓŁ <span class="blue-highlight-text">PRZEWAGI</span></h2>
        <p class="system-disclaimer-blue">// Dane surowe. Analiza wielopoziomowa.</p>
      </div>
    </div>

    <div class="system-data-grid-blue">
      <div class="data-block-blue border-green">
        <div class="data-top-blue">
          <span class="data-label-blue">SKUTECZNOŚĆ METODOLOGII</span>
          <span class="data-value-blue color-green">94.2% [STABLE]</span>
        </div>
        <div class="progress-bar-blue">
          <div class="progress-fill-blue bg-green" style="--target-width: 94.2%;"></div>
        </div>
        <p class="data-desc-blue">Eliminujemy 94% błędów, które kładą początkujące firmy. Reszta to zmienne rynkowe, na które przygotowujemy Twój system.</p>
      </div>

      <div class="data-block-blue border-blue">
        <div class="data-top-blue">
          <span class="data-label-blue">OPTYMALIZACJA PROCESÓW</span>
          <span class="data-value-blue color-blue">87.5% [OPTIMIZED]</span>
        </div>
        <div class="progress-bar-blue">
          <div class="progress-fill-blue bg-blue" style="--target-width: 87.5%;"></div>
        </div>
        <p class="data-desc-blue">Automatyzacja przejmuje krytyczne procesy. Pozostałe 12.5% to Twoje decyzje, których nie zastąpi żaden algorytm.</p>
      </div>

      <div class="data-block-blue border-yellow">
        <div class="data-top-blue">
          <span class="data-label-blue">GOTOWOŚĆ INFRASTRUKTURY</span>
          <span class="data-value-blue color-yellow">91.0% [READY]</span>
        </div>
        <div class="progress-bar-blue">
          <div class="progress-fill-blue bg-yellow" style="--target-width: 91%;"></div>
        </div>
        <p class="data-desc-blue">Fundamenty silniejsze niż u 9/10 konkurencji. Resztę budujesz Ty, dopasowując system pod własną, unikalną wizję.</p>
      </div>
    </div>

    <div class="system-footer-blue">
      <div class="status-indicator-blue">
        <div class="status-dot-blue"></div>
        <span>SYSTEM STATUS: OPERATIONAL_MULTISPECTRAL</span>
      </div>
      <div class="system-coords-blue">52.2297° N, 21.0122° E</div>
    </div>
  </div>
</div>

<style>
  /* GŁÓWNY WRAPPER Z REDUKCJĄ ODSTĘPU */
  .multispectral-adjust {
    --u-blue: #3d5afe;
    --u-green: #00ff41;
    --u-yellow: #ffea00;
    background-color: #050505 !important;
    position: relative;
    overflow: hidden;
    font-family: 'Plus Jakarta Sans', sans-serif !important;
    color: #ffffff;
    width: 100%;
    padding: 40px 0 100px 0; /* Zmniejszony górny padding z 100px na 40px */
  }

  .blue-v2-grid-overlay {
    position: absolute; inset: 0;
    background-image: linear-gradient(rgba(61, 90, 254, 0.07) 1px, transparent 1px), linear-gradient(90deg, rgba(61, 90, 254, 0.07) 1px, transparent 1px);
    background-size: 50px 50px;
    mask-image: radial-gradient(circle at 50% 50%, black, transparent 90%);
    pointer-events: none; z-index: 1;
  }

  .system-why-container {
    max-width: 900px;
    margin: 0 auto;
    position: relative;
    z-index: 10;
    padding: 0 5%;
  }

  .system-header {
    margin-bottom: 50px;
    border-left: 3px solid var(--u-blue);
    padding-left: 25px;
  }

  .system-code-blue {
    color: #444;
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    display: block;
    margin-bottom: 8px;
  }

  .system-title-blue {
    font-family: 'Unbounded', sans-serif !important;
    font-weight: 900;
    font-size: clamp(1.6rem, 4vw, 2.5rem);
    margin: 0;
    text-transform: uppercase;
  }

  .blue-highlight-text {
    color: var(--u-blue);
    text-shadow: 0 0 20px rgba(61, 90, 254, 0.4);
  }

  .system-disclaimer-blue {
    font-size: 10px;
    color: #333;
    font-family: 'JetBrains Mono', monospace;
    margin-top: 8px;
  }

  /* BLOKI DANYCH */
  .system-data-grid-blue { display: flex; flex-direction: column; gap: 30px; }

  .data-block-blue {
    background: rgba(255, 255, 255, 0.01);
    padding: 25px;
    border-radius: 16px;
    border: 1px solid rgba(255, 255, 255, 0.05);
    transition: 0.4s;
  }

  /* KOLORYSTYKA INDYWIDUALNA */
  .border-green:hover { border-color: rgba(0, 255, 65, 0.3); background: rgba(0, 255, 65, 0.02); }
  .border-blue:hover { border-color: rgba(61, 90, 254, 0.3); background: rgba(61, 90, 254, 0.02); }
  .border-yellow:hover { border-color: rgba(255, 234, 0, 0.3); background: rgba(255, 234, 0, 0.02); }

  .color-green { color: var(--u-green) !important; }
  .color-blue { color: var(--u-blue) !important; }
  .color-yellow { color: var(--u-yellow) !important; }

  .bg-green { background: var(--u-green); box-shadow: 0 0 15px var(--u-green); }
  .bg-blue { background: var(--u-blue); box-shadow: 0 0 15px var(--u-blue); }
  .bg-yellow { background: var(--u-yellow); box-shadow: 0 0 15px var(--u-yellow); }

  .data-top-blue {
    display: flex;
    justify-content: space-between;
    margin-bottom: 15px;
    font-weight: 800;
    font-size: 11px;
    font-family: 'JetBrains Mono', monospace;
  }

  /* PASKI POSTĘPU */
  .progress-bar-blue {
    height: 5px;
    background: rgba(255, 255, 255, 0.03);
    width: 100%;
    margin-bottom: 15px;
    border-radius: 10px;
    overflow: hidden;
  }

  .progress-fill-blue {
    height: 100%;
    width: 0;
    animation: fillUpProgress 2.5s cubic-bezier(0.19, 1, 0.22, 1) forwards;
  }

  @keyframes fillUpProgress {
    from { width: 0; }
    to { width: var(--target-width); }
  }

  .data-desc-blue { color: #777; font-size: 13px; line-height: 1.5; margin: 0; }

  /* FOOTER */
  .system-footer-blue {
    margin-top: 50px;
    padding-top: 20px;
    border-top: 1px solid rgba(255, 255, 255, 0.05);
    display: flex;
    justify-content: space-between;
    font-size: 9px;
    font-family: 'JetBrains Mono', monospace;
    color: #333;
  }

  .status-indicator-blue { display: flex; align-items: center; gap: 8px; }
  .status-dot-blue {
    width: 6px; height: 6px; background: var(--u-blue); border-radius: 50%;
    box-shadow: 0 0 8px var(--u-blue); animation: blinkBlue 1.5s infinite;
  }

  @keyframes blinkBlue { 0%, 100% { opacity: 1; } 50% { opacity: 0.3; } }

  @media (max-width: 768px) {
    .system-footer-blue { flex-direction: column; gap: 10px; }
    .data-top-blue { flex-direction: column; gap: 5px; }
  }
</style>









<div class="kursify-main-wrapper unique-bg-isolated prevent-select" oncontextmenu="return false;">
    <div class="isolated-grid-overlay"></div>
    <div class="isolated-neon-glow"></div>

    <div class="content-layout">
        <div class="promo-column promo-left">
            <div class="promo-badge-mono tech-badge-green">#SYSTEM_v2.0 // INNOWACJA</div>
            <h2 class="promo-title title-green">E-Book Kursify:<br>Nowa era nauki</h2>
            <ul class="promo-list list-green">
                <li>Dostęp natychmiastowy</li>
                <li>Instrukcje krok po kroku</li>
                <li>Dożywotnie aktualizacje</li>
                <li>Systemowe podejście</li>
                <li>Przystępna cena</li>
            </ul>
            <a href="https://kursiify.myshopify.com/products/sklep-ktory-po-prostu-dziala-e-book?variant=52212676690262" class="promo-btn">KUPUJĘ E-BOOKA</a>
        </div>

        <div class="kursify-comparison-box vertical-box" id="slider-box-v2">
            <img src="https://cdn.shopify.com/s/files/1/0984/8343/7910/files/Zrzut_ekranu_1411.png?v=1768642733" class="slider-img" alt="Tradycyjny" draggable="false">
            <div class="slider-after-layer" id="after-img-cont-v2">
                <img src="https://cdn.shopify.com/s/files/1/0984/8343/7910/files/22.png?v=1768145383" class="slider-img overlay-a4-fix" alt="Ebook" draggable="false">
            </div>
            <div class="slider-drag-handle" id="handle-v2"></div>
        </div>

        <div class="promo-column promo-right">
            <div class="promo-badge-mono tech-badge-red">#LEGACY_v1.0 // PRZESZŁOŚĆ</div>
            <h2 class="promo-title title-red">Tradycyjny kurs:<br>Relikt przeszłości</h2>
            <ul class="promo-list list-red">
                <li>Czekasz godzinami na dostęp</li>
                <li>Statyczna, nudna wiedza</li>
                <li>Szybka utrata motywacji</li>
                <li>Lanie wody (puste treści)</li>
                <li>Nierealnie wysoka cena</li>
            </ul>
            <p class="red-warning">Zastanów się, czy warto tracić czas?</p>
        </div>
    </div>
</div>

<style>
    /* IMPORTY CZCIONEK */
    @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@500;800&family=Unbounded:wght@900&family=Plus+Jakarta+Sans:wght@400;700&display=swap');

    :root {
        --u-neon: #00ff41;
        --u-red: #ff4d4d;
        --u-blue: #3d5afe;
    }

    .prevent-select { -webkit-user-select: none; user-select: none; }

    /* GŁÓWNY WRAPPER SEKCJI */
    .unique-bg-isolated {
        width: 100%; padding: 120px 0; display: flex; justify-content: center; 
        position: relative; overflow: hidden; 
        background: #050505 !important; 
        z-index: 1; 
        font-family: 'Plus Jakarta Sans', sans-serif !important;
    }

    /* SIATKA I POŚWIATA */
    .isolated-grid-overlay {
        position: absolute; inset: 0;
        background-image: linear-gradient(rgba(61, 90, 254, 0.2) 1px, transparent 1px), 
                          linear-gradient(90deg, rgba(61, 90, 254, 0.2) 1px, transparent 1px);
        background-size: 50px 50px;
        -webkit-mask-image: radial-gradient(ellipse at center, black 0%, transparent 80%), 
                            linear-gradient(to bottom, transparent 0%, black 15%, black 85%, transparent 100%);
        mask-image: radial-gradient(ellipse at center, black 0%, transparent 80%), 
                    linear-gradient(to bottom, transparent 0%, black 15%, black 85%, transparent 100%);
        -webkit-mask-composite: source-in;
        mask-composite: intersect;
        pointer-events: none; z-index: 1;
    }

    .isolated-neon-glow {
        position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%);
        width: 850px; height: 850px;
        background: radial-gradient(circle, rgba(61, 90, 254, 0.15) 0%, transparent 75%);
        filter: blur(130px); z-index: 1; pointer-events: none;
    }

    /* UKŁAD TREŚCI */
    .content-layout { display: flex; align-items: stretch; justify-content: center; gap: 30px; max-width: 1300px; width: 95%; z-index: 2; }

    .promo-column { 
        flex: 1; padding: 50px 40px; border-radius: 35px; 
        background: rgba(8, 8, 8, 0.95); backdrop-filter: blur(20px); 
        border: 1px solid rgba(255, 255, 255, 0.05); position: relative;
        display: flex; flex-direction: column;
    }
    
    .promo-left { border-color: rgba(0, 255, 65, 0.2); }
    .promo-right { border-color: rgba(255, 77, 77, 0.2); }

    /* TECHNICZNE BADGE (SKRYPTOWE) */
    .promo-badge-mono {
        font-family: 'JetBrains Mono', monospace !important;
        font-size: 11px;
        letter-spacing: 2px;
        padding: 6px 14px;
        border-radius: 6px;
        width: fit-content;
        margin-bottom: 25px;
        font-weight: 800;
        text-transform: uppercase;
    }

    .tech-badge-green {
        color: var(--u-neon);
        background: rgba(0, 255, 65, 0.05);
        border: 1px solid rgba(0, 255, 65, 0.3);
        box-shadow: 0 0 15px rgba(0, 255, 65, 0.1);
    }

    .tech-badge-red {
        color: var(--u-red);
        background: rgba(255, 77, 77, 0.05);
        border: 1px solid rgba(255, 77, 77, 0.3);
        box-shadow: 0 0 15px rgba(255, 77, 77, 0.1);
    }

    .promo-title { font-family: 'Unbounded', sans-serif !important; font-size: 26px; margin-bottom: 30px; text-transform: uppercase; font-weight: 900; color: #fff; line-height: 1.2; }
    .promo-list { padding: 0; margin-bottom: 35px; flex-grow: 1; list-style: none; }
    .promo-list li { margin-bottom: 15px; color: #ccc; position: relative; padding-left: 35px; font-size: 15px; }
    .list-green li::before { content: "→"; position: absolute; left: 0; color: var(--u-neon); font-weight: 900; }
    .list-red li::before { content: "✕"; position: absolute; left: 0; color: var(--u-red); font-weight: 900; }

    .promo-btn {
        display: block; padding: 22px; text-align: center; text-decoration: none; 
        font-family: 'Unbounded', sans-serif; font-weight: 900; border-radius: 12px; 
        background: var(--u-neon); color: #000 !important; text-transform: uppercase; font-size: 13px;
        transition: 0.3s; letter-spacing: 1px;
    }

    /* SLIDER KURS / E-BOOK */
    .kursify-comparison-box.vertical-box {
        position: relative; width: 350px; aspect-ratio: 1 / 1.414; overflow: hidden;
        border: 1px solid rgba(255, 255, 255, 0.1); border-radius: 25px; flex-shrink: 0;
        cursor: ew-resize; z-index: 5; box-shadow: 0 30px 60px rgba(0,0,0,0.8); touch-action: none;
    }
    .slider-img { position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover !important; }
    .slider-after-layer { position: absolute; top: 0; left: 0; width: 50%; height: 100%; overflow: hidden; z-index: 2; border-right: 2px solid var(--u-neon); }
    .slider-drag-handle { position: absolute; top: 0; bottom: 0; left: 50%; width: 2px; background: var(--u-neon); z-index: 3; transform: translateX(-50%); }
    .slider-drag-handle::after { 
        content: "⇄"; position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); 
        width: 40px; height: 40px; background: #000; border: 2px solid var(--u-neon); 
        border-radius: 50%; color: var(--u-neon); display: flex; justify-content: center; align-items: center; font-weight: bold;
    }

    .red-warning { color: var(--u-red); font-weight: 700; text-align: center; margin-top: 10px; font-size: 12px; text-transform: uppercase; opacity: 0.8; }

    /* WERSJA MOBILNA - POPRAWKI KOLEJNOŚCI I ODSTĘPU */
    @media (max-width: 1100px) {
        .unique-bg-isolated { 
            padding: 50px 0 100px 0; /* Zmniejszony odstęp górny */
        }
        .content-layout { flex-direction: column; align-items: center; gap: 40px; }
        .promo-column { width: 100%; }
        
        .promo-left { order: 1; } /* E-book Kursify na samej górze */
        .kursify-comparison-box.vertical-box { order: 2; width: 100%; max-width: 350px; }
        .promo-right { order: 3; } /* Przeszłość na samym dole */
    }
</style>

<script>
    (function() {
        const box = document.getElementById('slider-box-v2');
        const after = document.getElementById('after-img-cont-v2');
        const handle = document.getElementById('handle-v2');
        if (!box || !after || !handle) return;
        let active = false;
        const moveSlider = (e) => {
            if (!active) return;
            window.getSelection().removeAllRanges();
            let x = (e.type.includes('touch')) ? e.touches[0].clientX : e.clientX;
            let rect = box.getBoundingClientRect();
            let position = ((x - rect.left) / rect.width) * 100;
            position = Math.max(0, Math.min(100, position));
            after.style.width = position + '%';
            handle.style.left = position + '%';
        };
        box.addEventListener('mousedown', () => active = true);
        window.addEventListener('mouseup', () => active = false);
        window.addEventListener('mousemove', moveSlider);
        box.addEventListener('touchstart', () => active = true, { passive: false });
        window.addEventListener('touchend', () => active = false);
        window.addEventListener('touchmove', moveSlider, { passive: false });
    })();
</script>










<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Unbounded:wght@700;900&family=Plus+Jakarta+Sans:wght@400;600;800&family=JetBrains+Mono:wght@500&display=swap" rel="stylesheet">

<div class="blue-v2-full-wrapper">
  <div class="blue-v2-grid-overlay"></div>
  <div class="blue-v2-neon-glow"></div>

  <div class="blue-v2-section">
    <div class="blue-v2-flex-container">
      
      <div class="blue-v2-text-box">
        <h2 class="blue-v2-main-title">
          STRUKTURA,<br>
          <span class="blue-v2-highlight">KTÓRA</span><br>
          SPRZEDAJE
        </h2>

        <div class="blue-v2-countdown-container">
          <p class="blue-v2-countdown-label">PIERWSZE WYDANIE 20 MARCA O 00:00</p>
          <div class="blue-v2-timer-grid">
            <div class="blue-v2-timer-item"><span id="blue-v2-days">00</span><small>DNI</small></div>
            <div class="blue-v2-timer-item"><span id="blue-v2-hours">00</span><small>GODZ</small></div>
            <div class="blue-v2-timer-item"><span id="blue-v2-minutes">00</span><small>MIN</small></div>
            <div class="blue-v2-timer-item"><span id="blue-v2-seconds">00</span><small>SEK</small></div>
          </div>
        </div>
        
        <div class="blue-v2-cta-price-group">
          <a href="https://kursiify.myshopify.com/products/struktura-ktora-sprzedaje-edycja-marzec-2026?variant=52512668713302" class="blue-v2-cta-button pulse-animation">
            ZAMÓW PREORDER
          </a>

          <div class="blue-v2-price-container">
            <div class="blue-v2-price-row">
              <span class="blue-v2-price-old">213,99 zł</span>
              <span class="blue-v2-price-new">127,99 zł</span>
            </div>
            <p class="blue-v2-tax-info">
              *Najniższa cena z ostatnich 30 dni: 127,99 zł. W cenę wliczono podatki.
            </p>
          </div>
        </div>
      </div>

      <div class="blue-v2-visual-box">
        <div class="preorder-sticker">PRZEDSPRZEDAŻ!</div>
        <div class="blue-v2-image-float">
          <a href="https://kursiify.myshopify.com/products/struktura-ktora-sprzedaje-edycja-marzec-2026?variant=52512668713302" class="blue-v2-product-link">
            <div class="blue-v2-neon-frame">
              <img src="https://cdn.shopify.com/s/files/1/0984/8343/7910/files/STRUKTURA_KTORA_SPRZEDAJE_1.png?v=1770227159" alt="E-book Kursify">
            </div>
          </a>
        </div>
      </div>

    </div>
  </div>

  <div class="benefits-v2-outer">
    <div class="benefits-v2-grid">
      <div class="benefit-v2-card">
        <div class="benefit-v2-dot benefit-v2-blue-pulse"></div>
        <h3>0% Szumu</h3>
        <p>Konkretna wiedza bez zbędnych wypełniaczy. Tylko to, co faktycznie zarabia.</p>
      </div>
      <div class="benefit-v2-card">
        <div class="benefit-v2-dot benefit-v2-blue-pulse"></div>
        <h3>100% Kontroli</h3>
        <p>Zbuduj system, który daje Ci wolność, a nie kolejny etat u samego siebie.</p>
      </div>
      <div class="benefit-v2-card">
        <div class="benefit-v2-dot benefit-v2-blue-pulse"></div>
        <h3>Bez stresu</h3>
        <p>Proste rozwiązania e-commerce, które po prostu działają bez technicznego chaosu.</p>
      </div>
    </div>
    
    <div class="benefits-v2-footer">
      <div class="cta-wrapper">
        <a href="https://kursiify.myshopify.com/products/struktura-ktora-sprzedaje-edycja-marzec-2026?variant=52512668713302" class="blue-v2-cta-button pulse-animation">
          SPRAWDŹ PEŁNĄ OFERTĘ
        </a>
        <div class="bottom-glow-effect"></div>
      </div>
    </div>
  </div>
</div>

<style>
  .blue-v2-full-wrapper {
    --u-blue: #3d5afe;
    background-color: #050505 !important;
    position: relative;
    overflow: hidden;
    font-family: 'Plus Jakarta Sans', sans-serif !important;
    color: #ffffff;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .blue-v2-grid-overlay {
    position: absolute; inset: 0;
    background-image: linear-gradient(rgba(61, 90, 254, 0.07) 1px, transparent 1px), linear-gradient(90deg, rgba(61, 90, 254, 0.07) 1px, transparent 1px);
    background-size: 50px 50px;
    mask-image: radial-gradient(circle at 50% 50%, black, transparent 90%);
    pointer-events: none; z-index: 1;
  }

  .blue-v2-section { padding: 80px 5% 40px 5%; width: 100%; display: flex; justify-content: center; position: relative; z-index: 10; }
  .blue-v2-flex-container { display: flex; gap: 60px; max-width: 1200px; width: 100%; align-items: center; }
  .blue-v2-text-box { flex: 1.2; display: flex; flex-direction: column; align-items: center; text-align: center; }
  .blue-v2-visual-box { flex: 1; position: relative; max-width: 420px; width: 100%; }

  .blue-v2-main-title { color: #fff !important; font-family: 'Unbounded', sans-serif !important; font-size: clamp(34px, 5vw, 68px); line-height: 0.95; margin: 0 0 30px 0; text-transform: uppercase; font-weight: 900; }
  .blue-v2-highlight { color: var(--u-blue); text-shadow: 0 0 25px rgba(61, 90, 254, 0.5); }

  .blue-v2-countdown-container { background: rgba(61, 90, 254, 0.05); padding: 25px; border-radius: 20px; border: 1px solid rgba(61, 90, 254, 0.15); margin-bottom: 35px; width: 100%; max-width: 450px; }
  .blue-v2-countdown-label { font-size: 10px; letter-spacing: 2px; color: #888; margin-bottom: 15px; font-family: 'JetBrains Mono', monospace; font-weight: 700; text-transform: uppercase; }
  .blue-v2-timer-grid { display: flex; gap: 25px; justify-content: center; }
  .blue-v2-timer-item span { display: block; font-family: 'Unbounded', sans-serif; font-size: clamp(24px, 3vw, 32px); color: #fff; line-height: 1; }
  .blue-v2-timer-item small { font-size: 9px; color: var(--u-blue); font-weight: 800; margin-top: 8px; display: block; text-transform: uppercase; }

  @keyframes float { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-20px); } }
  .blue-v2-image-float { animation: float 6s ease-in-out infinite; }
  .blue-v2-neon-frame { border: 3px solid var(--u-blue); border-radius: 40px; padding: 15px; background: rgba(10, 10, 10, 0.8); box-shadow: 0 0 50px rgba(61, 90, 254, 0.2); transition: 0.4s; }
  .blue-v2-image-float:hover .blue-v2-neon-frame { transform: scale(1.02); border-color: #fff; box-shadow: 0 0 70px rgba(61, 90, 254, 0.4); }
  .blue-v2-neon-frame img { width: 100%; height: auto; border-radius: 25px; display: block; }

  .blue-v2-price-container { margin-top: 25px; text-align: center; }
  .blue-v2-price-row { display: flex; align-items: center; gap: 20px; justify-content: center; }
  .blue-v2-price-old { color: rgba(255, 255, 255, 0.3); text-decoration: line-through; font-size: 22px; font-weight: 600; }
  .blue-v2-price-new { color: var(--u-blue); font-size: 46px; font-weight: 900; font-family: 'Unbounded', sans-serif; }
  .blue-v2-tax-info { color: #444; font-size: 11px; margin-top: 10px; font-weight: 600; letter-spacing: 0.3px; }

  .blue-v2-cta-button {
    display: flex; align-items: center; justify-content: center; text-align: center;
    background-color: var(--u-blue) !important; color: #fff !important; padding: 24px 50px; 
    border-radius: 18px; font-family: 'Unbounded', sans-serif !important; font-weight: 900; 
    text-decoration: none !important; text-transform: uppercase; font-size: 18px; 
    transition: 0.3s; border: none; cursor: pointer; width: fit-content; margin: 0 auto;
  }
  .blue-v2-cta-button:hover { filter: brightness(1.2); transform: translateY(-3px) scale(1.02); box-shadow: 0 15px 45px rgba(61, 90, 254, 0.5); }

  @keyframes bluePulse { 0%, 100% { transform: scale(1); box-shadow: 0 10px 40px rgba(61, 90, 254, 0.3); } 50% { transform: scale(1.03); box-shadow: 0 10px 60px rgba(61, 90, 254, 0.6); } }
  .pulse-animation { animation: bluePulse 2s infinite; }

  /* BENEFITS - POWRÓT DO NIEBIESKIEGO */
  .benefits-v2-outer { padding: 40px 5% 100px 5%; width: 100%; display: flex; flex-direction: column; align-items: center; position: relative; z-index: 10; }
  .benefits-v2-grid { display: flex; gap: 25px; justify-content: center; flex-wrap: wrap; max-width: 1200px; margin-bottom: 60px; }
  
  .benefit-v2-card { 
    background: rgba(10, 10, 10, 0.9); border: 1px solid rgba(61, 90, 254, 0.4); 
    box-shadow: 0 0 30px rgba(61, 90, 254, 0.1); padding: 45px 35px; 
    border-radius: 30px; width: 350px; text-align: left; transition: 0.4s; 
  }
  .benefit-v2-card:hover { border-color: var(--u-blue); transform: translateY(-10px); box-shadow: 0 15px 45px rgba(61, 90, 254, 0.2); }

  /* NIEBIESKA KROPKA */
  .benefit-v2-dot { 
    width: 12px; height: 12px; background: var(--u-blue) !important; 
    border-radius: 50%; margin-bottom: 25px; box-shadow: 0 0 15px var(--u-blue) !important;
  }
  
  @keyframes blueDotPulse {
    0% { transform: scale(0.95); box-shadow: 0 0 0 0 rgba(61, 90, 254, 0.7); }
    70% { transform: scale(1); box-shadow: 0 0 0 10px rgba(61, 90, 254, 0); }
    100% { transform: scale(0.95); box-shadow: 0 0 0 0 rgba(61, 90, 254, 0); }
  }
  .benefit-v2-blue-pulse { animation: blueDotPulse 2s infinite; }

  .benefit-v2-card h3 { font-family: 'Unbounded', sans-serif !important; font-weight: 900; font-size: 22px; color: #fff; margin-bottom: 15px; text-transform: uppercase; }
  .benefit-v2-card p { color: #888; line-height: 1.6; font-size: 15px; }

  .benefits-v2-footer { width: 100%; display: flex; justify-content: center; }
  .cta-wrapper { position: relative; }
  .bottom-glow-effect { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 160%; height: 160%; background: radial-gradient(circle, rgba(61, 90, 254, 0.3) 0%, transparent 70%); filter: blur(35px); z-index: -1; }
  .preorder-sticker { position: absolute; top: -15px; right: -10px; background: var(--u-blue); color: #fff; padding: 12px 20px; font-family: 'Unbounded', sans-serif; font-weight: 900; font-size: 14px; border-radius: 10px; transform: rotate(8deg); z-index: 20; box-shadow: 0 10px 30px rgba(0,0,0,0.5); }

  @media (max-width: 900px) { 
    .blue-v2-flex-container { flex-direction: column-reverse; } 
    .benefit-v2-card { width: 100%; } 
    .blue-v2-cta-button { width: 100%; max-width: 320px; padding: 20px 20px; }
  }
</style>

<script>
  (function() {
    function updateBlueTimer() {
      const now = new Date().getTime();
      const target = new Date(2026, 2, 20, 0, 0, 0).getTime();
      const diff = target - now;
      if (diff <= 0) return;
      document.getElementById("blue-v2-days").innerText = Math.floor(diff / (1000 * 60 * 60 * 24)).toString().padStart(2, '0');
      document.getElementById("blue-v2-hours").innerText = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)).toString().padStart(2, '0');
      document.getElementById("blue-v2-minutes").innerText = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60)).toString().padStart(2, '0');
      document.getElementById("blue-v2-seconds").innerText = Math.floor((diff % (1000 * 60)) / 1000).toString().padStart(2, '0');
    }
    setInterval(updateBlueTimer, 1000); updateBlueTimer();
  })();
</script>












<div class="refined-aura-divider"></div>

<style>
  .refined-aura-divider {
    width: 100%;
    /* Bardzo niska wysokość, żeby nie zajmować miejsca */
    height: 1px; 
    background: #050505; /* Zmieniono z #000000 na #050505 */
    position: relative;
    z-index: 100;
    
    /* Zmniejszony margines ujemny - tylko tyle, by aura dotknęła sekcji */
    margin: -10px 0; 
    
    /* Aura w kolorze #050505 dla idealnego wtapiania się w sekcje */
    box-shadow: 0 0 30px 15px #050505; 
    
    pointer-events: none;
  }

  @media (max-width: 768px) {
    .refined-aura-divider {
      box-shadow: 0 0 20px 10px #050505;
      margin: -5px 0;
    }
  }
</style>






<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Unbounded:wght@700;900&family=Plus+Jakarta+Sans:wght@400;600;800&family=JetBrains+Mono:wght@500&display=swap" rel="stylesheet">

<div class="green-v3-section">
  <div class="green-v3-neon-glow"></div>
  <div class="green-v3-grid-overlay"></div>

  <div class="green-v3-flex-container">
    
    <div class="green-v3-visual-box">
      <a href="https://kursiify.myshopify.com/products/sklep-ktory-po-prostu-dziala-e-book?variant=52212676690262" class="green-v3-product-link">
        <div class="green-v3-neon-frame">
          <img src="https://cdn.shopify.com/s/files/1/0984/8343/7910/files/7.png?v=1768345192" alt="E-book Kursify">
        </div>
      </a>
    </div>

    <div class="green-v3-text-box">
      <h2 class="green-v3-main-title">
        SKLEP, KTÓRY<br>
        <span class="green-v3-highlight">PO PROSTU</span><br>
        DZIAŁA
      </h2>

      <div class="green-v3-countdown-container">
        <p class="green-v3-countdown-label">PROMOCJA KOŃCZY SIĘ W ŚRODĘ O 23:59:</p>
        <div class="green-v3-timer-grid">
          <div class="green-v3-timer-item"><span id="green-v3-days">00</span><small>DNI</small></div>
          <div class="green-v3-timer-item"><span id="green-v3-hours">00</span><small>GODZ</small></div>
          <div class="green-v3-timer-item"><span id="green-v3-minutes">00</span><small>MIN</small></div>
          <div class="green-v3-timer-item"><span id="green-v3-seconds">00</span><small>SEK</small></div>
        </div>
      </div>
      
      <div class="green-v3-cta-price-group">
        <a href="https://kursiify.myshopify.com/products/sklep-ktory-po-prostu-dziala-e-book?variant=52212676690262" class="green-v3-cta-button">
          KUP TERAZ I ZYSKAJ 
        </a>

        <div class="green-v3-price-tag">
          <span class="green-v3-price-old">96,99 zł</span>
          <span class="green-v3-price-new">57,99 zł</span>
        </div>
        
        <p class="green-v3-tax-info">
          *Najniższa cena z ostatnich 30 dni: 57,99 zł. W cenę wliczono podatki.
        </p>
      </div>
    </div>

  </div>
</div>

<style>
  .green-v3-section {
    --u-green: #2ecc71;
    background-color: #050505 !important;
    padding: 100px 5%;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 750px;
    position: relative;
    overflow: hidden;
    font-family: 'Plus Jakarta Sans', sans-serif !important;
    color: #ffffff;
    z-index: 1;
  }

  .green-v3-grid-overlay {
    position: absolute; inset: 0;
    background-image: 
      linear-gradient(rgba(46, 204, 113, 0.05) 1px, transparent 1px), 
      linear-gradient(90deg, rgba(46, 204, 113, 0.05) 1px, transparent 1px);
    background-size: 50px 50px;
    mask-image: radial-gradient(circle at 50% 50%, black, transparent 90%);
    pointer-events: none;
  }

  .green-v3-neon-glow {
    position: absolute;
    width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(46, 204, 113, 0.12) 0%, transparent 70%);
    filter: blur(80px);
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    pointer-events: none;
  }

  .green-v3-flex-container {
    display: flex; 
    flex-direction: row;
    gap: 60px;
    max-width: 1200px; 
    width: 100%; 
    align-items: center; 
    z-index: 10;
  }

  .green-v3-visual-box { flex: 1; position: relative; max-width: 420px; }
  
  /* WYŚRODKOWANIE TEKSTU I ELEMENTÓW */
  .green-v3-text-box { 
    flex: 1.2; 
    text-align: center; 
    display: flex;
    flex-direction: column;
    align-items: center; 
  }

  .green-v3-neon-frame {
    border: 3px solid var(--u-green);
    border-radius: 40px; padding: 15px;
    background: rgba(10, 10, 10, 0.8);
    box-shadow: 0 0 50px rgba(46, 204, 113, 0.15);
    transition: 0.4s;
  }
  .green-v3-product-link:hover .green-v3-neon-frame { transform: scale(1.02) rotate(-1deg); }
  .green-v3-neon-frame img { width: 100%; height: auto; border-radius: 25px; display: block; }

  .green-v3-main-title {
    color: #fff !important; font-family: 'Unbounded', sans-serif !important;
    font-size: clamp(34px, 5vw, 68px); line-height: 0.95; margin: 0 0 30px 0;
    text-transform: uppercase; font-weight: 900;
  }

  .green-v3-highlight {
    color: var(--u-green); text-shadow: 0 0 20px rgba(46, 204, 113, 0.3);
  }

  .green-v3-countdown-container { 
    background: rgba(255,255,255,0.03); padding: 20px; border-radius: 20px; 
    border: 1px solid rgba(255,255,255,0.05); margin-bottom: 35px; width: 100%; max-width: 450px;
  }
  .green-v3-countdown-label { 
    font-size: 10px; letter-spacing: 2px; color: #666; margin: 0 0 15px 0; 
    font-family: 'JetBrains Mono', monospace; font-weight: 700;
  }
  .green-v3-timer-grid { display: flex; gap: 20px; justify-content: center; }
  .green-v3-timer-item span { 
    display: block; font-family: 'Unbounded', sans-serif; 
    font-size: clamp(20px, 3vw, 28px); color: #fff; line-height: 1;
  }
  .green-v3-timer-item small { font-size: 9px; color: var(--u-green); font-weight: 800; margin-top: 8px; display: block; }

  .green-v3-cta-price-group { display: flex; flex-direction: column; align-items: center; gap: 20px; width: 100%; }

  .green-v3-cta-button {
    display: inline-block; background-color: var(--u-green) !important;
    color: #000 !important; padding: 24px 45px; border-radius: 18px;
    font-family: 'Unbounded', sans-serif !important; font-weight: 900;
    text-decoration: none !important; text-transform: uppercase; font-size: 18px;
    transition: 0.3s; text-align: center; box-shadow: 0 10px 40px rgba(46, 204, 113, 0.25);
  }

  .green-v3-price-tag { display: flex; align-items: center; gap: 20px; justify-content: center; }
  .green-v3-price-old { color: rgba(255, 255, 255, 0.3); text-decoration: line-through; font-size: 22px; }
  .green-v3-price-new { color: var(--u-green); font-size: 42px; font-weight: 900; font-family: 'Unbounded', sans-serif; }

  .green-v3-tax-info { color: #444; font-size: 11px; margin: 0; font-weight: 600; }

  @media (max-width: 900px) {
    .green-v3-flex-container { flex-direction: column; }
    .green-v3-visual-box { width: 90%; max-width: 320px; }
  }
</style>

<script>
  (function() {
    function updateGreenTimer() {
      const now = new Date();
      const target = new Date();
      target.setDate(now.getDate() + (3 + 7 - now.getDay()) % 7);
      target.setHours(23, 59, 59, 0);
      if (target <= now) target.setDate(target.getDate() + 7);

      const diff = target - now;
      document.getElementById("green-v3-days").innerText = Math.floor(diff / 86400000).toString().padStart(2, '0');
      document.getElementById("green-v3-hours").innerText = Math.floor((diff % 86400000) / 3600000).toString().padStart(2, '0');
      document.getElementById("green-v3-minutes").innerText = Math.floor((diff % 3600000) / 60000).toString().padStart(2, '0');
      document.getElementById("green-v3-seconds").innerText = Math.floor((diff % 60000) / 1000).toString().padStart(2, '0');
    }
    setInterval(updateGreenTimer, 1000); updateGreenTimer();
  })();
</script>





<div class="green-v2-full-wrapper support-minimal-adjust">
  <div class="m-grid-base m-grid-green"></div>
  
  <div class="green-v2-subtle-glow"></div>

  <div class="minimal-support-content">
    <div class="support-line-decorator"></div>
    
    <h2 class="minimal-support-title">
      NIE KUPUJESZ TYLKO PLIKU.<br>
      <span class="green-v2-highlight">KUPUJESZ SPOKÓJ.</span>
    </h2>

    <div class="minimal-support-text">
      <p>
        Wiemy, że technologia i budowanie struktur potrafią przytłoczyć. Dlatego 
        <strong>nie zostawiamy Cię z tym samego.</strong> Jeśli utkniesz w martwym punkcie, lub
        masz pytanie o konkretny element systemu, postaramy się Tobie pomóc – jesteśmy po drugiej stronie ekranu.
      </p>
      <p class="support-signature">Kliknij poniżej, aby skopiować e-mail.</p>
    </div>

    <div class="minimal-support-action">
      <button id="copy-email-btn-final" class="support-mail-link" data-email="kursify@wp.pl">
        <span class="mail-icon">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>
        </span>
        <span class="btn-text">kursify@wp.pl</span>
      </button>
      <div id="copy-toast-final" class="copy-feedback">Skopiowano do schowka!</div>
    </div>
  </div>
</div>

<style>
  .support-minimal-adjust {
    --u-green: #2ecc71;
    background-color: #050505 !important;
    position: relative;
    overflow: hidden;
    padding: 90px 5% 70px 5%; 
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    width: 100%;
    min-height: 350px;
  }

  .m-grid-base {
    position: absolute;
    inset: 0;
    background-size: 50px 50px;
    pointer-events: none;
    z-index: 1;
  }

  .m-grid-green {
    background-image: 
      linear-gradient(rgba(46, 204, 113, 0.07) 1px, transparent 1px), 
      linear-gradient(90deg, rgba(46, 204, 113, 0.07) 1px, transparent 1px);
    
    /* MODYFIKACJA: Maska działająca na GÓRĘ i DÓŁ */
    -webkit-mask-image: 
      linear-gradient(to bottom, transparent 0%, black 15%, black 85%, transparent 100%),
      radial-gradient(circle at center, black 30%, transparent 85%);
    mask-image: 
      linear-gradient(to bottom, transparent 0%, black 15%, black 85%, transparent 100%),
      radial-gradient(circle at center, black 30%, transparent 85%);
    
    -webkit-mask-composite: source-in;
    mask-composite: intersect;
  }

  .green-v2-subtle-glow {
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    width: 500px; height: 350px;
    background: radial-gradient(circle, rgba(46, 204, 113, 0.04) 0%, transparent 70%);
    filter: blur(80px);
    pointer-events: none;
    z-index: 2;
  }

  .minimal-support-content { max-width: 750px; width: 100%; position: relative; z-index: 10; }
  .support-line-decorator { width: 60px; height: 3px; background: var(--u-green); margin: 0 auto 30px auto; border-radius: 10px; box-shadow: 0 0 15px rgba(46, 204, 113, 0.3); }
  .minimal-support-title { font-family: 'Unbounded', sans-serif !important; font-weight: 900; font-size: clamp(24px, 4vw, 42px); line-height: 1.1; margin-bottom: 30px; color: #fff !important; text-transform: uppercase; letter-spacing: -0.04em; }
  .green-v2-highlight { color: var(--u-green); text-shadow: 0 0 20px rgba(46, 204, 113, 0.2); }
  .minimal-support-text { font-family: 'Plus Jakarta Sans', sans-serif !important; color: #aaa; font-size: clamp(15px, 2vw, 18px); line-height: 1.8; }
  .support-signature { font-family: 'JetBrains Mono', monospace; font-size: 13px; color: var(--u-green) !important; margin-top: 35px; text-transform: uppercase; }
  .minimal-support-action { margin-top: 30px; }
  .support-mail-link { display: inline-flex; align-items: center; gap: 12px; color: #fff !important; font-family: 'Unbounded', sans-serif; font-weight: 700; font-size: 16px; padding: 15px 35px; border: 1px solid rgba(255, 255, 255, 0.1); border-radius: 100px; transition: 0.3s; background: rgba(255, 255, 255, 0.02); cursor: pointer; }
  .support-mail-link:hover { border-color: var(--u-green); background: rgba(46, 204, 113, 0.05); transform: translateY(-3px); }
  .mail-icon { color: var(--u-green); display: flex; }
  .copy-feedback { margin-top: 15px; font-family: 'JetBrains Mono', monospace; font-size: 11px; color: var(--u-green); opacity: 0; transition: 0.3s; text-transform: uppercase; }
  .copy-feedback.show { opacity: 1; }

  @media (max-width: 768px) {
    .support-minimal-adjust { padding: 60px 5% 50px 5%; }
  }
</style>

<script>
  (function() {
    const btn = document.getElementById('copy-email-btn-final');
    const toast = document.getElementById('copy-toast-final');
    if(!btn) return;
    btn.addEventListener('click', function() {
      const email = this.getAttribute('data-email');
      const btnText = this.querySelector('.btn-text');
      navigator.clipboard.writeText(email).then(() => {
        const originalText = btnText.innerText;
        btnText.innerText = "SKOPIOWANO!";
        if(toast) toast.classList.add('show');
        setTimeout(() => {
          btnText.innerText = originalText;
          if(toast) toast.classList.remove('show');
        }, 2000);
      });
    });
  })();
</script>








<div class="opinions-modern-section unique-opinions-v2">
    <div class="m-bg-layers">
        <div class="m-grid-overlay"></div>
        <div class="m-central-glow"></div>
        <div class="m-grain"></div>
    </div>
    
    <div class="m-container">
        <div class="m-header">
            <div class="m-badge">#TRUST_SYSTEM // v2.0</div>
            <h2 class="m-main-title">CO MÓWIĄ<br><span class="green-text-highlight">STUDENCI?</span></h2>
        </div>

        <div class="m-slider-container">
            <div class="m-track" id="mTrackV2">
                <div class="m-slide"><div class="m-card"><div class="m-num">01</div><p class="m-text">A ja myślałem, że to jest jakieś skomplikowane... Czegoś takiego mi brakowało.</p><div class="m-user"><span class="m-name-tag">Tomasz L.</span><span class="m-role-tag">Verified Student</span></div></div></div>
                <div class="m-slide"><div class="m-card"><div class="m-num">02</div><p class="m-text">Wszystko czytelne i nowoczesne. Zupełnie co innego niż inne kursy. Żadnego lania wody.</p><div class="m-user"><span class="m-name-tag">Radek W.</span><span class="m-role-tag">Verified Student</span></div></div></div>
                <div class="m-slide"><div class="m-card"><div class="m-num">03</div><p class="m-text">Szybkie efekty, wszystko krok po kroku i wiele przydatnych informacji- tego szukałem.</p><div class="m-user"><span class="m-name-tag">Piotr K.</span><span class="m-role-tag">Verified Student</span></div></div></div>
                <div class="m-slide"><div class="m-card"><div class="m-num">04</div><p class="m-text">Instrukcje są tak proste, że nawet dziecko sobie poradzi. Mega!</p><div class="m-user"><span class="m-name-tag">Kacper S.</span><span class="m-role-tag">Verified Student</span></div></div></div>
                <div class="m-slide"><div class="m-card"><div class="m-num">05</div><p class="m-text">Oszczędziłem mnóstwo czasu na szukaniu rozwiązań w sieci.</p><div class="m-user"><span class="m-name-tag">Robert B.</span><span class="m-role-tag">Verified Student</span></div></div></div>
                <div class="m-slide"><div class="m-card"><div class="m-num">06</div><p class="m-text">Kursify to nowa jakość na polskim rynku e-learningu.</p><div class="m-user"><span class="m-name-tag">Łukasz M.</span><span class="m-role-tag">Verified Student</span></div></div></div>
                <div class="m-slide"><div class="m-card"><div class="m-num">07</div><p class="m-text">Profesjonalne podejście i świetny kontakt z autorem.</p><div class="m-user"><span class="m-name-tag">Karol J.</span><span class="m-role-tag">Verified Student</span></div></div></div>
                <div class="m-slide"><div class="m-card"><div class="m-num">08</div><p class="m-text">Wdrożyłem wszystko w 2 dni, zabieram się za reklamy!</p><div class="m-user"><span class="m-name-tag">Adrian W.</span><span class="m-role-tag">Verified Student</span></div></div></div>
                <div class="m-slide"><div class="m-card"><div class="m-num">09</div><p class="m-text">Bardzo estetyczne wydanie i najważniejsza wiedza w pigułce.</p><div class="m-user"><span class="m-name-tag">Dominik G.</span><span class="m-role-tag">Verified Student</span></div></div></div>
                <div class="m-slide"><div class="m-card"><div class="m-num">10</div><p class="m-text">Podoba mi się innowacyjne podejście i brak wciskania kitu.</p><div class="m-user"><span class="m-name-tag">Olek P.</span><span class="m-role-tag">Verified Student</span></div></div></div>
            </div>
        </div>

        <div class="m-footer-nav">
            <div class="m-progress-bar-bg">
                <div class="m-progress-fill" id="mFillV2"></div>
            </div>
            <div class="m-controls">
                <span id="mCurrV2">01</span>
                <span class="m-sep-v2">/</span>
                <span class="m-total-v2">10</span>
            </div>
        </div>
    </div>
</div>

<style>
    .unique-opinions-v2 {
        --accent-green: #2ecc71;
        --bg-deep-black: #050505;
        background: var(--bg-deep-black) !important;
        color: #fff;
        padding: 120px 0;
        font-family: 'Plus Jakarta Sans', sans-serif;
        position: relative;
        overflow: hidden;
    }

    .unique-opinions-v2 .m-bg-layers { position: absolute; inset: 0; pointer-events: none; z-index: 1; }
    
    .unique-opinions-v2 .m-grid-overlay { 
        position: absolute; inset: 0; 
        background-image: linear-gradient(rgba(46, 204, 113, 0.15) 1px, transparent 1px), 
                          linear-gradient(90deg, rgba(46, 204, 113, 0.15) 1px, transparent 1px);
        background-size: 50px 50px;
        
        /* MOCNA WINIETA: Łączymy gradient liniowy (góra-dół) z radialnym (boki) */
        -webkit-mask-image: 
            linear-gradient(to bottom, transparent 5%, black 40%, black 60%, transparent 95%),
            radial-gradient(circle at center, black 0%, transparent 75%);
        mask-image: 
            linear-gradient(to bottom, transparent 5%, black 40%, black 60%, transparent 95%),
            radial-gradient(circle at center, black 0%, transparent 75%);
        -webkit-mask-composite: source-in;
        mask-composite: intersect;
    }

    .unique-opinions-v2 .m-central-glow { 
        position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%);
        width: 600px; height: 600px; 
        background: radial-gradient(circle, rgba(46, 204, 113, 0.12) 0%, transparent 70%);
        filter: blur(120px); z-index: 1; opacity: 0.6;
    }

    .unique-opinions-v2 .m-grain { 
        position: absolute; inset: 0; 
        background-image: url('https://grainy-gradients.vercel.app/noise.svg'); 
        opacity: 0.02; z-index: 2; 
    }

    .unique-opinions-v2 .m-container { max-width: 1100px; margin: 0 auto; padding: 0 25px; position: relative; z-index: 10; }

    .unique-opinions-v2 .m-badge { 
        font-family: 'JetBrains Mono', monospace; font-size: 11px; font-weight: 800; letter-spacing: 2px; color: var(--accent-green);
        background: rgba(46, 204, 113, 0.05); padding: 8px 16px; border-radius: 4px; display: inline-block; margin-bottom: 20px;
        border: 1px solid rgba(46, 204, 113, 0.2);
    }

    .unique-opinions-v2 .m-main-title { 
        font-family: 'Unbounded', sans-serif !important; 
        font-size: clamp(38px, 7vw, 85px); 
        font-weight: 900; line-height: 1; margin: 0 0 40px 0; 
        letter-spacing: -2px; text-transform: uppercase; color: #ffffff;
    }
    .unique-opinions-v2 .green-text-highlight { color: var(--accent-green); }

    .unique-opinions-v2 .m-slider-container { position: relative; overflow: hidden; }
    .unique-opinions-v2 .m-track { 
        display: flex; will-change: transform;
        transition: transform 0.6s cubic-bezier(0.16, 1, 0.3, 1); 
    }
    .unique-opinions-v2 .m-slide { flex: 0 0 100%; }

    .unique-opinions-v2 .m-card { 
        background: #0a0a0a; border: 1px solid rgba(255, 255, 255, 0.08);
        padding: 50px; border-radius: 30px; position: relative; margin: 10px;
    }
    
    .unique-opinions-v2 .m-num { 
        position: absolute; top: 30px; right: 40px; font-family: 'JetBrains Mono', monospace;
        font-size: 50px; font-weight: 800; opacity: 0.05; color: var(--accent-green);
    }
    .unique-opinions-v2 .m-text { font-size: clamp(17px, 3.5vw, 28px); font-weight: 700; line-height: 1.3; margin-bottom: 40px; color: #fff; }
    
    .unique-opinions-v2 .m-user { display: flex; align-items: center; gap: 15px; }
    .unique-opinions-v2 .m-name-tag { font-size: 20px; font-weight: 800; color: #fff; }
    .unique-opinions-v2 .m-role-tag { font-family: 'JetBrains Mono', monospace; font-size: 11px; color: var(--accent-green); text-transform: uppercase; border-left: 2px solid var(--accent-green); padding-left: 10px; }

    .unique-opinions-v2 .m-footer-nav { margin-top: 40px; display: flex; justify-content: space-between; align-items: center; }
    .unique-opinions-v2 .m-progress-bar-bg { flex-grow: 1; height: 2px; background: rgba(255,255,255,0.05); margin-right: 30px; position: relative; }
    .unique-opinions-v2 .m-progress-fill { position: absolute; left: 0; top: 0; height: 100%; background: var(--accent-green); width: 0%; }
    
    .unique-opinions-v2 .m-controls { font-family: 'JetBrains Mono', monospace; font-size: 20px; font-weight: 800; color: #fff; }

    @media (max-width: 768px) {
        .unique-opinions-v2 { padding: 60px 0 20px 0; }
        .unique-opinions-v2 .m-card { padding: 35px 20px; border-radius: 20px; }
    }
</style>

<script>
    (function() {
        const track = document.getElementById('mTrackV2');
        const fill = document.getElementById('mFillV2');
        const currTxt = document.getElementById('mCurrV2');
        const slides = document.querySelectorAll('.unique-opinions-v2 .m-slide');
        let index = 0;
        const total = slides.length;
        const intervalTime = 5000;

        function slide() {
            if(!track) return;
            track.style.transform = `translate3d(-${index * 100}%, 0, 0)`;
            if(currTxt) currTxt.innerText = (index + 1).toString().padStart(2, '0');
            
            if(fill) {
                fill.style.transition = 'none';
                fill.style.width = '0%';
                void fill.offsetWidth; 
                fill.style.transition = `width ${intervalTime}ms linear`;
                fill.style.width = '100%';
            }
            index = (index + 1) % total;
        }

        slide();
        setInterval(slide, intervalTime);
    })();
</script>





<div class="quote-focus-section">
    <div class="q-bg-layers">
        <div class="q-grid"></div>
        <div class="q-glow"></div>
        <div class="q-grain"></div>
    </div>

    <div class="sq-wrapper">
        <div class="sq-content">
            <blockquote class="sq-quote">
                <span class="sq-mark">"</span>
                <p class="sq-line-1">Czekanie to nie</p>
                <p class="sq-line-2 green-highlight">Prokrastynacja...</p>
                <p class="sq-line-3">To robienie czegoś niebezpieczniejszego</p>
                <span class="sq-mark">"</span>
            </blockquote>
            <div class="sq-author">
                <cite>MEL ROBBINS</cite>
            </div>
        </div>
    </div>
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@900&family=Inter:wght@200;400;700&family=JetBrains+Mono:wght@700&display=swap');

    .quote-focus-section {
        --p: #2ecc71;
        --bg: #050505;
        background: var(--bg) !important;
        color: #fff;
        /* GÓRA: 40px (mało), DÓŁ: 140px (dużo) */
        padding: 40px 0 140px 0; 
        position: relative;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .q-bg-layers { position: absolute; inset: 0; pointer-events: none; }
    
    .q-grid { 
        position: absolute; inset: 0; 
        background-image: linear-gradient(rgba(46, 204, 113, 0.08) 1px, transparent 1px), 
                          linear-gradient(90deg, rgba(46, 204, 113, 0.08) 1px, transparent 1px);
        background-size: 50px 50px;
        -webkit-mask-image: radial-gradient(ellipse at center, black 0%, transparent 80%);
        mask-image: radial-gradient(ellipse at center, black 0%, transparent 80%);
    }

    .q-glow {
        position: absolute; top: 40%; left: 50%; transform: translate(-50%, -50%);
        width: 700px; height: 400px; 
        background: radial-gradient(circle, rgba(46, 204, 113, 0.08) 0%, transparent 70%);
        filter: blur(100px);
        opacity: 0.6;
    }

    .q-grain {
        position: absolute; inset: 0;
        background-image: url('https://grainy-gradients.vercel.app/noise.svg');
        opacity: 0.02; z-index: 5;
    }

    .sq-wrapper { 
        max-width: 1000px; 
        width: 90%; 
        position: relative; 
        z-index: 10; 
    }
    
    .sq-content { 
        text-align: center; 
        position: relative; 
    }

    .sq-mark { 
        display: block; 
        font-family: 'JetBrains Mono', monospace; 
        color: var(--p); 
        font-size: clamp(30px, 5vw, 45px); 
        opacity: 0.4; 
        margin: 0;
    }
    
    .sq-line-1 { 
        font-family: 'Big Shoulders Display', sans-serif !important; 
        font-size: clamp(35px, 7vw, 75px); 
        text-transform: uppercase; 
        margin: 0; 
        line-height: 1; 
        letter-spacing: -1px;
    }

    .sq-line-2 { 
        font-family: 'Big Shoulders Display', sans-serif !important; 
        font-size: clamp(45px, 10vw, 110px); 
        text-transform: uppercase; 
        margin: 5px 0; 
        line-height: 0.85; 
        letter-spacing: -4px;
    }
    
    .green-highlight { 
        color: var(--p); 
        text-shadow: 0 0 45px rgba(46, 204, 113, 0.4); 
    }
    
    .sq-line-3 { 
        font-family: 'Inter', sans-serif !important; 
        font-size: clamp(10px, 1.5vw, 18px); 
        font-weight: 200; 
        letter-spacing: 5px; 
        text-transform: uppercase; 
        color: rgba(255,255,255,0.6); 
        margin-top: 20px;
        display: block;
    }

    .sq-author { 
        margin-top: 40px; 
        text-align: center; 
    }

    .sq-author cite { 
        font-family: 'JetBrains Mono', monospace !important; 
        font-size: 13px; 
        letter-spacing: 5px; 
        color: var(--p); 
        font-style: normal; 
        font-weight: 700; 
        text-transform: uppercase; 
    }

    @media (min-width: 992px) {
        .sq-author { 
            position: absolute; 
            right: 0; 
            bottom: -30px; 
            text-align: right; 
            margin-top: 0; 
        }
    }

    @media (max-width: 768px) {
        .quote-focus-section { padding: 30px 0 100px 0; }
    }
</style>





<div class="refined-aura-divider v2-black-edition"></div>

<style>
  /* Celujemy precyzyjnie w ten jeden konkretny separator */
  .refined-aura-divider.v2-black-edition {
    width: 100%;
    height: 1px; 
    background: #000000 !important; /* Przywrócony czysty czarny */
    position: relative;
    z-index: 100;
    margin: -10px 0; 
    
    /* Aura w kolorze czystej czerni */
    box-shadow: 0 0 30px 15px #000000 !important;
    
    pointer-events: none;
    display: block;
  }

  @media (max-width: 768px) {
    .refined-aura-divider.v2-black-edition {
      box-shadow: 0 0 20px 10px #000000 !important;
      margin: -5px 0;
    }
  }
</style>





<style>
    @import url('https://fonts.googleapis.com/css2?family=Syncopate:wght@400;700&family=Inter:wght@400;900&display=swap');

    /* Kontener sekcji z wymuszonym czarnym tłem */
    .footer-kursify-brand {
        background-color: #000000 !important; /* Sztywny czarny kolor */
        width: 100%;
        padding: 60px 0; 
        display: flex;
        justify-content: center;
        align-items: center;
        overflow: hidden;
        margin: 0; /* Usuwa ewentualne marginesy z motywu Shopify */
    }

    .brand-wrapper-footer {
        text-align: center;
        opacity: 0;
        transform: translateY(20px);
        filter: blur(10px);
        transition: all 1s cubic-bezier(0.22, 1, 0.36, 1);
    }

    /* Aktywacja animacji po zjechaniu do stopki */
    .footer-kursify-brand.is-visible .brand-wrapper-footer {
        opacity: 1;
        transform: translateY(0);
        filter: blur(0);
    }

    .logo-footer-main {
        font-family: 'Syncopate', sans-serif !important;
        font-weight: 700;
        font-size: clamp(28px, 6vw, 55px);
        color: #ffffff;
        letter-spacing: 0.25em;
        margin: 0;
        text-transform: uppercase;
        text-shadow: 0 0 15px rgba(255, 255, 255, 0.2);
    }

    .logo-footer-sub {
        font-family: 'Inter', sans-serif !important;
        font-weight: 400;
        font-size: 11px;
        color: #4af626; /* Twój zielony neon */
        letter-spacing: 1em;
        margin-top: 12px;
        text-transform: uppercase;
        display: block;
        text-indent: 1em;
        opacity: 0.9;
    }

    /* Neonowa linia pod logotypem */
    .brand-wrapper-footer::after {
        content: '';
        display: block;
        width: 0;
        height: 2px;
        background: #4af626;
        margin: 20px auto 0;
        box-shadow: 0 0 15px rgba(74, 246, 38, 0.7);
        transition: width 1s ease-out 0.6s;
    }

    .footer-kursify-brand.is-visible .brand-wrapper-footer::after {
        width: 50px;
    }
</style>

<div class="footer-kursify-brand" id="footer-trigger">
    <div class="brand-wrapper-footer">
        <h2 class="logo-footer-main">KURSIFY</h2>
        <span class="logo-footer-sub">Est 2025</span>
    </div>
</div>

<script>
    (function() {
        // Skrypt sprawdza, kiedy stopka pojawi się na ekranie
        const observerOptions = { threshold: 0.15 };
        const footerObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('is-visible');
                    // Odkomentuj poniższą linię, aby animacja wykonała się tylko raz
                    // footerObserver.unobserve(entry.target);
                }
            });
        }, observerOptions);

        const target = document.querySelector('#footer-trigger');
        if (target) footerObserver.observe(target);
    })();
</script>

