<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Nurk's - Ropa Creativa</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Montserrat', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f9f9f9;
      color: #333;
    }
    header, footer {
      background-color: #2c3e50;
      color: white;
      padding: 1em;
      text-align: center;
    }
    nav a {
      margin: 0 15px;
      color: #ecf0f1;
      text-decoration: none;
      font-weight: bold;
    }
    nav a:hover {
      text-decoration: underline;
    }
    section {
      padding: 2em;
    }
    .productos {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2em;
    }
    .producto {
      background-color: white;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      padding: 1em;
      text-align: center;
      transition: transform 0.3s;
    }
    .producto:hover {
      transform: translateY(-5px);
    }
    .producto img {
      max-width: 100%;
      height: auto;
      border-radius: 8px;
    }
    h2, h3 {
      color: #2c3e50;
    }
    form {
      max-width: 400px;
      margin: auto;
      display: flex;
      flex-direction: column;
      gap: 1em;
    }
    input, textarea {
      padding: 0.8em;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    button {
      padding: 0.8em;
      background-color: #2c3e50;
      color: white;
      border: none;
      cursor: pointer;
      border-radius: 5px;
      transition: background-color 0.3s;
    }
    button:hover {
      background-color: #34495e;
    }
    #carrito {
      padding: 1em;
      border-top: 2px solid #ccc;
      margin-top: 2em;
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.05);
    }
    #carrito ul {
      list-style: none;
      padding: 0;
    }
    #carrito li {
      margin: 5px 0;
    }
  </style>
</head>
<body>
  <header>
    <h1>Nurk's</h1>
    <nav>
      <a href="#inicio">Inicio</a>
      <a href="#catalogo">Catálogo</a>
      <a href="#nosotros">Sobre Nosotros</a>
      <a href="#contacto">Contacto</a>
    </nav>
  </header>

  <section id="inicio">
    <h2>Bienvenido a Nurk's</h2>
    <p>Moda hecha con pasión y bordados personalizados para gente con estilo propio.</p>
  </section>

  <section id="catalogo">
    <h2>Catálogo</h2>
    <!-- Productos omitidos por brevedad, no se modifican -->
    [Contenido de productos aquí]
  </section>

  <section id="carrito">
    <h2>Carrito de Compras</h2>
    <ul id="lista-carrito"></ul>
    <p><strong>Total:</strong> <span id="total">0</span> €</p>
    <button onclick="pagarConPayPal()">Pagar con PayPal</button>
  </section>

  <section id="nosotros">
    <h2>Sobre Nosotros</h2>
    <p>Nurk's nace de la pasión por el diseño y el bordado. Cada prenda está hecha a mano con materiales de calidad.</p>
  </section>

  <section id="contacto">
    <h2>Contacto</h2>
    <form>
      <input type="text" placeholder="Tu nombre" required>
      <input type="email" placeholder="Tu email" required>
      <textarea placeholder="Escribe tu mensaje" rows="5" required></textarea>
      <button type="submit">Enviar</button>
    </form>
  </section>

  <footer>
    <p>&copy; 2025 Nurk's. Todos los derechos reservados.</p>
    <p>Síguenos en Instagram, TikTok y Facebook</p>
  </footer>

  <script>
    let carrito = [];

    function agregarAlCarrito(producto, precio) {
      carrito.push({ producto, precio });
      renderizarCarrito();
    }

    function renderizarCarrito() {
      const lista = document.getElementById('lista-carrito');
      lista.innerHTML = '';
      let total = 0;
      carrito.forEach(item => {
        const li = document.createElement('li');
        li.textContent = `${item.producto} - ${item.precio} €`;
        lista.appendChild(li);
        total += item.precio;
      });
      document.getElementById('total').textContent = total.toFixed(2);
    }

    function pagarConPayPal() {
      alert('Integración de PayPal aquí (requiere cuenta y configuración en servidor)');
    }
  </script>
</body>
</html>
