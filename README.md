<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MJM CONSTRUÇÃO - Construção Civil em Cuiabá e Várzea Grande</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #ffd700;
        }

        .whatsapp-btn {
            background: #25D366;
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 25px;
            text-decoration: none;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(37,211,102,0.4);
        }

        .whatsapp-btn:hover {
            background: #20ba5a;
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(37,211,102,0.6);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%231e3c72" width="1200" height="600"/><path fill="%232a5298" d="M0 300 Q300 100 600 300 T1200 300 V600 H0 Z"/></svg>');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 70px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease 0.2s both;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease 0.4s both;
        }

        .btn {
            padding: 1rem 2rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            font-size: 1.1rem;
        }

        .btn-primary {
            background: #ffd700;
            color: #1e3c72;
        }

        .btn-primary:hover {
            background: #ffed4a;
            transform: translateY(-3px);
        }

        /* Sections */
        section {
            padding: 5rem 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #1e3c72;
        }

        /* Services */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            text-align: center;
            transition: all 0.3s;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }

        .service-icon {
            font-size: 3rem;
            color: #25D366;
            margin-bottom: 1rem;
        }

        /* About */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-image {
            width: 100%;
            height: 400px;
            background: linear-gradient(45deg, #1e3c72, #2a5298);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 4rem;
            position: relative;
            overflow: hidden;
        }

        .about-image::before {
            content: "🏗️";
            font-size: 8rem;
            position: absolute;
            animation: float 3s ease-in-out infinite;
        }

        .about-text h3 {
            color: #1e3c72;
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        /* Coverage */
        .coverage {
            background: #f8f9fa;
        }

        .coverage-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            text-align: center;
        }

        .coverage-item i {
            font-size: 3rem;
            color: #25D366;
            margin-bottom: 1rem;
        }

        /* Contact */
        .contact {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            text-align: center;
        }

        .contact-info h3 {
            margin-bottom: 2rem;
            font-size: 1.5rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
            padding: 1rem;
            background: rgba(255,255,255,0.1);
            border-radius: 10px;
        }

        .whatsapp-float {
            position: fixed;
            width: 60px;
            height: 60px;
            bottom: 40px;
            right: 40px;
            background: #25D366;
            color: #FFF;
            border-radius: 50px;
            text-align: center;
            font-size: 30px;
            box-shadow: 2px 2px 3px #999;
            z-index: 100;
            animation: pulse 2s infinite;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            .whatsapp-float {
                width: 50px;
                height: 50px;
                font-size: 25px;
                bottom: 20px;
                right: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">🏗️ MJM CONSTRUÇÃO</div>
            <ul class="nav-links">
                <li><a href="#home">Início</a></li>
                <li><a href="#servicos">Serviços</a></li>
                <li><a href="#sobre">Sobre</a></li>
                <li><a href="#atendimento">Atendimento</a></li>
                <li><a href="#contato">Contato</a></li>
            </ul>
            <a href="https://wa.me/5565993390383?text=Olá!%20Gostaria%20de%20um%20orçamento%20para%20MJM%20Construção" class="whatsapp-btn" target="_blank">
                <i class="fab fa-whatsapp"></i> WhatsApp
            </a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>MJM CONSTRUÇÃO</h1>
            <p>Construindo seu sonho com qualidade e confiança em Cuiabá e Várzea Grande</p>
            <div class="cta-buttons">
                <a href="https://wa.me/5565993390383?text=Olá!%20Quero%20um%20orçamento%20para%20construção!" class="btn btn-primary" target="_blank">
                    <i class="fab fa-whatsapp"></i> Fale pelo WhatsApp
                </a>
                <a href="#servicos" class="btn" style="background: transparent; border: 2px solid white; color: white;">
                    Nossos Serviços
                </a>
            </div>
        </div>
    </section>

    <!-- Services -->
    <section id="servicos" class="container">
        <h2>Nossos Serviços</h2>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-hammer"></i>
                </div>
                <h3>Construção Residencial</h3>
                <p>Casas, sobrados e reformas completas com acabamento de alta qualidade.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-building"></i>
                </div>
                <h3>Construção Comercial</h3>
                <p>Lojas, escritórios e galpões comerciais com projetos personalizados.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-tools"></i>
                </div>
                <h3>Reformas e Reparos</h3>
                <p>Reformas gerais, pintura, elétrica, hidráulica e acabamentos.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-drafting-compass"></i>
                </div>
                <h3>Projetos e Orçamentos</h3>
                <p>Projetos arquitetônicos e orçamentos detalhados sem compromisso.</p>
            </div>
        </div>
    </section>

    <!-- About -->
    <section id="sobre" class="container">
        <h2>Sobre a MJM Construção</h2>
        <div class="about-content">
            <div class="about-image">
                <!-- Aqui você pode substituir por uma foto real -->
            </div>
            <div class="about-text">
                <h3>15 anos de experiência na construção civil</h3>
                <p>Somos uma empresa consolidada em Cuiabá e Várzea Grande, especializada em obras de qualidade com prazos cumpridos e preços justos. Nossa equipe é formada por profissionais qualificados e utilizamos materiais de primeira linha.</p>
                <p><strong>Garantimos:</strong></p>
                <ul style="text-align: left; margin-top: 1rem;">
                    <li>✅ Orçamento sem compromisso</li>
                    <li>✅ Prazos cumpridos</li>
                    <li>✅ Materiais de qualidade</li>
                    <li>✅ Equipe especializada</li>
                    <li>✅ Garantia nas obras</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Coverage -->
    <section id="atendimento" class="coverage">
        <div class="container">
            <h2>Atendemos em:</h2>
            <div class="coverage-grid">
                <div class="coverage-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <h3>Cuiabá - MT</h3>
                    <p>Todo o município</p>
                </div>
                <div class="coverage-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <h3>Várzea Grande - MT</h3>
                    <p>Todo o município</p>
                </div>
                <div class="coverage-item">
                    <i class="fas fa-truck"></i>
                    <h3>Entrega de materiais</h3>
                    <p>Direto na obra</p>
                </div>
                <div class="coverage-item">
                    <i class="fas fa-clock"></i>
                    <h3>Atendimento 24h</h3>
                    <p>Resposta rápida</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section id="contato" class="contact">
        <div class="container">
            <h2>Entre em Contato</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item">
                        <i class="fas fa-phone" style="font-size: 1.5rem;"></i>
                        <div>
                            <h4>WhatsApp</h4>
                            <a href="https://wa.me/5565993390383" style="color: #25D366; text-decoration: none; font-weight: bold;">(65) 99339-0383</a>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-envelope" style="font-size: 1.5rem;"></i>
                        <div>
                            <h4>Email</h4>
                            <p>contato@mjmconstrucao.com.br</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt" style="font-size: 1.5rem;"></i>
                        <div>
                            <h4>Atendimento</h4>
                            <p>Cuiabá e Várzea Grande - MT</p>
                        </div>
                    </div>
                </div>
                <div style="text-align: center;">
                    <h3>Peça seu orçamento agora!</h3>
                    <a href="https://wa.me/5565993390383?text=Olá!%20Gostaria%20de%20um%20orçamento%20da%20MJM%20Construção" class="btn btn-primary" style="background: #25D366; color: white; padding: 1.2rem 3rem; font-size: 1.2rem; display: inline-block;" target="_blank">
                        <i class="fab fa-whatsapp"></i> Falar no WhatsApp
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Floating WhatsApp -->
    <a href="https://wa.me/5565993390383?text=Oi!%20Vi%20o%20site%20da%20MJM%20Construção%20e%20gostaria%20de%20mais%20informações!" class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <script>
        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Navbar scroll effect
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(30, 60, 114, 0.95)';
                header.style.backdropFilter = 'blur(10px)';
            } else {
                header.style.background = 'linear-gradient(135deg, #1e3c72 0%, #2a5298 100%)';
                header.style.backdropFilter = 'none';
            }
        });
    </script>
</body>
</html>
