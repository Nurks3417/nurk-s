<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Nurk's - Ropa Creativa</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; }
    header, footer { background-color: #111; color: white; padding: 1em; text-align: center; }
    nav a { margin: 0 15px; color: white; text-decoration: none; }
    section { padding: 2em; }
    .productos { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1em; }
    .producto { border: 1px solid #ddd; padding: 1em; border-radius: 8px; text-align: center; }
    .producto img { max-width: 100%; height: auto; }
    form { max-width: 400px; margin: auto; display: flex; flex-direction: column; gap: 1em; }
    input, textarea { padding: 0.5em; }
    button { padding: 0.7em; background-color: #111; color: white; border: none; cursor: pointer; }
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
    <div class="productos">
      <div class="producto">
        <img src="https://via.placeholder.com/200x200.png?text=Sudadera" alt="Sudadera">
        <h3>Sudadera Bordada</h3>
        <p>45 €</p>
        <button>Añadir al carrito</button>
      </div>
      <div class="producto">
        <img src="https://via.placeholder.com/200x200.png?text=Pantalon" alt="Pantalon">
        <h3>Pantalón Vaquero</h3>
        <p>35 €</p>
        <button>Añadir al carrito</button>
      </div>
    </div>
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
</body>
</html>
