# Winter 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Winter Activities</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            background: linear-gradient(45deg, #e0f7fa, #0288d1);
            color: #fff;
            padding: 20px;
            margin: 0;
            overflow: hidden;
            position: relative;
        }
        h1 {
            color: #fff;
            font-size: 2.5em; /* Reduced font size */
            margin-bottom: 20px; /* Reduced margin */
            font-family: 'Georgia', serif;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
        }
        .bubble {
            display: inline-block;
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: linear-gradient(145deg, #0288d1, #03a9f4);
            color: white;
            text-align: center;
            line-height: 120px;
            margin: 20px;
            cursor: pointer;
            font-size: 1.2em;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease, background-color 0.3s ease;
            animation: bubbleAnimation 4s infinite ease-in-out;
        }
        .bubble:hover {
            transform: scale(1.2);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            background-color: #0288d1;
        }
        .bubble i {
            font-size: 2em;
            transition: transform 0.3s ease;
        }
        .bubble:hover i {
            transform: rotate(20deg);
        }
        .activity-list {
            display: none;
            margin-top: 30px;
            animation: fadeIn 1s ease-in-out;
        }
        .active {
            display: block;
            animation: slideIn 0.5s ease-out;
        }
        @keyframes fadeIn {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }
        @keyframes slideIn {
            0% { transform: translateY(20px); opacity: 0; }
            100% { transform: translateY(0); opacity: 1; }
        }
        @keyframes bubbleAnimation {
            0% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0); }
        }
        .activity-list ul {
            list-style-type: none;
            padding: 0;
        }
        .activity-list li {
            font-size: 1.5em;
            margin: 10px 0;
            background-color: rgba(255, 255, 255, 0.1);
            padding: 10px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: background-color 0.3s ease;
        }
        .activity-list li:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }
        .floating-bubbles {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            animation: floatingBubbles 5s infinite ease-in-out;
        }
        @keyframes floatingBubbles {
            0% { opacity: 0.2; transform: translate(-50%, -50%) scale(0.8); }
            50% { opacity: 0.8; transform: translate(-50%, -50%) scale(1.2); }
            100% { opacity: 0.2; transform: translate(-50%, -50%) scale(0.8); }
        }
        .floating-bubbles div {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.4);
            position: absolute;
            animation: floatBubble 5s infinite ease-in-out;
        }
        .floating-bubbles div:nth-child(1) { left: 20%; animation-delay: 0s; }
        .floating-bubbles div:nth-child(2) { left: 40%; animation-delay: 1s; }
        .floating-bubbles div:nth-child(3) { left: 60%; animation-delay: 2s; }
        .floating-bubbles div:nth-child(4) { left: 80%; animation-delay: 3s; }

        @keyframes floatBubble {
            0% { transform: translateY(0); opacity: 0.5; }
            50% { transform: translateY(-30px); opacity: 1; }
            100% { transform: translateY(0); opacity: 0.5; }
        }
    </style>
    <script>
        function toggleActivities(category) {
            var list = document.getElementById(category);
            list.classList.toggle('active');
        }
    </script>
</head>
<body>
    <h1>Ways to Stay Active & Get Outdoors This Winter</h1>
    <div class="floating-bubbles">
        <div></div><div></div><div></div><div></div>
    </div>

    <div class="bubble" onclick="toggleActivities('outdoor')">
        <i class="fas fa-snowflake"></i><br>Outdoor Activities
    </div>

    <div id="outdoor" class="activity-list">
        <h2>Outdoor Activities</h2>
        <ul>
            <li>Snowshoeing</li>
            <li>Skiing</li>
            <li>Ice Skating</li>
            <li>Snowball Fight</li>
            <li>Winter Hiking</li>
            <li>Sledding</li>
        </ul>
    </div>
</body>
</html>
