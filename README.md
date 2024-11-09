<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>Calculate</title>
   <style>
      body {
         display: flex;
         justify-content: center;
         height: 100vh;
         background-color: rgb(89, 74, 74);

      }
      #calculator {
         font-family: Arial,sans-serif;
         background-color: rgb(75, 55, 55);
         border-radius: 15px;
         max-width: 500px;
         overflow: hidden;
      }
      #display {
         width: 100%;
         padding: 20px;
         font-size: 5rem;
         border:none;
         background-color: rgb(14, 6, 6);
         color: aliceblue;
      }
   button {
      width: 100px;
      height: 100px;
      border-radius: 50px;
      border: none;
      background-color: rgb(139, 148, 131);
      font-size: 20px;
      color: aliceblue;
      font-weight: bold;
      cursor: pointer;
   }
   #key {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 10px;
      padding: 25px;
   }
   button:hover{
      background-color: rgb(227, 205, 149);
   }
   .operator-btn {
      background-color: yellowgreen;
   }
   .operator-btn1{
      background-color: red;
   }
  .operator-btn2{
   background-color: green;
   
  }
   </style>
</head>
<body>
    <div id="calculator">
      <input id="display" readonly>
      <div id="key">
         <button onclick="appendToDisplay('+')" class="operator-btn">+</button>
         <button onclick="appendToDisplay('7')">7</button>
         <button onclick="appendToDisplay('8')">8</button>
         <button onclick="appendToDisplay('9')">9</button>
         <button onclick="appendToDisplay('-')" class="operator-btn">-</button>
         <button onclick="appendToDisplay('4')">4</button>
         <button onclick="appendToDisplay('5')">5</button>
         <button onclick="appendToDisplay('6')">6</button>
         <button onclick="appendToDisplay('*')" class="operator-btn">*</button>
         <button onclick="appendToDisplay('1')">1</button>
         <button onclick="appendToDisplay('2')">2</button>
         <button onclick="appendToDisplay('3')">3</button>
         <button onclick="appendToDisplay('/')" class="operator-btn">/</button>
         <button onclick="appendToDisplay('0')">0</button>
         <button onclick="appendToDisplay('.')" class="operator-btn">.</button>
         <button onclick="calculate()" class="operator-btn2" >=</button>
         <button onclick="clearDisplay()" class="operator-btn1">C</button>
      </div>
    </div>
   <script>
   const display =document.getElementById('display');

   function appendToDisplay(input){
  display.value +=input ;
   }
   function clearDisplay(){
display.value = "";
   }
   function calculate(){
display.value = eval(display.value);
   }
   </script>
   
</body>
</html>

