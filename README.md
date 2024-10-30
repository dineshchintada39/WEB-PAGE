
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Diwali</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #87CEEB;
            margin: 0;
        }

        .container {
            text-align: center;
            background-color: #ea8dce;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            filter: drop-shadow(1px 1px 20px rgb(244, 243, 244));
            width: 90%;
            max-width: 400px;
        }

        h1 {
            font-size: 2.5em;
            color: white;
            margin-bottom: 10px;
            font-family: 'Sacramento', cursive;
            text-shadow: 2px 2px 4px rgb(34, 33, 34);
        }

        p {
            font-size: 1.2em;
            color: #333;
        }

        form {
            margin-top: 15px;
        }

        input[type="text"] {
            padding: 10px;
            width: 80%;
            margin-bottom: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1em;
        }

        button {
            padding: 10px 20px;
            background-color: #32CD32;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1em;
        }

        button:hover {
            background-color: #228B22;
        }

        .hidden {
            display: none;
        }

        #greeting {
            margin-top: 15px;
            font-size: 1.5em;
            color: #ffffff;
            text-shadow: 2px 2px 4px rgb(34, 33, 34);

        }

        .submit {
            text-decoration: none;
        }

        /* Mobile view adjustments */
        @media (max-width: 600px) {
            h1 {
                font-size: 2em;
            }
            p {
                font-size: 1em;
            }
            input[type="text"] {
                width: 100%;
            }
            button {
                width: 100%;
                padding: 10px;
            }
            #greeting {
                font-size: 1.2em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Best Wishes</h1>
        <p>Enter your name to receive a Diwali greeting:</p>
        <form id="nameForm">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" placeholder="Enter your name" required>
            <button type="submit" class="submit">Submit</button>
        </form>
        <p id="greeting" class="hidden">Happy Diwali, <span id="userName"></span>!</p>
    </div>

    <script>
        document.getElementById("nameForm").addEventListener("submit", function(event) {
            event.preventDefault();
            var name = document.getElementById("name").value;
            if (name) {
                document.getElementById("userName").textContent = name;
                document.getElementById("greeting").classList.remove("hidden");
            }
        });
    </script>
</body>


