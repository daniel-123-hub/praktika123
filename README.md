<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ландшафтная компания "Зелёный Рай"</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background-color: #2e8b57;
            color: white;
            padding: 20px 0;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 28px;
            font-weight: bold;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: #d4e6a5;
        }
        
        .hero {
            background: url('https://images.unsplash.com/photo-1585320806297-9794b3e4eeae') no-repeat center center/cover;
            height: 500px;
            display: flex;
            align-items: center;
            color: white;
            text-align: center;
            position: relative;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            width: 100%;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
        }
        
        .btn {
            display: inline-block;
            background: #2e8b57;
            color: white;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 5px;
            transition: background 0.3s;
        }
        
        .btn:hover {
            background: #3cb371;
        }
        
        .services {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 36px;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            border: 1px solid #ddd;
            border-radius: 5px;
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .service-img {
            height: 200px;
            overflow: hidden;
        }
        
        .service-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .service-card:hover .service-img img {
            transform: scale(1.1);
        }
        
        .service-content {
            padding: 20px;
        }
        
        .service-content h3 {
            margin-bottom: 15px;
            font-size: 22px;
        }
        
        .about {
            background: #f9f9f9;
            padding: 80px 0;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-text {


flex: 1;
        }
        
        .about-img {
            flex: 1;
            border-radius: 5px;
            overflow: hidden;
        }
        
        .about-img img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .portfolio {
            padding: 80px 0;
        }
        
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }
        
        .portfolio-item {
            position: relative;
            overflow: hidden;
            border-radius: 5px;
            height: 250px;
        }
        
        .portfolio-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .portfolio-item:hover img {
            transform: scale(1.1);
        }
        
        .portfolio-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(46, 139, 87, 0.8);
            color: white;
            padding: 20px;
            transform: translateY(100%);
            transition: transform 0.3s;
        }
        
        .portfolio-item:hover .portfolio-overlay {
            transform: translateY(0);
        }
        
        .contact {
            padding: 80px 0;
            background: #f9f9f9;
        }
        
        .contact-content {
            display: flex;
            gap: 50px;
        }
        
        .contact-info {
            flex: 1;
        }
        
        .contact-info h3 {
            margin-bottom: 20px;
            font-size: 24px;
        }
        
        .contact-info p {
            margin-bottom: 15px;
        }
        
        .contact-form {
            flex: 1;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        
        .form-group textarea {
            height: 150px;
        }
        
        footer {
            background: #2e8b57;
            color: white;
            text-align: center;
            padding: 30px 0;
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
                justify-content: center;
            }
            
            .about-content,
            .contact-content {
                flex-direction: column;
            }
            
            .hero h1 {
                font-size: 36px;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-content">
            <div class="logo">Зелёный Рай</div>
            <nav>
                <ul>
                    <li><a href="#services">Услуги</a></li>
                    <li><a href="#about">О нас</a></li>
                    <li><a href="#portfolio">Портфолио</a></li>
                    <li><a href="#contact">Контакты</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <section class="hero">
        <div class="hero-content container">
            <h1>Профессиональный ландшафтный дизайн</h1>
            <p>Создаем гармоничное пространство для вашего отдыха и наслаждения природой</p>
            <a href="#contact" class="btn">Заказать проект</a>
        </div>
    </section>
    
    <section id="services" class="services">
        <div class="container">
            <h2 class="section-title">Наши услуги</h2>
            <div class="services-grid">
                <div class="service-card">


<div class="service-img">
                        <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c" alt="Ландшафтное проектирование">
                    </div>
                    <div class="service-content">
                        <h3>Ландшафтное проектирование</h3>
                        <p>Разработка индивидуальных проектов с учетом особенностей участка и пожеланий клиента.</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-img">
                        <img src="https://images.unsplash.com/photo-1600566752229-250ed79470b5" alt="Озеленение">
                    </div>
                    <div class="service-content">
                        <h3>Озеленение</h3>
                        <p>Посадка деревьев, кустарников, цветников, создание газонов и живых изгородей.</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-img">
                        <img src="https://images.unsplash.com/photo-1585320806297-9794b3e4eeae" alt="Системы полива">
                    </div>
                    <div class="service-content">
                        <h3>Системы полива</h3>
                        <p>Проектирование и монтаж автоматических систем полива для вашего участка.</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-img">
                        <img src="https://images.unsplash.com/photo-1600566753190-17f0baa2a6c3" alt="Садовое освещение">
                    </div>
                    <div class="service-content">
                        <h3>Садовое освещение</h3>
                        <p>Создание эффектного и функционального освещения для вашего сада.</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-img">
                        <img src="https://images.unsplash.com/photo-1600566752355-35792bedcfea" alt="Малые архитектурные формы">
                    </div>
                    <div class="service-content">
                        <h3>Малые архитектурные формы</h3>
                        <p>Беседки, перголы, садовая мебель, мостики и другие элементы декора.</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-img">
                        <img src="https://images.unsplash.com/photo-1600566752229-250ed79470b5" alt="Уход за садом">
                    </div>
                    <div class="service-content">
                        <h3>Уход за садом</h3>
                        <p>Комплексные услуги по уходу за растениями и поддержанию ландшафта.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">О компании</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Ландшафтная компания "Зелёный Рай" работает на рынке с 2010 года. За это время мы реализовали более 500 проектов различной сложности.</p>
                    <p>Наша команда состоит из профессиональных дизайнеров, архитекторов и садовников, которые любят свое дело и создают по-настоящему уникальные ландшафты.</p>
                    <p>Мы используем только качественные материалы и растения, а также даем гарантию на все виды работ.</p>
                    <p>Наш подход - индивидуальное внимание к каждому клиенту и создание пространства, которое будет радовать вас долгие годы.</p>
                </div>
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1600566753190-17f0baa2a6c3" alt="Наша команда">
                </div>
            </div>


</div>
    </section>
    
    <section id="portfolio" class="portfolio">
        <div class="container">
            <h2 class="section-title">Наши работы</h2>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1600566752229-250ed79470b5" alt="Проект 1">
                    <div class="portfolio-overlay">
                        <h3>Частный сад в Подмосковье</h3>
                        <p>Площадь: 15 соток</p>
                    </div>
                </div>
                
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c" alt="Проект 2">
                    <div class="portfolio-overlay">
                        <h3>Ландшафт загородного дома</h3>
                        <p>Площадь: 25 соток</p>
                    </div>
                </div>
                
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1600566752355-35792bedcfea" alt="Проект 3">
                    <div class="portfolio-overlay">
                        <h3>Сад в японском стиле</h3>
                        <p>Площадь: 8 соток</p>
                    </div>
                </div>
                
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1585320806297-9794b3e4eeae" alt="Проект 4">
                    <div class="portfolio-overlay">
                        <h3>Парковая зона отеля</h3>
                        <p>Площадь: 1 га</p>
                    </div>
                </div>
                
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1600566753190-17f0baa2a6c3" alt="Проект 5">
                    <div class="portfolio-overlay">
                        <h3>Двор городского особняка</h3>
                        <p>Площадь: 12 соток</p>
                    </div>
                </div>
                
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1600566752229-250ed79470b5" alt="Проект 6">
                    <div class="portfolio-overlay">
                        <h3>Сад у реки</h3>
                        <p>Площадь: 18 соток</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Контакты</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Свяжитесь с нами</h3>
                    <p><strong>Адрес:</strong> г. Москва, ул. Садовая, 15</p>
                    <p><strong>Телефон:</strong> +7 (495) 123-45-67</p>
                    <p><strong>Email:</strong> info@greenparadise.ru</p>
                    <p><strong>Режим работы:</strong> Пн-Пт: 9:00-18:00</p>
                </div>
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Ваше имя</label>
                            <input type="text" id="name" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">Телефон</label>
                            <input type="tel" id="phone" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email">
                        </div>
                        <div class="form-group">
                            <label for="message">Сообщение</label>
                            <textarea id="message"></textarea>
                        </div>
                        <button type="submit" class="btn">Отправить</button>
                    </form>


</div>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="container">
            <p>&copy; 2023 Ландшафтная компания "Зелёный Рай". Все права защищены.</p>
        </div>
    </footer>
</body>
</html>
