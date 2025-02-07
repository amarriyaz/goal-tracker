# goal-tracker
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Goal Progress Tracker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 20px;
        }
        .progress-container {
            width: 100%;
            max-width: 400px;
            background-color: #e0e0e0;
            border-radius: 25px;
            padding: 5px;
            margin: 20px auto;
        }
        .progress-bar {
            width: 0%;
            height: 30px;
            background-color: #7671EA;
            border-radius: 20px;
            transition: width 0.5s ease-in-out;
        }
        button {
            background-color: #7671EA;
            color: white;
            border: none;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
            font-size: 16px;
            border-radius: 5px;
        }
        button:disabled {
            background-color: #ccc;
        }
    </style>
</head>
<body>
    <h2>Goal Progress Tracker</h2>
    <div class="progress-container">
        <div class="progress-bar" id="progressBar"></div>
    </div>
    <p id="progressText">0%</p>
    <button onclick="increaseProgress()">Increase Progress</button>
    <button onclick="resetProgress()">Reset</button>

    <script>
        let progress = 0;

        function increaseProgress() {
            if (progress < 100) {
                progress += 10;
                document.getElementById("progressBar").style.width = progress + "%";
                document.getElementById("progressText").innerText = progress + "%";
            }
        }

        function resetProgress() {
            progress = 0;
            document.getElementById("progressBar").style.width = progress + "%";
            document.getElementById("progressText").innerText = progress + "%";
        }
    </script>
</body>
</html>
