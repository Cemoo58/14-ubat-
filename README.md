# 14-ubat-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Red Heart</title>
<style>
  .heart {
    position: relative;
    width: 100px;
    height: 90px;
    transform: rotate(-45deg);
    background-color: red;
    border-radius: 50px 50px 0 0;
    margin: 50px auto;
    animation: heartBeat 1s infinite alternate;
  }

  .heart:before,
  .heart:after {
    content: '';
    position: absolute;
    top: 0;
    width: 100px;
    height: 150px;
    background-color: red;
    border-radius: 100px 100px 0 0;
  }

  .heart:before {
    left: -50px;
    transform: rotate(-45deg);
  }

  .heart:after {
    left: 0;
    transform: rotate(45deg);
  }

  @keyframes heartBeat {
    0% {
      transform: scale(1);
    }

    100% {
      transform: scale(1.1);
    }
  }

  .white-heart {
    background-color: white;
    animation: changeColor 2s forwards;
  }

  @keyframes changeColor {
    0% {
      background-color: red;
    }

    100% {
      background-color: white;
    }
  }
</style>
</head>
<body>
<div class="heart"></div>
<script>
  setTimeout(function() {
    document.querySelector('.heart').classList.add('white-heart');
  }, 30000); // 3 saniye sonra rengi değiştir
</script>
</body>
</html>
