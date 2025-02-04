<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nisha, Be My Valentine?</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

        body {
            background-color: black;
            text-align: center;
            color: white;
            font-family: 'Pacifico', cursive;
            overflow: hidden;
        }

        h1 {
            font-size: 3em;
            margin-top: 50px;
            color: #ffcc00;
            text-shadow: 3px 3px 5px rgba(255, 255, 255, 0.5);
        }

        .dots {
            color: red;
            font-size: 1.2em;
        }

        .message {
            font-size: 1.5em;
            margin-top: 20px;
            color: white;
        }

        .button {
            display: inline-block;
            background-color: #ff4500;
            color: white;
            padding: 15px 30px;
            font-size: 1.5em;
            border-radius: 10px;
            margin-top: 30px;
            text-decoration: none;
            box-shadow: 0px 4px 6px rgba(255, 255, 255, 0.5);
            cursor: pointer;
        }

        .button:hover {
            background-color: #e63946;
        }

        .heart {
            position: absolute;
            color: red;
            font-size: 2rem;
            animation: floatUp 3s linear infinite;
            opacity: 0;
        }

        @keyframes floatUp {
            0% {
                transform: translateY(0);
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh);
                opacity: 0;
            }
        }
    </style>
</head>
<body>
    <h1>N<span class="dots">●</span>I<span class="dots">●</span>S<span class="dots">●</span>H<span class="dots">●</span>A</h1>
    <p class="message">Will you be my Valentine?</p>
    <button class="button" onclick="showHearts()">YES!</button>

    <script>
        function showHearts() {
            for (let i = 0; i < 50; i++) {
                let heart = document.createElement('div');
                heart.innerHTML = '❤️';
                heart.classList.add('heart');
                document.body.appendChild(heart);

                let x = Math.random() * window.innerWidth;
                let y = window.innerHeight;

                heart.style.left = x + 'px';
                heart.style.top = y + 'px';
                heart.style.fontSize = Math.random() * 2 + 1 + 'rem';
                heart.style.animationDuration = Math.random() * 3 + 2 + 's';

                setTimeout(() => {
                    heart.remove();
                }, 3000);
            }
        }
    </script>
</body>
</html>
