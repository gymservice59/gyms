
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ремонт тренажеров - профессиональный ремонт и обслуживание</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --shadow: 0 4px 6px rgba(0,0,0,0.1);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
            overflow-x: hidden;
        }

        .hero {
            background: linear-gradient(rgba(44, 62, 80, 0.9), rgba(44, 62, 80, 0.9)), 
                        url('https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80') no-repeat center center/cover;
            height: 90vh;
            display: flex;
            align-items: center;
            color: white;
            text-align: center;
            position: relative;
            margin-top: 80px;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2.5rem;
            opacity: 0.9;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 1rem 2rem;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 1.1rem;
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
            text-align: center;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            transition: var(--transition);
        }

        .btn:hover::before {
            left: 100%;
        }

        .btn:hover {
            background-color: #2980b9;
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.2);
        }

        .btn-accent {
            background-color: var(--accent);
        }

        .btn-accent:hover {
            background-color: #c0392b;
        }

        .btn-outline {
            background-color: transparent;
            border: 2px solid white;
        }

        .btn-outline:hover {
            background-color: rgba(255,255,255,0.1);
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        header {
            background-color: var(--primary);
            color: white;
            padding: 1rem 0;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .header-scrolled {
            padding: 0.5rem 0;
            background-color: rgba(44, 62, 80, 0.95);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            display: flex;
            align-items: center;
        }

        .logo span {
            color: var(--secondary);
        }

        .logo i {
            margin-right: 10px;
            color: var(--secondary);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 1.5rem;
            position: relative;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            transition: var(--transition);
            font-weight: 500;
            padding: 5px 0;
        }

        nav ul li a:hover {
            color: var(--secondary);
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--secondary);
            transition: var(--transition);
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        .features {
            padding: 8rem 0 6rem 0;
            background-color: white;
        }

        .section-title {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--dark);
            margin-bottom: 1rem;
            position: relative;
            display: inline-block;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background: var(--secondary);
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
        }

        .section-title p {
            color: #7f8c8d;
            max-width: 700px;
            margin: 0 auto;
            font-size: 1.1rem;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2.5rem;
        }

        .feature-card {
            background-color: white;
            border-radius: 10px;
            padding: 2.5rem 2rem;
            text-align: center;
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--secondary);
            transform: scaleX(0);
            transition: var(--transition);
            transform-origin: left;
        }

        .feature-card:hover::before {
            transform: scaleX(1);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }

        .feature-icon {
            font-size: 3.5rem;
            color: var(--secondary);
            margin-bottom: 1.5rem;
            display: inline-block;
            transition: var(--transition);
        }

        .feature-card:hover .feature-icon {
            transform: scale(1.1);
            color: var(--accent);
        }

        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--dark);
        }

        .feature-card p {
            color: #7f8c8d;
            line-height: 1.7;
        }

        .services {
            padding: 6rem 0;
            background-color: #f8f9fa;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2.5rem;
        }

        .service-card {
            background: white;
            border-radius: 10px;
            padding: 2.5rem;
            box-shadow: var(--shadow);
            transition: var(--transition);
            text-align: center;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }

        .service-icon {
            font-size: 3.5rem;
            color: var(--secondary);
            margin-bottom: 1.5rem;
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--dark);
        }

        .service-card p {
            color: #7f8c8d;
            margin-bottom: 1.5rem;
        }

        .service-list {
            text-align: left;
        }

        .service-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 1rem;
        }

        .service-item i {
            color: var(--secondary);
            margin-right: 1rem;
            font-size: 1.2rem;
            margin-top: 0.2rem;
        }

        .cta {
            padding: 6rem 0;
            background: linear-gradient(rgba(44, 62, 80, 0.9), rgba(44, 62, 80, 0.9)), 
                        url('https://images.unsplash.com/photo-1571902943202-507ec2618e8f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1075&q=80') no-repeat center center/cover;
            color: white;
            text-align: center;
        }

        .cta-content {
            max-width: 700px;
            margin: 0 auto;
        }

        .cta h2 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
        }

        .cta p {
            font-size: 1.2rem;
            margin-bottom: 2.5rem;
            opacity: 0.9;
        }

        .contact {
            padding: 6rem 0;
            background: var(--primary);
            color: white;
            text-align: center;
        }

        .contact-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            max-width: 900px;
            margin: 0 auto;
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: white;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 1.5rem;
            text-align: left;
        }

        .contact-item i {
            margin-right: 1rem;
            color: var(--secondary);
            font-size: 1.2rem;
            margin-top: 0.2rem;
        }

        .contact-actions {
            margin-top: 2rem;
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .contact-actions .btn {
            margin: 0;
        }

        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 0 1.5rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-column h3 {
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
            color: var(--secondary);
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 0.8rem;
        }

        .footer-column ul li a {
            color: #bdc3c7;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-column ul li a:hover {
            color: white;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
            justify-content: center;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: #34495e;
            color: white;
            border-radius: 50%;
            text-decoration: none;
            transition: var(--transition);
        }

        .social-links a:hover {
            background: var(--secondary);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid #34495e;
            color: #bdc3c7;
            font-size: 0.9rem;
        }

        .notification {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: var(--secondary);
            color: white;
            padding: 1rem 1.5rem;
            border-radius: 5px;
            box-shadow: var(--shadow);
            display: none;
            z-index: 1000;
            animation: slideInRight 0.3s ease;
        }

        @keyframes slideInRight {
            from { transform: translateX(100%); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }

        .progress-bar {
            position: fixed;
            top: 0;
            left: 0;
            height: 4px;
            background: var(--secondary);
            width: 0%;
            z-index: 1001;
            transition: width 0.3s ease;
        }

        @media (max-width: 768px) {
            .hero {
                height: auto;
                padding: 8rem 0 6rem;
                margin-top: 70px;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .header-content {
                flex-direction: column;
                text-align: center;
            }

            nav ul {
                margin-top: 1rem;
                justify-content: center;
                flex-wrap: wrap;
            }

            nav ul li {
                margin: 0.5rem;
            }

            .mobile-menu-btn {
                display: block;
                position: absolute;
                top: 1rem;
                right: 1rem;
            }

            .contact-actions {
                flex-direction: column;
                align-items: center;
            }

            .contact-actions .btn {
                width: 100%;
                max-width: 250px;
            }
        }
    </style>
</head>

<body>
    <div class="progress-bar" id="progressBar"></div>
    
    <header id="header">
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-dumbbell"></i>
                    Ремонт<span>Тренажеров</span>
                </div>
                <button class="mobile-menu-btn" id="mobileMenuBtn">
                    <i class="fas fa-bars"></i>
                </button>
                <nav>
                    <ul>
                        <li><a href="#features">Преимущества</a></li>
                        <li><a href="#services">Услуги</a></li>
                        <li><a href="#contact">Контакты</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <section class="hero">
        <div class="hero-content">
            <h1>Ремонт, сборка и обслуживание спортивных тренажёров</h1>
            <p>Быстро, качественно и с гарантией. Выезд мастера в течение 24 часов.</p>
            <div class="hero-buttons">
                <a href="tel:+79991120555" class="btn">
                    <i class="fas fa-phone"></i> Вызвать мастера
                </a>
                <a href="#services" class="btn btn-outline">
                    <i class="fas fa-info-circle"></i> Наши услуги
                </a>
            </div>
        </div>
    </section>

    <section class="features" id="features">
        <div class="container">
            <div class="section-title">
                <h2>Наши преимущества</h2>
                <p>Почему клиенты выбирают именно нашу компанию для ремонта тренажеров</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-tools"></i>
                    </div>
                    <h3>Опытные мастера</h3>
                    <p>Наши специалисты имеют многолетний опыт работы с тренажерами различных брендов и сложности.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-clock"></i>
                    </div>
                    <h3>Быстрый выезд</h3>
                    <p>Мастер приедет к вам в течение 24 часов после обращения. Срочный выезд в день обращения.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>Гарантия качества</h3>
                    <p>Предоставляем гарантию на все виды работ и используемые запчасти.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-ruble-sign"></i>
                    </div>
                    <h3>Доступные цены</h3>
                    <p>Прозрачное ценообразование без скрытых платежей. Диагностика бесплатно при заказе ремонта.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-cogs"></i>
                    </div>
                    <h3>Оригинальные запчасти</h3>
                    <p>Используем только оригинальные запчасти и комплектующие от проверенных поставщиков.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-home"></i>
                    </div>
                    <h3>Выезд на дом</h3>
                    <p>Ремонт осуществляется на дому у клиента. Вам не нужно везти тренажер в сервисный центр.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="services" id="services">
        <div class="container">
            <div class="section-title">
                <h2>Наши услуги</h2>
                <p>Полный спектр услуг по ремонту, сборке и обслуживанию тренажеров</p>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-running"></i>
                    </div>
                    <h3>Кардиотренажеры</h3>
                    <p>Ремонт и обслуживание всех видов кардиотренажеров</p>
                    <div class="service-list">
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Беговые дорожки</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Велотренажеры</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Эллиптические</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Степперы</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Гребные тренажеры</div>
                        </div>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-dumbbell"></i>
                    </div>
                    <h3>Силовые тренажеры</h3>
                    <p>Ремонт и сборка силового оборудования</p>
                    <div class="service-list">
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Тренажеры со свободными весами</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Блочные тренажеры</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Мультистанции</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Скамьи и стойки</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Тренажеры Смита</div>
                        </div>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-tools"></i>
                    </div>
                    <h3>Сборка и обслуживание</h3>
                    <p>Полный комплекс услуг по сборке и техническому обслуживанию</p>
                    <div class="service-list">
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Профессиональная сборка</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Регулярное обслуживание</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Чистка и смазка</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Регулировка и калибровка</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Замена изношенных деталей</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Перевозка и установка</div>
                        </div>
                        <div class="service-item">
                            <i class="fas fa-check"></i>
                            <div>Ремонт электроники</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="cta">
        <div class="cta-content">
            <h2>Нужен ремонт тренажера?</h2>
            <p>Оставьте заявку прямо сейчас и получите бесплатную диагностику!</p>
            <div class="hero-buttons">
                <a href="tel:+79991120555" class="btn">
                    <i class="fas fa-phone"></i> Позвонить
                </a>
                <a href="https://t.me/perm_Gym_service_059" class="btn btn-accent" target="_blank">
                    <i class="fab fa-telegram"></i> Написать в Telegram
                </a>
            </div>
        </div>
    </section>

    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Свяжитесь с нами</h2>
                <p>Позвоните или напишите нам для консультации и вызова мастера</p>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Наши контакты</h3>
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <div>
                            <h4>Телефон</h4>
                            <p>+7 (999) 112-05-55</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fab fa-telegram"></i>
                        <div>
                            <h4>Telegram</h4>
                            <p>@perm_Gym_service_059</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fab fa-vk"></i>
                        <div>
                            <h4>ВКонтакте</h4>
                            <p>vk.com/club232252573</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <div>
                            <h4>Адрес</h4>
                            <p>г. Пермь, Бульвар Гагарина 46</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-clock"></i>
                        <div>
                            <h4>График работы</h4>
                            <p>Пн-Пт: 9:00 - 20:00, Сб-Вс: 10:00 - 18:00</p>
                        </div>
                    </div>
                    <div class="social-links">
                        <a href="https://t.me/perm_Gym_service_059" target="_blank"><i class="fab fa-telegram"></i></a>
                        <a href="https://vk.com/club232252573" target="_blank"><i class="fab fa-vk"></i></a>
                        <a href="tel:+79991120555"><i class="fas fa-phone"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Ремонт тренажеров</h3>
                    <p>Профессиональный ремонт, сборка и обслуживание тренажеров любой сложности с гарантией качества.</p>
                </div>
                <div class="footer-column">
                    <h3>Услуги</h3>
                    <ul>
                        <li><a href="#">Ремонт кардиотренажеров</a></li>
                        <li><a href="#">Ремонт силовых тренажеров</a></li>
                        <li><a href="#">Сборка тренажеров</a></li>
                        <li><a href="#">Техническое обслуживание</a></li>
                        <li><a href="#">Ремонт электроники</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Контакты</h3>
                    <ul>
                        <li><i class="fas fa-phone"></i> +7 (999) 112-05-55</li>
                        <li><i class="fab fa-telegram"></i> @perm_Gym_service_059</li>
                        <li><i class="fab fa-vk"></i> vk.com/club232252573</li>
                        <li><i class="fas fa-map-marker-alt"></i> г. Пермь, Бульвар Гагарина 46</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Ремонт тренажеров. Все права защищены.</p>
            </div>
        </div>
    </footer>

    <div class="notification" id="notification">
        <span id="notificationText">Уведомление</span>
    </div>

    <script>
        // Плавная прокрутка
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Изменение шапки при скролле
        window.addEventListener('scroll', function() {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('header-scrolled');
            } else {
                header.classList.remove('header-scrolled');
            }
            
            // Прогресс бар
            const winHeight = window.innerHeight;
            const docHeight = document.documentElement.scrollHeight;
            const scrollTop = window.pageYOffset;
            const trackLength = docHeight - winHeight;
            const progress = Math.floor(scrollTop / trackLength * 100);
            document.getElementById('progressBar').style.width = progress + '%';
        });

        // Функция показа уведомлений
        function showNotification(text) {
            const notification = document.getElementById('notification');
            const notificationText = document.getElementById('notificationText');
            
            notificationText.textContent = text;
            notification.style.display = 'block';
            
            setTimeout(() => {
                notification.style.display = 'none';
            }, 3000);
        }

        // Инициализация при загрузке страницы
        window.addEventListener('DOMContentLoaded', function() {
            // Показываем приветственное уведомление
            setTimeout(() => {
                showNotification('Добро пожаловать! Мы готовы помочь с ремонтом вашего тренажера');
            }, 1000);
        });
    </script>
</body>
</html>
