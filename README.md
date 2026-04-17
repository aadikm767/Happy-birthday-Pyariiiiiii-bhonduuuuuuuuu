# Happy-birthday-Pyariiiiiii-bhonduuuuuuuuu
This is for you
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Birthday Surprise</title>
    <style>
        /* Basic Styling */
        body {
            margin: 0; padding: 0;
            font-family: 'Arial', sans-serif;
            background-color: #fff0f3;
            display: flex; justify-content: center; align-items: center;
            height: 100vh; overflow: hidden;
        }

        .container {
            text-align: center;
            width: 90%; max-width: 400px;
            background: white; padding: 30px;
            border-radius: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            z-index: 10;
        }

        /* Hide pages by default */
        .page { display: none; }
        /* Show the active page */
        .active { display: block !important; }

        .profile-img {
            width: 150px; height: 150px; border-radius: 50%;
            border: 5px solid #ff85a2; object-fit: cover;
            margin-bottom: 20px;
        }

        input {
            padding: 12px; width: 80%; border: 2px solid #ff85a2;
            border-radius: 20px; margin-bottom: 15px; outline: none;
        }

        button {
            background: #ff85a2; color: white; border: none;
            padding: 12px 25px; border-radius: 20px; cursor: pointer;
            font-weight: bold; font-size: 16px;
        }

        .gift-box { font-size: 80px; cursor: pointer; margin: 20px 0; }
        .grid { display: flex; justify-content: center; gap: 15px; }
        .small-box { font-size: 40px; cursor: pointer; padding: 10px; background: #fff0f3; border-radius: 10px; }

        /* Modal styling */
        .modal {
            display: none; position: fixed; top: 0; left: 0;
            width: 100%; height: 100%; background: rgba(0,0,0,0.7);
            justify-content: center; align-items: center; z-index: 100;
        }
    </style>
</head>
<body>

    <audio id="bgMusic" loop>
        <source src="https://docs.google.com/uc?export=download&id=1v7OxNPdOqlXrTus4x-xNmzFKwd2UIGOS" type="audio/mpeg">
    </audio>

    <div id="page1" class="container page active">
        <img src="https://docs.google.com/uc?export=download&id=1QO6l3p3zUNc1sZblGxMvhXaOSW1cT7fQ" class="profile-img">
        <h2 style="color: #ff4d6d;">Hey My Panda! ❤️</h2>
        <p>Enter the secret code to enter:</p>
        <input type="password" id="passInput" placeholder="Password...">
        <br>
        <button onclick="goToPage2()">Unlock 🔓</button>
    </div>

    <div id="page2" class="container page">
        <h2 style="color: #ff4d6d;">A Surprise for You...</h2>
        <div class="gift-box" onclick="goToPage3()">🎁</div>
        <p>Tap the box to open it!</p>
    </div>

    <div id="page3" class="container page">
        <h2 style="color: #ff4d6d;">Choose a Gift! ✨</h2>
        <div class="grid">
            <div class="small-box" onclick="openGift(1)">📦</div>
            <div class="small-box" onclick="openGift(2)">📦</div>
            <div class="small-box" onclick="openGift(3)">📦</div>
        </div>
    </div>

    <div id="modal" class="modal" onclick="closeModal()">
        <div class="container" onclick="event.stopPropagation()">
            <div id="modal-content"></div>
            <button onclick="closeModal()">Close</button>
        </div>
    </div>

    <script>
        const music = document.getElementById('bgMusic');

        function goToPage2() {
            const pw = document.getElementById('passInput').value.toLowerCase();
            if(pw === 'panda') {
                // Change visibility
                document.getElementById('page1').classList.remove('active');
                document.getElementById('page2').classList.add('active');
                // Play Music
                music.play().catch(e => console.log("Music needs interaction"));
            } else {
                alert("Wrong passcode! Hint: Panda 🐼");
            }
        }

        function goToPage3() {
            document.getElementById('page2').classList.remove('active');
            document.getElementById('page3').classList.add('active');
        }

        function openGift(num) {
            const modal = document.getElementById('modal');
            const content = document.getElementById('modal-content');
            modal.style.display = 'flex';

            if(num === 1) {
                content.innerHTML = `
                    <h3>Gift #1: Blow the Candle! 🕯️</h3>
                    <img src="https://cdn-icons-png.flaticon.com/512/3132/3132715.png" width="100" id="cake" onclick="this.style.opacity='0.5'; document.getElementById('cmsg').innerHTML='<h3>Happy birthday bhonduuuu! 🎉</h3>'">
                    <div id="cmsg"></div>
                `;
            } else if (num === 2) {
                content.innerHTML = `
                    <h3>Gift #2: You're Cute! ✨</h3>
                    <img src="https://docs.google.com/uc?export=download&id=1rdVd6sgKWsodlG2BhqGrRQnK875DrOVe" width="100%" style="border-radius:10px">
                `;
            } else if (num === 3) {
                content.innerHTML = `
                    <h3>Gift #3: My Heart 💌</h3>
                    <p style="text-align:left; font-size:14px">Happy Birthday pyaari Bhonduuuu! 🎂❤️<br><br>Tumhe pata hai na ki tum mere liye kitni special hai? Tum thodi si buddhu ho thodi si ziddi bhi... I promise ki main hamesha tumahre saath khada raunga. Stay the same, my favorite Bhonduuuu! ✨</p>
                `;
            }
        }

        function closeModal() {
            document.getElementById('modal').style.display = 'none';
        }
    </script>
</body>
</html>
