<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #00b894;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .login-form {
            background-color: #2d3436;
            color: #ffffff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
            width: 300px;
            text-align: center;
        }

        .login-form h2 {
            margin-bottom: 20px;
        }

        .login-form input[type="email"],
        .login-form input[type="password"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .login-form button {
            width: 100%;
            padding: 10px;
            background-color: #00cec9;
            border: none;
            border-radius: 5px;
            color: #ffffff;
            font-size: 16px;
            cursor: pointer;
            margin-bottom: 10px;
        }

        .login-form button:hover {
            background-color: #0984e3;
        }

        .login-form a {
            color: #74b9ff;
            text-decoration: none;
        }

        .login-form a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <div class="login-form">
        <h2>Login Form</h2>
        <form id="loginForm">
            <input type="email" id="email" placeholder="Email Address" required>
            <input type="password" id="password" placeholder="Password" required>
            <button type="submit">Login</button>
            <div>
                <a href="#">Forgot password?</a>
            </div>
        </form>
        <p>Not a member? <a href="#">Sign up now</a></p>
    </div>

    <script>
        document.getElementById('loginForm').addEventListener('submit', function(event) {
            event.preventDefault();

            const email = document.getElementById('email').value;
            const password = document.getElementById('password').value;

            if (email && password) {
                alert(`Login Successful!\nEmail: ${email}`);
            } else {
                alert('Please fill in all fields.');
            }
        });
    </script>
</body>
</html>
