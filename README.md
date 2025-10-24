[Uploading akassdsfs.htm…]()
<!DOCTYPE html>
<html lang="ha">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Simple Calculator</title>
  <style>
    body {
      background:;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      color: #fff;
      margin: 0;
    }
    .calculator {
      background-color:black;
      border-radius: 15px;
      box-shadow: 0 8px 15px rgba(0,0,0,0.3);
      padding: 20px;
      width: 360px;
      text-align:center;
    }
    .display {
      background:white;
      border-radius: 10px;
      font-size: 2.5rem;
      padding: 10px 10px;
      margin-bottom: 25px;
      text-align:right;
      font-weight: 500;
      letter-spacing: 2px;
      color:black;
      user-select: none;
      min-height: 50px;
      word-wrap: break-word;
    }
    .buttons {
      display:grid;
      grid-template-columns: repeat(4,1fr);
      gap: 15px;
    }
    ol{
      color: black;
      font-family: 'Times New Roman', Times, serif;
      font-size:x-large;
    }
    .calculator,h1{
      font-family: 'Times New Roman', Times, serif;
      
    }
    button {
      
      border-radius: 30px;
      font-size: 1.5rem;
      padding: 15px;
      color:black;
      background:white;
      font-weight: bold;
      cursor: pointer;
      box-shadow: 0 5px 12px rgba(118,75,162,0.6);
      transition: background 0.3s ease, color 0.3s ease;
    }
    button:hover {
      background: #764ba2;
      color: white;
    }
    .operator {
      background:orange;
      color: white;
      box-shadow: 0 5px 12px rgba(255,159,67,0.6);
    }
    .operator:hover {
      background: #27221d;
    }
    .equal {
      grid-column: span 2;
      background:rgb(40, 145, 186);
      color: white;
      box-shadow: 0 5px 12px rgba(52,172,224,0.6);
    }
    .equal:hover {
      background: #042d40;
    }
    .clear {
      background: #ff0303;
      color: #f0e8e8;
      box-shadow: 0 5px 12px rgba(255,107,107,0.6);
    }
    .clear:hover {
      background: #970505;
    }
  </style>
</head>
<body>
  <ol>
    <li>SHAFA'U ABDUSSALAM</li>
    <li>ABDURRAHMAN MUHD RABI'U</li>
    <li>FATIMA LABARAN SUNUSI</li>
    <li>MA'AMAR ABUBAKAR MUHD</li>
    <li>ABDULLAHI ABUBAKAR BASHIR</li>
    <li>USAMA MUHAMMAD ABDULLAHI</li>
    <li>AHMAD RABI'U UMAR</li>
    <li>ABUBAKAR MUHAMMAD SANI</li>
    <li>ABDURRA'UF ADAM SULAIMAN</li>
    <li>ZAKARIYYA MUHAMMAD AMINU</li>
    <li>MUSTAFA RABI'U BUHARI</li>
  
  </ol>

<div class="calculator">
    <H1>CALCULATOR GROUP D</H1>
    <div id="display" class="display">0</div>
    <div class="buttons">
      <button class="clear" onclick="clearDisplay()">C</button>
      <button onclick="appendValue('(')">(</button>
      <button onclick="appendValue(')')">)</button>
      <button class="operator" onclick="appendValue('/')">÷</button>

      <button onclick="appendValue('7')">7</button>
      <button onclick="appendValue('8')">8</button>
      <button onclick="appendValue('9')">9</button>
      <button class="operator" onclick="appendValue('*')">×</button>

      <button onclick="appendValue('4')">4</button>
      <button onclick="appendValue('5')">5</button>
      <button onclick="appendValue('6')">6</button>
      <button class="operator" onclick="appendValue('-')">−</button>

      <button onclick="appendValue('1')">1</button>
      <button onclick="appendValue('2')">2</button>
      <button onclick="appendValue('3')">3</button>
      <button class="operator" onclick="appendValue('+')">+</button>

      <button onclick="appendValue('00')">00</button>
      <button onclick="appendValue('0')">0</button>
      <button onclick="appendValue('.')">.</button>
      <button class="equal" onclick="calculateResult()">=</button>
    </div>
  </div>

  <script>
    const display = document.getElementById('display');

    function appendValue(value) {
      if (display.innerText === "0" && value !== ".") {
        display.innerText = value;
      } else {
        display.innerText += value;
      }
    }

    function clearDisplay() {
      display.innerText = "0";
    }

    function calculateResult() {
      try {
        let expression = display.innerText.replace(/÷/g, '/').replace(/×/g, '*');
        let result = eval(expression);
        display.innerText = result;
      } catch {
        display.innerText = "Kuskure!";
      }
    }
  </script>
</body>
</html>
