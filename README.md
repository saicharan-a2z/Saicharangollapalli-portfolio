<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portfolio - Sai Charan Gollapalli</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap');
    body {
      margin: 0;
      padding: 0;
      background-color: black;
      color: white;
      font-family: 'Poppins', sans-serif;
      background-image: radial-gradient(#333 1px, transparent 1px);
      background-size: 20px 20px;
    }
    .navbar {
      background-color: #222;
      padding: 15px 30px;
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
    }
    .nav-links {
      display: flex;
      gap: 30px;
    }
    .nav-links button {
      background-color: #39FF14;
      border: none;
      padding: 10px 20px;
      color: black;
      font-weight: bold;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .nav-links button:hover {
      background-color: #32e812;
    }
    .menu {
      background-color: transparent;
      border: none;
      cursor: pointer;
      color: #39FF14;
      font-size: 1.8rem;
      padding: 5px;
    }
    .dropdown {
      display: none;
      position: absolute;
      background-color: #222;
      padding: 10px;
      right: 30px;
      top: 60px;
      width: 150px;
      box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.3);
      border-radius: 5px;
    }
    .dropdown a {
      display: block;
      padding: 10px;
      color: #39FF14;
      text-decoration: none;
    }
    .dropdown a:hover {
      background-color: #333;
    }
    .main-content {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      padding-top: 100px;
      gap: 20px;
      text-align: center;
    }
    .profile-pic {
      width: 170px;
      height: 170px;
      border-radius: 50%;
      background-color: yellow;
      border: 2px solid #39FF14;
      object-fit: cover;
    }
    h1 {
      font-size: 2.5rem;
      font-weight: 700;
      margin: 0;
    }
    h2 {
      font-weight: 500;
      font-size: 1.5rem;
      margin-top: 0;
      color: #39FF14;
    }
    p {
      max-width: 600px;
      font-weight: 300;
      font-size: 1.1rem;
      margin: 10px auto;
      line-height: 1.5;
      color: #ccc;
    }
    .social-buttons {
      display: flex;
      gap: 15px;
      justify-content: center;
    }
    .social-buttons a {
      text-decoration: none;
      padding: 10px 20px;
      color: white;
      font-weight: bold;
      border-radius: 5px;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .social-buttons .instagram {
      background-color: #E1306C;
    }
    .social-buttons .linkedin {
      background-color: #0077B5;
    }
    @media (max-width: 768px) {
      .nav-links {
        gap: 15px;
      }
      .menu {
        font-size: 2rem;
      }
      .dropdown {
        width: 120px;
        right: 20px;
      }
      h1 {
        font-size: 2rem;
      }
      h2 {
        font-size: 1.2rem;
      }
    }
  </style>
</head>
<body>
  <div class="navbar">
    <div class="nav-links">
      <button>About</button>
      <button>Skills</button>
      <button>Resume</button>
    </div>
    <button class="menu" onclick="toggleDropdown()">☰</button>
    <div class="dropdown" id="dropdown">
      <a href="mailto:yourmail@example.com">Mail</a>
      <a href="#">Contact</a>
    </div>
  </div>

  <div class="main-content">
    <img src="circular_profile_adjusted.png" alt="Sai Charan Gollapalli" class="profile-pic" />
    <h1>Sai Charan Gollapalli</h1>
    <h2>Frontend Developer</h2>
    <p>
      I am Sai Charan, a passionate and aspiring web developer aiming to build a strong foundation in web development. As I grow, I plan to explore various fields of computer science. My current abilities include creating visually appealing and functional websites using HTML, CSS, and JavaScript.
    </p>
    <div class="social-buttons">
      <a href="#" class="instagram">Instagram</a>
      <a href="#" class="linkedin">LinkedIn</a>
    </div>
  </div>

  <script>
    function toggleDropdown() {
      const dropdown = document.getElementById('dropdown');
      dropdown.style.display = dropdown.style.display === 'block' ? 'none' : 'block';
    }
    // Close dropdown if clicking outside
    window.onclick = function(event) {
      const dropdown = document.getElementById('dropdown');
      const menuBtn = document.querySelector('.menu');
      if (event.target !== menuBtn && !menuBtn.contains(event.target)) {
        dropdown.style.display = 'none';
      }
    }
  </script>
</body>
</html>
