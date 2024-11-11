<!DOCTYPE html>

<html lang="en">

<head>

 <meta charset="UTF-8">

 <meta name="viewport" content="width=device-width, initial-scale=1.0">

 <title>Document</title>

</head>

<body>

 <h2>Calculator</h2>

 <input type="text" id="display" readonly><br><br>

 <button onclick="clearDisplay()">C</button>

 <button onclick="appendToDisplay('1')">1</button>

 <button onclick="appendToDisplay('2')">2</button>

 <button onclick="appendToDisplay('3')">3</button>

 <button onclick="appendToDisplay('+')">+</button><br>

 <button onclick="appendToDisplay('4')">4</button>

 <button onclick="appendToDisplay('5')">5</button>

 <button onclick="appendToDisplay('6')">6</button>

 <button onclick="appendToDisplay('-')">-</button><br>

 <button onclick="appendToDisplay('7')">7</button>

 <button onclick="appendToDisplay('8')">8</button>

 <button onclick="appendToDisplay('9')">9</button>

 <button onclick="appendToDisplay('*')">*</button><br>

 <button onclick="appendToDisplay('0')">0</button>

 <button onclick="appendToDisplay('.')">.</button>

 <button onclick="calculateResult()">=</button>

 <button onclick="appendToDisplay('/')">/</button>

 <script>

 function appendToDisplay(value) {
 document.getElementById("display").value = document.getElementById("display").value + 

value;

 }

 function clearDisplay() {

 document.getElementById("display").value = '';

 }

 function calculateResult() {

 const display = document.getElementById("display");

 try {

 display.value = eval(display.value);

 } catch {

 display.value = "";

 }

 }

 </script>

</body>

</html>
