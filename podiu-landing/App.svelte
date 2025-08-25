1<script>
    let menuOpen = false;
    
    const toggleMenu = () => {
        menuOpen = !menuOpen;
    };
    
    const scrollToSection = (id) => {
        document.getElementById(id)?.scrollIntoView({ behavior: 'smooth' });
        menuOpen = false;
    };
</script>

<main>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="container">
            <div class="logo">podiu</div>
            <button class="menu-button" on:click={toggleMenu} aria-label="Menú">
                <span class={menuOpen ? 'open' : ''}></span>
                <span class={menuOpen ? 'open' : ''}></span>
                <span class={menuOpen ? 'open' : ''}></span>
            </button>
            <div class={`nav-links ${menuOpen ? 'active' : ''}`}>
                <a href="#inicio" on:click|preventDefault={() => scrollToSection('inicio')}>Inicio</a>
                <a href="#servicios" on:click|preventDefault={() => scrollToSection('servicios')}>Servicios</a>
                <a href="#contacto" on:click|preventDefault={() => scrollToSection('contacto')}>Contacto</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="inicio" class="hero">
        <div class="container">
            <h1>Impulsamos tu marca en Chile y el mundo</h1>
            <p>Soluciones de marketing digital a medida para hacer crecer tu negocio en la era digital.</p>
            <a href="#contacto" class="cta-button" on:click|preventDefault={() => scrollToSection('contacto')}>Contáctanos</a>
        </div>
    </section>

    <!-- Services Section -->
    <section id="servicios" class="services">
        <div class="container">
            <h2>Nuestros Servicios</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">📈</div>
                    <h3>Estrategia Digital</h3>
                    <p>Desarrollamos planes personalizados para maximizar tu presencia en línea.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🎨</div>
                    <h3>Diseño de Marca</h3>
                    <p>Creamos identidades visuales memorables que destacan tu negocio.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">📱</div>
                    <h3>Redes Sociales</h3>
                    <p>Gestionamos y potenciamos tus perfiles en redes sociales.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contacto" class="contact">
        <div class="container">
            <h2>Contáctanos</h2>
            <p>¿Listo para impulsar tu marca? Escríbenos y te contactaremos a la brevedad.</p>
            <form class="contact-form">
                <div class="form-group">
                    <input type="text" placeholder="Nombre" required />
                </div>
                <div class="form-group">
                    <input type="email" placeholder="Correo electrónico" required />
                </div>
                <div class="form-group">
                    <textarea placeholder="Mensaje" rows="5" required></textarea>
                </div>
                <button type="submit" class="cta-button">Enviar mensaje</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">podiu</div>
                <p>© {new Date().getFullYear()} podiu. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>
</main>
