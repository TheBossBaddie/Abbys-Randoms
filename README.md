<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Epos's Ultimate Movie Zone</title>
  <style>
    body {
      margin: 0;
      font-family: 'Comic Sans MS', sans-serif;
      background: linear-gradient(to right, #1e90ff, #00ffcc);
      color: white;
      text-align: center;
    }

    header {
      padding: 20px;
      font-size: 2.5em;
      background-color: rgba(0, 0, 0, 0.3);
    }

    .movie-container {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 20px;
      padding: 20px;
    }

    .movie-card {
      background: rgba(255, 255, 255, 0.1);
      border-radius: 15px;
      width: 250px;
      padding: 15px;
      transition: transform 0.3s ease;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
    }

    .movie-card:hover {
      transform: scale(1.05);
    }

    .movie-card img {
      width: 100%;
      border-radius: 10px;
    }

    .movie-title {
      margin-top: 10px;
      font-size: 1.3em;
      color: yellow;
    }

    iframe {
      width: 100%;
      border-radius: 10px;
      margin-top: 10px;
    }

    .quiz {
      background: rgba(0, 0, 0, 0.3);
      padding: 20px;
      margin: 40px;
      border-radius: 15px;
    }

    .quiz button {
      background: yellow;
      color: black;
      border: none;
      padding: 10px 20px;
      font-weight: bold;
      cursor: pointer;
      border-radius: 10px;
      margin-top: 10px;
    }

    .result {
      margin-top: 20px;
      font-size: 1.5em;
      color: #fff200;
    }

    footer {
      margin-top: 30px;
      padding: 15px;
      font-size: 1em;
      background-color: rgba(0, 0, 0, 0.2);
    }
  </style>
</head>
<body>

  <header>
    🎬 Epos's Ultimate Movie Zone 🚀
  </header>

  <!-- Background Music -->
  <audio autoplay loop>
    <source src="https://www.bensound.com/bensound-music/bensound-epic.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

  <!-- Movie Cards with YouTube Trailers -->
  <div class="movie-container">
    <div class="movie-card">
      <img src="https://upload.wikimedia.org/wikipedia/en/3/3e/Sonic_the_Hedgehog_film_poster.jpg" alt="Sonic">
      <div class="movie-title">Sonic the Hedgehog</div>
      <iframe src="https://www.youtube.com/embed/szby7ZHLnkA" title="Sonic Trailer" allowfullscreen></iframe>
    </div>

    <div class="movie-card">
      <img src="https://upload.wikimedia.org/wikipedia/en/9/94/Godzilla_vs._Kong.png" alt="Godzilla vs Kong">
      <div class="movie-title">Godzilla vs Kong</div>
      <iframe src="https://www.youtube.com/embed/odM92ap8_c0" title="Godzilla Trailer" allowfullscreen></iframe>
    </div>
  </div>

  <!-- Fun Quiz Section -->
  <div class="quiz">
    <h2>🤖 Which Movie Character Are You?</h2>
    <p>Pick your favorite superpower:</p>
    <select id="power">
      <option value="speed">Super Speed</option>
      <option value="strength">Super Strength</option>
      <option value="intelligence">Genius Mind</option>
      <option value="web">Web-Slinging</option>
    </select>
    <br>
    <button onclick="getCharacter()">Find Out!</button>
    <div class="result" id="resultText"></div>
  </div>

  <footer>
    Made with 💥 by Epos the Movie Master © 2025
  </footer>

  <script>
    function getCharacter() {
      const choice = document.getElementById('power').value;
      let result = '';

      if (choice === 'speed') result = "You're Sonic! Gotta go fast! 🦔💨";
      else if (choice === 'strength') result = "You're Godzilla! King of the Monsters! 🦖🔥";
      else if (choice === 'intelligence') result = "You're Tony Stark aka Iron Man! 💼🔧";
      else if (choice === 'web') result = "You're Spider-Man! Swinging through the city! 🕸🕷";

      document.getElementById('resultText').textContent = result;
    }
  </script>

</body>
</html>
