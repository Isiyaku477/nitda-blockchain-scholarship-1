<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Front-End Tasks</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      display: flex;
      min-height: 100vh;
      background: #f4f4f4;
    }

    /* Sidebar */
    .sidebar {
      width: 250px;
      background: #222;
      color: white;
      transition: 0.3s;
      overflow: hidden;
    }

    .sidebar.closed {
      width: 70px;
    }

    .logo {
      padding: 20px;
      text-align: center;
      font-weight: bold;
      background: #111;
    }

    .menu {
      list-style: none;
    }

    .menu li {
      padding: 15px 20px;
      border-bottom: 1px solid #333;
      cursor: pointer;
    }

    .menu li:hover {
      background: #444;
    }

    .toggle-btn {
      position: absolute;
      top: 20px;
      left: 260px;
      padding: 10px 15px;
      cursor: pointer;
    }

    .sidebar.closed + .toggle-btn {
      left: 80px;
    }

    /* Main Content */
    .main {
      flex: 1;
      padding: 30px;
    }

    /* Contact Form */
    .form-container {
      max-width: 500px;
      background: white;
      padding: 25px;
      border-radius: 8px;
      margin-top: 40px;
    }

    .form-container h2 {
      margin-bottom: 20px;
    }

    .form-group {
      margin-bottom: 15px;
    }

    .form-group label {
      display: block;
      margin-bottom: 5px;
    }

    .form-group input,
    .form-group textarea {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button {
      padding: 10px 20px;
      border: none;
      background: #222;
      color: white;
      cursor: pointer;
      border-radius: 5px;
    }

    button:hover {
      background: #555;
    }

    /* Mobile Responsive */
    @media (max-width: 600px) {
      .sidebar {
        position: absolute;
        height: 100%;
        z-index: 10;
      }

      .toggle-btn {
        left: 20px;
      }
    }
  </style>
</head>

<body>

  <!-- Sidebar -->
  <div class="sidebar" id="sidebar">
    <div class="logo">LOGO</div>
    <ul class="menu">
      <li>🏠 Home</li>
      <li>👤 Profile</li>
      <li>📁 Projects</li>
      <li>📞 Contact</li>
      <li>⚙ Settings</li>
    </ul>
  </div>

  <button class="toggle-btn" onclick="toggleSidebar()">☰</button>

  <!-- Main Content -->
  <div class="main">
    <h1>Front-End Web Development Tasks</h1>
    <p>This page contains a collapsible sidebar and a responsive contact form.</p>

    <!-- Contact Form -->
    <div class="form-container">
      <h2>Contact Us</h2>

      <div class="form-group">
        <label>Full Name</label>
        <input type="text" placeholder="Enter your name">
      </div>

      <div class="form-group">
        <label>Email Address</label>
        <input type="email" placeholder="Enter your email">
      </div>

      <div class="form-group">
        <label>Subject</label>
        <input type="text" placeholder="Subject">
      </div>

      <div class="form-group">
        <label>Message</label>
        <textarea rows="4" placeholder="Your message"></textarea>
      </div>

      <button type="submit">Send Message</button>
    </div>
  </div>

  <script>
    function toggleSidebar() {
      document.getElementById("sidebar").classList.toggle("closed");
    }
  </script>

</body>
</html>

