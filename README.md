# lerning-englais
English Zone* is a *free* website that helps Arabic speakers learn English from scratch.
<!DOCTYPE html>
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Apprendre l'anglais · English Zone</title>
    <!-- Feuille de style simple et claire -->
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Roboto, system-ui, -apple-system, sans-serif;
            background: linear-gradient(145deg, #f6f9fc 0%, #e6f0f5 100%);
            color: #1a2b3c;
            line-height: 1.5;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }

        /* HEADER */
        .header {
            background-color: #003153; /* bleu profond */
            color: white;
            padding: 1.2rem 2rem;
            box-shadow: 0 6px 12px rgba(0,20,30,0.2);
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
        }

        .logo h1 {
            font-size: 2rem;
            font-weight: 500;
            letter-spacing: 1px;
        }

        .logo span {
            font-weight: 300;
            background: #ffb347;
            color: #003153;
            padding: 0.2rem 0.8rem;
            border-radius: 40px;
            font-size: 1rem;
            margin-left: 0.5rem;
        }

        .tagline {
            font-style: italic;
            font-size: 1.1rem;
            opacity: 0.9;
            background: rgba(255,255,255,0.15);
            padding: 0.4rem 1rem;
            border-radius: 30px;
        }

        /* MAIN CONTENT */
        .container {
            max-width: 1300px;
            margin: 2rem auto;
            padding: 0 2rem;
            flex: 1;
        }

        /* Introduction */
        .intro-card {
            background: white;
            border-radius: 30px;
            padding: 2rem 2.5rem;
            margin-bottom: 2.5rem;
            box-shadow: 0 15px 25px -8px rgba(0,40,60,0.2);
            border-left: 10px solid #ffb347;
        }

        .intro-card h2 {
            font-size: 2.2rem;
            font-weight: 400;
            color: #003153;
            margin-bottom: 0.5rem;
        }

        .intro-card p {
            font-size: 1.2rem;
            color: #2c3e50;
            max-width: 85%;
        }

        /* Grille de leçons / catégories */
        .section-title {
            font-size: 1.9rem;
            font-weight: 400;
            color: #003153;
            margin: 2rem 0 1rem 0;
            border-bottom: 3px solid #ffb347;
            padding-bottom: 0.5rem;
            display: inline-block;
        }

        .lesson-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
            gap: 1.8rem;
            margin: 2rem 0 3rem 0;
        }

        .card {
            background: white;
            border-radius: 24px;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0, 30, 50, 0.1);
            transition: transform 0.15s ease, box-shadow 0.2s;
            border: 1px solid rgba(255,180,70,0.2);
            display: flex;
            flex-direction: column;
        }

        .card:hover {
            transform: translateY(-6px);
            box-shadow: 0 20px 30px -5px rgba(0,70,100,0.3);
            border-color: #ffb347;
        }

        .card-image {
            height: 130px;
            background-color: #bed9e9;
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: flex-end;
            padding: 0.5rem;
            color: white;
            text-shadow: 2px 2px 3px black;
            font-weight: bold;
            font-size: 1.5rem;
            background-blend-mode: overlay;
        }

        /* images fictives avec dégradés */
        .img-greetings { background: linear-gradient(145deg, #1d7ab3, #54b4d4); }
        .img-grammar { background: linear-gradient(145deg, #b3642b, #e69d4b); }
        .img-vocab { background: linear-gradient(145deg, #2f7d5a, #5fb38b); }
        .img-verbs { background: linear-gradient(145deg, #a14b75, #d57fb0); }
        .img-listening { background: linear-gradient(145deg, #4f6294, #8599cf); }
        .img-speaking { background: linear-gradient(145deg, #b16348, #df9e7c); }
        .card-image span {
            background: rgba(0,0,0,0.5);
            padding: 0.2rem 1rem;
            border-radius: 30px;
        }

        .card-content {
            padding: 1.5rem 1.2rem 1.2rem 1.2rem;
            flex: 1;
        }

        .card h3 {
            font-size: 1.6rem;
            font-weight: 500;
            color: #003153;
            margin-bottom: 0.75rem;
        }

        .card p {
            color: #2c3e50;
            margin-bottom: 1.2rem;
            font-size: 0.95rem;
        }

        .btn-small {
            background: none;
            border: 2px solid #ffb347;
            color: #003153;
            padding: 0.4rem 1.2rem;
            border-radius: 40px;
            font-weight: 600;
            cursor: pointer;
            font-size: 0.9rem;
            transition: 0.2s;
            text-decoration: none;
            display: inline-block;
        }

        .btn-small:hover {
            background: #ffb347;
            color: #003153;
            border-color: #ffb347;
        }

        /* Boîte d'exercice interactif */
        .practice-box {
            background: #003153;
            color: white;
            border-radius: 40px;
            padding: 2.5rem;
            margin: 3rem 0;
            box-shadow: 0 20px 30px -5px #001f33;
        }

        .practice-box h3 {
            font-size: 2rem;
            font-weight: 400;
            margin-bottom: 0.25rem;
        }

        .practice-box .sub {
            color: #ffcd94;
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }

        .exercise {
            background: #e7f0f9;
            color: #003153;
            border-radius: 40px;
            padding: 2rem;
        }

        .question {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
        }

        .options {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 2rem;
        }

        .option-btn {
            background: white;
            border: 2px solid #ffb347;
            padding: 0.8rem 1.8rem;
            border-radius: 60px;
            font-size: 1.2rem;
            font-weight: 600;
            color: #003153;
            cursor: pointer;
            transition: 0.15s;
            flex: 1 0 auto;
            max-width: 200px;
        }

        .option-btn:hover {
            background: #ffb347;
            color: #1e3b4f;
        }

        .feedback {
            font-size: 1.2rem;
            background: white;
            padding: 1rem 2rem;
            border-radius: 60px;
            display: inline-block;
            font-weight: 500;
        }

        .footer {
            background: #1b2f40;
            color: #cbdbe9;
            text-align: center;
            padding: 2rem;
            margin-top: 2.5rem;
            font-size: 1rem;
            border-top: 6px solid #ffb347;
        }

        .footer a {
            color: #ffcd94;
            text-decoration: none;
        }

        /* phrase d'exemple / aide */
        .example-box {
            background: #fef7e9;
            border-radius: 20px;
            padding: 1.2rem 2rem;
            margin: 1.5rem 0;
            border-left: 8px solid #ffb347;
            font-size: 1.2rem;
        }

        .example-box i {
            color: #0066aa;
        }
    </style>
</head>
<body>

<header class="header">
    <div class="logo">
        <h1>🗽 English Zone <span>free</span></h1>
    </div>
    <div class="tagline">Apprendre l'anglais · simplement</div>
</header>

<main class="container">

    <!-- Introduction rassurante -->
    <div class="intro-card">
        <h2>🇬🇧 Your English journey starts here</h2>
        <p>Des leçons claires, du vocabulaire, des exercices — 100% gratuits et en français pour bien démarrer.</p>
    </div>

    <!-- SECTION : leçons thématiques -->
    <h2 class="section-title">📚 Leçons par thème</h2>
    <div class="lesson-grid">
        <div class="card">
            <div class="card-image img-greetings"><span>👋 1</span></div>
            <div class="card-content">
                <h3>Greetings</h3>
                <p>Dire bonjour, se présenter, les formules de politesse de base. (A1)</p>
                <a href="#" class="btn-small">Voir la leçon →</a>
            </div>
        </div>
        <div class="card">
            <div class="card-image img-grammar"><span>📌 2</span></div>
            <div class="card-content">
                <h3>Grammaire starter</h3>
                <p>Être/avoir, pronoms, articles “a/an/the”. Règles simples.</p>
                <a href="#" class="btn-small">Voir la leçon →</a>
            </div>
        </div>
        <div class="card">
            <div class="card-image img-vocab"><span>🍎 3</span></div>
            <div class="card-content">
                <h3>Mots du quotidien</h3>
                <p>Nourriture, famille, maison, animaux. Plus de 150 mots illustrés.</p>
                <a href="#" class="btn-small">Voir la leçon →</a>
            </div>
        </div>
        <div class="card">
            <div class="card-image img-verbs"><span>⚡ 4</span></div>
            <div class="card-content">
                <h3>Verbes essentiels</h3>
                <p>Les 20 verbes les plus utilisés : to be, have, do, go, get…</p>
                <a href="#" class="btn-small">Voir la leçon →</a>
            </div>
        </div>
        <div class="card">
            <div class="card-image img-listening"><span>🎧 5</span></div>
            <div class="card-content">
                <h3>Listening A1</h3>
                <p>Comprendre des phrases lentes, des dialogues simples.</p>
                <a href="#" class="btn-small">Voir la leçon →</a>
            </div>
        </div>
        <div class="card">
            <div class="card-image img-speaking"><span>🗣️ 6</span></div>
            <div class="card-content">
                <h3>Speaking practice</h3>
                <p>Prononciation, phrases types pour commander, demander son chemin.</p>
                <a href="#" class="btn-small">Voir la leçon →</a>
            </div>
        </div>
    </div>

    <!-- Bloc EXERCICE INTERACTIF simple (JavaScript) -->
    <div class="practice-box">
        <h3>✏️ Mini exercice · présent simple</h3>
        <div class="sub">Choisis la bonne réponse</div>

        <div class="exercise" id="exerciseBox">
            <div class="question" id="questionText">She _____ (to work) in a hospital.</div>
            <div class="options" id="optionsContainer">
                <button class="option-btn" onclick="checkAnswer('work')">work</button>
                <button class="option-btn" onclick="checkAnswer('works')">works</button>
                <button class="option-btn" onclick="checkAnswer('working')">working</button>
            </div>
            <div class="feedback" id="feedbackMessage">➡️ Clique sur une réponse</div>
        </div>
    </div>

    <!-- Mini vocabulaire / astuce du jour -->
    <h2 class="section-title">💡 Astuce du jour</h2>
    <div class="example-box">
        <p>🇫🇷 « Faire » se dit souvent <i><strong>to do</strong></i> (activités) ou <i><strong>to make</strong></i> (fabriquer).</p>
        <p>✔️ <strong>do</strong> the homework — ✔️ <strong>make</strong> a cake.</p>
    </div>

    <!-- Bloc Ressources supplémentaires -->
    <div style="display: flex; gap: 1.5rem; flex-wrap: wrap; margin: 3rem 0 1rem;">
        <div style="background: white; border-radius: 28px; padding: 1.8rem; flex: 1; min-width: 200px; box-shadow: 0 10px 15px rgba(0,0,0,0.05);">
            <h3 style="color: #003153;">📖 Fiches à imprimer</h3>
            <p style="margin: 1rem 0;">Listes de vocabulaire, conjugaisons, exercices PDF.</p>
            <a href="#" class="btn-small">Télécharger</a>
        </div>
        <div style="background: white; border-radius: 28px; padding: 1.8rem; flex: 1; min-width: 200px; box-shadow: 0 10px 15px rgba(0,0,0,0.05);">
            <h3 style="color: #003153;">🎬 Vidéos pour débutants</h3>
            <p style="margin: 1rem 0;">Séries courtes sous-titrées anglais/français.</p>
            <a href="#" class="btn-small">Regarder</a>
        </div>
        <div style="background: white; border-radius: 28px; padding: 1.8rem; flex: 1; min-width: 200px; box-shadow: 0 10px 15px rgba(0,0,0,0.05);">
            <h3 style="color: #003153;">👥 Conversation</h3>
            <p style="margin: 1rem 0;">Pratique avec d'autres learners. Groupes d'échange.</p>
            <a href="#" class="btn-small">Rejoindre</a>
        </div>
    </div>
</main>

<footer class="footer">
    <p>© 2025 English Zone · créé pour apprendre l'anglais · <a href="#">À propos</a> · <a href="#">Contact</a></p>
    <p style="margin-top: 0.8rem; font-size: 0.9rem;">🌟 “The beautiful thing about learning is that no one can take it away from you.”</p>
</footer>

<!-- Petit script pour l'exercice interactif -->
<script>
    function checkAnswer(selected) {
        const correct = "works";   // la bonne réponse pour "She _____ (to work)"
        const feedback = document.getElementById('feedbackMessage');

        if (selected === correct) {
            feedback.innerHTML = "✅ Correct ! 'She works' (he/she/it ➔ verbe + s)";
            feedback.style.background = "#d9f2e4";
            feedback.style.color = "#004d40";
        } else {
            feedback.innerHTML = "❌ Pas tout à fait. Essaie encore (indice : 3e personne du singulier)";
            feedback.style.background = "#ffefef";
            feedback.style.color = "#a12";
        }
    }
</script>

<!-- Note : tous les liens sont des ancres (#) car c'est une démo statique. 
     Dans un vrai site, on pointerait vers des pages ou des sections. -->
</body>
</html>
