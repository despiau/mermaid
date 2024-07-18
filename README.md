Sure! I can create an SVG animation where six apples plus three oranges appear sequentially, followed by an input form to enter the answer. When the answer is submitted, the number will be displayed as points. Here's the SVG code with a form included:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>SVG Animation with Input Form</title>
  <style>
    @keyframes jump {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-20px); }
    }

    #apple1 { animation: jump 1s 1s infinite; }
    #apple2 { animation: jump 1s 2s infinite; }
    #apple3 { animation: jump 1s 3s infinite; }
    #apple4 { animation: jump 1s 4s infinite; }
    #apple5 { animation: jump 1s 5s infinite; }
    #apple6 { animation: jump 1s 6s infinite; }

    #orange1 { animation: jump 1s 7s infinite; }
    #orange2 { animation: jump 1s 8s infinite; }
    #orange3 { animation: jump 1s 9s infinite; }

    #plus, #equals, #name {
      animation: appear 1s ease-in-out infinite;
    }

    @keyframes appear {
      0% { opacity: 0; }
      100% { opacity: 1; }
    }

    .hidden {
      display: none;
    }
  </style>
</head>
<body>
  <svg width="600" height="200" xmlns="http://www.w3.org/2000/svg">
    <!-- Apples -->
    <circle id="apple1" cx="30" cy="150" r="20" fill="red" visibility="hidden"/>
    <circle id="apple2" cx="70" cy="150" r="20" fill="red" visibility="hidden"/>
    <circle id="apple3" cx="110" cy="150" r="20" fill="red" visibility="hidden"/>
    <circle id="apple4" cx="150" cy="150" r="20" fill="red" visibility="hidden"/>
    <circle id="apple5" cx="190" cy="150" r="20" fill="red" visibility="hidden"/>
    <circle id="apple6" cx="230" cy="150" r="20" fill="red" visibility="hidden"/>

    <!-- Oranges -->
    <circle id="orange1" cx="330" cy="150" r="20" fill="orange" visibility="hidden"/>
    <circle id="orange2" cx="370" cy="150" r="20" fill="orange" visibility="hidden"/>
    <circle id="orange3" cx="410" cy="150" r="20" fill="orange" visibility="hidden"/>

    <!-- Plus Sign -->
    <text id="plus" x="260" y="155" font-size="30" fill="black" visibility="hidden">+</text>

    <!-- Equals Sign -->
    <text id="equals" x="450" y="155" font-size="30" fill="black" visibility="hidden">=</text>

    <!-- Name Alejandro -->
    <text id="name" x="250" y="50" font-size="30" fill="blue" visibility="hidden">Alejandro</text>
  </svg>

  <div id="input-container" style="text-align:center; margin-top:20px;" class="hidden">
    <label for="answer">Enter the number:</label>
    <input type="number" id="answer" name="answer">
    <button onclick="submitAnswer()">Submit</button>
  </div>

  <div id="result" style="text-align:center; margin-top:20px;" class="hidden"></div>

  <script>
    function showElement(id, delay) {
      setTimeout(() => {
        document.getElementById(id).setAttribute("visibility", "visible");
      }, delay);
    }

    showElement("apple1", 1000);
    showElement("apple2", 2000);
    showElement("apple3", 3000);
    showElement("apple4", 4000);
    showElement("apple5", 5000);
    showElement("apple6", 6000);
    showElement("plus", 7000);
    showElement("orange1", 8000);
    showElement("orange2", 9000);
    showElement("orange3", 10000);
    showElement("equals", 11000);
    showElement("name", 12000);

    setTimeout(() => {
      document.getElementById('input-container').classList.remove('hidden');
    }, 13000);

    function submitAnswer() {
      const answer = document.getElementById('answer').value;
      document.getElementById('result').innerHTML = `<strong>${answer} points!</strong>`;
      document.getElementById('result').classList.remove('hidden');
      document.getElementById('input-container').classList.add('hidden');
    }
  </script>
</body>
</html>
```

This HTML code includes the SVG animation with six apples and three oranges, plus an input form that appears after the animation. When the user submits their answer, the entered number is displayed as points. You can save this code as an HTML file and open it in a web browser to see the animation and interactive form in action.
