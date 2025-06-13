
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>КодУм - Программирование для детей</title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Comic+Neue:wght@400;700&family=Rubik+Bubbles&display=swap">
    <style>
        :root {
            --primary: #6c5ce7;
            --secondary: #a29bfe;
            --accent: #fd79a8;
            --light: #f8f9fa;
            --dark: #2d3436;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Comic Neue', cursive;
            background-color: #f0f8ff;
            color: var(--dark);
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            padding: 1rem 2rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .logo {
            font-family: 'Rubik Bubbles', cursive;
            font-size: 2rem;
            color: white;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            transition: all 0.3s ease;
        }
        
        nav a:hover {
            background-color: rgba(255,255,255,0.2);
            transform: translateY(-2px);
        }
        
        .hero {
            background: url('https://images.unsplash.com/photo-1581094794329-c8112a89af12?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            position: relative;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            padding: 0 2rem;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            font-family: 'Rubik Bubbles', cursive;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 1rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.2rem;
            transition: all 0.3s ease;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.3);
            background-color: #e84393;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 4rem 2rem;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2.5rem;
            color: var(--primary);
            font-family: 'Rubik Bubbles', cursive;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .feature-card {
            background-color: white;
            border-radius: 20px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 8px 16px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 12px 24px rgba(0,0,0,0.15);
        }
        
        .feature-icon {
            font-size: 3rem;
            color: var(--accent);
            margin-bottom: 1.5rem;
        }
        
        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        .courses {
            background-color: var(--light);
        }
        
        .course-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }
        
        .course-card {
            background-color: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 8px 16px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        .course-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 12px 24px rgba(0,0,0,0.15);
        }
        
        .course-img {
            height: 200px;
            width: 100%;
            object-fit: cover;
        }
        
        .course-content {
            padding: 1.5rem;
        }
        
        .course-content h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        .course-content p {
            margin-bottom: 1.5rem;
        }
        
        .testimonials {
            background-color: var(--secondary);
            color: white;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .testimonial-card {
            background-color: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 20px;
            backdrop-filter: blur(10px);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 1.5rem;
        }
        
        .testimonial-author {
            font-weight: bold;
        }
        
        .cta {
            text-align: center;
            padding: 6rem 2rem;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
        }
        
        .cta h2 {
            font-size: 3rem;
            margin-bottom: 2rem;
            font-family: 'Rubik Bubbles', cursive;
        }
        
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 2rem;
            text-align: center;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-links a {
            color: white;
            text-decoration: none;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 2rem;
        }
        
        .social-icon {
            color: white;
            font-size: 1.5rem;
        }
        
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                gap: 1rem;
            }
            
            nav ul {
                gap: 1rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header>
        <div class="header-container">
            <div class="logo">КодУм</div>
            <nav>
                <ul>
                    <li><a href="#about">О нас</a></li>
                    <li><a href="#courses">Курсы</a></li>
                    <li><a href="#features">Преимущества</a></li>
                    <li><a href="#testimonials">Отзывы</a></li>
                    <li><a href="#contact">Контакты</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <section class="hero">
        <div class="hero-content">
            <h1>Программирование - это весело!</h1>
            <p>Интерактивные курсы по программированию для детей 7-12 лет. Учимся играя!</p>
            <a href="#courses" class="btn">Начать обучение</a>
        </div>
    </section>
    
    <section id="about" class="container">
        <h2 class="section-title">О нашей школе</h2>
        <div class="features">
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-child"></i>
                </div>
                <h3>Для детей</h3>
                <p>Специально разработанная программа для младшего школьного возраста</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-gamepad"></i>
                </div>
                <h3>Игровой формат</h3>
                <p>Учимся через создание игр и анимаций</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-graduation-cap"></i>
                </div>
                <h3>Квалифицированные педагоги</h3>
                <p>Опытные преподаватели с любовью к детям</p>
            </div>
        </div>
    </section>
    
    <section id="courses" class="container courses">
        <h2 class="section-title">Наши курсы</h2>
        <div class="course-grid">
            <div class="course-card">
                <img src="https://images.unsplash.com/photo-1551033406-611cf9a28f67?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Scratch" class="course-img">
                <div class="course-content">
                    <h3>Scratch для начинающих</h3>
                    <p>Создаем первые игры с помощью визуального программирования. Идеальный старт для детей 7-9 лет.</p>
                    <a href="#" class="btn">Подробнее</a>
                </div>
            </div>
            <div class="course-card">
                <img src="https://images.unsplash.com/photo-1542831371-29b0f74f9713?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Python" class="course-img">
                <div class="course-content">
                    <h3>Python в Minecraft</h3>
                    <p>Программируем на Python, создавая моды для Minecraft. Для детей 10-12 лет.</p>
                    <a href="#" class="btn">Подробнее</a>
                </div>
            </div>
            <div class="course-card">
                <img src="https://images.unsplash.com/photo-1581093057305-3ec4d576d1e8?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Робототехника" class="course-img">
                <div class="course-content">
                    <h3>Робототехника Lego</h3>
                    <p>Собираем и программируем роботов. Развиваем логику и креативность.</p>
                    <a href="#" class="btn">Подробнее</a>
                </div>
            </div>
        </div>
    </section>
    
    <section id="features" class="container">
        <h2 class="section-title">Почему выбирают нас</h2>
        <div class="features">
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-users"></i>
                </div>
                <h3>Маленькие группы</h3>
                <p>Занятия в группах до 8 человек для индивидуального подхода</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-laptop-code"></i>
                </div>
                <h3>Современные технологии</h3>
                <p>Используем актуальные языки и платформы для обучения</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-certificate"></i>
                </div>
                <h3>Сертификат</h3>
                <p>По окончании курса каждый ученик получает сертификат</p>
            </div>
        </div>
    </section>
    
    <section id="testimonials" class="testimonials">
        <div class="container">
            <h2 class="section-title">Отзывы родителей</h2>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <p class="testimonial-text">Мой сын в восторге от занятий! Теперь вместо игр на телефоне создает свои. Спасибо за такой подход к обучению!</p>
                    <p class="testimonial-author">- Анна, мама Максима (9 лет)</p>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">Дочь ждет каждое занятие с нетерпением. Заметно улучшилась логика и успеваемость в школе по математике.</p>
                    <p class="testimonial-author">- Ольга, мама Софии (8 лет)</p>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">Отличные преподаватели, которые умеют заинтересовать детей. Сын начал сам изучать дополнительные материалы!</p>
                    <p class="testimonial-author">- Иван, папа Артема (10 лет)</p>
                </div>
            </div>
        </div>
    </section>
    
    <section class="cta">
        <h2>Готовы начать?</h2>
        <p>Запишитесь на бесплатный пробный урок прямо сейчас!</p>
        <a href="#contact" class="btn">Записаться</a>
    </section>
    
    <section id="contact" class="container">
        <h2 class="section-title">Контакты</h2>
        <div style="text-align: center; margin-bottom: 3rem;">
            <p><i class="fas fa-map-marker-alt"></i> г. Москва, ул. Программистов, 42</p>
            <p><i class="fas fa-phone"></i> +7 (123) 456-78-90</p>
            <p><i class="fas fa-envelope"></i> info@kodum.ru</p>
        </div>
        <form style="max-width: 600px; margin: 0 auto;">
            <div style="display: grid; gap: 1rem; margin-bottom: 1.5rem;">
                <input type="text" placeholder="Ваше имя" style="padding: 1rem; border-radius: 10px; border: 1px solid #ddd;">
                <input type="email" placeholder="Ваш email" style="padding: 1rem; border-radius: 10px; border: 1px solid #ddd;">
                <textarea placeholder="Ваше сообщение" rows="5" style="padding: 1rem; border-radius: 10px; border: 1px solid #ddd;"></textarea>
            </div>
            <button type="submit" class="btn" style="margin: 0 auto; display: block;">Отправить</button>
        </form>
    </section>
    
    <footer>
        <div class="footer-links">
            <a href="#about">О нас</a>
            <a href="#courses">Курсы</a>
            <a href="#features">Преимущества</a>
            <a href="#testimonials">Отзывы</a>
            <a href="#contact">Контакты</a>
        </div>
        <div class="social-icons">
            <a href="#" class="social-icon"><i class="fab fa-vk"></i></a>
            <a href="#" class="social-icon"><i class="fab fa-telegram"></i></a>
            <a href="#" class="social-icon"><i class="fab fa-youtube"></i></a>
            <a href="#" class="social-icon"><i class="fab fa-instagram"></i></a>
        </div>
        <p>&copy; 2023 КодУм - Школа программирования для детей. Все права защищены.</p>
    </footer>
    
    <script>
        // Плавная прокрутка для якорных ссылок
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Обработка формы
        document.querySelector('form')?.addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Спасибо! Мы свяжемся с вами в ближайшее время.');
            this.reset();
        });
    </script>
</body>
</html>
