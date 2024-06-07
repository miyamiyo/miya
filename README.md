<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lato:400,700|Montserrat:900">
    <title>Document</title>
    <style>

body{
    background-color: white;
}
  
#timer {
  color: #eeeeee;
  text-align: center;
  text-transform: uppercase;
  font-family: 'Lato', sans-serif;
  font-size: .7em;
  letter-spacing: 5px;
}

.days {
  display: inline-block;
  padding: 20px;
  width: 100px;
  border-radius: 5px;
}

.days {
  background: #EF2F3C;
}

.numbers {
  font-family: 'Montserrat', sans-serif;
  color:  #183059;
  font-size: 4em;
  text-align: center;
}

.white {
  position: absolute;
  background:  #eeeeee;
  height: 85px;
  width: 75px;
  left: 30%;
  top: 2%;
}


    </style>
</head>
<body>
    
<div id="timer">

    <div class="days"> 
        <div id="days" class="numbers "> </div>days</div>  
      </div>

</div>

</body>
<script>
    const year = new Date().getFullYear();
const myDate = new Date('May 13, 2025 00:00:00');
console.log(myDate);

// countdown
let timer = setInterval(function() {

  // get today's date
  const today = new Date();

  // get the difference
  const diff = myDate - today;

  // math
  let days = Math.floor(diff / (1000 * 60 * 60 * 24));

  // display
  document.getElementById("days").innerHTML=days



}, 1);
</script>
</html>
