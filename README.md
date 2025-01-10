<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #000000, #ffffff); /* Black to white gradient */
            color: #fff;
            text-align: center;
            padding: 20px;
        }
        h1 {
            font-size: 3em;
            margin-top: 50px;
        }
        p {
            font-size: 1.2em;
        }
        .form-container {
            margin-top: 30px;
        }
        input[type="text"] {
            padding: 10px;
            font-size: 1em;
            border: none;
            border-radius: 5px;
            margin-right: 10px;
        }
        button {
            padding: 10px 20px;
            font-size: 1em;
            background-color: #4caf50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        .welcome-message {
            margin-top: 50px;
            font-size: 2em;
            display: none; /* Hidden by default */
        }
    </style>
</head>
<body>
    <h1>Welcome to My Page!</h1>
    <p>Enter your name below to receive a welcome gift From Rafeu. 😊</p>

    <div class="form-container">
        <input type="text" id="nameInput" placeholder="Enter your name">
        <button onclick="displayWelcome()">Submit</button>
    </div>

    <div class="welcome-message" id="welcomeMessage">
        <p id="greeting"></p>
    </div>

    <script>
        function displayWelcome() {
            // Get the name entered by the user
            const name = document.getElementById("nameInput").value;

            // Display the welcome message
            if (name) {
                const welcomeMessage = document.getElementById("welcomeMessage");
                const greeting = document.getElementById("greeting");
                greeting.textContent = `Welcome, ${name}! 🌟 I am so happy to see you here!`;
                welcomeMessage.style.display = "block"; // Show the message
            } else {
                alert("Please enter your name! 😊");
            }
        }
    </script>
</body>
</html>
