---
title: Home
academia: true
---

### Welcome to Zero's website! Here, you can learn more about him and his work.

<div>
    <strong>His local time (Pacific) is</strong>:
    <span id="datetime-text"></span>
</div>


**What is Zero up to?**

<i id="custom-text"></i>
<script>
function refreshTime() {
  let customTextDiv = document.getElementById("custom-text");
  let datetimeTextDiv = document.getElementById("datetime-text");
  const showingDate = new Date().toLocaleString("en-US", {
        timeZone: "America/Los_Angeles",
        year: 'numeric',
        month: 'short',
        day: '2-digit',
        hour: "2-digit",
        minute: "2-digit",
        second: "2-digit",
        hour12: false,
  })
  const fixedDate = new Date().toLocaleString("en-US", {
    timeZone: "America/Los_Angeles",
    hour: "2-digit",
    minute: "2-digit",
    hour12: false,
  });
  const datetimeText = showingDate;
  const [specificHour, specificMinute] = fixedDate.split(":").map(Number);
  const currentDaytime = `${specificHour}:${specificMinute}`;
  let displayText = "";
  function isTimeInRange(checkTime, startTime, endTime) {
    const [checkHour, checkMinute] = checkTime.split(":").map(Number);
    const [startHour, startMinute] = startTime.split(":").map(Number);
    const [endHour, endMinute] = endTime.split(":").map(Number);
    const checkTotalMinutes = checkHour * 60 + checkMinute;
    const startTotalMinutes = startHour * 60 + startMinute;
    const endTotalMinutes = endHour * 60 + endMinute;
    if (startTotalMinutes <= endTotalMinutes) {
      return (
        checkTotalMinutes >= startTotalMinutes &&
        checkTotalMinutes <= endTotalMinutes
      );
    } else {
      return (
        checkTotalMinutes >= startTotalMinutes ||
        checkTotalMinutes <= endTotalMinutes
      );
    }
  }
  if (isTimeInRange(currentDaytime, "07:01", "08:00")) {
    displayText = "He is eating a hearty breakfast.";
  } else if (isTimeInRange(currentDaytime, "08:01", "12:00")) {
    displayText =
      "He is diligently working. Sometimes he is teaching, other times he is doing research in his cave.";
  } else if (isTimeInRange(currentDaytime, "12:01", "13:00")) {
    displayText =
      "He is eating a low-carb meal and debating whether to drink Dr. Pepper.";
  } else if (isTimeInRange(currentDaytime, "13:01", "16:00")) {
    displayText =
      "He is diligently working. Sometimes he is teaching, other times he is doing research in his cave.";
  } else if (isTimeInRange(currentDaytime, "16:01", "18:00")) {
    displayText = "He is tangling with his kids.";
  } else if (isTimeInRange(currentDaytime, "18:01", "19:00")) {
    displayText = "He is pouring a glass of wine.";
  } else if (isTimeInRange(currentDaytime, "19:01", "20:00")) {
    displayText = "He is resting.";
  } else if (isTimeInRange(currentDaytime, "20:01", "21:00")) {
    displayText = "He is enjoying a fine cigar."
  }
  else if (isTimeInRange(currentDaytime, "21:01", "22:00")) {
    displayText = "He is enjoying a movie.";
  } else if (isTimeInRange(currentDaytime, "22:01", "07:00")) {
    displayText = "He is sleeping.";
  } else {
    displayText = "He is in meditation.";
  }
  customTextDiv.innerHTML = displayText;
  datetimeTextDiv.innerHTML = datetimeText;
}
refreshTime()
setInterval(refreshTime, 1000); // refresh every min
</script>

<style>
#datetime-text {
    white-space: nowrap;
}
</style>