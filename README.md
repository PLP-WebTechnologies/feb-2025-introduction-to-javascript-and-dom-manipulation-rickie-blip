week5.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DOM Manipulation Example</title>
  <link rel="stylesheet" href="style.css"> <!-- Optional CSS file -->
</head>
<body>

  <!-- Header section -->
  <header>
    <h1>Interactive DOM Manipulation</h1>
  </header>

  <!-- Main content -->
  <main>
    <section>
      <p id="textContent">This is some text that will change dynamically.</p>
      <button id="changeTextBtn">Change Text</button>
    </section>

    <section>
      <p id="styleContent">Click to change my style!</p>
      <button id="changeStyleBtn">Change Style</button>
    </section>

    <section>
      <button id="addElementBtn">Add New Element</button>
      <button id="removeElementBtn">Remove Last Element</button>
    </section>
  </main>

  <!-- Footer section -->
  <footer>
    <p>Made with ❤️ by You</p>
  </footer>

  <!-- Link to the script.js file -->
  <script src="script.js"></script>
</body>
</html>
week5.js
// Change text content dynamically
document.getElementById("changeTextBtn").addEventListener("click", function() {
    document.getElementById("textContent").textContent = "The text has been updated!";
  });
  
  // Modify CSS styles dynamically
  document.getElementById("changeStyleBtn").addEventListener("click", function() {
    let styleContent = document.getElementById("styleContent");
    styleContent.style.color = "blue";
    styleContent.style.fontSize = "20px";
    styleContent.style.fontWeight = "bold";
  });
  
  // Add a new element dynamically
  document.getElementById("addElementBtn").addEventListener("click", function() {
    let newElement = document.createElement("p");
    newElement.textContent = "This is a newly added paragraph.";
    document.body.appendChild(newElement);
  });
  
  // Remove the last added element dynamically
  document.getElementById("removeElementBtn").addEventListener("click", function() {
    let lastElement = document.body.lastElementChild;
    if (lastElement && lastElement !== document.body) { // Prevent removing <body> itself
      document.body.removeChild(lastElement);
    }
  });
  style.css
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
  }
  
  header, footer {
    background-color: #f4f4f4;
    padding: 10px;
    text-align: center;
  }
  
  h1 {
    color: #333;
  }
  
  button {
    margin: 10px;
    padding: 10px 20px;
    cursor: pointer;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 5px;
  }
  
  button:hover {
    background-color: #45a049;
  }
  
  section {
    margin-bottom: 20px;
  }
  

