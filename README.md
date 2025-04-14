<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mon Parcours Pro</title>
    <style>
        body {
            font-family: sans-serif; /* Police de caractères par défaut */
            margin: 0;
            padding: 0;
            background-color: #f9f9f9; /* Couleur de fond générale */
            color: #333; /* Couleur de texte par défaut */
            line-height: 1.6;
        }

        /* Section supérieure bleue */
        .top-section {
            background-color: #003366; /* Bleu foncé */
            color: white;
            padding: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .top-left {
            max-width: 50%;
            padding-right: 20px;
        }

        .top-left h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
        }

        .top-left p {
            font-size: 1.1em;
            line-height: 1.8;
            margin-bottom: 15px;
        }

        .top-left .cta-button {
            background-color: #007bff; /* Bleu clair */
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            display: inline-block;
        }

        .top-right {
            max-width: 45%;
        }

        .top-right img {
            width: 100%;
            height: auto;
            border-radius: 5px; /* Légers bords arrondis */
        }

        /* Section CV principale */
        .cv-section {
            background-color: white;
            padding: 30px;
            margin: 20px auto;
            max-width: 960px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); /* Légère ombre */
            border-radius: 5px;
        }

        /* Informations personnelles */
        .personal-info {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
            border-bottom: 1px solid #eee;
            padding-bottom: 20px;
        }

        .personal-info img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 20px;
        }

        .personal-info h2 {
            font-size: 1.8em;
            margin-bottom: 5px;
        }

        .personal-info p {
            color: #777;
            margin: 0;
        }

        /* Sections de contenu (Expérience, Formation, etc.) */
        .section-title {
            font-size: 1.5em;
            color: #003366;
            margin-top: 25px;
            margin-bottom: 15px;
            border-bottom: 2px solid #003366;
            padding-bottom: 5px;
        }

        .experience-item, .education-item {
            margin-bottom: 20px;
        }

        .experience-item h3, .education-item h3 {
            font-weight: bold;
            margin-bottom: 5px;
        }

        .experience-item .date, .education-item .date {
            color: #777;
            font-style: italic;
            margin-bottom: 5px;
        }

        .experience-item p, .education-item p {
            margin-bottom: 10px;
        }

        /* Section Projets */
        .project-item {
            margin-bottom: 20px;
            border-left: 3px solid #007bff; /* Bande bleue pour les projets */
            padding-left: 15px;
        }

        .project-item h3 {
            font-size: 1.2em;
            margin-bottom: 5px;
            color: #333;
        }

        .project-item p {
            color: #555;
            margin-bottom: 8px;
        }

        .project-item a {
            color: #007bff;
            text-decoration: none;
        }

        .project-item a:hover {
            text-decoration: underline;
        }

        /* Section Réseaux Sociaux */
        .social-links {
            margin-top: 20px;
            text-align: center;
        }

        .social-links a {
            display: inline-block;
            margin: 0 15px;
            color: #555;
            font-size: 1.1em;
            text-decoration: none;
        }

        .social-links a:hover {
            color: #007bff;
        }

        /* Section Compétences */
        .skills-section {
            text-align: center;
            margin-top: 30px;
            padding: 20px;
            border-top: 1px solid #eee;
        }

        .skills-section h2 {
            font-size: 1.5em;
            color: #003366;
            margin-bottom: 15px;
        }

        .skills-list {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .skill-item {
            text-align: center;
            margin: 15px;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            width: calc(33% - 30px); /* Pour trois colonnes avec un peu d'espace */
            box-sizing: border-box;
        }

        .skill-item h4 {
            margin-bottom: 5px;
            color: #555;
        }

        .skill-item p {
            color: #777;
            font-size: 0.9em;
        }

        /* Section "Mettez en avant votre parcours dès aujourd'hui" */
        .offer-section {
            background-color: #f0f8ff; /* Couleur de fond bleu très clair */
            color: #2e8b57; /* Couleur de texte vert moyen */
            padding: 30px 20px;
            margin-top: 30px;
            border-radius: 5px;
            display: flex;
            justify-content: space-around;
            align-items: center;
            flex-wrap: wrap;
        }

        .offer-text {
            max-width: 500px;
            text-align: left;
        }

        .offer-text h2 {
            font-size: 1.8em;
            margin-bottom: 10px;
        }

        .offer-text p {
            font-size: 1.1em;
            line-height: 1.7;
            margin-bottom: 15px;
        }

        .offer-text ul {
            list-style-type: none;
            padding-left: 0;
            margin-bottom: 15px;
        }

        .offer-text ul li {
            margin-bottom: 8px;
        }

        .offer-text ul li::before {
            content: "✅ "; /* Ajouter une coche verte */
            color: #2e8b57;
            font-weight: bold;
            margin-right: 8px;
        }

        .offer-text .cta-button {
            background-color: #007bff; /* Couleur du bouton "Commencer maintenant" */
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            display: inline-block;
            font-size: 1.1em;
        }

        .offer-text .cta-button:hover {
            background-color: #0056b3;
        }

        .offer-image {
            max-width: 400px;
            text-align: center;
        }

        .offer-image img {
            width: 100%;
            height: auto;
            border-radius: 5px;
            box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
        }

        /* Pied de page */
        footer {
            background-color: #f0f0f0;
            padding: 20px;
            text-align: center;
            color: #777;
            font-size: 0.9em;
            border-top: 1px solid #eee;
        }

        footer .social-icons a {
            display: inline-block;
            margin: 0 10px;
            color: #555;
            text-decoration: none;
            font-size: 1.2em;
        }

        /* Responsive Design (pour les petits écrans) */
        @media (max-width: 768px) {
            .top-section {
                flex-direction: column;
                text-align: center;
            }

            .top-left, .top-right {
                max-width: 100%;
                margin-bottom: 20px;
            }

            .personal-info {
                flex-direction: column;
                align-items: center;
                text-align: center;
            }

            .personal-info img {
                margin-right: 0;
                margin-bottom: 15px;
            }

            .skills-list {
                flex-direction: column;
                align-items: center;
            }

            .skill-item {
                width: 80%;
                margin: 15px auto;
            }

            .offer-section {
                flex-direction: column;
                text-align: center;
            }

            .offer-text, .offer-image {
                max-width: 100%;
                margin-bottom: 20px;
            }

            .offer-text h2 {
                font-size: 1.8em;
            }

            .offer-text p {
                font-size: 1em;
            }

            .offer-text .cta-button {
                font-size: 1em;
            }
        }
    </style>
</head>
<body>
    <div class="top-section">
        <div class="top-left">
            <h1>Construisez votre parcours professionnel avec Mon Parcours Pro</h1>
            <p>Explorez des outils et des ressources pour développer vos compétences et atteindre vos objectifs de carrière.</p>
            <a href="#" class="cta-button">Découvrir les outils</a>
        </div>
        <div class="top-right">
            <img src="1.jpg" alt="Image de présentation">
        </div>
    </div>

    <div class="cv-section">
        <div class="personal-info">
            <img src="2.jpg" alt="Photo de profil de Sugira Yannick">
            <div>
                <h2>SUGIRA YANNICK</h2>
                <p>Développeur Web | Passionné par l'innovation et les technologies émergentes</p>
            </div>
        </div>

        <div class="section-title">Expérience Professionnelle</div>
        <div class="experience-item">
            <h3>Développeur Front-end</h3>
            <p class="date">2020 - Présent | Entreprise XYZ</p>
            <p>Conception et développement d'interfaces utilisateur interactives et responsives en utilisant HTML, CSS et JavaScript. Participation à l'amélioration de l'expérience utilisateur et à l'optimisation des performances.</p>
        </div>
        <div class="experience-item">
            <h3>Stagiaire Développement Web</h3>
            <p class="date">2019 | Agence ABC</p>
            <p>Participation au développement de sites web et d'applications web sous la supervision de développeurs seniors. Apprentissage des méthodologies de développement agile.</p>
        </div>

        <div class="section-title">Formation</div>
        <div class="education-item">
            <h3>Master en Informatique</h3>
            <p class="date">2017 - 2019 | Université de Lyon</p>
            <p>Spécialisation en développement web et mobile.</p>
        </div>
        <div class="education-item">
            <h3>Licence en Sciences Informatiques</h3>
            <p class="date">2014 - 2017 | Université de Grenoble</p>
        </div>

        <div class="section-title">Projets</div>
        <div class="project-item">
            <h3>Portfolio Personnel</h3>
            <p>Développement d'un site web personnel pour présenter mes projets et mes compétences.</p>
            <p><a href="#">Voir le projet</a></p>
        </div>
        <div class="project-item">
            <h3>Application Web de Gestion de Tâches</h3>
            <p>Création d'une application web pour organiser et suivre les tâches quotidiennes.</p>
            <p><a href="#">Voir le projet</a></p>
        </div>

        <div class="section-title">Réseaux Sociaux</div>
        <p class="social-links"><a href="#">LinkedIn</a> | <a href="#">GitHub</a> | <a href="#">Twitter</a></p>
    </div>

    <div class="skills-section">
        <h2>Compétences</h2>
        <div class="skills-list">
            <div class="skill-item">
                <h4>Développement Web</h4>
                <p>HTML, CSS, JavaScript, React, Angular</p>
            </div>
            <div class="skill-item">
                <h4>Back-end</h4>
                <p>Node.js, Python, PHP, SQL</p>
            </div>
            <div class="skill-item">
                <h4>Outils & Méthodes</h4>
                <p>Git, Agile, Scrum, Figma</p>
            </div>
            <div class="skill-item">
                <h4>Développement Web</h4>
                <p>HTML, CSS, JavaScript, React, Angular</p>
            </div>
            <div class="skill-item">
                <h4>Back-end</h4>
                <p>Node.js, Python, PHP, SQL</p>
            </div>
            <div class="skill-item">
                <h4>Outils & Méthodes</h4>
                <p>Git, Agile, Scrum, Figma</p>
            </div>  
            <div class="skill-item">
                <h4>Développement Web</h4>
                <p>HTML, CSS, JavaScript, React, Angular</p>
            </div>
            <div class="skill-item">
                <h4>Back-end</h4>
                <p>Node.js, Python, PHP, SQL</p>
            </div>
            <div class="skill-item">
                <h4>Outils & Méthodes</h4>
                <p>Git, Agile, Scrum, Figma</p>
            </div>
            <div class="skill-item">
                <h4>Développement Web</h4>
                <p>HTML, CSS, JavaScript, React, Angular</p>
            </div>
            <div class="skill-item">
                <h4>Back-end</h4>
                <p>Node.js, Python, PHP, SQL</p>
            </div>
            <div class="skill-item">
                <h4>Outils & Méthodes</h4>
                <p>Git, Agile, Scrum, Figma</p>
            </div>
            <div class="skill-item">
                <h4>Développement Web</h4>
                <p>HTML, CSS, JavaScript, React, Angular</p>
            </div>
            <div class="skill-item">
                <h4>Back-end</h4>
                <p>Node.js, Python, PHP, SQL</p>
            </div>
            <div class="skill-item">
                <h4>Outils & Méthodes</h4>
                <p>Git, Agile, Scrum, Figma</p>
            </div>       

        </div>
    </div>

    <div class="offer-section">
        <div class="offer-text">
            <h2>Mettez en avant votre parcours dès aujourd'hui</h2>
            <p>Avec Mon Parcours Pro, valorisez vos compétences et expériences professionnelles pour atteindre vos objectifs.</p>
            <ul>
                <li>✅ Design intuitif</li>
                <li>✅ Facilité d'utilisation</li>
                <li>✅ Adapté à tous les secteurs</li>
                <li>✅ Mise en valeur personnalisée</li>
            </ul>
            <a href="#" class="cta-button">Commencer maintenant <i class="fas fa-arrow-right"></i></a>
        </div>
        <div class="offer-image">
            <img src="https://github.com/Sugira-Yannick/Sugira-Yannick.github.io/blob/main/3.jpg" alt="Mettez en avant votre parcours">
        </div>
    </div>

    <footer>
        <div class="social-icons">
            <a href="#"><i class="fab fa-linkedin"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-github"></i></a>
        </div>
        <p>&copy; 2025 Mon Parcours Pro</p>
    </footer>

    <script src="https://kit.fontawesome.com/your_fontawesome_kit.js" crossorigin="anonymous"></script>
</body>
</html>
