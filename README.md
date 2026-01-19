<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <title>Kỷ niệm của chúng ta 💖</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: 'Segoe UI', sans-serif;
      scroll-snap-type: y mandatory;
      overflow-y: scroll;
      background: #ffd6e7;
      color: #8b004f;
    }
    section {
      height: 100vh;
      scroll-snap-align: start;
      padding: 40px 20px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
    }
    h1, h2 { margin-bottom: 20px; }

    /* Password screen */
    #lock {
      position: fixed;
      inset: 0;
      background: #ffd6e7;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      z-index: 1000;
    }
    input {
      padding: 10px;
      border-radius: 10px;
      border: 1px solid #ff5fa2;
      margin: 10px;
      font-size: 16px;
    }
    button {
      padding: 10px 20px;
      border: none;
      border-radius: 20px;
      background: #ff5fa2;
      color: white;
      font-size: 16px;
      cursor: pointer;
    }

    /* Hearts */
    .heart {
      position: fixed;
      top: -10px;
      color: #ff5fa2;
      animation: fall 8s linear infinite;
      font-size: 20px;
    }
    @keyframes fall { to { transform: translateY(110vh); } }

    /* Flip cards */
    .grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 15px;
      max-width: 600px;
    }
    .card { perspective: 1000px; cursor: pointer; }
    .card-inner {
      width: 100%; padding-top: 100%; position: relative;
      transition: transform 0.6s; transform-style: preserve-3d;
    }
    .card.flipped .card-inner { transform: rotateY(180deg); }
    .card-face {
      position: absolute; inset: 0; border-radius: 12px;
      backface-visibility: hidden; display: flex;
      align-items: center; justify-content: center;
      background: #ffb3d9;
    }
    .card-back {
      transform: rotateY(180deg);
      background-size: cover; background-position: center;
    }

    video { max-width: 90%; border-radius: 16px; margin-bottom: 20px; }

    .letter {
      max-width: 900px;
      height: 70vh;
      overflow-y: auto;
      background: rgba(255,255,255,0.6);
      padding: 30px;
      border-radius: 20px;
      text-align: left;
      line-height: 1.8;
      font-size: 17px;
    }
  </style>
</head>
<body>

<!-- Password -->
<div id="lock">
  <h2>💗 Chỉ dành cho chúng ta 💗</h2>
  <p>Gợi ý: ngày sinh của tôi và  cộng lại – tháng sinh cộng lại – năm sinh của cả hai</p>
  <input type="password" id="pass" placeholder="Nhập mật khẩu" />
  <button onclick="unlock()">Mở khoá</button>
</div>

<!-- Music -->
<audio autoplay loop controls style="position:fixed;bottom:10px;left:10px;z-index:10">
  <source src="binh-yen-vu.mp3" type="audio/mpeg">
</audio>

<section>
  <h1>💖 21/01/2023 💖</h1>
  <h2>Chúng ta đã bên nhau <span id="days"></span> ngày</h2>
  <p>Kéo xuống nhé 👇</p>
</section>

<section>
  <h2>Những khoảnh khắc bên nhau</h2>
  <div class="grid">
    <div class="card" onclick="flip(this)"><div class="card-inner"><div class="card-face">💌</div><div class="card-face card-back" style="background-image:url('img1.jpg')"></div></div></div>
    <div class="card" onclick="flip(this)"><div class="card-inner"><div class="card-face">💗</div><div class="card-face card-back" style="background-image:url('img2.jpg')"></div></div></div>
    <div class="card" onclick="flip(this)"><div class="card-inner"><div class="card-face">💕</div><div class="card-face card-back" style="background-image:url('img3.jpg')"></div></div></div>
    <div class="card" onclick="flip(this)"><div class="card-inner"><div class="card-face">💞</div><div class="card-face card-back" style="background-image:url('img4.jpg')"></div></div></div>
  </div>
</section>

<section>
  <h2>Lá thư của chúng tôi</h2>
  <div class="letter">
    <p><b>Em yêu à,</b></p>
    <p>(Cảm ơn em vì đã tới bên đời tui và đã ở bên nhau được tới bây giờ, dù nhiều chyện xảy ra dù cả hai đôi khi thấy mệt mỏi, dù có khi mọi chuyện trở nên tồi tệ, nhưng sau tất vẫn thấy rất hạnh phúc vì chúng mình còn bên nhau vẫn trân trọng, hạnh phúc mỗi khi thức dậy mở mắt kế bên vẫn là em. Những đêm ngủ có người kề bên ấm áp và dịu êm. Thực lòng mong em sẽ mãi luôn bên tui để cùng nhau bước tiếp đồng hành vượt qua sóng gió trưởng thành và mong năm mới tới cùng nhau phát triển, cùng bước tới vùng đất mới, trải nghiệm những thử thách,những trò chơi, những điều mới lạ mà cả hai chưa từng thử. Và thực khách trung thành của tui vẫn sẽ tiếp tục ủng hộ những bữa cơm ấm áp, dù đôi khi có những món ăn chưa hoàn hảo nhưng vẫn mong iem sẽ vẫn là vị khách đặc biệt mỗi sáng, trưa, tối của đầu bếp vụng về này. Yêu em nhiều lắm dù em lì nhất nhưng khi em tới bên đời tui thật sự rất hạnh phúc và thấy may mắn khi mình bên nhau như một gia đình, người thân của nhau cùng nhau thăm gia đình. Sắp tới mong em vẫn sẽ bên cạnh tui chăm sóc và được tui chăm sóc nhé! Yêu em rất rất nhìu <3)</p>
  </div>
</section>

<section>
  <h2>Chúng ta 💕</h2>
  <video controls autoplay muted loop>
    <source src="love-video.mp4" type="video/mp4">
  </video>
</section>

<script>
  function flip(card){ card.classList.toggle('flipped'); }
  function unlock(){
    if(document.getElementById('pass').value === '46-12-2004'){
      document.getElementById('lock').style.display='none';
    } else { alert('Sai mật khẩu rồi 😢'); }
  }
  const start = new Date('2023-01-21');
  const now = new Date();
  const diff = Math.floor((now - start)/(1000*60*60*24));
  document.getElementById('days').innerText = diff;

  setInterval(() => {
    const heart = document.createElement('div');
    heart.className = 'heart'; heart.innerText = '❤';
    heart.style.left = Math.random()*100 + 'vw';
    heart.style.fontSize = (16 + Math.random()*20) + 'px';
    document.body.appendChild(heart);
    setTimeout(()=>heart.remove(),8000);
  }, 400);
</script>
</body>
</html>
# anniversary-love-
