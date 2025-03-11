
 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phrasal Verbs: Sleep & Energy</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            text-align: center;
            padding: 20px;
        }
        .container {
            background: #ffffff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
            max-width: 600px;
            margin: auto;
        }
        h1 {
            color: #4CAF50;
        }
        .question {
            margin: 15px 0;
            font-size: 18px;
        }
        input {
            padding: 5px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 5px;
            width: 60%;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 15px;
            margin-top: 15px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 5px;
        }
        button:hover {
            background-color: #45a049;
        }
        .result {
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
        }
        .correct {
            color: green;
        }
        .incorrect {
            color: red;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Phrasal Verbs: Sleep & Energy 🌙⚡</h1>
        <p>Fill in the blanks with the correct phrasal verb. (Use: burn out, calm down, chill out, doze off, perk up, race off, sleep over, turn in)</p>
        
        <div class="question">1. I was so tired that I started to _______ during the meeting. 😴 <br>
            <input type="text" id="q1">
        </div>
        <div class="question">2. She was very stressed, so I told her to _______ and relax. 🧘‍♀️ <br>
            <input type="text" id="q2">
        </div>
        <div class="question">3. He was exhausted and completely _______ after working too much. 🔥 <br>
            <input type="text" id="q3">
        </div>
        <div class="question">4. I need to _______ early tonight because I have a big day tomorrow. 🛏️ <br>
            <input type="text" id="q4">
        </div>
        <div class="question">5. The coffee really helped me _______ this morning! ☕ <br>
            <input type="text" id="q5">
        </div>
        <div class="question">6. They decided to _______ at their friend's house after the party. 🏡 <br>
            <input type="text" id="q6">
        </div>
        <div class="question">7. He had no time to talk, he just _______ to his next meeting. 🏃‍♂️ <br>
            <input type="text" id="q7">
        </div>
        <div class="question">8. When the baby started crying, she tried to _______ and put him to sleep. 🤱 <br>
            <input type="text" id="q8">
        </div>
        
        <button onclick="checkAnswers()">Check Answers ✅</button>
        
        <div id="result" class="result"></div>
    </div>

    <script>
        function checkAnswers() {
            let answers = [
                "doze off", "chill out", "burn out", "turn in", "perk up", 
                "sleep over", "race off", "calm down"
            ];
            let score = 0;
            let feedback = "<p>Correct Answers:</p>";
            
            for (let i = 1; i <= 8; i++) {
                let userAnswer = document.getElementById("q" + i).value.trim().toLowerCase();
                let correctAnswer = answers[i - 1];
                if (userAnswer === correctAnswer) {
                    feedback += `<p class='correct'>${i}. ${userAnswer} ✅</p>`;
                    score++;
                } else {
                    feedback += `<p class='incorrect'>${i}. ${userAnswer || "(blank)"} ❌ (Correct: ${correctAnswer})</p>`;
                }
            }
            
            if (score === 8) {
                feedback = "🌟 Excellent! You got all answers correct! 🌟<br>" + feedback;
            } else if (score >= 5) {
                feedback = `👍 Good job! You got ${score}/8 correct. Keep practicing!<br>` + feedback;
            } else {
                feedback = `💡 You got ${score}/8 correct. Try again and review the phrasal verbs!<br>` + feedback;
            }
            
            document.getElementById("result").innerHTML = feedback;
        }
    </script>
</body>
</html>
