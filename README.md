# Happy-birthday-Pyariiiiiii-bhonduuuuuuuuu
This is for you
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Bhondu ❤️</title>
    <style>
        :root {
            --pink: #ff85a2;
            --dark-pink: #ff4d6d;
            --soft-white: #fff0f3;
        }

        body, html {
            margin: 0; padding: 0; height: 100%; width: 100%;
            font-family: 'Arial', sans-serif;
            background-color: var(--soft-white);
            display: flex; justify-content: center; align-items: center;
            overflow: hidden;
        }

        .page {
            position: absolute; width: 100%; height: 100%;
            display: flex; flex-direction: column;
            justify-content: center; align-items: center;
            text-align: center; padding: 20px; box-sizing: border-box;
            background-color: var(--soft-white);
            transition: opacity 0.5s ease;
        }

        .hidden { display: none !important; }

        /* Page 1: Login */
        .main-img {
            width: 180px; height: 180px; border-radius: 50%;
            border: 5px solid white; box-shadow: 0 8px 15px rgba(0,0,0,0.1);
            object-fit: cover; animation: bounce 3s infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-15px); }
        }

        input {
            padding: 12px; border-radius: 20px; border: 2px solid var(--pink);
            margin-top: 20px; width: 200px; text-align: center; outline: none;
        }

        /* Page 2: The Big Gift Box */
        .gift-box-large {
            font-size: 100px; cursor: pointer;
            animation: wiggle 1s infinite;
        }

        @keyframes wiggle {
            0%, 100% { transform: rotate(0); }
            25% { transform: rotate(-5deg); }
            75% { transform: rotate(5deg); }
        }

        /* Page 3: The Three Gifts */
        .gift-grid { display: flex; gap: 15px; }
        .gift-item {
            font-size: 50px; background: white; padding: 20px;
            border-radius: 15px; cursor: pointer; box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        /* Modals/Popups */
        .modal {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.5); display: flex;
            justify-content: center; align-items: center; z-index: 1000;
        }

        .modal-content {
            background: white; padding: 30px; border-radius: 20px;
            width: 80%; max-width: 350px; text-align: center;
            position: relative;
        }

        .btn {
            background: var(--pink); color: white; border: none;
            padding: 10px 20px; border-radius: 20px; cursor: pointer;
            margin-top: 15px; font-weight: bold;
        }

        #cake-icon { width: 120px; cursor: pointer; }
        .photo-frame { width: 100%; border-radius: 10px; margin-top: 10px; }
    </style>
</head>
<body>

    <audio id="myAudio" loop>
        <source src="https://docs.google.com/uc?export=download&id=1v7OxNPdOqlXrTus4x-xNmzFKwd2UIGOS" type="audio/mpeg">
    </audio>

    <div id="page1" class="page">
        <img src="https://docs.google.com/uc?export=download&id=1QO6l3p3zUNc1sZblGxMvhXaOSW1cT7fQ" class="main-img">
        <h2 style="color: var(--dark-pink);">Hello My Panda! ❤️</h2>
        <input type="password" id="passInput" placeholder="Enter Password...">
        <button class="btn" onclick="startExperience()">Unlock My Heart 🔓</button>
    </div>

    <div id="page2" class="page hidden">
        <h1 style="color: var(--dark-pink);">A Surprise is Waiting...</h1>
        <div class="gift-box-large" onclick="openSurprise()">🎁</div>
        <p>Click the box to open!</p>
    </div>

    <div id="page3" class="page hidden">
        <h2 style="color: var(--dark-pink);">Choose Your Surprise!</h2>
        <div class="gift-grid">
            <div class="gift-item" onclick="openModal('modal1')">📦</div>
            <div class="gift-item" onclick="openModal('modal2')">📦</div>
            <div class="gift-item" onclick="openModal('modal3')">📦</div>
        </div>
    </div>

    <div id="modal1" class="modal hidden">
        <div class="modal-content">
            <h3>Make a Wish! 🕯️</h3>
            <img src="https://cdn-icons-png.flaticon.com/512/3132/3132715.png" id="cake-icon" onclick="blowCandle()">
            <div id="cake-status"></div>
            <button class="btn" onclick="closeModal('modal1')">Close</button>
        </div>
    </div>

    <div id="modal2" class="modal hidden">
        <div class="modal-content">
            <h3>You look so cute! ✨</h3>
            <img src="https://docs.google.com/uc?export=download&id=1rdVd6sgKWsodlG2BhqGrRQnK875DrOVe" class="photo-frame">
            <button class="btn" onclick="closeModal('modal2')">Close</button>
        </div>
    </div>

    <div id="modal3" class="modal hidden">
        <div class="modal-content">
            <h3>From My Heart 💌</h3>
            <p style="text-align: left; font-size: 14px; line-height: 1.5;">
                Happy Birthday pyaari Bhonduuuu! 🎂❤️<br><br>
                Tumhe pata hai na ki tum mere liye kitni special hai? Tum thodi si buddhu ho thodi si ziddi bhi 😝😝 lekin jaisi bhi ho... Bestest ever ho!<br><br>
                I promise ki main hamesha tumahre saath khada raunga tumhari saari baate sunne ke liye aur tumhe har mushkil mein sambhalne ke liye. Tum hamesha aise hi hasti rehna kyunki tumhari smile dekh kar mera din ban jata hai.<br><br>
                Stay the same, my favorite Bhonduuuu! ✨🥹🎈
            </p>
            <button class="btn" onclick="closeModal('modal3')">Close</button>
        </div>
    </div>

    <script>
        const audio = document.getElementById('myAudio');

        function startExperience() {
            const pass = document.getElementById('passInput').value.toLowerCase();
            if (pass === 'panda') {
                document.getElementById('page1').classList.add('hidden');
                document.getElementById('page2').classList.remove('hidden');
                // Play music on click to satisfy browser rules
                audio.play().catch(e => console.log("Audio play failed"));
            } else {
                alert("Incorrect password, Bhondu! 😉");
            }
        }

        function openSurprise() {
            document.getElementById('page2').classList.add('hidden');
            document.getElementById('page3').classList.remove('hidden');
        }

        function openModal(id) {
            document.getElementById(id).classList.remove('hidden');
        }

        function closeModal(id) {
            document.getElementById(id).classList.add('hidden');
        }

        function blowCandle() {
            document.getElementById('cake-icon').style.opacity = '0.4';
            document.getElementById('cake-status').innerHTML = "<h2 style='color: #ff4d6d'>Happy Birthday Bhonduuuu! 🎉</h2>";
        }
    </script>
</body>
</html>
