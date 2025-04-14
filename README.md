<!doctype html>
<html> 
 <head> 
  <title>Simple Portfolio</title> 
  <link rel="stylesheet" href="styles.css"> 
  <style>
    .anime-logo {
      display: block;
      margin: 0 auto 20px auto;
      width: 150px;
      height: 150px;
      border-radius: 50%;
      border: 2px solid #0f0;
      box-shadow: 0 0 15px rgba(0, 255, 0, 0.3);
      object-fit: cover;
    }
    h1 {
      margin-top: 20px;
    }
    .project-content {
      display: none; /* Initially hide project content */
    }
  </style> 
 <style type="text/css" id="dcoder_stylesheet">body {
  font-family: sans-serif;
  margin: 100px;
  font-size: 18px;
  color: #0f0; 
  position: relative;
  overflow: hidden; 
  background-color: #000;
}

/* Animated background effect */
body::before {
  content: "";
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: 
    repeating-linear-gradient(
      0deg,
      rgba(1, 255, 1, 0.1) 0px,
      rgba(1, 255, 1, 0.1) 1px,
      transparent 1px,
      transparent 20px
    ),
    repeating-linear-gradient(
      90deg,
      rgba(0, 255, 0, 0.1) 0px,
      rgba(0, 255, 0, 0.1) 1px,
      transparent 1px,
      transparent 20px
    );
  background-size: 20px 20px;
  animation: gridScroll 10s linear infinite;
  z-index: -2;
}

@keyframes gridScroll {
  from { background-position: 0 0; }
  to { background-position: 0 1000px; }
}

/* Matrix-like rain effect overlay */
body::after {
  content: "";
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    to bottom,
    rgba(0, 0, 0, 0.9) 10%,
    rgba(0, 255, 0, 0.1) 50%,
    rgba(0, 0, 0, 0.9) 90%
  );
  animation: scan 6s linear infinite;
  pointer-events: none;
  z-index: -1;
}

@keyframes scan {
  0% { background-position: 0 -100%; }
  100% { background-position: 0 100%; }
}

.container {
  max-width: 800px;
  margin: 20px auto;
  padding: 20px;
  background-color: rgba(0, 20, 0, 0.9);
  border-radius: 4px;
  box-shadow: 0 0 20px rgba(0, 255, 0, 0.2);
  border: 1px solid rgba(0, 255, 0, 0.1);
  position: relative;
  backdrop-filter: blur(2px);
}

h1 {
  text-align: center;
  color: #0f0;
  text-shadow: 0 0 10px #0f0;
  margin-bottom: 30px;
}

h2 {
  color: #0f0;
  border-bottom: 1px solid rgba(0, 255, 0, 0.3);
  padding-bottom: 5px;
}

.project-button, .contact-button {
  background-color: #0f0; /* Green background */
  color: #000; /* Black text */
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

/* Hover effect */
.project-button:hover, .contact-button:hover {
  background-color: #00ff00; /* Darker green */
}</style></head> 
 <body> 
  <div class="container"> 
   <img src="https://i.ibb.co/CKMmq3qN/images-62.jpg" class="anime-logo" alt="Anime Girl Logo"> 
   <h1>My Portfolio</h1> 
  </div> 
  <div class="container"> 
   <section> 
    <h2>About Me</h2> 
    <p>I'm John Mark C Baet, a 2nd year IT student. </p> 
    <p>This is my portfolio showcasing some of my projects.</p> 
   </section> 
  </div> 
  <div class="container"> 
   <section> 
    <h2>Projects</h2> <button class="project-button" data-project="inventory">Inventory System</button> <button class="project-button" data-project="networking">Networking System</button> 
    <div id="inventoryContent" class="project-content"> 
     <h2>Inventory System</h2> 
     <p>This is a simple inventory management system that allows users to track items, quantities, and prices. It's designed for small businesses to keep track of their stock.</p> 
     <p>Implementation Date: 2024-03-15</p> 
    </div> 
    <div id="networkingContent" class="project-content"> 
     <h2>Networking System</h2> 
     <p>This project simulates a basic network topology, allowing users to visualize network connections and analyze data flow. It's a great learning tool for understanding network concepts.</p> 
     <p>Implementation Date: 2023-10-28</p> 
    </div> 
   </section> 
  </div> 
  <div class="container"> 
   <section> 
    <h2>Contact</h2> 
    <p>Email: baetjm74@gmail.com</p> 
   </section> 
  </div> 
  <script src="script.js"></script> 
 
<script type="text/javascript" id="dcoder_script">document.addEventListener('DOMContentLoaded', function() {
  // Get all project buttons
  const projectButtons = document.querySelectorAll('.project-button');

  // Get the project content divs
  const inventoryContent = document.getElementById('inventoryContent');
  const networkingContent = document.getElementById('networkingContent');

  // Loop through each project button
  projectButtons.forEach(button => {
    button.addEventListener('click', function(event) {
      const projectName = event.target.dataset.project;
      console.log(`Project clicked: ${projectName}`);

      // Show the corresponding project content:
      if (projectName === "inventory") {
        inventoryContent.style.display = 'block';
        networkingContent.style.display = 'none'; 
      } else if (projectName === "networking") {
        inventoryContent.style.display = 'none';
        networkingContent.style.display = 'block';
      }
    });
  });
});</script></body></html>
