# ODD23-24-WT-JavaScript
# AIM:
To create a form with java script code to calculate electricity bill.

# DESIGNING PROCEDURE:
STEP 1:
Start define the document as HTML.

STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.

STEP 3:
Define the function for the program as calc().

STEP 4:
Give the necessary input that is required for calculating the electricity bill like var prev,curr,units,amt. Get the number for input using document.getElementById.

STEP 5:
Give the necessary condition using if-else condition. Close the script and head tags.

STEP 6:
Give the input type in the body of the HTML.

STEP 7 :
End the HTML structure.

# PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Electricity Calculator</title>
    <style>
        body {
            background-color: aliceblue;
            margin: 20px;
        }
        h2 {
            font-weight: bolder;
            color: green;
        }
        form {
            max-width: 400px;
            margin: auto;
        }
        input {
            padding: 10px;
            width: 100%;
            margin: 8% auto;
            box-sizing: border-box;
            border-color: aqua;
            background-color: ghostwhite;
        }
        button {
            background-color: greenyellow;
            box-sizing: border-box;
            font-weight: 900;
            max-width: 50%;
        }
    </style>
</head>
<body>
    <h2><center>ELECTRICITY CALCULATOR</center></h2>
    <form>
        <label for="curr readings">Enter current readings:</label>
        <input type="text" id="curr">
        <label for="prev readings">Enter previous readings:</label>
        <input type="text" id="prev">
        <center><button type="button" value="calculate" onclick="show()">Calculate</button></center>
        <input type="text" id="rate" readonly>
    </form>

    <script>
        function show() {
            var units, curr, prev, rate;
            curr = Number(document.getElementById("curr").value);
            prev = Number(document.getElementById('prev').value);
            units = curr - prev;

            if (units <= 100) {
                document.getElementById('rate').value = "No cost";
            } else if(units<=200){
                document.getElementById('rate').value = "Cost = 200";
            }else{
                document.getElementById('rate').value=  " Cost = 500 "
            }
        }
    </script>
</body>
</html>

```
# OUTPUT:
![Screenshot 2023-12-31 222135](https://github.com/rajamanikandanravikumar/ODD23-24-WT-JavaScript/assets/145742839/6ed35eb4-50be-4af1-bc86-57ee86f1255b)
# RESULT:
Thus the java code executed to calculate the electricity bill.

# PROGRAM 2
# AIM:
To create a form with java script code to compute the factorial of a given number without recursion.

# DESIGNING PROCEDURE:
STEP 1:
Start define the document as HTML.

STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.

STEP 3:
Define the function for the program as show().

STEP 4:
Give the necessary input that is require to compute the factorial like var i, n, fact. Get the number for input using document.getElementById.

STEP 5:
Using for-loop condition calculate the factorial. Close the script and head tags.

STEP 6:
Give the input type in the body of the HTML.

STEP 6 :
End the HTML structure.

# PROGRAM
````
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1.0">
 <title>Factorial Calculator</title>
</head>
<body>

 <h2>Factorial Calculator</h2>

 <form>
   <label for="number">Enter a Number:</label>
   <input type="number" id="number" required>

   <button type="button" onclick="calculateFactorial()">Compute Factorial</button>
 </form>

 <h3>Result:</h3>
 <p id="result"></p>

 <script>
   function calculateFactorial() {
     var number = parseInt(document.getElementById('number').value);

     if (isNaN(number)) {
       alert("Please enter a valid number.");
       return;
     }

     var factorial = 1;
     for (var i = 2; i <= number; i++) {
       factorial *= i;
     }

     document.getElementById('result').innerHTML = "Factorial: " + factorial;
   }
 </script>

</body>
</html>

````
# OUTPUT:
![Screenshot 2023-12-31 222949](https://github.com/rajamanikandanravikumar/ODD23-24-WT-JavaScript/assets/145742839/6ec3b02d-735a-4e0d-a2bc-76d6d74f4ec7)
# RESULT
Thus the java code executed to compute the factorial of a given number without recursion.

# PROGRAM 3
# AIM:
To construct a JavaScript code to generate ‘N’ prime numbers.

# DESIGNING PROCEDURE:
STEP 1:
Start define the document as HTML.

STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.

STEP 3:
Define the function for the program as show().

STEP 4:
Give the necessary input that is required to construct a java code to generate ‘N’ prime numbers . Get the number for input using document.getElementById.

STEP 5:
Using for-loop condition generate ‘N’ prime numbers. Close the script and head tags.

STEP 6:
Give the input type in the body of the HTML.

STEP 7 :
End the HTML structure.
# PROGRAM:
`````
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Prime Number Generator</title>
</head>
<body>

  <h2>Prime Number Generator</h2>

  <form>
    <label for="count">Enter the number of primes (N):</label>
    <input type="number" id="count" required>

    <button type="button" onclick="generatePrimes()">Generate Primes</button>
  </form>

  <h3>Prime Numbers:</h3>
  <p id="result"></p>

  <script>
    function isPrime(num) {
      for (let i = 2; i < num; i++) {
        if (num % i === 0) {
          return false;
        }
      }
      return num > 1;
    }

    function generatePrimes() {
      var count = parseInt(document.getElementById('count').value);
      var primes = [];
      var num = 2;

      while (primes.length < count) {
        if (isPrime(num)) {
          primes.push(num);
        }
        num++;
      }

      document.getElementById('result').innerHTML = primes.join(', ');
    }
  </script>

