
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EmmNeDy Portfolio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }
        .container:hover {
            transform: scale(1.05);
        }
        .title {
            font-size: 24px;
            margin-bottom: 10px;
        }
        .content {
            font-size: 16px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="title">Welcome to My Portfolio</div>
        <div class="content">
            <p>Hover over this box to see the animation!</p>
        </div>
    </div>
</body>
</html>
