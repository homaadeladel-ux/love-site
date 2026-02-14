<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<title>لعيونك انتي ❤️</title>
<style>
body {
    background: linear-gradient(to right, #ff758c, #ff7eb3);
    text-align: center;
    font-family: Arial, sans-serif;
    color: white;
    padding: 50px;
    overflow-x: hidden;
}
#content {
    display: none;
}
input {
    padding: 10px;
    font-size: 16px;
    border-radius: 20px;
    border: none;
    margin-top: 10px;
}
button {
    padding: 10px 20px;
    font-size: 16px;
    background: white;
    color: #ff4f81;
    border: none;
    border-radius: 20px;
    cursor: pointer;
    margin-top: 10px;
}
.hearts {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
  overflow: hidden;
}
.heart {
  position: absolute;
  width: 20px;
  height: 20px;
  background: red;
  transform: rotate(45deg);
  animation: float 5s linear infinite;
}
.heart:before,
.heart:after {
  content: "";
  position: absolute;
  width: 20px;
  height: 20px;
  background: red;
  border-radius: 50%;
}
.heart:before { top: -10px; left: 0; }
.heart:after { left: 10px; top: 0; }
@keyframes float {
  0% { transform: translateY(0) rotate(45deg); opacity: 1; }
  100% { transform: translateY(-600px) rotate(45deg); opacity: 0; }
}
</style>
</head>
<body>

<h2>الموقع ده مخصوص ليكي ❤️</h2>

<div id="login">
    <p>اكتبي كلمة السر يا قلبي 💕</p>
    <input type="password" id="password" placeholder="ادخلي الباسورد">
    <br>
    <button onclick="checkPassword()">دخول 💖</button>
</div>

<div id="content">
    <h1>كل عيد حب وإنتي قلبي ❤️</h1>
    <p>بحبك أكتر من أي حاجة في الدنيا 💘</p>
    <p>من يوم ما عرفتك وأنا عايش أحلى أيام حياتي 💕</p>
    <p>انتِ سبب كل سعادتي 😍</p>
</div>

<div class="hearts"></div>

<audio autoplay loop>
  <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
  متصفحك مش بيدعم الصوت
</audio>

<script>
function checkPassword() {
    var pass = document.getElementById("password").value;
    if(pass === "1913") {  // غير "حبيبي" للباسورد اللي انت عايزه
        document.getElementById("login").style.display = "none";
        document.getElementById("content").style.display = "block";
    } else {
        alert("غلط يا قلبي 😅");
    }
}

// القلوب المتحركة
function createHeart() {
  const heart = document.createElement('div');
  heart.className = 'heart';
  heart.style.left = Math.random() * 100 + '%';
  heart.style.animationDuration = (Math.random() * 3 + 2) + 's';
  document.querySelector('.hearts').appendChild(heart);
  setTimeout(() => heart.remove(), 5000);
}
setInterval(createHeart, 300);
</script>

</body>
</html>
