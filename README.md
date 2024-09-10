<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title><b>EmmNeDy</b> Portfolio Under Maintenance</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #e0f7fa;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            flex-direction: column;
        }
        .container {
            text-align: center;
        }
        .title {
            font-size: 36px;
            color: #00796b;
        }
        .message {
            font-size: 18px;
            color: #004d40;
        }
        .animation {
            width: 100px;
            height: 100px;
            border: 10px solid #00897b;
            border-top: 10px solid #004d40;
            border-radius: 50%;
            animation: spin 2s linear infinite;
            margin: 20px auto;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        .game {
            margin-top: 20px;
        }
        
#gameCanvas {
    border: 1px solid #00897b;
    background-color: #ffffff;
    position: relative;
}

#gameCanvas::before {
    content: "EmmReX";
    color: #00796b;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 20px; /* Adjust as needed */
    z-index: 1; /* Ensure it appears above the background */
    pointer-events: none; /* Ensure it doesn’t interfere with canvas interactions */
}
        #gameCanvas {
            border: 1px solid #00796b;
            background-color: #ffffff;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="animation"></div>
        <div class="title">Under Maintenance</div>
        <div class="message">portfolio belongs to <b>EmmNeDy</b>, aspiring Coder n Security Engineer , <p>I enjoy learning new Programming languages and exploring the world of Tech</p></div>
        <div class="message">We are currently working on something awesome. Stay tuned!</div>
        <div class="game">
            <div class="message">How about a game!</div>
            <canvas id="gameCanvas" width="200" height="200"></canvas>
            <button onclick="startGame()">Start Game</button>
        </div>
    </div>
    <script>
        let canvas = document.getElementById('gameCanvas');
        let context = canvas.getContext('2d');
        let x = canvas.width / 2;
        let y = canvas.height - 30;
        let dx = 2;
        let dy = -2;
        let ballRadius = 10;

function drawBall() {
            context.beginPath();
            context.arc(x, y, ballRadius, 0, Math.PI * 2);
            context.fillStyle = '#00796b';
            context.fill();
            context.closePath();
        }

function draw() {
            context.clearRect(0, 0, canvas.width, canvas.height);
            drawBall();
            if (x + dx > canvas.width - ballRadius || x + dx < ballRadius) {
                dx = -dx;
            }
            if (y + dy > canvas.height - ballRadius || y + dy < ballRadius) {
                dy = -dy;
            }
            x += dx;
            y += dy;
        }

function startGame() {
            setInterval(draw, 10);
        }
    </script>
</body>
</html>
