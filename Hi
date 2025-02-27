<!DOCTYPE html>
<html>
<head>
    <title>For My Amazing Nica 💖</title>
    <style>
        body {
            margin: 0;
            height: 100vh;
            overflow: hidden;
            background: linear-gradient(45deg, #ff69b4, #ff1493, #ff007f);
            animation: bgAnim 15s infinite;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Arial', sans-serif;
        }

        .container {
            text-align: center;
            position: relative;
            z-index: 2;
        }

        h1 {
            color: white;
            font-size: 4em;
            text-shadow: 3px 3px 0px #ff007f;
            margin-bottom: 20px;
            animation: fadeIn 2s;
        }

        .message {
            color: white;
            font-size: 1.5em;
            max-width: 600px;
            margin: 0 auto;
            position: relative;
        }

        .heart {
            position: absolute;
            color: #ff69b4;
            animation: float 6s infinite;
            opacity: 0;
        }

        @keyframes bgAnim {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        @keyframes float {
            0% { transform: translateY(0) scale(0.5); opacity: 0; }
            50% { opacity: 1; }
            100% { transform: translateY(-100vh) scale(1.5); opacity: 0; }
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .secret-btn {
            margin-top: 30px;
            padding: 15px 30px;
            font-size: 1.2em;
            background: rgba(255,255,255,0.2);
            border: 2px solid white;
            color: white;
            border-radius: 50px;
            cursor: pointer;
            transition: 0.3s;
        }

        .secret-btn:hover {
            background: rgba(255,255,255,0.3);
            transform: scale(1.1);
        }

        #typing-effect {
            border-right: 2px solid white;
            padding-right: 5px;
            animation: blink 0.5s infinite;
        }

        @keyframes blink {
            0%, 100% { border-color: transparent; }
            50% { border-color: white; }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Nica, You're Amazing! 💖</h1>
        <div class="message" id="main-message"></div>
        <button class="secret-btn" onclick="showSurprise()">Click for Magic!</button>
    </div>

    <script>
        // Typing effect for main message
        const messages = [
            "Every moment with you feels like a beautiful dream...",
            "Your smile lights up my world brighter than any star ✨",
            "You're the most incredible person I've ever known 💫",
            "I feel so lucky to have you in my life 🌟",
            "You make my heart beat faster than any code could ❤️"
        ];

        let msgIndex = 0;
        let charIndex = 0;
        const messageElement = document.getElementById('main-message');

        function typeMessage() {
            if (charIndex < messages[msgIndex].length) {
                messageElement.innerHTML = messages[msgIndex].substring(0, charIndex + 1) + '<span id="typing-effect"></span>';
                charIndex++;
                setTimeout(typeMessage, 50);
            } else {
                setTimeout(nextMessage, 2000);
            }
        }

        function nextMessage() {
            msgIndex = (msgIndex + 1) % messages.length;
            charIndex = 0;
            typeMessage();
        }

        // Create floating hearts
        function createHeart() {
            const heart = document.createElement('div');
            heart.innerHTML = '❤️';
            heart.className = 'heart';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = (Math.random() * 3 + 3) + 's';
            document.body.appendChild(heart);
            
            setTimeout(() => heart.remove(), 6000);
        }

        // Surprise function
        function showSurprise() {
            for(let i = 0; i < 100; i++) {
                setTimeout(() => {
                    createHeart();
                    if(i % 10 === 0) {
                        document.body.style.background = `hsl(${Math.random() * 360}, 70%, 60%)`;
                    }
                }, i * 30);
            }
            
            const btn = document.querySelector('.secret-btn');
            btn.innerHTML = "You're My Favorite Person! 🌈";
            setTimeout(() => btn.innerHTML = "Click Again for More Magic!", 3000);
        }

        // Start animations
        setInterval(createHeart, 300);
        typeMessage();

        // Add background animation
        document.body.style.backgroundSize = "400% 400%";
    </script>
</body>
</html>
