<!DOCTYPE html>
<html>
<head>
    <title>8 Ball</title>
    <style>
        body {
            text-align: center;
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
        }
        h1 {
            color: #333333;
            margin-top: 50px;
        }   
        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-top: 50px;
        }
        input[type="text"] {
            width: 300px;
            height: 30px;
            padding: 5px;
            font-size: 16px;
            margin-bottom: 20px;
        }
        .btn {
            padding: 10px 20px;
            font-size: 18px;
            font-weight: bold;
            text-transform: uppercase;
            background-color: #ff4d4d;
            color: #ffffff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .btn:hover {
            background-color: #ff3333;
        }
        .answer {
            margin-top: 30px;
            font-size: 20px;
            color: #333333;
        }
    </style>
    <script>
        function shake() {
            var question = document.getElementById("question").value;
            var answers = [
                "It is certain.",
                "It is decidedly so.",
                "Without a doubt.",
                "Yes, definitely.",
                "You may rely on it.",
                "As I see it, yes.",
                "Most likely.",
                "Outlook good.",
                "Yes.",
                "Signs point to yes.",
                "Reply hazy, try again.",
                "Ask again later.",
                "Better not tell you now.",
                "Cannot predict now.",
                "Concentrate and ask again.",
                "Don't count on it.",
                "My reply is no.",
                "My sources say no.",
                "Outlook not so good.",
                "Very doubtful."
                "Idk."
                "Nah."
            ];
            var randomIndex = Math.floor(Math.random() * answers.length);
            var answer = answers[randomIndex];
            document.getElementById("answer").innerHTML = answer;
        }
    </script>
</head>
<body>
    <div class="container">
        <h1>8 Ball</h1>
        <input type="text" id="question" placeholder="Ask a Question">
        <button class="btn" onclick="shake()">Shake</button>
        <div id="answer" class="answer"></div>
    </div>
</body>
</html>
