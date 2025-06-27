<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bloxify</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
    }
    header {
      background-color: #333;
      color: white;
      padding: 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .logo {
      height: 40px;
    }
    nav {
      display: flex;
      gap: 15px;
    }
    nav button {
      padding: 10px 15px;
      border: none;
      background-color: #555;
      color: white;
      cursor: pointer;
      border-radius: 4px;
    }
    nav button:hover {
      background-color: #777;
    }
    main {
      padding: 20px;
    }
    .section {
      margin-bottom: 20px;
      background-color: white;
      padding: 15px;
      border-radius: 5px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
  </style>
</head>
<body>
  <header>
    <img src="logo.png" alt="Logo" class="logo">
    <nav>
      <button onclick="addSection()">Add Section</button>
      <button onclick="addButton()">Add Button</button>
    </nav>
  </header>
  <main id="main-content">
    <div class="section">Welcome to your simple website!</div>
  </main>

  <script>
    function addSection() {
      const section = document.createElement('div');
      section.className = 'section';
      section.textContent = 'New section content here.';
      document.getElementById('main-content').appendChild(section);
    }

    function addButton() {
      const button = document.createElement('button');
      button.textContent = 'New Button';
      button.style.marginRight = '10px';
      button.onclick = () => alert('You clicked the new button!');
      document.getElementById('main-content').appendChild(button);
    }
  </script>
</body>
</html>
