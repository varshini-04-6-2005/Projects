<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Login & Sign Up</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f5f5f5;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .container {
      background: white;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      width: 300px;
    }
    .container h2 {
      text-align: center;
    }
    input {
      width: 100%;
      margin-bottom: 1rem;
      padding: 0.5rem;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    button {
      width: 100%;
      padding: 0.7rem;
      background: #007bff;
      border: none;
      color: white;
      border-radius: 4px;
      cursor: pointer;
    }
    button:hover {
      background: #0056b3;
    }
    .toggle-link {
      text-align: center;
      margin-top: 1rem;
      color: #007bff;
      cursor: pointer;
    }
    .hidden {
      display: none;
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- Login form -->
    <form id="login-form">
      <h2>Login</h2>
      <input type="text" id="login-username" placeholder="Username" required />
      <input type="password" id="login-password" placeholder="Password" required />
      <button type="submit">Login</button>
      <div class="toggle-link" onclick="showSignUp()">Don't have an account? Sign up</div>
    </form>

    <!-- Sign-up form -->
    <form id="signup-form" class="hidden">
      <h2>Sign Up</h2>
      <input type="text" id="signup-username" placeholder="Username" required />
      <input type="password" id="signup-password" placeholder="Password" required />
      <input type="password" id="signup-confirm" placeholder="Confirm Password" required />
      <button type="submit">Sign Up</button>
      <div class="toggle-link" onclick="showLogin()">Already have an account? Login</div>
    </form>
  </div>

  <script>
    const loginForm = document.getElementById('login-form');
    const signupForm = document.getElementById('signup-form');

    // store fake users for demo
    const users = {};

    function showSignUp() {
      loginForm.classList.add('hidden');
      signupForm.classList.remove('hidden');
    }

    function showLogin() {
      signupForm.classList.add('hidden');
      loginForm.classList.remove('hidden');
    }

    signupForm.addEventListener('submit', function(e) {
      e.preventDefault();
      const username = document.getElementById('signup-username').value;
      const password = document.getElementById('signup-password').value;
      const confirm = document.getElementById('signup-confirm').value;

      if(password !== confirm) {
        alert('Passwords do not match');
        return;
      }
      if(users[username]) {
        alert('Username already exists');
        return;
      }

      users[username] = password;
      alert('Sign up successful, please login.');
      showLogin();
    });

    loginForm.addEventListener('submit', function(e) {
      e.preventDefault();
      const username = document.getElementById('login-username').value;
      const password = document.getElementById('login-password').value;

      if(users[username] && users[username] === password) {
        alert('Login successful!');
        // you can redirect here, for example
      } else {
        alert('Invalid username or password');
      }
    });
  </script>
</body>
</html>
