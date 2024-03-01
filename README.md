<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Interactive Invite</title>
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
  }
  #question {
    font-size: 24px;
    margin-bottom: 20px;
  }
  .answer-btn {
    padding: 10px 20px;
    font-size: 18px;
    cursor: pointer;
    margin: 0 10px;
    border: 2px solid #000;
    background-color: #fff;
    transition: transform 0.3s;
  }
  .answer-btn:hover {
    transform: scale(1.1);
  }
  #hearts {
    font-size: 40px;
    margin-top: 20px;
  }
</style>
</head>
<body>

<div id="question">Facciamo pace?</div>
<button class="answer-btn" onclick="handleAnswer(true)">Si, ti voglio bene</button>
<button class="answer-btn" onclick="handleAnswer(false)">No, ti odio</button>

<div id="hearts"></div>

<script>
  let heartsCount = 0;

  function handleAnswer(isPositive) {
    const heartsDiv = document.getElementById('hearts');
    if (isPositive) {
      heartsDiv.innerHTML += '❤️';
    } else {
      heartsDiv.innerHTML += '💔';
      heartsCount++;
    }
  }
</script>

</body>
</html>
