<html>
  <head>
    <title>TESTUNG</title>
    <style>
      body {
        background-color: #ffa500;
      }
      h1 {
        text-align: center;
        font-weight: bold;
      }
      .input-group {
        display: flex;
        align-items: center;
        justify-content: center;
      }
      .input-group label {
        margin-right: 10px;
      }
      button {
        display: block;
        margin: 0 auto;
      }
      #result {
        text-align: center;
      }
    </style>
  </head>
  <body>
    <h1>TESTUNG</h1>
    
    <script>
      function calculate(value1, value2) {
        // Calculate the result for each input field
        var result1 = value1 * 100;
        var result2 = value2 * 200;
        
        // Add the results together
        var totalResult = result1 + result2;
        
        // Use toLocaleString to add thousand separators
        totalResult = totalResult.toLocaleString();
        
        // Display the total result
        document.getElementById("result").innerHTML = totalResult;
      }
    </script>
    
    <div class="input-group">
      <label for="gold100">100 x Gold</label>
      <input type="number" id="gold100" name="gold100">
    </div>
    
    <div class="input-group">
      <label for="gold200">200 x Gold</label>
      <input type="number" id="gold200" name="gold200">
    </div>
    
    <br>
    <button type="button" onclick="calculate(
      document.getElementById('gold100').value,
      document.getElementById('gold200').value
    )">Berechnen</button>
    <br>
   

<br><br>
<div id="result" style="font-weight: bold; color: white;"></div>

  </body>
</html>