</body>
</html>
`````
# OUTPUT:
![Screenshot 2023-12-31 223301](https://github.com/rajamanikandanravikumar/ODD23-24-WT-JavaScript/assets/145742839/2de3e315-6fa7-4587-b85f-79721bdb4bb9)
# RESULT
Thus the java code executed to construct a JavaScript code to generate ‘N’ prime numbers

# PROGRAM 4
# AIM:
To construct a JavaScript program to implement a simple calculator.

# DESIGNING PROCEDURE:
STEP 1:
Start define the document as HTML.

STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.

STEP 3:
Define the function for the program as function f1() for addition, function f2() for subtraction, function f3() for multiplication, function f4() for division, function f5() for sin(a), function f6() for cos(a) ,function f7() for tan(a), function f8() for a*a , function f9() for clear.

STEP 4:
Give the necessary input that is required to implement a simple calculator. Get the number for input using document.getElementById.

STEP 5:
Close the script and head tags.

STEP 6:
Give the input type in the body of the HTML.

STEP 7 :
End the HTML structure.

# PROGRAM:
``````
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
    }
    input {
      width: 50px;
      margin: 5px;
    }
  </style>
</head>
<body>

  <h2>Simple Calculator</h2>

  <form>
    <input type="text" id="result" readonly>
    <br>
    <button type="button" onclick="appendToResult('1')">1</button>
    <button type="button" onclick="appendToResult('2')">2</button>
    <button type="button" onclick="appendToResult('3')">3</button>
    <button type="button" onclick="appendToResult('+')">+</button>
    <br>
    <button type="button" onclick="appendToResult('4')">4</button>
    <button type="button" onclick="appendToResult('5')">5</button>
    <button type="button" onclick="appendToResult('6')">6</button>
    <button type="button" onclick="appendToResult('-')">-</button>
    <br>
    <button type="button" onclick="appendToResult('7')">7</button>
    <button type="button" onclick="appendToResult('8')">8</button>
    <button type="button" onclick="appendToResult('9')">9</button>
    <button type="button" onclick="appendToResult('*')">*</button>
    <br>
    <button type="button" onclick="appendToResult('0')">0</button>
    <button type="button" onclick="clearResult()">C</button>
    <button type="button" onclick="calculateResult()">=</button>
    <button type="button" onclick="appendToResult('/')">/</button>
  </form>

  <script>
    function appendToResult(value) {
      document.getElementById('result').value += value;
    }

    function clearResult() {
      document.getElementById('result').value = '';
    }

    function calculateResult() {
      var result = eval(document.getElementById('result').value);
      document.getElementById('result').value = result;
    }
  </script>

</body>
</html>

``````
# OUTPUT:
![Screenshot 2023-12-31 223628](https://github.com/rajamanikandanravikumar/ODD23-24-WT-JavaScript/assets/145742839/6feee33e-6118-4f21-a463-01db3448b6a0)
# RESULT :
Thus the java code executed to implement a simple calculator.

# PROGRAM 5
# AIM:
To design a simple text editor JavaScript application where we can manipulate the user input in different styles, edit the input, capitalize, and many string operations.

# DESIGNING PROCEDURE:
STEP 1:
Start define the document as HTML.

STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.

STEP 3:
Define the function for the program as function f1() for bold, function f2() for italics, function f3() for uppercase, function f4() for lowercase, function f5() for capitalize, function f6() for right ,function f7() for left, function f8() for center, function f9() for clear formatting.

STEP 4:
Give the necessary input that is required to design a simple text editor JavaScript application where we can manipulate the user input in different styles, edit the input, capitalize, and many string operations. Get the number for input using document.getElementById.

STEP 5:
Close the script and head tags.

STEP 6:
Give the input type in the body of the HTML.

STEP 7 :
End the HTML structure.

# PROGRAM
`````
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript">
function f1()
{
document.getElementById("num").style.fontWeight="bold";
}
function f2()
{
document.getElementById("num").style.fontStyle="italic";
}
function f3()
{
document.getElementById("num").style.textTransform="uppercase";
}
function f4()
{
document.getElementById("num").style.textTransform="lowercase";
}
function f5()
{
document.getElementById("num").style.textTransform="capitalize";
}
function f6()
{
document.getElementById("num").style.textAlign="right";
}
function f7()
{
document.getElementById("num").style.textAlign="left";
}
function f8()
{
document.getElementById("num").style.textAlign="center";
}



