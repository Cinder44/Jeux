<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Je n'ai jamais - Couple & Alcool</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background-color: #fef6f9;
      margin: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }
    h1 {
      color: #d6336c;
    }
    #card {
      background-color: #fff;
      border-radius: 20px;
      padding: 2rem;
      box-shadow: 0 0 10px rgba(0,0,0,0.2);
      text-align: center;
      width: 90%;
      max-width: 500px;
      transition: all 0.3s ease;
    }
    #card p {
      font-size: 1.5rem;
    }
    .romantique { border-left: 10px solid #ff85a2; }
    .fun { border-left: 10px solid #ffd166; }
    .alcool { border-left: 10px solid #6ec6ff; }
    .spicy { border-left: 10px solid #f17c67; }
    .coquin { border-left: 10px solid #ce64b5; }
    .extreme { border-left: 10px solid #8b0000; color: #8b0000; }
    button {
      margin-top: 1rem;
      padding: 0.8rem 1.5rem;
      background-color: #d6336c;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      font-size: 1rem;
    }
    img {
      max-height: 60px;
      margin-bottom: 1rem;
    }
  </style>
</head>
<body>
  <h1>🎴 Je n'ai jamais - Couple & Alcool</h1>
  <div id="card" class="romantique">
    <img id="icon" src="https://cdn-icons-png.flaticon.com/512/1077/1077035.png" alt="icone">
    <p id="statement">Clique sur le bouton pour commencer !</p>
  </div>
  <button onclick="nextCard()">➡️ Carte suivante</button>

  <script>
    const cards = [
      { text: "Je n’ai jamais écrit une lettre d’amour.", type: "romantique", icon: "https://cdn-icons-png.flaticon.com/512/1077/1077035.png" },
      { text: "Je n’ai jamais dansé nu(e) chez moi.", type: "fun", icon: "https://cdn-icons-png.flaticon.com/512/4151/4151724.png" },
      { text: "Je n’ai jamais vomi à cause de l’alcool.", type: "alcool", icon: "https://cdn-icons-png.flaticon.com/512/1046/1046784.png" },
      { text: "Je n’ai jamais utilisé un jouet sexuel.", type: "spicy", icon: "https://cdn-icons-png.flaticon.com/512/3094/3094626.png" },
      { text: "Je n’ai jamais pensé à toi en me masturbant.", type: "coquin", icon: "https://cdn-icons-png.flaticon.com/512/2762/2762085.png" },
      { text: "Je n’ai jamais eu une relation anale.", type: "extreme", icon: "https://cdn-icons-png.flaticon.com/512/2913/2913465.png" },
      { text: "Je n’ai jamais crié le nom de mon/ma partenaire pendant un orgasme.", type: "extreme", icon: "https://cdn-icons-png.flaticon.com/512/2913/2913465.png" },
      { text: "Je n’ai jamais fait un strip-tease.", type: "spicy", icon: "https://cdn-icons-png.flaticon.com/512/3094/3094626.png" },
      { text: "Je n’ai jamais envoyé un message que je regrette à cause de l’alcool.", type: "alcool", icon: "https://cdn-icons-png.flaticon.com/512/1046/1046784.png" },
      { text: "Je n’ai jamais regardé un porno avec mon/ma partenaire.", type: "coquin", icon: "https://cdn-icons-png.flaticon.com/512/2762/2762085.png" },
      { text: "Je n’ai jamais pleuré à cause d’un film d’amour.", type: "romantique", icon: "https://cdn-icons-png.flaticon.com/512/1077/1077035.png" },
    ];

    function nextCard() {
      const card = cards[Math.floor(Math.random() * cards.length)];
      const el = document.getElementById("card");
      el.className = card.type;
      document.getElementById("statement").textContent = card.text;
      document.getElementById("icon").src = card.icon;
    }
  </script>
</body>
</html>
