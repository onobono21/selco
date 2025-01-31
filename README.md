<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selco Sitesi</title>
    <style>
        body { text-align: center; font-family: Arial, sans-serif; margin-top: 50px; }
        h1 { color: red; }
        #timer { font-size: 24px; font-weight: bold; }
    </style>
</head>
<body>
    <h1>Çok Güzelsin Selco</h1>
    <p>08/04/2024 tarihinden bu yana geçen süre:</p>
    <div id="timer">Yükleniyor...</div>

    <script>
        function updateTimer() {
            let startDate = new Date("2024-04-08T00:00:00");
            let now = new Date();
            let diff = Math.floor((now - startDate) / 1000);

            let days = Math.floor(diff / (24 * 3600));
            let hours = Math.floor((diff % (24 * 3600)) / 3600);
            let minutes = Math.floor((diff % 3600) / 60);
            let seconds = diff % 60;

            document.getElementById("timer").innerHTML = 
                days + " gün " + hours + " saat " + minutes + " dakika " + seconds + " saniye";
        }
        setInterval(updateTimer, 1000);
        updateTimer();
    </script>
</body>
</html>
