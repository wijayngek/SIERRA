<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Webpage bakit ba</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }

    /* Header styling */
    header {
      background-color: #444;
      color: white;
      padding: 20px;
      text-align: center;
    }

    /* Vertical menu bar styling */
    .menu-bar {
      background-color: #333;
      color: white;
      width: 200px;
      height: 100vh;
      position: fixed;
      top: 0;
      left: 0;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      padding: 20px;
      transition: transform 0.3s ease;
      transform: translateX(-100%);
      z-index: 1000;
    }

    .menu-bar.active {
      transform: translateX(0);
    }

    .menu-bar a {
      color: white;
      text-decoration: none;
      margin: 10px 0;
      padding: 10px;
      width: 100%;
      text-align: left;
      border-radius: 5px;
    }

    .menu-bar a:hover {
      background-color: #575757;
    }

    .menu-bar .back-button {
      align-self: flex-start;
      margin-bottom: 20px;
      padding: 10px 15px;
      background-color: #444;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    .menu-bar .back-button:hover {
      background-color: #555;
    }

    .search-bar {
      margin-top: 20px;
      width: 100%;
    }

    .search-bar input[type="text"] {
      width: 100%;
      padding: 5px;
      border: none;
      border-radius: 5px;
    }

    .search-bar button {
      margin-top: 10px;
      padding: 10px;
      width: 100%;
      border: none;
      background-color: #555;
      color: white;
      border-radius: 5px;
      cursor: pointer;
    }

    .search-bar button:hover {
      background-color: #666;
    }

    /* Content styling to adjust for toggleable menu */
    .content {
      margin-left: 20px;
      padding: 20px;
    }

    /* Dropdown button styling */
    .dropdown {
      position: relative;
      display: inline-block;
      margin-top: 20px;
    }

    .dropdown button {
      background-color: #444;
      color: white;
      padding: 10px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    .dropdown-content {
      display: none;
      position: absolute;
      background-color: teal;
      min-width: 150px;
      box-shadow: 0px 8px 16px rgba(0,0,0,0.2);
      z-index: 1;
    }

    .dropdown-content a {
      color: white;
      padding: 10px;
      text-decoration: none;
      display: block;
    }

    .dropdown-content a:hover {
      background-color: teal;
    }

    .dropdown:hover .dropdown-content {
      display: block;
    }

    /* Task bar styling */
    .task-bar {
      background-color: #f4f4f4;
      padding: 10px;
      display: flex;
      justify-content: center;
      border-top: 1px solid #ccc;
    }

    .task-bar a {
      margin: 0 15px;
      color: #333;
      text-decoration: none;
    }

    .task-bar a:hover {
      text-decoration: underline;
    }

    /* Footer styling */
    footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 10px;
      margin-top: 20px;
    }

    /* ICT Info box */
    #ict-info {
      display: none;
      margin: 20px;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
      background-color: #f9f9f9;
    }

    /* Menu toggle button */
    .menu-toggle {
      position: fixed;
      top: 20px;
      left: 20px;
      background-color: #444;
      color: white;
      border: none;
      padding: 10px 20px;
      cursor: pointer;
      z-index: 1000;
    }

    .menu-toggle:hover {
      background-color: #555;
    }
    
  </style>
</head>
<body>

  <!-- Menu Toggle Button -->
  <button class="menu-toggle" onclick="toggleMenu()">☰</button>

  <!-- Vertical Menu Bar -->
  <div class="menu-bar" id="menu-bar">
    <button class="back-button" onclick="closeMenu()">← </button>
    <a href="groupings.html">Home</a>
    <a href="iloveyoumero.html">About</a>
    <div class="search-bar">
      <input type="text" id="search-input" placeholder="Search...">
      <button onclick="searchICT()">Search</button>
    </div>
  </div>

  <!-- Header -->
  <header>
    <h1>SIERRA</h1>
    <p>Student’s Integrity in Education, Resilience, Responsibility, and Achievement </p>
  </header>

  <!-- Main Content -->
  <div class="content">
    <div class="dropdown">
      <button>Sierra Madre</button>
      <div class="dropdown-content">
        <a href="Schedule Table.html">Schedule Table</a>
        <a href="Deped Mission.html">Deped Mission</a>
        <a href="Deped Vision.html">Deped Vision</a>
        <a href="Core Values.html">Core Values</a>
      </div>
    </div>
   
    <div id="ict-info">
      <h2>What is ICT?</h2>
      <p>ICT, or information and communications technology (or technologies), is the infrastructure and components that enable modern computing. Among the goals of IC technologies, tools and systems is to improve the way humans create, process and share data or information with each other. Another is to help them improve their abilities in numerous areas, including business; education; medicine; real-world problem-solving; and even leisure activities related to sports, music, and movies.<br><br>

There is no single, universal definition of ICT because the technologies, devices and even ideas related to ICT are constantly evolving. However, the term is generally accepted to mean all devices, networking components and applications. When combined, these help people and organizations interact in the digital world.</p>
    </div>
  </div>

  <!-- Task Bar -->
  <div class="task-bar">
    <a href="mero1.html">Computer</a>
    <a href="mero2.html">HTML</a>
    <a href="mero3.html">ICT</a>
  </div>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 All Rights Reserved.</p>
  </footer>

  <script>
    // Function to toggle the menu bar visibility
    function toggleMenu() {
      const menuBar = document.getElementById('menu-bar');
      menuBar.classList.toggle('active');
    }

    // Function to close the menu bar using the back button
    function closeMenu() {
      const menuBar = document.getElementById('menu-bar');
      menuBar.classList.remove('active');
    }

    // Function to display ICT information
    function searchICT() {
      const input = document.getElementById("search-input").value.toLowerCase();
      const ictInfo = document.getElementById("ict-info");

      if (input === "ict") {
        ictInfo.style.display = "block";
      } else {
        ictInfo.style.display = "none";
        alert("No results found for your search.");
      }
    }
  </script>
  
</body>
</html>
