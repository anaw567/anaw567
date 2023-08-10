<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FC Efficiency Challenge Countdown</title>
<style>
  body {
    margin: 0;
    padding: 0;
 
    background-size: cover;
    font-family: Arial, sans-serif;
    color: gray;
  }
  .container {
    text-align: center;
    padding-top: 200px;
  }
  .title {
    font-size: 80px;
    color: rgb(7, 92, 204);
  }
  .countdown {
    font-size: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
  }
  .countdown-item {
    text-align: center;
    margin: 0 20px;
  }
  .countdown-label {
    font-size: 20px;
    margin-top: 5px;
  }
</style>
</head>
<body>
<div class="container">
  <div class="title">FC Efficiency Challenge</div>
   <div class="body">October 12, 2023 - 10:00am</div>
  <div class="countdown">
    <div class="countdown-item">
      <span id="days"></span>
      <div class="countdown-label">Days</div>
    </div>
    <div class="countdown-item">
      <span id="hours"></span>
      <div class="countdown-label">Hours</div>
    </div>
    <div class="countdown-item">
      <span id="minutes"></span>
      <div class="countdown-label">Minutes</div>
    </div>
    <div class="countdown-item">
      <span id="seconds"></span>
      <div class="countdown-label">Seconds</div>
    </div>
  </div>
</div>
<script>
  const targetDate = new Date("October 12, 2023 10:00:00").getTime();

  const updateCountdown = () => {
    const now = new Date().getTime();
    const timeLeft = targetDate - now;

    const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
    const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);

    document.getElementById("days").textContent = days;
    document.getElementById("hours").textContent = hours;
    document.getElementById("minutes").textContent = minutes;
    document.getElementById("seconds").textContent = seconds;
  };

  updateCountdown();
  setInterval(updateCountdown, 1000);
</script>
</body>
</html>
