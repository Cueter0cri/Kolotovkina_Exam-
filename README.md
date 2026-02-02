# Kolotovkina_Exam-
Исип-33
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>IT-Блог</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- Внешние стили -->
    <link rel="stylesheet" href="style.css">
</head>
<body>

<header class="header">
    <div class="header__container">
        <a href="#" class="logo">IT-Блог</a>

        <!-- Бургер -->
        <button class="burger" id="burger">
            <span></span>
            <span></span>
            <span></span>
        </button>

        <nav class="nav" id="nav">
            <a href="#">Главная</a>
            <a href="#">Статьи</a>
            <a href="#">О проекте</a>
            <a href="#">Контакты</a>
        </nav>
    </div>
    <hr>
</header>

<main class="main fade-in">
    <h1>Последние статьи</h1>

    <section class="articles">
        <article class="article">
            <img src="images/article_1.jpg" alt="Статья 1">
            <h2>Заголовок статьи 1</h2>
            <p>Краткое описание статьи. Несколько предложений для примера текста.</p>
            <a href="#" class="btn">Читать далее...</a>
        </article>

        <article class="article">
            <img src="images/article_2.jpg" alt="Статья 2">
            <h2>Заголовок статьи 2</h2>
            <p>Краткое описание статьи. Несколько предложений для примера текста.</p>
            <a href="#" class="btn">Читать далее...</a>
        </article>

        <article class="article">
            <img src="images/article_3.jpg" alt="Статья 3">
            <h2>Заголовок статьи 3</h2>
            <p>Краткое описание статьи. Несколько предложений для примера текста.</p>
            <a href="#" class="btn">Читать далее...</a>
        </article>

        <article class="article">
            <img src="images/article_4.jpg" alt="Статья 4">
            <h2>Заголовок статьи 4</h2>
            <p>Краткое описание статьи. Несколько предложений для примера текста.</p>
            <a href="#" class="btn">Читать далее...</a>
        </article>
    </section>
</main>

<footer class="footer">
    <hr>
    <div class="footer__content">
        <p>© IT-Блог, 2026. Все права защищены.</p>

        <ul class="socials">
            <li><a href="https://site.com"><img src="images/vk.png" alt="VK"></a></li>
            <li><a href="https://site.com"><img src="images/rutube.png" alt="RuTube"></a></li>
            <li><a href="https://site.com"><img src="images/telegram.png" alt="Telegram"></a></li>
        </ul>
    </div>
</footer>

<!-- Модальное окно -->
<div class="modal" id="modal">
    <span class="modal__close" id="modalClose">&times;</span>
    <img class="modal__img" id="modalImg">
</div>

<script src="script.js"></script>
</body>
</html>



/* =========================
   СБРОС И ПЕРЕМЕННЫЕ
========================= */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    --primary: #2c3e50;
    --accent: #3498db;
    --bg: #f4f6f8;
    --text: #333;
    --radius: 10px;
    --transition: 0.3s ease;
}

body {
    font-family: Arial, sans-serif;
    background-color: var(--bg);
    color: var(--text);
}

/* =========================
   HEADER
========================= */
.header {
    background: #fff;
}

.header__container {
    max-width: 1200px;
    margin: auto;
    padding: 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.logo {
    font-size: 24px;
    font-weight: bold;
    color: var(--primary);
    text-decoration: none;
}

.nav {
    display: flex;
    gap: 20px;
}

.nav a {
    text-decoration: none;
    color: var(--primary);
    transition: var(--transition);
}

.nav a:hover {
    color: var(--accent);
}

/* Бургер */
.burger {
    display: none;
    flex-direction: column;
    gap: 5px;
    background: none;
    border: none;
    cursor: pointer;
}

.burger span {
    width: 25px;
    height: 3px;
    background: var(--primary);
}

/* =========================
   MAIN
========================= */
.main {
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
}

h1 {
    margin-bottom: 30px;
}

/* Grid */
.articles {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
}

.article {
    background: #fff;
    padding: 15px;
    border-radius: var(--radius);
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    transition: var(--transition);
}

.article:hover {
    box-shadow: 0 10px 25px rgba(0,0,0,0.15);
}

.article img {
    width: 100%;
    border-radius: var(--radius);
    cursor: pointer;
    transition: var(--transition);
}

.article img:hover {
    transform: scale(1.03);
}

.article h2 {
    margin: 15px 0 10px;
}

.article p {
    margin-bottom: 15px;
}

.btn {
    display: block;
    text-align: center;
    background: var(--accent);
    color: #fff;
    padding: 10px;
    border-radius: var(--radius);
    text-decoration: none;
    transition: var(--transition);
}

.btn:hover {
    background: #217dbb;
}

/* =========================
   FOOTER
========================= */
.footer {
    background: #fff;
    margin-top: 40px;
}

.footer__content {
    max-width: 1200px;
    margin: auto;
    padding: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.socials {
    display: flex;
    gap: 15px;
    list-style: none;
}

.socials img {
    width: 24px;
}

/* =========================
   MODAL
========================= */
.modal {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.8);
    justify-content: center;
    align-items: center;
}

.modal__img {
    max-width: 90%;
    max-height: 90%;
}

.modal__close {
    position: absolute;
    top: 20px;
    right: 30px;
    font-size: 40px;
    color: #fff;
    cursor: pointer;
}

/* =========================
   АНИМАЦИИ
========================= */
.fade-in {
    animation: fade 0.8s ease;
}

@keyframes fade {
    from { opacity: 0; }
    to { opacity: 1; }
}

/* =========================
   АДАПТИВ
========================= */
@media (max-width: 1024px) {
    .articles {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 768px) {
    .articles {
        grid-template-columns: 1fr;
    }

    .nav {
        position: absolute;
        top: 70px;
        right: 0;
        background: #fff;
        flex-direction: column;
        width: 200px;
        padding: 20px;
        display: none;
    }

    .nav.active {
        display: flex;
    }

    .burger {
        display: flex;
    }
}



// Бургер-меню
const burger = document.getElementById('burger');
const nav = document.getElementById('nav');

burger.addEventListener('click', () => {
    nav.classList.toggle('active');
});

// Галерея
const images = document.querySelectorAll('.article img');
const modal = document.getElementById('modal');
const modalImg = document.getElementById('modalImg');
const modalClose = document.getElementById('modalClose');

images.forEach(img => {
    img.addEventListener('click', () => {
        modal.style.display = 'flex';
        modalImg.src = img.src;
    });
});

modalClose.addEventListener('click', () => {
    modal.style.display = 'none';
});

modal.addEventListener('click', (e) => {
    if (e.target === modal) {
        modal.style.display = 'none';
    }
});
