# Portafolio
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi Portafolio</title>
  <style>
    :root {
      --color-primario: #0077b6;
      --color-secundario: #0096c7;
      --color-fondo: #f8f9fa;
      --color-texto: #333;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      color: var(--color-texto);
      line-height: 1.6;
      background-color: var(--color-fondo);
    }

    /* Navbar */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: var(--color-primario);
      padding: 1rem;
      color: #fff;
    }

    .navbar .logo {
      font-weight: bold;
    }

    .nav-links {
      list-style: none;
      display: flex;
    }

    .nav-links li {
      margin-left: 20px;
    }

    .nav-links a {
      color: #fff;
      text-decoration: none;
    }

    .hamburger {
      display: none;
      font-size: 24px;
      background: none;
      border: none;
      color: white;
      cursor: pointer;
    }

    /* Hero */
    .hero {
      text-align: center;
      padding: 100px 20px;
      background: linear-gradient(135deg, var(--color-primario), var(--color-secundario));
      color: #fff;
    }

    .hero h1 span {
      color: yellow;
    }

    .btn {
      display: inline-block;
      background: tomato;
      color: #fff;
      padding: 10px 20px;
      margin-top: 20px;
      text-decoration: none;
      border-radius: 5px;
    }

    /* Acerca */
    .about {
      padding: 50px 20px;
      text-align: center;
    }

    .about-container {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
    }

    .about img {
      width: 150px;
      border-radius: 50%;
    }

    /* Habilidades */
    .skills {
      padding: 50px 20px;
    }

    .skill {
      margin: 20px 0;
    }

    .progress {
      background: #ddd;
      border-radius: 20px;
      overflow: hidden;
    }

    .progress-bar {
      height: 20px;
      width: 0;
      background: var(--color-primario);
      transition: width 2s;
    }

    /* Proyectos */
    .projects {
      padding: 50px 20px;
      background: #fff;
    }

    .project-cards {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
      justify-content: center;
    }

    .card {
      background: #f1f1f1;
      padding: 20px;
      border-radius: 10px;
      width: 300px;
      transition: transform 0.3s;
    }

    .card:hover {
      transform: translateY(-10px);
    }

    /* Contacto */
    .contact {
      padding: 50px 20px;
    }

    .contact-container {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
    }

    .contact-info {
      flex: 1;
    }

    form {
      flex: 1;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    form input, form textarea {
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    form button {
      background: var(--color-secundario);
      color: white;
      border: none;
      padding: 10px;
      cursor: pointer;
      border-radius: 5px;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 20px;
      background: var(--color-primario);
      color: white;
    }

    /* Responsive */
    @media(max-width: 768px) {
      .nav-links {
        display: none;
        flex-direction: column;
        background: var(--color-primario);
        position: absolute;
        top: 60px;
        right: 0;
        width: 200px;
        padding: 20px;
      }
      .nav-links.show {
        display: flex;
      }
      .hamburger {
        display: block;
      }
      .about-container, .contact-container {
        flex-direction: column;
        text-align: center;
      }
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <nav class="navbar">
      <div class="logo">Mi Portafolio</div>
      <button class="hamburger" id="hamburger">&#9776;</button>
      <ul class="nav-links" id="nav-links">
        <li><a href="#inicio">Inicio</a></li>
        <li><a href="#acerca">Acerca de</a></li>
        <li><a href="#habilidades">Habilidades</a></li>
        <li><a href="#proyectos">Proyectos</a></li>
        <li><a href="#contacto">Contacto</a></li>
      </ul>
    </nav>
  </header>

  <!-- Inicio -->
  <section id="inicio" class="hero">
    <h1>¡Hola! Soy <span>[Tu Nombre]</span></h1>
    <p>Desarrollador web frontend apasionado por crear experiencias digitales increíbles</p>
    <a href="#contacto" class="btn">¡Contáctame!</a>
  </section>

  <!-- Acerca de mí -->
  <section id="acerca" class="about">
    <h2>Acerca de Mí</h2>
    <div class="about-container">
      <img src="https://via.placeholder.com/150" alt="Foto de perfil">
      <p>
        Soy un desarrollador web frontend con pasión por crear interfaces de usuario atractivas y funcionales. 
        Me especializo en HTML, CSS y JavaScript, y siempre estoy buscando aprender nuevas tecnologías y mejorar mis habilidades.
      </p>
    </div>
  </section>

  <!-- Habilidades -->
  <section id="habilidades" class="skills">
    <h2>Mis Habilidades</h2>
    <div class="skill">
      <p>HTML5</p>
      <div class="progress"><div class="progress-bar" data-skill="90"></div></div>
    </div>
    <div class="skill">
      <p>CSS3</p>
      <div class="progress"><div class="progress-bar" data-skill="85"></div></div>
    </div>
    <div class="skill">
      <p>JavaScript</p>
      <div class="progress"><div class="progress-bar" data-skill="80"></div></div>
    </div>
    <div class="skill">
      <p>Responsive Design</p>
      <div class="progress"><div class="progress-bar" data-skill="95"></div></div>
    </div>
  </section>

  <!-- Proyectos -->
  <section id="proyectos" class="projects">
    <h2>Mis Proyectos</h2>
    <div class="project-cards">
      <div class="card">
        <h3>Sitio Web Corporativo</h3>
        <p>Un sitio web moderno y responsive para una empresa local, desarrollado con HTML, CSS y JavaScript.</p>
      </div>
      <div class="card">
        <h3>Aplicación Web Interactiva</h3>
        <p>Una aplicación web que permite a los usuarios gestionar sus tareas con funcionalidades avanzadas de JavaScript.</p>
      </div>
      <div class="card">
        <h3>Landing Page Creativa</h3>
        <p>Una página de aterrizaje con animaciones CSS y efectos de parallax implementados con JavaScript.</p>
      </div>
    </div>
  </section>

  <!-- Contacto -->
  <section id="contacto" class="contact">
    <h2>Contáctame</h2>
    <div class="contact-container">
      <div class="contact-info">
        <p><strong>Email:</strong> juanva0809.com</p>
        <p><strong>Teléfono:</strong> +093 980 8580</p>
        <p><strong>Ubicación:</strong> Guayaquil, Ecuador</p>
      </div>
      <form id="contact-form">
        <input type="text" id="nombre" name="nombre" placeholder="Nombre" required>
        <input type="email" id="email" name="email" placeholder="Email" required>
        <textarea id="mensaje" name="mensaje" placeholder="Mensaje" required></textarea>
        <button type="submit" class="btn">Enviar Mensaje</button>
      </form>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 mi portafolio. Todos los derechos reservados.</p>
    <div class="socials">
      <a href="#">Instagram</a> | <a href="#">GitHub</a> | <a href="#">Threads</a>
    </div>
  </footer>

  <script>
    // Menú hamburguesa
    const hamburger = document.getElementById("hamburger");
    const navLinks = document.getElementById("nav-links");

    hamburger.addEventListener("click", () => {
      navLinks.classList.toggle("show");
    });

    // Animación de barras de progreso al hacer scroll
    const progressBars = document.querySelectorAll(".progress-bar");

    window.addEventListener("scroll", () => {
      progressBars.forEach(bar => {
        const skillValue = bar.getAttribute("data-skill");
        const barPosition = bar.getBoundingClientRect().top;
        const screenHeight = window.innerHeight;
        if (barPosition < screenHeight) {
          bar.style.width = skillValue + "%";
        }
      });
    });

    // Validación de formulario en tiempo real
    const form = document.getElementById("contact-form");
    const nombre = document.getElementById("nombre");
    const email = document.getElementById("email");
    const mensaje = document.getElementById("mensaje");

    form.addEventListener("submit", (e) => {
      e.preventDefault();
      if (nombre.value === "" || email.value === "" || mensaje.value === "") {
        alert("Por favor completa todos los campos");
      } else {
        alert("Mensaje enviado correctamente ✅");
        form.reset();
      }
    });

    email.addEventListener("input", () => {
      const regex = /^[^ ]+@[^ ]+\.[a-z]{2,3}$/;
      if (!regex.test(email.value)) {
        email.style.border = "2px solid red";
      } else {
        email.style.border = "2px solid green";
      }
    });
  </script>
</body>
</html>

