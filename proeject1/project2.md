second beginner project 
BGMI

``` html   ```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>

        body{ background:gray}
        button{ width: 150px;
  height: 35px;
  margin-left: 90px;
  margin-top: 25px;
  background-color: #fff;
  padding: 1px 30px;
  border-radius: 8px;
  color: #212121;
   }
   #weight-guide {
  margin-left: 75px;
  margin-top: 25px;
}

.container {
  width: 575px;
  height: 825px;

  background-color: #797978;
  padding-left: 30px;
}

    </style>
</head>
<body>
    <nav>
        <a href="https://stackblitz.com/edit/dom-project-chaiaurcode?file=1-" home></a>
        <a href="https://stackblitz.com/edit/dom-project-chaiaurcode?file=1-" facebbook></a>


    </nav>
     <div class="container">
    <h1>BMI CALCULATER</h1>
    <FORM>
        <p><lable > Height in cm:</lable><input type="text" id ="height"></p>
        <p><lable > weight in kg:</lable><input type="text" id ="weight"></p>
       <button>Calculator</button>
       <div id="results"></div>
       <div id="weight-guide">
       <h3>  BMI Weight guide</h3>
       <p>under weight = less than 18.7</p>
       <p> normal range =18.6 and 24.9</p>
       <p> overweight= greater than  24.9</p>

       </div>


        











    </FORM>
<script>

```   javascript
```

const form = document.querySelector('form');
// this usecase will give you empty
// const height = parseInt(document.querySelector('#height').value)

form.addEventListener('submit', function (e) {
  e.preventDefault();

  const height = parseInt(document.querySelector('#height').value);
  const weight = parseInt(document.querySelector('#weight').value);
  const results = document.querySelector('#results');

  if (height === '' || height < 0 || isNaN(height)) {
    results.innerHTML = `Please give a valid height ${height}`;
  } else if (weight === '' || weight < 0 || isNaN(weight)) {
    results.innerHTML = `Please give a valid weight ${weight}`;
  } else {
    const bmi = (weight / ((height * height) / 10000)).toFixed(2);
    //show the result
    results.innerHTML = `<span>${bmi}</span>`;
  }
  });



















    </script>
</body>
</html>