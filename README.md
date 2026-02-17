<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Mystery Button Maze</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(120deg, #1e3c72, #2a5298);
      color: white;
      text-align: center;
      padding: 50px;
    }

    .page {
      display: none;
    }

    .active {
      display: block;
    }

    button {
      padding: 15px 25px;
      margin: 10px;
      font-size: 16px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      background: #ff9800;
      color: black;
      transition: 0.2s;
    }

    button:hover {
      background: #ffc107;
      transform: scale(1.05);
    }

    h1 {
      margin-bottom: 20px;
    }
  </style>
</head>
<body>

  <!-- PAGE 1 -->
  <div class="page active" id="page1">
    <h1>Page 1: The Beginning</h1>
    <p>Welcome to the Button Maze. Choose wisely.</p>
    <button onclick="goToPage(2)">Go to Page 2</button>
    <button onclick="goToPage(3)">Go to Page 3</button>
    <button onclick="goToPage(4)">Go to Page 4</button>
  </div>

  <!-- PAGE 2 -->
  <div class="page" id="page2">
    <h1>Page 2: Confusion</h1>
    <p>You feel slightly lost.</p>
    <button onclick="goToPage(5)">Page 5</button>
    <button onclick="goToPage(6)">Page 6</button>
    <button onclick="goToPage(1)">Back to Page 1</button>
  </div>

  <!-- PAGE 3 -->
  <div class="page" id="page3">
    <h1>Page 3: Deeper</h1>
    <p>The buttons multiply.</p>
    <button onclick="goToPage(7)">Page 7</button>
    <button onclick="goToPage(8)">Page 8</button>
    <button onclick="goToPage(2)">Back to Page 2</button>
  </div>

  <!-- PAGE 4 -->
  <div class="page" id="page4">
    <h1>Page 4: Distraction</h1>
    <p>So many paths…</p>
    <button onclick="goToPage(9)">Page 9</button>
    <button onclick="goToPage(3)">Back to Page 3</button>
  </div>

  <!-- PAGE 5 -->
  <div class="page" id="page5">
    <h1>Page 5: Almost There</h1>
    <button onclick="goToPage(10)">Page 10</button>
    <button onclick="goToPage(6)">Page 6</button>
  </div>

  <!-- PAGE 6 -->
  <div class="page" id="page6">
    <h1>Page 6: Wrong Turn</h1>
    <button onclick="goToPage(1)">Start Over</button>
    <button onclick="goToPage(7)">Page 7</button>
  </div>

  <!-- PAGE 7 -->
  <div class="page" id="page7">
    <h1>Page 7: Getting Warmer</h1>
    <button onclick="goToPage(8)">Page 8</button>
    <button onclick="goToPage(10)">Page 10</button>
  </div>

  <!-- PAGE 8 -->
  <div class="page" id="page8">
    <h1>Page 8: Button Hell</h1>
    <button onclick="goToPage(9)">Page 9</button>
    <button onclick="goToPage(11)">Page 11</button>
    <button onclick="goToPage(4)">Page 4</button>
  </div>

  <!-- PAGE 9 -->
  <div class="page" id="page9">
    <h1>Page 9: Almost Almost</h1>
    <button onclick="goToPage(12)">Page 12</button>
    <button onclick="goToPage(10)">Page 10</button>
  </div>

  <!-- PAGE 10 -->
  <div class="page" id="page10">
    <h1>Page 10: Fake End</h1>
    <p>You thought it was over.</p>
    <button onclick="goToPage(11)">Page 11</button>
    <button onclick="goToPage(13)">Page 13</button>
  </div>

  <!-- PAGE 11 -->
  <div class="page" id="page11">
    <h1>Page 11: The Long Way</h1>
    <button onclick="goToPage(12)">Page 12</button>
    <button onclick="goToPage(14)">Page 14</button>
  </div>

  <!-- PAGE 12 -->
  <div class="page" id="page12">
    <h1>Page 12: Are You Tired?</h1>
    <button onclick="goToPage(15)">Final Path</button>
    <button onclick="goToPage(6)">Wrong Path</button>
  </div>

  <!-- PAGE 13 -->
  <div class="page" id="page13">
    <h1>Page 13: Nope</h1>
    <button onclick="goToPage(1)">Restart</button>
  </div>

  <!-- PAGE 14 -->
  <div class="page" id="page14">
    <h1>Page 14: Last Door</h1>
    <button onclick="goToPage(15)">Open Final Door</button>
  </div>

  <!-- PAGE 15 FINAL -->
  <div class="page" id="page15">
    <h1>FINAL PAGE</h1>
    <button onclick="reveal()">Press Me</button>
    <h2 id="secretText" style="display:none;">Aunty Ji Namsate 😁</h2>
  </div>

  <script>
    function goToPage(num) {
      let pages = document.querySelectorAll(".page");
      pages.forEach(p => p.classList.remove("active"));
      document.getElementById("page" + num).classList.add("active");
    }

    function reveal() {
      document.getElementById("secretText").style.display = "block";
    }
  </script>

</body>
</html>
