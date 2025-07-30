# nusrat-love-care
<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>নুসরাতের জন্য বিশেষ বার্তা ❤️</title>
    <style>
        body {
            font-family: "Hind Siliguri", Arial, sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
            text-align: center;
            padding: 20px;
            color: #d32f2f;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            background-color: rgba(255, 255, 255, 0.9);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #c2185b;
            margin-bottom: 30px;
        }
        .heart {
            font-size: 60px;
            animation: heartbeat 1.5s infinite;
            margin: 20px 0;
        }
        @keyframes heartbeat {
            0% { transform: scale(1); }
            25% { transform: scale(1.1); }
            50% { transform: scale(1); }
            75% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        button {
            background-color: #e91e63;
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 18px;
            border-radius: 50px;
            cursor: pointer;
            margin: 20px 0;
            transition: all 0.3s;
        }
        button:hover {
            background-color: #c2185b;
            transform: scale(1.05);
        }
        .hidden-message {
            display: none;
            font-size: 18px;
            line-height: 1.6;
            margin-top: 20px;
            background-color: #fce4ec;
            padding: 20px;
            border-radius: 10px;
            border-left: 5px solid #e91e63;
        }
        .signature {
            font-style: italic;
            margin-top: 30px;
            color: #7b1fa2;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="heart">❤️</div>
        <h1>প্রিয় নুসরাত,</h1>
        <p>এই ছোট্ট বার্তাটি শুধুমাত্র তোমার জন্যই তৈরি করা হয়েছে</p>
        
        <button onclick="showMessage()">আমার বার্তাটি পড়ুন</button>
        
        <div id="secretMessage" class="hidden-message">
            <p>"তুমি যখন হাসো, আমার সমস্ত বিশ্বটা আলোয় ভরে যায়। তোমার একটি মুহূর্তের অসুখও আমার হৃদয়ে তীব্র ব্যথা আনে। জানো কি, তুমি আমার জীবনের সবচেয়ে সুন্দর অনুভূতি?"</p>
            <p>চিরকাল তোমার পাশে থাকার প্রতিশ্রুতিতে,</p>
            <div class="signature">- তোমারই একজন</div>
        </div>
    </div>

    <script>
        function showMessage() {
            document.getElementById("secretMessage").style.display = "block";
            // কনফে্টি এফেক্ট
            const colors = ['#ff0000', '#00ff00', '#0000ff', '#ffff00', '#ff00ff'];
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    const confetti = document.createElement('div');
                    confetti.style.position = 'fixed';
                    confetti.style.width = '10px';
                    confetti.style.height = '10px';
                    confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                    confetti.style.borderRadius = '50%';
                    confetti.style.left = Math.random() * window.innerWidth + 'px';
                    confetti.style.top = '-10px';
                    confetti.style.zIndex = '9999';
                    document.body.appendChild(confetti);
                    
                    const animation = confetti.animate([
                        { top: '-10px', opacity: 1 },
                        { top: window.innerHeight + 'px', opacity: 0 }
                    ], {
                        duration: 2000 + Math.random() * 3000,
                        easing: 'cubic-bezier(0.1, 0.2, 0.3, 1)'
                    });
                    
                    animation.onfinish = () => confetti.remove();
                }, i * 100);
            }
        }
    </script>
</body>
</html>
