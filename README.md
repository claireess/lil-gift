# lil-gift
<!DOCTYPE html>

<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>A Special Package</title>
  <style>
    body {
      margin: 0;
      min-height: 100vh;
      background: linear-gradient(180deg, #0b1d3a, #4a0f1f);
      font-family: Arial, sans-serif;
      color: white;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .box {
      width: 90%;
      max-width: 500px;
      background: rgba(0,0,0,0.5);
      padding: 20px;
      border-radius: 16px;
    }
    button {
      width: 100%;
      padding: 12px;
      margin-top: 15px;
      font-size: 16px;
      border: none;
      border-radius: 10px;
    }
    .cats {
      text-align: center;
      margin-top: 12px;
      font-size: 22px;
    }
  </style>
</head>
<body>

<div class="box">
  <div id="text">
    Hello! Excuse me. I didn't mean to bother!<br><br>
    I promise I won't take up much of your time.<br><br>
    I'm on a mission, actually.<br>
    I need to deliver this package to a very special person.
  </div>

<button onclick="next()">Continue</button>

  <div class="cats">🐱 💙 🐱 ❤️ 🐱</div>
</div>

<script>
  let step = 0;
  let name = "";
  const text = document.getElementById("text");

  function next() {
    step++;

    if (step === 1) {
      text.innerHTML = "Before I continue...<br><br>May I ask your name?";
      return;
    }

    if (step === 2) {
      name = prompt("Your name:");
      if (!name) return;
      text.innerHTML = "Oh, " + name + "... Is that really you?";
      return;
    }

    if (step === 3) {
      text.innerHTML = "Okay, so... In the letter it says:<br><br>Dear " + name + ",<br><br>I hope this letter finds you well. It took me a pretty long time until I finally had an idea of something nice to do for you. I wanted it to be meaningful and speacial for you. After all, you deserve absolutely the best, everything of good in this whole world. You are an amazing girl and I couldn't be any more grateful to have in my life. Thank you for being so kind and gentle to me all the time. You're an angel that just appeared in my life out of nowhere. I plan to keep you in my life, if you'll have me. Well, I don't really know what to say, but I hope you know just how happy you make me and how much I appreciate you. I love you, " + name + ". So, you said you'd give me something on 31/12/2025, correct? (but i'm giving this to you earlier haha) So, I decided to give you this. It wouldn't be nice if you gave me something and I didn't give you anything in return, right? Anyways... It's so interesting how people can simply appear in your life and change it so quickly, isn't it? Hahah, I still can't believe on how fast everything happened, but it's not all bad, actually. I already like you so much. So...<br><br>My dear Ania...<br><br>Would you be my girlfriend?";
      return;
    }

    if (step === 4) {
      text.innerHTML = "I love you, my sweet girl.<br><br>With love,<br>Your very new girlfriend, Clarice. <3";
      return;
    }
  }
</script>

</body>
</html>
