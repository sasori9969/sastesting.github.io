<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>TOW Rechner</title>
  <style>
    body {
      background-color: #FFA07A; /* Helles Orange */
    }
    h1 {
      text-align: center;
    }
    .input-container {
      display: flex;
      align-items: center;
      margin-bottom: 10px;
    }
    .spacer {
      width: 20px;
    }
    .result {
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>TOW Rechner</h1>
  <div class="input-container">
    <label for="input-1">125</label>
    <span class="spacer"></span>
    <input id="input-1" type="text" placeholder="Eingabefeld 1">
  </div>
  <div class="input-container">
    <label for="input-2">250</label>
    <span class="spacer"></span>
    <input id="input-2" type="text" placeholder="Eingabefeld 2">
  </div>
  <!-- Weitere Eingabefelder -->
  <div class="input-container">
    <label for="input-12">1500</label>
    <span class="spacer"></span>
    <input id="input-12" type="text" placeholder="Eingabefeld 12">
  </div>
  <button onclick="calculate()">Berechnen</button>
  <p id="result"></p>
  <script>
    function calculate() {
      // Hole alle Eingabefelder
      const inputFields = document.querySelectorAll('input[type="text"]');
      // Gehe durch jedes Eingabefeld
      inputFields.forEach((inputField, index) => {
        // Hole das Label für das aktuelle Eingabefeld
        const label = inputField.previousElementSibling;
        // Hole den Wert des Labels als Zahl
        const labelValue = Number(label.textContent);
        // Hole den Wert des Eingabefelds als Zahl
        const inputValue = Number(inputField.value);
        // Multipliziere den Wert des Labels mit dem Wert des Eingabefelds und zeige das Ergebnis an
        document.getElementById('result').innerHTML += `<div>Ergebnis für Eingabefeld ${index + 1}: ${labelValue * inputValue}</div>`;
      });
    }
  </script>
</body>
</html>

