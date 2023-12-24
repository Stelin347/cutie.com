
<html lang="en">
<head>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 90vh;
            background-color: #F8C8DC;
        }

        #noButton {
            position: absolute;
            margin-left: 150px;
            transition: 0.5s;
        }

        #yesButton {
            position: absolute;
            margin-right: 150px;
        }

        .header_text {
            font-family: 'Nunito';
            font-size: 40px;
            font-weight: bold;
            color: white;
            text-align: center;
            margin-top: 20px;
            margin-bottom: 0px;
        }

        .buttons {
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: center;
            margin-top: 20px;
            margin-left: 20px;
        }

        .btn {
            background-color: #FFB6C1;
            color: white;
            padding: 15px 32px;
            text-align: center;
            display: inline-block;
            font-size: 16px;
            margin: 4px 2px;
            cursor: pointer;
            border: none;
            border-radius: 12px;
            transition: background-color 0.3s ease;
        }

        .gif_container {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-left: 90px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div>
            <h1 class="header_text">cutie,please talk with me once i miss you so much</h1>
        </div>
        <div class="gif_container">
            <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExcDdtZ2JiZDR0a3lvMWF4OG8yc3p6Ymdvd3g2d245amdveDhyYmx6eCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/cLS1cfxvGOPVpf9g3y/giphy.gif" alt="Cute animated illustration">
        </div>
        <div class="buttons">
            <button class="btn" id="yesButton" onclick="nextPage()">Yes</button>
            <button class="btn" id="noButton" onmouseover="moveButton()" onclick="moveButton()">No</button>
            <script>
                function nextPage() {
                    window.location.href = "yes.html";
                }

                function moveButton() {
                    var x = Math.random() * (window.innerWidth - document.getElementById('noButton').offsetWidth);
                    var y = Math.random() * (window.innerHeight - document.getElementById('noButton').offsetHeight);
                    document.getElementById('noButton').style.left = `${x}px`;
                    document.getElementById('noButton').style.top = `${y}px`;
                }
            </script>
        </div>
    </div>
</body>
</html>
