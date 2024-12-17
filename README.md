<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>힐링 카드 뽑기</title>
  <link href="https://fonts.googleapis.com/css2?family=Cute+Font&family=Gaegu&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background-image: url('https://images.unsplash.com/photo-1448375240586-882707db888b?q=80&w=2670&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
      background-size: cover;
      background-position: center;
      background-attachment: fixed;
      color: #ffffff;
    }
    
    .container {
      text-align: center;
      background-color: rgba(0, 0, 0, 0.6);
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
      max-width: 400px;
    }
    
    h1 {
      font-size: 1.8em;
      margin-bottom: 20px;
      color: #ff9ff3;
      font-family: "Gaegu", sans-serif;
    }
    
    .card {
      background-color: rgba(255, 255, 255, 0.9);
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      margin-bottom: 20px;
      min-height: 100px;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    
    .card p {
      margin: 0;
      font-size: 1.2em;
      color: #2d3436;
      text-align: center;
      font-family: "Gaegu", sans-serif;
    }
    
    button {
      background-color: #74b9ff;
      color: white;
      border: none;
      padding: 10px 20px;
      font-size: 1em;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s;
      font-family: "Gaegu", sans-serif;
    }
    
    button:hover {
      background-color: #0984e3;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>힐링 카드 뽑기</h1>
    <div class="card" id="card">
      <p>오늘의 힐링 메시지를 뽑아보세요!</p>
    </div>
    <button onclick="pickCard()">카드 뽑기</button>
  </div>
  <script>
    const messages = [
      "넌 지금도 충분히 잘하고 있어!",
      "작은 휴식이 큰 힘이 돼.",
      "걱정하지 마, 모든 게 잘 될 거야.",
      "너는 사랑받기 위해 태어났어.",
      "오늘도 스스로를 칭찬해줘!"
    ];
    
    function pickCard() {
      const randomIndex = Math.floor(Math.random() * messages.length);
      const cardElement = document.getElementById("card");
      cardElement.innerHTML = `<p>${messages[randomIndex]}</p>`;
    }
  </script>
</body>
</html>
