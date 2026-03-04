# Happy-birthdayy
Happy birthday greeting page
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Kaka 🎂</title>

<style>
body {
    margin: 0;
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #ff9a9e, #fad0c4);
    text-align: center;
    color: white;
    overflow: hidden;
}

.container {
    padding: 40px 20px;
    position: relative;
    z-index: 2;
}

.card {
    background: rgba(255,255,255,0.15);
    padding: 30px;
    border-radius: 20px;
    backdrop-filter: blur(10px);
    box-shadow: 0 8px 20px rgba(0,0,0,0.2);
    max-width: 400px;
    margin: auto;
}

input {
    padding: 12px;
    width: 80%;
    border-radius: 10px;
    border: none;
    margin-top: 15px;
    text-align: center;
    font-size: 16px;
}

button {
    margin-top: 20px;
    padding: 12px 20px;
    border: none;
    border-radius: 30px;
    background: #ff4b2b;
    color: white;
    font-size: 16px;
    cursor: pointer;
    transition: 0.3s;
}

button:hover {
    background: #ff416c;
}

.message {
    margin-top: 20px;
    display: none;
}

.cake {
    font-size: 60px;
}

/* 🎈 BALON */
.balloon {
    position: absolute;
    bottom: -150px;
    font-size: 40px;
    animation: naik 10s linear infinite;
}

@keyframes naik {
    0% {transform: translateY(0);}
    100% {transform: translateY(-120vh);}
}
</style>
</head>

<body>

<!-- 🎵 Musik -->
<audio autoplay loop>
  <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
</audio>

<!-- 🎈 Balon -->
<div class="balloon" style="left:10%;">🎈</div>
<div class="balloon" style="left:30%; animation-delay:2s;">🎈</div>
<div class="balloon" style="left:50%; animation-delay:4s;">🎈</div>
<div class="balloon" style="left:70%; animation-delay:1s;">🎈</div>
<div class="balloon" style="left:90%; animation-delay:3s;">🎈</div>

<div class="container">
    <div class="card">
        <div class="cake">🎂🎉</div>
        <h2>Selamat Ulang Tahun Kaka 💖</h2>

        <input type="text" id="nama" placeholder="Masukkan Nama Kaka">
        <br>
        <button onclick="tampilkanUcapan()">Buka Ucapan 🎁</button>

        <div class="message" id="ucapan">
            <p id="isiUcapan"></p>
            <button onclick="kirimWA()">Balas di WhatsApp 💬</button>
        </div>
    </div>
</div>

<script>
function tampilkanUcapan() {
    var nama = document.getElementById("nama").value;
    if(nama === "") {
        alert("Masukkan dulu nama kaka ya 😊");
        return;
    }

    var teks = `
    🎉 Selamat Ulang Tahun ${nama}! 🎂✨ <br><br>
    Semoga panjang umur, sehat selalu, banyak rezeki dan bahagia terus 💖<br><br>
    Sekarang sudah makin tua nih 😜 uban mulai muncul 🤭<br>
    Tapi tetap jadi kaka terbaik sedunia ❤️🔥
    `;

    document.getElementById("isiUcapan").innerHTML = teks;
    document.getElementById("ucapan").style.display = "block";
}

function kirimWA() {
    var nama = document.getElementById("nama").value;
    var pesan = `Selamat ulang tahun ${nama}! 🎂🎉 Semoga panjang umur dan makin tua makin bijak ya 😆`;
    var url = "https://wa.me/?text=" + encodeURIComponent(pesan);
    window.open(url, "_blank");
}
</script>

</body>
</html>
