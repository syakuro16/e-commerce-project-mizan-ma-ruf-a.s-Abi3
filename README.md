# e-commerce-project-mizan-ma-ruf-a.s-Abi3
web
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1" />
  <title>Kedai Pisang Keju</title>
  <style>
    :root {
      --color-bg: #ffffff;
      --color-primary: #000000;
      --color-accent: #EF4444;
      --color-muted: #6b7280;
      --color-yellow: #F6EB61;
      --card-radius: 0.75rem;
      --max-width: 1200px;
      --font-heading: 'Poppins', Arial, sans-serif;
      --font-body: 'Inter', Arial, sans-serif;
    }

    /* Reset */
    *, *::before, *::after {
      box-sizing: border-box;
    }

    html, body {
      margin: 0;
      padding: 0;
      background: var(--color-bg);
      font-family: var(--font-body);
      color: var(--color-primary);
      min-height: 100vh;
      scroll-behavior: smooth;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      font-size: 16px; /* base font size for scaling */
      line-height: 1.5;
    }
    a {
      color: inherit;
      text-decoration: none;
      transition: color 0.3s ease;
    }
    a:hover, a:focus {
      color: var(--color-accent);
      outline: none;
    }
    .container {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 0 1.5rem;
      flex-shrink: 0;
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }
    nav[role="navigation"] {
      position: sticky;
      top: 0;
      background: var(--color-bg);
      border-bottom: 1px solid #e5e7eb;
      display: flex;
      justify-content: flex-start;
      align-items: center;
      padding: 1rem 1.5rem;
      user-select: none;
      z-index: 30;
      gap: 2rem;
      flex-wrap: wrap;
    }
    nav ul {
      list-style: none;
      display: flex;
      gap: 2rem;
      margin: 0;
      padding: 0;
      flex-wrap: wrap;
      flex-grow: 1;
      min-width: 200px;
    }
    nav ul li a {
      font-weight: 700;
      font-size: 1rem;
      color: var(--color-primary);
      padding: 0.25rem 0.5rem;
      border-radius: var(--card-radius);
      user-select: none;
      transition: background-color 0.3s ease, color 0.3s ease;
      cursor: pointer;
      display: inline-block;
      white-space: nowrap;
    }
    nav ul li a:hover,
    nav ul li a:focus,
    nav ul li a.active {
      background-color: var(--color-accent);
      color: var(--color-bg);
      outline: none;
    }
    .nav-cart {
      margin-left: auto;
      display: flex;
      align-items: center;
      gap: 0.75rem;
      user-select: none;
      flex-shrink: 0;
    }
    .cart-icon {
      font-size: 1.75rem;
      cursor: pointer;
      color: var(--color-primary);
      transition: color 0.3s ease;
      user-select: none;
      line-height: 1;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .cart-icon:hover,
    .cart-icon:focus {
      color: var(--color-accent);
      outline: none;
    }
    .cart-total {
      font-weight: 700;
      font-size: 1.125rem;
      color: var(--color-primary);
      user-select: none;
      white-space: nowrap;
    }

    header[role="banner"] {
      padding: 4rem 0 3rem 0;
      text-align: center;
      user-select: none;
      background-color: transparent;
      flex-shrink: 0;
    }
    header h1 {
      margin: 0 auto;
      display: inline-block;
      font-family: var(--font-heading);
      font-weight: 800;
      font-size: 3rem;
      line-height: 1.2;
      color: var(--color-primary);
      letter-spacing: -0.02em;
      padding: 0.5rem 2rem;
      border-radius: var(--card-radius);
      user-select: text;
      box-shadow: none;
    }

    /* Hero Section */
    #hero {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 100%;
      max-width: var(--max-width);
      height: 450px;
      margin: 0 auto 3rem auto;
      position: relative;
      border-radius: var(--card-radius);
      overflow: hidden;
      box-shadow: 0 12px 30px rgba(0,0,0,0.15);
      background-color: var(--color-accent);
      background-image: url('https://images.unsplash.com/photo-1620223627072-23d219dd490b?auto=format&fit=crop&w=1470&q=80');
      background-position: center center;
      background-repeat: no-repeat;
      background-size: cover;
      user-select: none;
      cursor: default;
      padding: 2rem;
      text-align: center;
      color: var(--color-bg);
    }
    #hero::before {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(180deg, rgba(0,0,0,0.5) 0%, rgba(0,0,0,0.3) 70%, rgba(0,0,0,0.6) 100%);
      z-index: 0;
    }
    #hero-content {
      position: relative;
      z-index: 1;
      max-width: 720px;
      width: 100%;
      margin: 0 auto;
      border-radius: var(--card-radius);
      background: rgba(255 255 255 / 0.15);
      backdrop-filter: saturate(180%) blur(20px);
      box-shadow: 0 8px 24px rgba(0,0,0,0.3);
      padding: 2rem 3rem;
    }
    #hero-content h2 {
      font-family: var(--font-heading);
      font-weight: 900;
      font-size: 3.75rem;
      margin: 0 0 0.5rem 0;
      color: #FFF;
      user-select: text;
      line-height: 1.1;
      text-shadow: 0 4px 8px rgba(0,0,0,0.6);
    }
    #hero-content p {
      font-size: 1.25rem;
      font-weight: 500;
      margin: 0 0 1.75rem 0;
      color: #fdf6af;
      user-select: text;
      text-shadow: 0 2px 4px rgba(0,0,0,0.6);
    }
    #hero-cta-btn {
      background-color: #F6EB61;
      color: #333;
      font-weight: 700;
      font-size: 1.25rem;
      padding: 0.75rem 2.5rem;
      border: none;
      border-radius: 1.5rem;
      cursor: pointer;
      box-shadow: 0 8px 20px rgba(246,235,97,0.7);
      transition: background-color 0.3s ease, box-shadow 0.3s ease;
      user-select: none;
    }
    #hero-cta-btn:hover,
    #hero-cta-btn:focus {
      background-color: #e3da50;
      box-shadow: 0 12px 28px rgba(230,218,60,0.8);
      outline: none;
    }

    main {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 0 1.5rem 5rem 1.5rem;
      flex-shrink: 0;
      display: block;
      transition: filter 0.3s ease;
    }
    main.hidden {
      display: none;
    }
    main.dimmed {
      filter: blur(4px) brightness(0.7);
      pointer-events: none;
      user-select: none;
    }

    section {
      margin-bottom: 4rem;
      user-select: none;
    }

    h2 {
      font-family: var(--font-heading);
      font-weight: 700;
      font-size: 3.5rem;
      margin-bottom: 1.75rem;
      color: var(--color-primary);
      user-select: text;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 2.5rem;
    }
    .product {
      background: var(--color-yellow);
      border-radius: var(--card-radius);
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
      padding: 1.5rem 1.75rem;
      text-align: center;
      transition: transform 0.3s cubic-bezier(0.4,0,0.2,1), box-shadow 0.3s ease;
      cursor: pointer;
      user-select: none;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1rem;
      position: relative;
    }
    .product:hover,
    .product:focus-within {
      transform: translateY(-8px);
      box-shadow: 0 16px 32px rgba(0,0,0,0.1);
      outline: none;
    }
    .product img {
      display: block;
      width: 100%;
      max-width: 120px;
      height: auto;
      border-radius: var(--card-radius);
      user-select: none;
      pointer-events: none;
      object-fit: cover;
    }
    .product h3 {
      font-weight: 800;
      font-size: 1.5rem;
      margin: 0 0 0.5rem 0;
      color: var(--color-primary);
      user-select: text;
    }
    .product p.description {
      color: var(--color-muted);
      font-size: 1.125rem;
      margin: 0 0 1rem 0;
      user-select: text;
    }
    .product p.price {
      font-weight: 700;
      font-size: 1.25rem;
      color: var(--color-accent);
      user-select: none;
      margin-bottom: 1rem;
    }
    button {
      cursor: pointer;
      background-color: var(--color-accent);
      border: none;
      border-radius: 0.5rem;
      color: white;
      font-weight: 700;
      padding: 0.5rem 1rem;
      font-size: 1rem;
      transition: background-color 0.3s ease;
      user-select: none;
      width: 100%;
      max-width: 250px;
    }
    button:hover,
    button:focus {
      background-color: #b71c1c;
      outline: none;
    }

    /* Toast for add to cart */
    #toast {
      position: fixed;
      bottom: 30px;
      left: 50%;
      transform: translateX(-50%);
      background: var(--color-accent);
      color: white;
      padding: 1rem 2rem;
      border-radius: var(--card-radius);
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.4s ease;
      font-weight: 700;
      user-select: none;
      z-index: 1050;
      max-width: 90vw;
      text-align: center;
      word-break: break-word;
    }
    #toast.show {
      opacity: 1;
      pointer-events: auto;
    }

    /* Tampilan khusus untuk keranjang */
    #cart-display {
      max-width: var(--max-width);
      margin: 2rem auto 5rem auto;
      background: var(--color-bg);
      border-radius: var(--card-radius);
      box-shadow: 0 8px 32px rgba(207, 59, 59, 0.15);
      padding: 2rem 2.5rem;
      user-select: none;
      display: none;
      flex-direction: column;
      gap: 1.25rem;
    }
    #cart-display.visible {
      display: flex;
    }
    #cart-display h2 {
      font-family: var(--font-heading);
      font-weight: 800;
      font-size: 2.5rem;
      color: var(--color-primary);
      margin: 0 0 1rem 0;
      user-select: text;
    }
    #cart-items-list {
      list-style: none;
      margin: 0;
      padding: 0;
      max-height: 300px;
      overflow-y: auto;
      display: flex;
      flex-direction: column;
      gap: 0.75rem;
    }
    #cart-items-list li {
      font-weight: 700;
      font-size: 1.125rem;
      color: var(--color-muted);
      border-bottom: 1px solid #e5e7eb;
      padding-bottom: 0.25rem;
      user-select: text;
    }
    #cart-empty-msg {
      color: var(--color-muted);
      font-style: italic;
      font-size: 1.125rem;
      text-align: center;
      user-select: none;
      margin: 1rem 0;
    }
    #cart-total-amount {
      font-weight: 800;
      font-size: 1.5rem;
      color: var(--color-accent);
      text-align: right;
      margin-top: 0.5rem;
      user-select: none;
    }
    #cart-pay-btn {
      margin-top: 1rem;
      background-color: var(--color-accent);
      border: none;
      border-radius: 0.75rem;
      color: white;
      font-weight: 700;
      font-size: 1.25rem;
      padding: 0.75rem;
      cursor: pointer;
      transition: background-color 0.3s ease;
      user-select: none;
      width: 100%;
      box-shadow: 0 6px 20px rgba(239,68,68,0.7);
      max-width: 400px;
      align-self: flex-end;
    }
    #cart-pay-btn:hover,
    #cart-pay-btn:focus {
      background-color: #b71c1c;
      outline: none;
    }

    footer {
      text-align: center;
      padding: 3rem 0;
      font-size: 1rem;
      color: var(--color-muted);
      user-select: none;
      border-top: 1px solid #e5e7eb;
      flex-shrink: 0;
    }

    /* Modal styles (unchanged) */
    .modal-overlay {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.4);
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 1000;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.3s ease;
    }
    .modal-overlay.active {
      opacity: 1;
      pointer-events: auto;
    }
    .modal-content {
      background: var(--color-bg);
      border-radius: var(--card-radius);
      box-shadow: 0 8px 24px rgba(0,0,0,0.15);
      max-width: 600px;
      width: 90%;
      max-height: 90vh;
      overflow-y: auto;
      padding: 2rem;
      display: flex;
      flex-direction: column;
      gap: 1rem;
      position: relative;
    }
    .modal-close {
      position: absolute;
      top: 1rem;
      right: 1rem;
      background: none;
      border: none;
      font-size: 1.5rem;
      cursor: pointer;
      color: var(--color-muted);
      transition: color 0.3s ease;
    }
    .modal-close:hover,
    .modal-close:focus {
      color: var(--color-accent);
      outline: none;
    }
    .modal-image {
      width: 100%;
      border-radius: var(--card-radius);
      object-fit: contain;
      user-select: none;
      pointer-events: none;
    }
    .modal-title {
      font-family: var(--font-heading);
      font-weight: 800;
      font-size: 2.5rem;
      margin: 0;
      color: var(--color-primary);
      user-select: text;
    }
    .modal-description {
      color: var(--color-muted);
      font-size: 1.125rem;
      margin: 0 0 1rem 0;
      user-select: text;
      flex-grow: 1;
    }
    .modal-price {
      font-weight: 700;
      font-size: 1.5rem;
      color: var(--color-accent);
      user-select: none;
      margin-bottom: 1rem;
    }
    .modal-actions {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1rem;
      flex-wrap: wrap;
    }
    .modal-button {
      padding: 0.5rem 1.5rem;
      background-color: var(--color-accent);
      border: none;
      border-radius: 0.5rem;
      color: white;
      font-weight: 700;
      font-size: 1rem;
      cursor: pointer;
      transition: background-color 0.3s ease;
      user-select: none;
      flex: 1 1 48%;
      min-width: 140px;
      text-align:center;
    }
    .modal-button:hover,
    .modal-button:focus {
      background-color: #b71c1c;
      outline: none;
    }

    /* Responsive */
    @media (max-width: 1024px) {
      #hero-content h2 {
        font-size: 3rem;
      }
      #hero-content p {
        font-size: 1.125rem;
      }
      h2 {
        font-size: 2.75rem;
      }
      #cart-pay-btn {
        max-width: 100%;
      }
    }
    @media (max-width: 768px) {
      header[role="banner"] h1 {
        font-size: 2.25rem;
        padding: 0.4rem 1.5rem;
      }
      nav ul {
        gap: 1.5rem;
        justify-content: center;
      }
      h2 {
        font-size: 2.5rem;
      }
      .products {
        grid-template-columns: 1fr;
        gap: 1.5rem;
      }
      .modal-content {
        max-width: 95%;
        padding: 1.5rem;
      }
      .modal-title {
        font-size: 2rem;
      }
      #hero {
        height: 300px;
        padding: 1.5rem 1.5rem;
      }
      #hero-content h2 {
        font-size: 2.5rem;
      }
      #hero-content p {
        font-size: 1rem;
      }
      #hero-cta-btn {
        font-size: 1rem;
        padding: 0.6rem 2rem;
      }
    }
    @media (max-width: 480px) {
      nav[role="navigation"] {
        justify-content: center;
        gap: 0.5rem;
      }
      nav ul {
        justify-content: center;
        flex-wrap: wrap;
        gap: 1rem;
        width: 100%;
        order: 1;
        margin-bottom: 0.5rem;
      }
      .nav-cart {
        order: 2;
        width: 100%;
        justify-content: center;
        margin-bottom: 1rem;
      }
      header[role="banner"] {
        padding: 2.5rem 1rem 3rem 1rem;
      }
      header h1 {
        font-size: 1.75rem;
      }
      #cart-display {
        margin: 1rem 1rem 3rem 1rem;
        padding: 1.5rem 2rem;
      }
      .products {
        grid-template-columns: 1fr;
        gap: 1.25rem;
      }
      .modal-actions {
        flex-direction: column;
      }
      .modal-button {
        flex: 1 1 100%;
      }
      #hero {
        height: 250px;
        padding: 1rem 1rem;
      }
      #hero-content {
        padding: 1rem 1.5rem;
      }
      #hero-content h2 {
        font-size: 1.75rem;
      }
      #hero-content p {
        font-size: 0.9rem;
      }
      #hero-cta-btn {
        font-size: 0.9rem;
        padding: 0.5rem 1.5rem;
      }
      .product:hover,
      .product:focus-within {
        transform: none;
        box-shadow: 0 4px 12px rgba(0,0,0,0.05);
      }
      .product img {
        max-width: 100px;
        height: auto;
      }
      button {
        font-size: 0.9rem;
        max-width: 100%;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <nav role="navigation" aria-label="Menu utama">
      <ul>
        <li><a href="#" id="nav-beranda" tabindex="0" class="active">Beranda</a></li>
        <li><a href="#" id="nav-produk" tabindex="0">Produk</a></li>
        <li><a href="#" id="nav-keranjang" tabindex="0">Buat Pesanan</a></li>
        <li><a href="#" id="nav-kontak" tabindex="0">Kontak</a></li>
      </ul>
      <div class="nav-cart" aria-label="Keranjang belanja" aria-live="polite" aria-atomic="true">
        <div class="cart-icon" role="button" tabindex="0" aria-label="Buka keranjang belanja">🛒</div>
        <span class="cart-total" id="cart-total">Total: Rp 0</span>
      </div>
    </nav>

    <header role="banner" aria-label="Judul Kedai Pisang Keju Bananagih">
      <h1>Kedai Pisang Keju Bananagih</h1>
    </header>

    <!-- Hero Section -->
    <section id="hero" role="img" aria-label="Gambar promosi pisang keju">
      <div id="hero-content">
        <h2>Selamat Datang di Kedai Pisang Keju</h2>
        <p>Rasakan kenikmatan pisang keju terbaik dengan keju premium dan cita rasa khas yang memanjakan lidah Anda.</p>
        <button id="hero-cta-btn" aria-label="Lihat Produk">Lihat Produk</button>
      </div>
    </section>

    <!-- Main Content -->
    <main id="main-content" class="">
      <section id="produk-terbaru" aria-labelledby="produk-terbaru-title">
        <h2 id="produk-terbaru-title">Produk Terbaru</h2>
        <div class="products" id="products-grid">
          <article class="product" tabindex="0" role="group" aria-label="Pisang Keju, harga sepuluh ribu rupiah" data-index="0">
            <img src="/Users/user/Downloads/WhatsApp Image 2025-04-20 at 19.45.03.jpeg" alt="Pisang Keju Original" loading="lazy" />
            <h3>Pisang Keju</h3>
            <p class="description">Lezat dan gurih dengan keju premium.</p>
            <p class="price">Rp 10.000</p>
            <button class="btn-add-cart" data-price="10000">Tambah ke Keranjang</button>
          </article>
          <article class="product" tabindex="0" role="group" aria-label="Pisang Coklat, harga sepuluh ribu rupiah" data-index="1">
            <img src="/Users/user/Downloads/WhatsApp Image 2025-04-20 at 19.45.04 (1).jpeg" alt="Pisang Coklat" loading="lazy" />
            <h3>Pisang Coklat</h3>
            <p class="description">Manis dengan taburan coklat.</p>
            <p class="price">Rp 10.000</p>
            <button class="btn-add-cart" data-price="10000">Tambah ke Keranjang</button>
          </article>
          <article class="product" tabindex="0" role="group" aria-label="Pisang Keju Coklat, harga sepuluh ribu rupiah" data-index="2">
            <img src="/Users/user/Downloads/WhatsApp Image 2025-04-20 at 19.45.03 (1).jpeg" alt="Pisang Keju Coklat" loading="lazy" />
            <h3>Pisang Keju Coklat</h3>
            <p class="description">Rasa kombinasi keju dan coklat yang menggoda.</p>
            <p class="price">Rp 10.000</p>
            <button class="btn-add-cart" data-price="10000">Tambah ke Keranjang</button>
          </article>
          <article class="product" tabindex="0" role="group" aria-label="Spesial Topping Double Keju, harga lima belas ribu rupiah" data-index="3">
            <img src="/Users/user/Documents/WhatsApp Image 2025-04-20 at 19.45.04 (2).jpeg" alt="Spesial Topping Double Keju" loading="lazy" />
            <h3>Spesial Topping Double Keju</h3>
            <p class="description">Pisang dan kejunya lebih banyak bikin nagih.</p>
            <p class="price">Rp 15.000</p>
            <button class="btn-add-cart" data-price="15000">Tambah ke Keranjang</button>
          </article>
          <article class="product" tabindex="0" role="group" aria-label="Spesial Topping Pisang Keju Coklat, harga lima belas ribu rupiah" data-index="4">
            <img src="/Users/user/Documents/WhatsApp Image 2025-04-20 at 19.45.04 (3).jpeg" alt="Spesial Topping Pisang Keju Coklat" loading="lazy" />
            <h3>Spesial Topping Pisang Keju Coklat</h3>
            <p class="description">Campuran keju dan coklat yang lebih banyak.</p>
            <p class="price">Rp 15.000</p>
            <button class="btn-add-cart" data-price="15000">Tambah ke Keranjang</button>
          </article>
        </div>
      </section>

      <!-- Tampilan Keranjang -->
      <section id="cart-display" aria-labelledby="cart-title" role="region" aria-live="polite" aria-atomic="true">
        <h2 id="cart-title">Keranjang Anda</h2>
        <ul id="cart-items-list" aria-live="polite" aria-relevant="additions removals" aria-atomic="true"></ul>
        <div id="cart-empty-msg" hidden>Keranjang kosong</div>
        <div id="cart-total-amount" aria-label="Total belanja">Total: Rp 0</div>
        <button id="cart-pay-btn" type="button">Bayar</button>
      </section>

      <section id="kategori" aria-labelledby="kategori-title">
        <h2 id="kategori-title">Kategori</h2>
        <p>Temukan berbagai varian pisang keju favorit Anda.</p>
      </section>

      <section id="tentang-kami" aria-labelledby="tentangkami-title">
        <h2 id="tentangkami-title">Tentang Kami</h2>
        <p>Kami adalah toko yang menyediakan pisang keju berkualitas tinggi dengan berbagai rasa yang menggugah selera.</p>
      </section>

      <section id="kontak" aria-labelledby="kontak-title" style="display:none;">
        <h2 id="kontak-title">Kontak Kami</h2>
        <p>Hubungi kami di nomor WhatsApp: <strong>085171203485</strong></p>
      </section>
    </main>

    <footer>
      <p>&copy; 2025 Kedai Pisang Keju. Semua Hak Dilindungi.</p>
    </footer>
  </div>

  <!-- Toast for cart feedback -->
  <div id="toast" role="alert" aria-live="assertive" aria-atomic="true"></div>

  <!-- Modal for product preview -->
  <div class="modal-overlay" id="product-modal" role="dialog" aria-modal="true" aria-labelledby="modal-title" aria-describedby="modal-description" tabindex="-1">
    <div class="modal-content">
      <button class="modal-close" aria-label="Tutup tampilan produk">&times;</button>
      <img src="" alt="" class="modal-image" id="modal-image" />
      <h3 class="modal-title" id="modal-title"></h3>
      <p class="modal-description" id="modal-description"></p>
      <p class="modal-price" id="modal-price"></p>
      <div class="modal-actions">
        <button class="modal-button" id="prev-product" aria-label="Produk sebelumnya">Sebelumnya</button>
        <button class="modal-button" id="next-product" aria-label="Produk berikutnya">Berikutnya</button>
      </div>
    </div>
  </div>

  <script>
    let totalAmount = 0;
    let cartItems = [];

    // Elemen tampilan keranjang
    const cartDisplaySection = document.getElementById('cart-display');
    const cartItemsList = document.getElementById('cart-items-list');
    const cartTotalAmount = document.getElementById('cart-total-amount');
    const cartEmptyMsg = document.getElementById('cart-empty-msg');
    const cartPayBtn = document.getElementById('cart-pay-btn');
    const cartTotalNav = document.getElementById('cart-total');

    // Fungsi update isi dan tampilan keranjang
    function updateCartDisplay() {
      cartItemsList.innerHTML = '';
      if (cartItems.length === 0) {
        cartEmptyMsg.hidden = false;
        cartTotalAmount.textContent = 'Total: Rp 0';
        cartTotalNav.textContent = 'Total: Rp 0';
      } else {
        cartEmptyMsg.hidden = true;
        cartItems.forEach(item => {
          const li = document.createElement('li');
          li.textContent = item.quantity > 1 ? `${item.name} x${item.quantity}` : item.name;
          cartItemsList.appendChild(li);
        });
        cartTotalAmount.textContent = 'Total: Rp ' + totalAmount.toLocaleString('id-ID');
        cartTotalNav.textContent = 'Total: Rp ' + totalAmount.toLocaleString('id-ID');
      }
    }

    // Fungsi tambah produk ke keranjang
    function addToCart(price, productName) {
      const existingItem = cartItems.find(item => item.name === productName);
      if (existingItem) {
        existingItem.quantity += 1;
      } else {
        cartItems.push({ name: productName, price: price, quantity: 1 });
      }
      totalAmount += price;
      updateCartDisplay();
      showToast(`Produk "${productName}" telah ditambahkan ke keranjang.`);
    }

    // Handler tombol bayar
    cartPayBtn.addEventListener('click', () => {
      if (cartItems.length === 0) {
        alert('Keranjang kosong! Silakan tambahkan produk terlebih dahulu.');
        return;
      }
      alert(`Total pembayaran Anda: Rp ${totalAmount.toLocaleString('id-ID')}. Terima kasih sudah berbelanja!`);
      // Kosongkan keranjang setelah bayar
      cartItems = [];
      totalAmount = 0;
      updateCartDisplay();
      // Sembunyikan tampilan keranjang setelah bayar
      cartDisplaySection.classList.remove('visible');
      setActiveMenu(navBeranda);
      window.scrollTo({ top: 0, behavior: 'smooth' });
    });

    // Menu navigasi dan toggle tampilan section
    const navBeranda = document.getElementById('nav-beranda');
    const navProduk = document.getElementById('nav-produk');
    const navKeranjang = document.getElementById('nav-keranjang');
    const navKontak = document.getElementById('nav-kontak');
    const kontakSection = document.getElementById('kontak');
    const heroSection = document.getElementById('hero');
    const produkSection = document.getElementById('produk-terbaru');

    const navLinks = document.querySelectorAll('nav ul li a');

    function setActiveMenu(selectedLink) {
      navLinks.forEach(a => a.classList.remove('active'));
      selectedLink.classList.add('active');
    }

    function hideAllMainSections() {
      heroSection.style.display = 'none';
      produkSection.style.display = 'none';
      kontakSection.style.display = 'none';
      cartDisplaySection.classList.remove('visible');
    }

    navBeranda.addEventListener('click', e => {
      e.preventDefault();
      hideAllMainSections();
      heroSection.style.display = 'flex';
      setActiveMenu(navBeranda);
      window.scrollTo({ top: 0, behavior: 'smooth' });
    });

    navProduk.addEventListener('click', e => {
      e.preventDefault();
      hideAllMainSections();
      produkSection.style.display = 'block';
      setActiveMenu(navProduk);
      produkSection.scrollIntoView({ behavior: 'smooth' });
    });

    navKeranjang.addEventListener('click', e => {
      e.preventDefault();
      hideAllMainSections();
      cartDisplaySection.classList.add('visible');
      setActiveMenu(navKeranjang);
      cartDisplaySection.scrollIntoView({ behavior: 'smooth' });
    });

    navKontak.addEventListener('click', e => {
      e.preventDefault();
      hideAllMainSections();
      kontakSection.style.display = 'block';
      setActiveMenu(navKontak);
      kontakSection.scrollIntoView({ behavior: 'smooth' });
    });

    document.getElementById('hero-cta-btn').addEventListener('click', () => {
      hideAllMainSections();
      produkSection.style.display = 'block';
      setActiveMenu(navProduk);
      produkSection.scrollIntoView({ behavior: 'smooth' });
    });

    // Pasang event listener tombol tambah ke keranjang
    document.querySelectorAll('.btn-add-cart').forEach(btn => {
      btn.addEventListener('click', e => {
        e.stopPropagation();
        const price = Number(btn.getAttribute('data-price'));
        const productCard = btn.closest('.product');
        const productName = productCard.querySelector('h3').textContent;
        addToCart(price, productName);
      });
    });

    // Toast notifikasi saat tambah produk ke keranjang
    function showToast(message) {
      const toast = document.getElementById('toast');
      toast.textContent = message;
      toast.classList.add('show');
      clearTimeout(toast.timeoutId);
      toast.timeoutId = setTimeout(() => {
        toast.classList.remove('show');
      }, 2500);
    }

    // Modal produk preview (tidak diubah)
    const modal = document.getElementById('product-modal');
    const modalImage = document.getElementById('modal-image');
    const modalTitle = document.getElementById('modal-title');
    const modalDescription = document.getElementById('modal-description');
    const modalPrice = document.getElementById('modal-price');
    const btnClose = modal.querySelector('.modal-close');
    const btnPrev = document.getElementById('prev-product');
    const btnNext = document.getElementById('next-product');
    const products = [
      {
        title: "Pisang Keju",
        description: "Lezat dan gurih dengan keju premium.",
        price: "Rp 10.000",
        img: "/Users/user/Downloads/WhatsApp Image 2025-04-20 at 19.45.03.jpeg"
      },
      {
        title: "Pisang Coklat",
        description: "Manis dengan taburan coklat.",
        price: "Rp 10.000",
        img: "/Users/user/Downloads/WhatsApp Image 2025-04-20 at 19.45.04 (1).jpeg"
      },
      {
        title: "Pisang Keju Coklat",
        description: "Rasa kombinasi keju dan coklat yang menggoda.",
        price: "Rp 10.000",
        img: "/Users/user/Downloads/WhatsApp Image 2025-04-20 at 19.45.03 (1).jpeg"
      },
      {
        title: "Spesial Topping Double Keju",
        description: "Pisang dan kejunya lebih banyak bikin nagih.",
        price: "Rp 15.000",
        img: "/Users/user/Documents/WhatsApp Image 2025-04-20 at 19.45.04 (2).jpeg"
      },
      {
        title: "Spesial Topping Pisang Keju Coklat",
        description: "Campuran keju dan coklat yang lebih banyak.",
        price: "Rp 15.000",
        img: "/Users/user/Documents/WhatsApp Image 2025-04-20 at 19.45.04 (3).jpeg"
      }
    ];

    let currentProductIndex = 0;

    function openModal(index) {
      currentProductIndex = index;
      updateModalContent();
      modal.classList.add('active');
      modal.focus();
    }
    function updateModalContent() {
      const product = products[currentProductIndex];
      modalImage.src = product.img;
      modalImage.alt = product.title;
      modalTitle.textContent = product.title;
      modalDescription.textContent = product.description;
      modalPrice.textContent = product.price;
      btnPrev.disabled = currentProductIndex === 0;
      btnNext.disabled = currentProductIndex === products.length - 1;
    }
    function closeModal() {
      modal.classList.remove('active');
    }
    btnPrev.addEventListener('click', () => {
      if (currentProductIndex > 0) {
        currentProductIndex--;
        updateModalContent();
      }
    });
    btnNext.addEventListener('click', () => {
      if (currentProductIndex < products.length - 1) {
        currentProductIndex++;
        updateModalContent();
      }
    });
    btnClose.addEventListener('click', closeModal);
    document.addEventListener('keydown', (e) => {
      if (e.key === 'Escape' && modal.classList.contains('active')) {
        closeModal();
      }
    });
    modal.addEventListener('click', (e) => {
      if (e.target === modal) {
        closeModal();
      }
    });

  </script>
</body>
</html>

