<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Tebak-Tebakan Kocak</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #fefefe;
      text-align: center;
      padding: 30px;
    }
    .box {
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px #ccc;
      max-width: 500px;
      margin: auto;
    }
    h1 {
      color: #333;
    }
    #question {
      font-size: 20px;
      margin: 20px 0;
    }
    #answer {
      font-size: 18px;
      color: green;
      margin: 10px 0;
    }
    button {
      padding: 10px 20px;
      margin: 10px;
      font-size: 16px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="box">
    <h1>Tebak-Tebakan Kocak</h1>
    <p>Skor: <span id="score">0</span></p>
    <div id="question">Klik tombol di bawah untuk mulai!</div>
    <div id="answer"></div>
    <button onclick="showAnswer()">Lihat Jawaban</button>
<button onclick="knewIt()">Saya Tahu Jawabannya</button>
    <button onclick="next()">Tebakan Selanjutnya</button>
  </div>

  <script>
    const tebakans = [
      { q: "Kenapa ayam menyebrang jalan?", a: "Karena dia mau ke seberang." },
      { q: "Kenapa kucing suka ngumpet?", a: "Karena dia malu-malu kucing." },
      { q: "Apa bedanya kamu sama kalender?", a: "Kalau kalender ada tanggalnya." },
      { q: "Kenapa komputer suka lembur?", a: "Takut kena virus malas." },
      { q: "Apa yang selalu naik tapi nggak pernah turun?", a: "Usia." },
      { q: "Kenapa ikan di laut diam semua?", a: "Kalau ngomong jadi asin." },
      { q: "Apa makanan favorit hantu?", a: "Setan goreng." },
      { q: "Gajah kalau nyebur ke laut jadi apa?", a: "Basah." },
      { q: "Apa bedanya tukang ojek sama tukang bakso?", a: "Kalau tukang ojek nganter orang, tukang bakso nganter rasa." },
      { q: "Kenapa roti tidak bisa berdiri?", a: "Karena dia empuk." },
      { q: "Kenapa matahari nggak pernah sakit?", a: "Karena dia punya sinar sehat." },
      { q: "Apa yang bisa kamu pecahkan tanpa menyentuh?", a: "Diam." },
      { q: "Kenapa sepeda nggak bisa berdiri sendiri?", a: "Karena dia dua kaki." },
      { q: "Kenapa handphone suka jatuh?", a: "Karena dia suka nge-drop sinyal." },
{ q: "Kucing apa yang bisa nyanyi?", a: "Kucing-cilan Cinta (Chacha-cinta)." },
      { q: "Kenapa kambing suka nabrak?", a: "Karena dia 'me'ndesak." },
      { q: "Apa bedanya pensil sama kamu?", a: "Pensil bisa dihapus, kamu nggak bisa dilupain." },
      { q: "Kenapa bulan malu-malu?", a: "Karena sering ditatap diam-diam." },
      { q: "Kenapa nasi suka sedih?", a: "Karena suka di-'makan' perasaan." },
      { q: "Sayur apa yang romantis?", a: "Sayur lodeh… I love you deh." }
    ];

    let index = 0;
    let score = 0;

    function load() {
      document.getElementById("question").textContent = tebakans[index].q;
      document.getElementById("answer").textContent = "";
    }

    function showAnswer() {
      document.getElementById("answer").textContent = tebakans[index].a;
    }

    function knewIt() {
      score++;
      document.getElementById("score").textContent = score;
      alert("Mantap! Skormu naik.");
    }

    function next() {
      index = (index + 1) % tebakans.length;
      load();
    }

    window.onload = load;
  </script>
</body>
</html>
