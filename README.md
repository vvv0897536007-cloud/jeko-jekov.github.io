<!DOCTYPE html>
<html lang="bg">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Всичко в едно</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #121212; color: #fff; text-align: center; }
        header { background: #b71c1c; color: white; padding: 20px; font-size: 22px; font-weight: bold; display: flex; align-items: center; justify-content: center; }
        .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; padding: 20px; }
        .card { background: #1e1e1e; padding: 25px 10px; border-radius: 15px; font-weight: bold; font-size: 15px; cursor: pointer; display: flex; flex-direction: column; align-items: center; justify-content: center; border-bottom: 5px solid; transition: transform 0.2s; }
        .card:hover { transform: scale(1.05); }
        .card:active { transform: scale(0.95); }
        .icon { font-size: 35px; margin-bottom: 10px; }
        #card-food { border-bottom-color: #4caf50; }
        #card-bank { border-bottom-color: #2196f3; }
        #card-vignette { border-bottom-color: #ff9800; }
        #card-horoscope { border-bottom-color: #9c27b0; }
        #card-laws { border-bottom-color: #f44336; }
        #card-garden { border-bottom-color: #ffeb3b; }
    </style>
</head>
<body>

    <header>🏛️ Всичко в едно - България</header>

    <div class="grid">
        <div class="card" id="card-food"><span class="icon">🍏</span>Храни & Аптеки</div>
        <div class="card" id="card-bank"><span class="icon">🏦</span>Банки & EasyPay</div>
        <div class="card" id="card-vignette"><span class="icon">🚗</span>Винетки & Каско</div>
        <div class="card" id="card-horoscope"><span class="icon">🔮</span>Хороскоп & Кафе</div>
        <div class="card" id="card-laws"><span class="icon">⚖️</span>Всички Закони</div>
        <div class="card" id="card-garden"><span class="icon">🌱</span>Лозя & Градина</div>
    </div>

    <script>
        // Тук са линковете, които ще се отварят при натискане на всяка картичка:
        const cardLinks = {
            'card-food': 'https://www.google.com',       // Линка за Храни & Аптеки
            'card-bank': 'https://www.google.com',       // Линка за Банки & EasyPay
            'card-vignette': 'https://www.google.com',   // Линка за Винетки & Каско
            'card-horoscope': 'https://www.google.com',  // Линка за Хороскоп & Кафе
            'card-laws': 'https://www.google.com',       // Линка за Всички Закони
            'card-garden': 'https://www.google.com'      // Линка за Лозя & Градина
        };

        document.querySelectorAll('.card').forEach(card => {
            card.addEventListener('click', () => {
                const cardId = card.id;
                const targetLink = cardLinks[cardId];
                if (targetLink) {
                    window.location.href = targetLink; // Директно пренасочва към сайта
                }
            });
        });
    </script>

</body>
</html>
