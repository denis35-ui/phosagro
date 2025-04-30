<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Пример сайта</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-size: cover;
            background-position: center;
        }
        header {
            background: rgba(76, 175, 80, 0.7); /* Полупрозрачный фон для заголовка */
            color: #fff;
            padding: 10px 0;
            text-align: center;
        }
        nav {
            margin: 20px 0;
        }
        nav a {
            margin: 0 15px;
            color: #4CAF50;
            text-decoration: none;
        }
        .container {
            max-width: 800px;
            margin: auto;
            padding: 20px;
            background: rgba(255, 255, 255, 0.9); /* Полупрозрачный фон для контейнера */
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        footer {
            text-align: center;
            padding: 10px 0;
            background: rgba(76, 175, 80, 0.7); /* Полупрозрачный фон для подвала */
            color: white;
            position: relative;
            bottom: 0;
            width: 100%;
            
        }
        .login-button {
            padding: 10px 20px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
        }
        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.4);
            padding-top: 60px;
        }
        .modal-content {
            background-color: #fefefe;
            margin: 5% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 300px;
            border-radius: 5px;
        }
        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
        }
        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
    <script>
        function openLoginModal() {
            document.getElementById('loginModal').style.display = 'block';
        }

        function closeLoginModal() {
            document.getElementById('loginModal').style.display = 'none';
        }

        window.onclick = function(event) {
            if (event.target == document.getElementById('loginModal')) {
                closeLoginModal();
            }
        }
    </script>
</head>
<body>

<header>
    <h1>Добро пожаловать на наш сайт</h1>
</header>

<nav>
    
    <button class="login-button" onclick="openLoginModal()">Вход</button>
</nav>

<div class="container">
    <section id="about">
        <h2>О нас</h2>
        <p>Здесь вы найдете информацию о нашей компании.</p>
    </section>

    <section id="services">
        <h2>Услуги</h2>
        <p>Мы предоставляем широкий спектр услуг для наших клиентов.</p>
    </section>

    <section id="contact">
        <h2>Контакты</h2>
        <p>Свяжитесь с нами по электронной почте: info@example.com</p>
    </section>
</div>

<footer>
    <p>&copy; 2025 ProАгро 
     <a href="http://lection.phosagra.ru">Перейти на сайт</a></p>
</footer>

<div id="loginModal" class="modal">
    <div class="modal-content">
        <span class="close" onclick="closeLoginModal()">&times;</span>
        <h2>Вход</h2>
        <label for="email">Электронная почта:</label><br>
        <input type="email" id="email" placeholder="Введите вашу почту"><br>
        <label for="password">Пароль:</label><br>
        <input type="password" id="password" placeholder="Введите ваш пароль"><br><br>
        <button class="login-button">Войти</button>
    </div>
</div>

</body>
</html>
