<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Une petite question...</title>
    <style>
        body {
            background-color: #ffebee;
            font-family: 'Arial', sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            text-align: center;
        }
        h1 { color: #d32f2f; }
        .buttons { margin-top: 20px; }
        button {
            padding: 15px 25px;
            font-size: 18px;
            cursor: pointer;
            border: none;
            border-radius: 10px;
            margin: 10px;
            transition: 0.3s;
        }
        #yesBtn { background-color: #ff5252; color: white; }
        #noBtn { background-color: #9e9e9e; color: white; position: absolute; }
        .gif-container img { width: 250px; border-radius: 15px; }
    </style>
</head>
<body>

    <div class="gif-container">
        <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOHp6eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/c76IJLufpNUMo/giphy.gif" alt="Mignon">
    </div>

    <h1>Veux-tu être ma Valentine Stessy ? ❤️</h1>

    <div class="buttons">
        <button id="yesBtn" onclick="celebrate()">OUI !</button>
        <button id="noBtn" onmouseover="moveButton()">Non</button>
    </div>

    <script>
        function moveButton() {
            const x = Math.random() * (window.innerWidth - 100);
            const y = Math.random() * (window.innerHeight - 50);
            const btn = document.getElementById('noBtn');
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';
        }

        function celebrate() {
            alert("YAY ! ❤️ J'ai trop hâte !");
            document.body.innerHTML = "<h1>On se voit le 14 ! 🌹✨</h1><img src='https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbmZ4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/l41lH4ADRtAYnGsLe/giphy.gif'>";
        }
    </script>
</body>
</html>
