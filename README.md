# Shade-Selection
<html>
<body>
  <label>Value 1: <input type="text" id="value1"></label><br>
  <label>Value 2: <input type="text" id="value2"></label><br>
  <label>Value 3: <input type="text" id="value3"></label><br>
  <button onclick="getAnswer()">Submit</button>
  <p>Answer: <span id="output"></span></p>

  <script>
    function getAnswer() {
      let v1 = document.getElementById("value1").value;
      let v2 = document.getElementById("value2").value;
      let v3 = document.getElementById("value3").value;
      
      let lookupTable = {
        "A,B,C": "Answer 1",
        "X,Y,Z": "Answer 2",
        "M,N,O": "Answer 3"
      };

      let key = `${v1},${v2},${v3}`;
      document.getElementById("output").innerText = lookupTable[key] || "No match found";
    }
  </script>
</body>
</html>
