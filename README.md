<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Un petit message pour toi...</title>
    <style>
        body {
            background-color: #ffebee;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
        }

        /* Style de l'enveloppe */
        .envelope-wrapper {
            cursor: pointer;
            transition: transform 0.3s;
        }
        .envelope-wrapper:hover { transform: scale(1.1); }
        .envelope { font-size: 100px; }
        .instruction { margin-top: 20px; color: #d32f2f; font-weight: bold; }

        /* Le contenu caché au début */
        #mainContent { display: none; text-align: center; }
        
        h1 { color: #d32f2f; }
        .buttons { margin-top: 20px; position: relative; height: 100px; }
        button {
            padding: 15px 25px;
            font-size: 18px;
            cursor: pointer;
            border: none;
            border-radius: 10px;
            margin: 10px;
        }
        #yesBtn { background-color: #ff5252; color: white; }
        #noBtn { background-color: #9e9e9e; color: white; position: absolute; }
        img { width: 250px; border-radius: 15px; }
    </style>
</head>
<body>

    <div id="envelopeArea" onclick="openLetter()">
        <div class="envelope-wrapper">
            <div class="envelope">✉️</div>
            <div class="instruction">Tu as reçu une lettre... Clique pour l'ouvrir</div>
        </div>
    </div>

    <div id="mainContent">
        <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOHp6eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/c76IJLufpNUMo/giphy.gif" alt="Mignon">
        <h1>Veux-tu être ma Valentine ? ❤️</h1>
        <div class="buttons">
            <button id="yesBtn" onclick="celebrate()">OUI !</button>
            <button id="noBtn" onmouseover="moveButton()">Non</button>
        </div>
    </div>

    <script>
        function openLetter() {
            document.getElementById('envelopeArea').style.display = 'none';
            document.getElementById('mainContent').style.display = 'block';
        }

        function moveButton() {
            const x = Math.random() * (window.innerWidth - 150);
            const y = Math.random() * (window.innerHeight - 150);
            const btn = document.getElementById('noBtn');
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';
        }

        function celebrate() {
            document.getElementById('mainContent').innerHTML = `
                <h1>YAY ! ❤️ J'ai trop hâte !</h1>
                <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbmZ4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/l41lH4ADRtAYnGsLe/giphy.gif">
                <h2>On se voit le 14 ! 🌹✨</h2>
            `;
        }
    </script>
</body>
</html>
