<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>معرض رسومات أخي - Poppy Playtime</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap');

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Cairo', sans-serif;
        }

        body {
            background-color: #05070a;
            color: white;
            overflow-x: hidden;
        }

        header {
            background-color: #0a0e14;
            padding: 30px;
            text-align: center;
            border-bottom: 4px solid #ff1909;
        }

        header h1 {
            font-size: 2.5rem;
            color: #ff1909;
            text-shadow: 0 0 15px rgba(255, 25, 9, 0.6);
            margin-bottom: 10px;
        }

        header p {
            color: #3b82f6;
            font-size: 1.2rem;
            font-weight: bold;
        }

        .gallery {
            padding: 50px 10%;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .art-card {
            background-color: #121821;
            border-radius: 20px;
            overflow: hidden;
            border: 2px solid #1e293b;
            transition: 0.4s;
            text-align: center;
            position: relative;
        }

        .art-card:hover {
            transform: translateY(-10px);
            border-color: #ff1909;
            box-shadow: 0 10px 30px rgba(255, 25, 9, 0.2);
        }

        .art-card img {
            width: 100%;
            height: 350px;
            object-fit: cover;
            border-bottom: 2px solid #1e293b;
        }

        .art-card h3 {
            padding: 15px 10px 5px;
            font-size: 1.5rem;
        }

        .art-card p {
            padding: 0 10px 15px;
            color: #94a3b8;
        }

        /* تنسيق زر اللايك */
        .like-section {
            padding-bottom: 20px;
        }

        .like-btn {
            background: #1e293b;
            border: 2px solid #3b82f6;
            color: white;
            padding: 10px 25px;
            border-radius: 30px;
            cursor: pointer;
            transition: 0.3s;
            font-size: 1.1rem;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .like-btn.active {
            background: #ff1909;
            border-color: #ff1909;
            transform: scale(1.1);
        }

        .like-btn:hover {
            background: #3b82f6;
        }

        footer {
            text-align: center;
            padding: 50px;
            color: #475569;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <header>
        <h1>مصنع رسومات Poppy Playtime</h1>
        <p>بإبداع الفنان عاشور عبد رحيم🎨</p>
    </header>

    <div class="gallery">
        <div class="art-card">
            <img src="https://i.postimg.cc/nzyJpXYY/WIN-20260306-10-58-43-Pro.jpg" alt="Huggy Wuggy">
            <h3>هاجي واجي</h3>
            <p>أول رسمة مرعبة في المجموعة!</p>
            <div class="like-section">
                <button class="like-btn" onclick="toggleLike(this)">
                    <span>❤</span> <span class="count">15</span>
                </button>
            </div>
        </div>

        <div class="art-card">
            <img src="https://i.postimg.cc/wjX3PpHz/WIN-20260306-15-37-25-Pro.jpg" alt="Mommy Long Legs">
            <h3>بروتوتايب</h3>
            <p>رسمة احترافية للأذرع الطويلة.</p>
            <div class="like-section">
                <button class="like-btn" onclick="toggleLike(this)">
                    <span>❤</span> <span class="count">22</span>
                </button>
            </div>
        </div>

        <div class="art-card">
            <img src="https://static.wikia.nocookie.net/poppy-playtime/images/0/06/Boxy_Boo_Render.png" alt="Boxy Boo">
            <h3>بوكسي بو</h3>
            <p>إبداع في رسم شخصية الصندوق.</p>
            <div class="like-section">
                <button class="like-btn" onclick="toggleLike(this)">
                    <span>❤</span> <span class="count">18</span>
                </button>
            </div>
        </div>
    </div>

    <footer>
        تصميم المبرمج أسامة 🚀 | معرض رسومات بوبي بلايتايم 2026
    </footer>

    <script>
        function toggleLike(btn) {
            const countSpan = btn.querySelector('.count');
            let currentCount = parseInt(countSpan.innerText);
            
            btn.classList.toggle('active');
            
            if (btn.classList.contains('active')) {
                countSpan.innerText = currentCount + 1;
            } else {
                countSpan.innerText = currentCount - 1;
            }
        }
    </script>

</body>
</html>
