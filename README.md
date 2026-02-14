<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #ff9a9e, #fecfef, #ffecd2);
            font-family: 'Arial', sans-serif;
            overflow: hidden;
            position: relative;
        }

        /* Floating hearts and sparkles */
        .floating {
            position: absolute;
            font-size: 2rem;
            animation: float 6s ease-in-out infinite;
            opacity: 0.7;
        }

        .heart {
            color: #ff6b9d;
        }

        .sparkle {
            color: #ffd700;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        .container {
            text-align: center;
            z-index: 1;
            max-width: 80%;
        }

        h1 {
            font-size: 3rem;
            color: #d63384;
            margin-bottom: 2rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }

        .buttons {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        button {
            padding: 1rem 2rem;
            font-size: 1.5rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }

        #yes {
            background: linear-gradient(45deg, #ff6b9d, #c44569);
            color: white;
            transform: scale(1.2);
        }

        #yes:hover {
            transform: scale(1.3);
            box-shadow: 0 6px 12px rgba(0,0,0,0.3);
        }

        #no {
            background: linear-gradient(45deg, #a8e6cf, #dcedc8);
            color: #333;
            position: relative;
        }

        #message {
            font-size: 1.2rem;
            color: #d63384;
            line-height: 1.6;
            display: none;
            text-align: center;
            max-width: 600px;
            margin: 0 auto;
        }
    </style>
</head>
<body>
    <!-- Floating decorations -->
    <div class="floating heart" style="top: 10%; left: 10%;">❤️</div>
    <div class="floating sparkle" style="top: 20%; right: 15%;">✨</div>
    <div class="floating heart" style="bottom: 15%; left: 20%;">💖</div>
    <div class="floating sparkle" style="bottom: 25%; right: 10%;">⭐</div>
    <div class="floating heart" style="top: 50%; left: 50%;">😍</div>

    <div class="container">
        <h1>Will you be my Valentine? 💕</h1>
        <div class="buttons">
            <button id="yes">YES</button>
            <button id="no">NO</button>
        </div>
        <div id="message">
            Happy Valentine Day sayanggggkuuu....cintakuuuu ,terimakasih telah hadir dan menghidupkan kembali warna yang telah lama mati. Bertemu denganmu adalah salah satu keberuntungan yang tidak bisa aku deskripsikan, kamu adalah salah satu bentuk bahagia yang selama ini aku impikan, aku sangat amat bersyukur Karena bisa dipertemukan dengan manusia sepertimu, jika karena bukan kamu aku tidak akan pernah tau bahwa aku layak untuk dicintai sebaik itu, karenamu aku menjadi lebih berharga dan vang terpenting adalah aku tidak harus menjadi orang lain, ungkapan terimakasihku untukmu adalah bentuk penghargaan yang tidak akan pernah ternilai iika dihitung, aku ingin mengucapkan terimakasih, terimakasih telah sabar menghadapiku, terimakasih telah menerimaku apa adanya terimakasih telah menguatkanku dalam segala hal yang membuatku patah dan terimakasih juga karena kamu telah menjadi support sistem terbaik dalam hidupku. 🎉❤️
        </div>
    </div>

    <script>
        const noButton = document.getElementById('no');
        const yesButton = document.getElementById('yes');
        const message = document.getElementById('message');

        // Function to move the NO button randomly
        function moveNoButton() {
            const container = document.querySelector('.container');
            const containerRect = container.getBoundingClientRect();
            const buttonRect = noButton.getBoundingClientRect();

            // Calculate random position within the container, avoiding edges
            const maxX = containerRect.width - buttonRect.width - 20;
            const maxY = containerRect.height - buttonRect.height - 20;
            const randomX = Math.random() * maxX;
            const randomY = Math.random() * maxY;

            noButton.style.position = 'absolute';
            noButton.style.left = randomX + 'px';
            noButton.style.top = randomY + 'px';
        }

        // Move NO button on hover or click
        noButton.addEventListener('mouseover', moveNoButton);
        noButton.addEventListener('click', moveNoButton);

        // YES button click event
        yesButton.addEventListener('click', () => {
            message.style.display = 'block';
            // Optionally hide buttons or add more effects
            document.querySelector('.buttons').style.display = 'none';
        });
    </script>
</body>
</html>
