<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday</title>
    <style>
        body, html {
            height: 100%;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #f0f0f0;
            font-family: 'Arial', sans-serif;
        }
        .container {
            text-align: center;
        }
        .birthday-wish {
            font-size: 3em;
            color: #ff4081;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        .image-container {
            position: relative;
            width: 100%; /* Ensure the image container takes full width */
            max-width: 500px; /* Set a maximum width for the image container */
            height: auto; /* Let the height adjust based on image size */
            overflow: hidden;
            margin-bottom: 20px;
            border-radius: 10px;
        }
        .image-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease-in-out;
            cursor: pointer;
        }
        .image-container img:hover {
            transform: scale(1.1);
        }
        .hidden-message {
            display: none;
            font-size: 2em;
            color: #333;
            font-weight: bold;
            text-align: center;
            animation: fadeIn 1s ease-in-out forwards;
        }
        .click-here {
            font-size: 1.2em;
            color: #333;
            cursor: pointer;
            text-decoration: underline;
            margin-bottom: 10px;
        }
        .click-here:hover {
            color: #ff4081;
        }
        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="click-here" onclick="showBirthdayWish()">Click here</div>
        <div class="hidden-message" id="message">Happy Birthday, Priya!<br>Wishing you a fantastic day filled with joy and laughter!</div>
        <div class="image-container" onclick="showBirthdayWish()">
            <img src="https://via.placeholder.com/500x300" alt="Birthday Image">
        </div>
    </div>

    <script>
        function showBirthdayWish() {
            var message = document.getElementById('message');
            message.style.display = 'block';
        }
    </script>
</body>
</html>
