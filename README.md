<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Learn Sinhala</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #00695c;
            color: #fff;
            padding: 20px;
            text-align: center;
        }
        main {
            padding: 20px;
        }
        .phrase-card {
            background-color: #fff;
            border: 1px solid #ddd;
            border-radius: 8px;
            padding: 20px;
            margin-bottom: 20px;
        }
        .phrase-card h2 {
            margin-top: 0;
        }
        .phrase {
            font-size: 1.5em;
            color: #00695c;
        }
        .translations {
            margin-top: 10px;
        }
    </style>
</head>
<body>

<header>
    <h1>Learn Sinhala</h1>
    <p>Learn Sinhala through English and Indonesian translations.</p>
</header>

<main>
    <!-- JavaScript will load phrases here -->
    <div id="phraseContainer"></div>
</main>

<script>
    // Sample phrases in Sinhala with English and Indonesian translations
    const phrases = [
        {
            sinhala: "ආයුබෝවන්",
            english: "Hello",
            indonesian: "Halo"
        },
        {
            sinhala: "කොහොමද?",
            english: "How are you?",
            indonesian: "Apa kabar?"
        },
        {
            sinhala: "සුභ දවසක්",
            english: "Good day",
            indonesian: "Selamat siang"
        },
        {
            sinhala: "ස්තූතියි",
            english: "Thank you",
            indonesian: "Terima kasih"
        }
    ];

    function loadPhrases() {
        const container = document.getElementById('phraseContainer');
        container.innerHTML = '';
        
        phrases.forEach(phrase => {
            const phraseCard = document.createElement('div');
            phraseCard.classList.add('phrase-card');

            phraseCard.innerHTML = `
                <h2 class="phrase">${phrase.sinhala}</h2>
                <div class="translations">
                    <p><strong>English:</strong> ${phrase.english}</p>
                    <p><strong>Indonesian:</strong> ${phrase.indonesian}</p>
                </div>
            `;

            container.appendChild(phraseCard);
        });
    }

    // Load phrases when the page loads
    window.onload = loadPhrases;
</script>

</body>
</html>
