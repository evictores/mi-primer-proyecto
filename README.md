<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Plata Pura — Joyas de plata 925</title>

  <style>
    /* --- Estilos básicos --- */
    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: Georgia, serif;
      background: #fafafa;
      color: #222;
      line-height: 1.6;
    }

    /* --- Cabecera --- */
    header {
      background: #fff;
      border-bottom: 1px solid #e5e5e5;
      padding: 16px 24px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
    }

    .logo {
      font-size: 1.4rem;
      letter-spacing: 2px;
      color: #555;
    }

    .cart {
      background: #333;
      color: #fff;
      border: none;
      padding: 8px 18px;
      border-radius: 30px;
      cursor: pointer;
      font-family: inherit;
      font-size: 0.9rem;
    }

    /* --- Portada --- */
    .hero {
      text-align: center;
      padding: 80px 24px;
      background: linear-gradient(135deg, #f0f0f0, #ffffff);
    }

    .hero h1 {
      font-size: 2.4rem;
      margin-bottom: 12px;
    }

    .hero p {
      color: #777;
      max-width: 500px;
      margin: 0 auto;
    }

    /* --- Catálogo --- */
    .catalog {
      max-width: 1000px;
      margin: 0 auto;
      padding: 60px 24px;
    }

    .catalog h2 {
      font-size: 1.6rem;
      margin-bottom: 30px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 24px;
    }

    /* --- Tarjeta de producto --- */
    .card {
      background: #fff;
      border: 1px solid #eee;
      border-radius: 12px;
      padding: 24px;
      text-align: center;
      transition: transform 0.2s;
    }

    .card:hover {
      transform: translateY(-4px);
      box-shadow: 0 10px 20px rgba(0,0,0,0.06);
    }

    .card .icon {
      font-size: 3rem;
      margin-bottom: 12px;
    }

    .card h3 {
      font-size: 1.1rem;
      margin-bottom: 6px;
    }

    .card .price {
      color: #888;
      margin-bottom: 16px;
    }

    .card button {
      background: #fff;
      border: 1px solid #333;
      color: #333;
      padding: 8px 22px;
      border-radius: 30px;
      cursor: pointer;
      font-family: inherit;
      transition: all 0.2s;
    }

    .card button:hover {
      background: #333;
      color: #fff;
    }

    /* --- Pie de página --- */
    footer {
      background: #222;
      color: #bbb;
      text-align: center;
      padding: 30px 24px;
      font-size: 0.9rem;
    }
  </style>
</head>
<body>

  <!-- CABECERA: logo y contador del carrito -->
  <header>
    <div class="logo">PLATA PURA</div>
    <button class="cart" onclick="verCarrito()">
      🛒 Carrito: <span id="contador">0</span>
    </button>
  </header>

  <!-- PORTADA -->
  <section class="hero">
    <h1>Joyas de plata 925</h1>
    <p>Piezas sencillas hechas a mano. Diseños que duran toda la vida.</p>
  </section>

  <!-- CATÁLOGO: cada producto es un <article> -->
  <section class="catalog">
    <h2>Colección</h2>
    <div class="grid">

      <article class="card">
        <div class="icon">💍</div>
        <h3>Anillo Luna</h3>
        <p class="price">29 €</p>
        <button onclick="añadir('Anillo Luna')">Añadir</button>
      </article>

      <article class="card">
        <div class="icon">📿</div>
        <h3>Collar Perla</h3>
        <p class="price">45 €</p>
        <button onclick="añadir('Collar Perla')">Añadir</button>
      </article>

      <article class="card">
        <div class="icon">💧</div>
        <h3>Pendientes Gota</h3>
        <p class="price">32 €</p>
        <button onclick="añadir('Pendientes Gota')">Añadir</button>
      </article>

      <article class="card">
        <div class="icon">🔗</div>
        <h3>Pulsera Cadena</h3>
        <p class="price">38 €</p>
        <button onclick="añadir('Pulsera Cadena')">Añadir</button>
      </article>

    </div>
  </section>

  <!-- PIE DE PÁGINA -->
  <footer>
    © 2025 Plata Pura · Joyas de plata 925 hechas con cariño
  </footer>

  <!-- JAVASCRIPT mínimo -->
  <script>
    
    let total = 0;

    
    function añadir(nombre) {
      total++;
      document.getElementById('contador').textContent = total;
      alert('✓ ' + nombre + ' añadido al carrito');
    }

    
    function verCarrito() {
      if (total === 0) {
        alert('Tu carrito está vacío. ¡Añade alguna joya!');
      } else {
        alert('Tienes ' + total + ' joya(s) en el carrito.');
      }
    }
  </script>

</body>
</html>
