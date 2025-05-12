<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Психологический центр "Гармония"</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }
        
        header {
            background: linear-gradient(135deg, #6e48aa 0%, #9d50bb 100%);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .container {
            width: 85%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .nav-links a:hover {
            color: #f1c40f;
        }
        
        .hero {
            background: url('https://images.unsplash.com/photo-1532094349884-543bc11b234d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            height: 80vh;
            display: flex;
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
            background: rgba(0,0,0,0.6);
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            width: 80%;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background: #f1c40f;
            color: #333;
            padding: 0.8rem 1.8rem;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background: #f39c12;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        section {
            padding: 5rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2.5rem;
            color: #6e48aa;
        }
        
        .services {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .service-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }
        
        .service-card h3 {
            color: #6e48aa;
            margin-bottom: 1rem;
        }
        
        .service-card i {
            font-size: 2.5rem;
            color: #9d50bb;
            margin-bottom: 1.5rem;
            display: block;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }
        
        .about-img img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }
        
        .blog-posts {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .post-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        .post-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }
        
        .post-img {
            height: 200px;
            overflow: hidden;
        }
        
        .post-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: all 0.5s ease;
        }
        
        .post-card:hover .post-img img {
            transform: scale(1.1);
        }
        
        .post-content {
            padding: 1.5rem;
        }
        
        .post-content h3 {
            margin-bottom: 0.5rem;
            color: #6e48aa;
        }
        
        .post-meta {
            color: #777;
            font-size: 0.9rem;
            margin-bottom: 1rem;
            display: block;
        }
        
        .contact-form {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            max-width: 600px;
            margin: 0 auto;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }
        
        .form-group textarea {
            height: 150px;
            resize: vertical;
        }
        
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 3rem;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            list-style: none;
            margin: 1rem 0;
        }
        
        .footer-links li {
            margin: 0 1rem;
        }
        
        .footer-links a {
            color: white;
            text-decoration: none;
        }
        
        .footer-links a:hover {
            color: #f1c40f;
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .about-content {
                grid-template-columns: 1fr;
            }
            
            .about-img {
                order: -1;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
</head>
<body>
    <header>
        <div class="container">
            <nav>
                <div class="logo">Гармония</div>
                <ul class="nav-links">
                    <li><a href="#home">Главная</a></li>
                    <li><a href="#about">О нас</a></li>
                    <li><a href="#services">Услуги</a></li>
                    <li><a href="#blog">Блог</a></li>
                    <li><a href="#contact">Контакты</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Психологическая помощь и поддержка</h1>
            <p>Мы помогаем обрести душевное равновесие и гармонию в жизни. Профессиональные психологи с многолетним опытом.</p>
            <a href="#contact" class="btn">Записаться на консультацию</a>
        </div>
    </section>

    <section id="about">
        <div class="container">
            <h2 class="section-title">О нашем центре</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Психологический центр "Гармония" работает с 2010 года, помогая людям справляться с жизненными трудностями, кризисами и психологическими проблемами.</p>
                    <p>Наша команда состоит из высококвалифицированных специалистов с опытом работы более 10 лет в различных направлениях психологии.</p>
                    <p>Мы создаем безопасное пространство, где каждый может получить поддержку, быть услышанным и найти решение своих проблем.</p>
                </div>
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1573497019940-1c28c88b4f3e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Психолог и клиент">
                </div>
            </div>
        </div>
    </section>

    <section id="services" style="background-color: #f1f1f1;">
        <div class="container">
            <h2 class="section-title">Наши услуги</h2>
            <div class="services">
                <div class="service-card">
                    <i class="fas fa-heart"></i>
                    <h3>Индивидуальная терапия</h3>
                    <p>Работа один на один с психологом, направленная на решение личных проблем, тревожности, депрессии и других состояний.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-users"></i>
                    <h3>Семейная терапия</h3>
                    <p>Помощь в решении конфликтов между партнерами, родителями и детьми, улучшение коммуникации в семье.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-child"></i>
                    <h3>Детская психология</h3>
                    <p>Специализированная помощь детям и подросткам в адаптации, обучении, решении возрастных кризисов.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-briefcase"></i>
                    <h3>Профориентация</h3>
                    <p>Помощь в выборе профессии, определении своих сильных сторон и карьерных возможностей.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-hand-holding-heart"></i>
                    <h3>Кризисная поддержка</h3>
                    <p>Экстренная психологическая помощь в сложных жизненных ситуациях, после травмирующих событий.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-brain"></i>
                    <h3>Тренинги и группы</h3>
                    <p>Групповые занятия по развитию эмоционального интеллекта, уверенности, стрессоустойчивости.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="blog">
        <div class="container">
            <h2 class="section-title">Психологический блог</h2>
            <div class="blog-posts">
                <div class="post-card">
                    <div class="post-img">
                        <img src="https://images.unsplash.com/photo-1493612276216-ee3925520721?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Стресс">
                    </div>
                    <div class="post-content">
                        <h3>Как справляться со стрессом на работе</h3>
                        <span class="post-meta">15 мая 2023 • Психология труда</span>
                        <p>Практические советы по снижению уровня стресса в профессиональной деятельности.</p>
                        <a href="#" class="btn" style="padding: 0.5rem 1rem; font-size: 0.9rem;">Читать далее</a>
                    </div>
                </div>
                <div class="post-card">
                    <div class="post-img">
                        <img src="https://images.unsplash.com/photo-1516589178581-6cd7833ae3b2?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Отношения">
                    </div>
                    <div class="post-content">
                        <h3>5 признаков здоровых отношений</h3>
                        <span class="post-meta">10 мая 2023 • Семейная психология</span>
                        <p>Как понять, что ваши отношения развиваются в правильном направлении.</p>
                        <a href="#" class="btn" style="padding: 0.5rem 1rem; font-size: 0.9rem;">Читать далее</a>
                    </div>
                </div>
                <div class="post-card">
                    <div class="post-img">
                        <img src="https://images.unsplash.com/photo-1506126613408-eca07ce68773?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Дети">
                    </div>
                    <div class="post-content">
                        <h3>Воспитание без наказаний: миф или реальность?</h3>
                        <span class="post-meta">5 мая 2023 • Детская психология</span>
                        <p>Альтернативные методы воспитания, которые помогут сохранить доверительные отношения с ребенком.</p>
                        <a href="#" class="btn" style="padding: 0.5rem 1rem; font-size: 0.9rem;">Читать далее</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" style="background-color: #f1f1f1;">
        <div class="container">
            <h2 class="section-title">Записаться на консультацию</h2>
            <div class="contact-form">
                <form>
                    <div class="form-group">
                        <label for="name">Ваше имя</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">Телефон</label>
                        <input type="tel" id="phone" name="phone">
                    </div>
                    <div class="form-group">
                        <label for="service">Интересующая услуга</label>
                        <select id="service" name="service" style="width: 100%; padding: 0.8rem; border: 1px solid #ddd; border-radius: 5px; font-size: 1rem;">
                            <option value="">-- Выберите услугу --</option>
                            <option value="individual">Индивидуальная терапия</option>
                            <option value="family">Семейная терапия</option>
                            <option value="children">Детская психология</option>
                            <option value="career">Профориентация</option>
                            <option value="crisis">Кризисная поддержка</option>
                            <option value="trainings">Тренинги и группы</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="message">Ваше сообщение</label>
                        <textarea id="message" name="message"></textarea>
                    </div>
                    <button type="submit" class="btn" style="border: none; cursor: pointer; width: 100%;">Отправить</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="logo" style="font-size: 2rem; margin-bottom: 1rem;">Гармония</div>
            <ul class="footer-links">
                <li><a href="#home">Главная</a></li>
                <li><a href="#about">О нас</a></li>
                <li><a href="#services">Услуги</a></li>
                <li><a href="#blog">Блог</a></li>
                <li><a href="#contact">Контакты</a></li>
            </ul>
            <p>г. Москва, ул. Психологическая, 15</p>
            <p>Телефон: +7 (495) 123-45-67</p>
            <p>Email: info@garmonia-psy.ru</p>
            <div style="margin-top: 1.5rem;">
                <a href="#" style="color: white; margin: 0 0.5rem; font-size: 1.5rem;"><i class="fab fa-vk"></i></a>
                <a href="#" style="color: white; margin: 0 0.5rem; font-size: 1.5rem;"><i class="fab fa-telegram"></i></a>
                <a href="#" style="color: white; margin: 0 0.5rem; font-size: 1.5rem;"><i class="fab fa-instagram"></i></a>
            </div>
            <p style="margin-top: 2rem; font-size: 0.9rem; color: #aaa;">© 2023 Психологический центр "Гармония". Все права защищены.</p>
        </div>
    </footer>
</body>
</html>