function f9()
{
document.getElementById("num").style.fontWeight = "normal";
document.getElementById("num").style.textAlign = "left";
document.getElementById("num").style.fontStyle = "normal";
}
</script>
</head>
<body>
<form>
<input type="button" onclick="f1()"  value="Bold">
<input type="button" onclick="f2()"  value="Italics">
<input type="button" onclick="f3()"  value="All Caps">
<input type="button" onclick="f4()"  value="Small Caps">
<input type="button" onclick="f5()"  value="Title Case">
<input type="button" onclick="f6()"  value="Align Right">
<input type="button" onclick="f7()"  value="Align Left">
<input type="button" onclick="f8()"  value="Align Center">
<input type="button" onclick="f9()"  value="Clear Formatting">
<textarea rows="10" cols="35" id="num">
Simple Text Editor using JavaScript
</textarea>
</form>
</body>
</html>
`````
# OUTPUT:
![Screenshot 2023-12-31 223906](https://github.com/rajamanikandanravikumar/ODD23-24-WT-JavaScript/assets/145742839/45701810-362e-4792-8d31-78299dc9a594)
# RESULT
Thus the java code executed to design a simple text editor JavaScript application where we can manipulate the user input in different styles, edit the input, capitalize, and many string operations.

# PROGRAM 6:
# AIM:
To design a JavaScript program which displays error messages when a field in form is entered incorrectly.

# DESIGNING PROCEDURE:
STEP 1:
Start define the document as HTML.

STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.

STEP 3:
Define the function for the program as validate().

STEP 4:
Give the necessary input that is required to design a JavaScript program which displays error messages when a field in form is entered incorrectly.Get the number for input using document.getElementById.

STEP 5:
Using for-loop condition and if-else condition displays error messages when a field in form is entered incorrectly. Close the script and head tags.

STEP 6:
Give the input type in the body of the HTML.

STEP 7:
End the HTML structure.

# PROGRAM :
`````
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Form Validation</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
    }
    form {
      width: 300px;
      margin: 20px auto;
    }
    label {
      display: block;
      margin-bottom: 5px;
    }
    input {
      width: 100%;
      padding: 8px;
      margin-bottom: 10px;
      box-sizing: border-box;
    }
    .error {
      color: red;
      font-size: 14px;
      margin-top: -10px;
    }
  </style>
</head>
<body>

  <h2>Form Validation Example</h2>

  <form onsubmit="return validateForm()">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name">
    <div id="nameError" class="error"></div>

    <label for="email">Email:</label>
    <input type="text" id="email" name="email">
    <div id="emailError" class="error"></div>

    <button type="submit">Submit</button>
  </form>

  <script>
    function validateForm() {
      var nameInput = document.getElementById('name');
      var emailInput = document.getElementById('email');
      var nameError = document.getElementById('nameError');
      var emailError = document.getElementById('emailError');

      // Reset error messages
      nameError.innerHTML = '';
      emailError.innerHTML = '';

      // Validate Name
      if (nameInput.value.trim() === '') {
        nameError.innerHTML = 'Name is required.';
        return false;
      }

      // Validate Email
      var emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      if (!emailRegex.test(emailInput.value.trim())) {
        emailError.innerHTML = 'Invalid email address.';
        return false;
      }

      // If validation passes, you can submit the form
      alert('Form submitted successfully!');
      return true;
    }
  </script>

</body>
</html>
`````
# OUTPUT:
![Screenshot 2023-12-31 224151](https://github.com/rajamanikandanravikumar/ODD23-24-WT-JavaScript/assets/145742839/31b4ad34-79a2-4ba1-88e7-9b1260d180b6)
# RESULT
Thus the java code executed to design a JavaScript program which displays error messages when a field in form is entered incorrectly.
