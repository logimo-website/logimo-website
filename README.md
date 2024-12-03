<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Logimo - Transport</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 15px;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #444;
        }
        nav a {
            color: white;
            text-decoration: none;
            padding: 10px 20px;
        }
        nav a:hover {
            background-color: #555;
        }
        .container {
            padding: 20px;
            max-width: 1200px;
            margin: auto;
        }
        .hero {
            text-align: center;
            padding: 50px 20px;
            background-color: #f4f4f4;
        }
        .hero img {
            max-width: 100%;
            height: auto;
        }
        .calculator {
            text-align: center;
            background-color: #f4f4f4;
            padding: 20px;
            margin-top: 20px;
        }
        .calculator input {
            margin: 10px;
            padding: 10px;
            width: 200px;
        }
        .calculator button {
            padding: 10px 20px;
            background-color: #333;
            color: white;
            border: none;
            cursor: pointer;
        }
        .calculator button:hover {
            background-color: #555;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
            margin-top: 20px;
        }
        @media (max-width: 768px) {
            nav {
                flex-direction: column;
            }
            .calculator input {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Logimo - Transport do 1 tony</h1>
    </header>
    <nav>
        <a href="#opis">O nas</a>
        <a href="#kalkulator">Kalkulator</a>
        <a href="#kontakt">Kontakt</a>
    </nav>
    <div class="container">
        <!-- Pierwsza strona: Opis -->
        <section id="opis" class="hero">
            <h2>O nas</h2>
            <p>Firma Logimo od 5 lat specjalizuje się w transporcie ładunków do 1 tony na terenie całej Polski. Zapewniamy szybkie, bezpieczne i punktualne dostawy.</p>
            <img src="your-logo-url.jpg" alt="Logo Logimo">
        </section>

        <!-- Druga strona: Kalkulator -->
        <section id="kalkulator" class="calculator">
            <h2>Kalkulator kosztów</h2>
            <p>Oblicz koszt transportu (2,50 PLN/km):</p>
            <input type="number" id="distance" placeholder="Podaj odległość w km">
            <button onclick="calculateCost()">Oblicz</button>
            <p id="result"></p>
        </section>
    </div>

    <footer>
        <p>Kontakt: Roman +48 730 603 110 | Rafał +48 576 880 325 | michalek.rafal@poczta.fm</p>
    </footer>

    <script>
        function calculateCost() {
            const distance = document.getElementById('distance').value;
            if (distance && distance > 0) {
                const cost = (distance * 2.5).toFixed(2);
                document.getElementById('result').innerText = `Koszt transportu: ${cost} PLN`;
            } else {
                document.getElementById('result').innerText = "Proszę podać poprawną odległość.";
            }
        }
    </script>
</body>
</html>

