<!DOCTYPE html>
<div lang="en" ></div>
<head>
  <meta charset="UTF-8" content="width=device-width, initial-scale=2.5">
  <title>KitchenConverter</title>
</head>
<header>
    <!-- partial:index.partial.html -->
    <div class="germanyFlag">
    </div>
        <div id="pageTitle" class="pageTitle">
        <h1>KitchenConverter</h1>
    </div>
</header>
<body>
  <link rel="stylesheet" href="./style.css">
<div class="wrapper">
  <div class="side-image">
    <img src="https://cdn.pixabay.com/photo/2017/03/13/13/39/pancakes-2139844_960_720.jpg" alt="Yummy pancakes">
    <img src="https://cdn.pixabay.com/photo/2020/10/30/16/33/cookies-5699047_1280.jpg">
  </div>
  <div class="subheader">
    <h2>Convert cups, tablespoons and teaspoons to grams or ounces</h2>
  </div>
    <div class="description">
  <p > You would like to cook or bake a recipe which uses American units of measurements,
  whereas you prefer to count in grams or ounces? KitchenConverter is the solution!😊</p>
    </div>
<div class="description2">
<p>Select the unit of measurement, an ingredient and the amount to be converted</p><br>
    <button>Switch Units</button>
</div>

  <div id="top" class="unitClass">
  <form>
    <group class="inline-radio" onchange="displayRadioValue()">
      <div><input type="radio" name="units" value="Cups" checked><label>Cups</label></div>
      <div><input type="radio" name="units" value="Tablespoons"><label>Tablespoons</label></div>
      <div><input type="radio" name="units" value="Teaspoons"><label>Teaspoons</label></div>
    </group>
  </form>
</div>
  <div class="secondForm">
      <form id="numberInput" style="font-size:22px">
          Select an Ingredient<br> <select id="ingrList" onchange="setIngrText()" style="width: 320px; font-size:16px">
              <option style="font-size:16px;color:grey" value="0">--Select--</option>
              <option style="font-size:16px" value="130">Flour</option>
              <option style="font-size:16px" value="200">Sugar</option>
              <option style="font-size:16px" value="224">Oil</option>
              <option style="font-size:16px" value="100">Almonds</option>
              <option style="font-size:16px" value="225">Butter</option>
              <option style="font-size:16px" value="128">Seeds</option>
              <option style="font-size:16px" value="240">Liquids</option>
              <option style="font-size:16px" value="340">Honey</option>
              <option style="font-size:16px" value="240">Cream/Yoghurt</option>
              <option style="font-size:16px" value="180">Salt</option>
          </select>

          <p id="errorIng" style="color:red; font-size:14px"></p><br>

          <input id="input" type="range" min="0" value="0" max="17" step="1" style="max-width:500px" onchange="transfer(), jumpToBottom()">
          <p id="output" style="color:#7FFFD4"></p><p id="errorAmt" style="color:red; font-size:14px"></p><br>

          <input class="btn" onclick="convertNumbers(),setIngrText()" type="button" value="Convert to grams">
          <input class="btn" onclick="convertToOunces(),setIngrText()" type="button" value="Convert to oz">
          <input class="btn" onclick="resetButton(),jumpToTop()" type="button" value="Reset">
      </form>
  </div>
</div>
  <div class="wrapper2">
  <div class="resultField">
  <label id="sentence" style="font-size:22px">Result:</label><br>
  <input id="result" disabled type="text" style="width: 150px; height:40px; text-align:center; font-size:30px; background-color:black; color:lightgrey"><br>
  </div>

<!-- partial -->
  <script  src="JavaScript.js"></script>
  <div id="bottom" class="lastQueries">
      <p>Your last queries:</p>
      <p style="color:#7fffd4; font-size:10px">Refresh the page to clear the list</p>
      <br>
      <ul id="queriesList" style="list-style-type:none"></ul>
  </div>
</body>
</div>
  <footer>

    <a href="#pageTitle" style="color:black">Jump to top</a>
  </footer>
</div>
