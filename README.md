<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Merry Christmas</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            text-align: center;
            background: linear-gradient(to bottom, #2b5876, #4e4376);
            color: #ffffff;
            overflow: hidden;
        }
        .card {
            margin: 20px auto;
            padding: 20px;
            border: 5px solid #ff4500;
            width: 90%; /* 更宽的自适应布局 */
            max-width: 600px; /* 限制最大宽度 */
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            z-index: 10;
            position: relative;
        }
        h1 {
            font-size: 5vw; /* 使用相对单位自适应屏幕 */
            color: #b22222;
        }
        p {
            font-size: 4vw; /* 使用相对单位自适应屏幕 */
            line-height: 1.6;
            color: #000000; /* 修改字体为黑色 */
        }
        .tree {
            font-size: 4vw; /* 树的大小也自适应 */
            line-height: 1.2;
            margin: 10px 0;
            color: #228b22;
        }
        .tree .ornament {
            color: red;
            font-size: 4.5vw; /* 彩球大小自适应 */
        }
        .snow {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        .snowflake {
            position: absolute;
            top: -10px;
            font-size: 24px;
            color: white;
            animation: fall 10s linear infinite;
        }
        @keyframes fall {
            0% {
                transform: translateY(0) rotate(0deg);
            }
            100% {
                transform: translateY(100vh) rotate(360deg);
            }
        }
        audio {
            margin-top: 20px;
            width: 90%; /* 音频控件也自适应 */
        }
    </style>
</head>
<body>
    <!-- 动态雪花 -->
    <div class="snow" id="snow-container"></div>

    <!-- 圣诞贺卡内容 -->
    <div class="card">
        <h1>Merry Christmas! 🎄</h1>
        <div class="tree">
            ★<br>
            <span class="ornament">🎄</span><br>
           🎄🎄🎄<br>
          🎄<span class="ornament">🎁</span>🎄🎄🎄<br>
         🎄🎄🎄<span class="ornament">🎁</span>🎄🎄<br>
        🎄🎄<span class="ornament">🎁</span>🎄🎄🎄🎄🎄<br>
       🎄🎄🎄🎄🎄🎄🎄🎄🎄<br>
        <br>
        </div>
        <p>圣诞到，雪花飘，圣诞老人把门叫。</p>
        <p>麋鹿跳，礼物到，快快开门把礼瞧。</p>
        <p>不是金不是银，手机微信有一条。</p>
        <p><b>祝大家圣诞节快乐，天天开心，事事顺利💕</b></p>
        <p>— Alvin</p>
        <audio controls>
            <source src="https://www.bensound.com/bensound-music/bensound-wishyouamerrychristmas.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
        </audio>
    </div>

    <script>
        // 动态雪花生成
        const snowContainer = document.getElementById('snow-container');
        for (let i = 0; i < 100; i++) {
            const snowflake = document.createElement('div');
            snowflake.className = 'snowflake';
            snowflake.style.left = Math.random() * 100 + 'vw';
            snowflake.style.animationDuration = Math.random() * 5 + 5 + 's';
            snowflake.style.fontSize = Math.random() * 10 + 10 + 'px';
            snowflake.textContent = '❄';
            snowContainer.appendChild(snowflake);
        }
    </script>
</body>
</html>
