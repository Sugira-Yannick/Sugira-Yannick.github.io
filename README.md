<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YANNICK SUGIRA | Technicien Systèmes Réseaux</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet" />
<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
<script>
  AOS.init();
</script>
<style>
        :root {
            --primary: #2563eb;
            --primary-light: #3b82f6;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #94a3b8;
            --card-bg: #ffffff;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            color: white;
            padding: 4rem 0 6rem;
            text-align: center;
            position: relative;
            clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
        }
        
        .profile-img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid rgba(255,255,255,0.2);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        
        h1 {
            font-size: 2.5rem;
            font-weight: 700;
            margin: 1rem 0 0.5rem;
        }
        
        h2 {
            font-size: 1.5rem;
            font-weight: 500;
            color: var(--gray);
            margin-bottom: 1.5rem;
        }
        
        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: -3rem;
            position: relative;
            z-index: 2;
        }
        
        .card {
            background: var(--card-bg);
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
            padding: 2rem;
            transition: transform 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
        }
        
        .card h3 {
            font-size: 1.25rem;
            margin-bottom: 1rem;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .skill-tag {
            display: inline-block;
            background: #e0e7ff;
            color: var(--primary);
            padding: 0.4rem 1rem;
            border-radius: 20px;
            font-size: 0.9rem;
            margin: 0.25rem;
        }
        
        .timeline-item {
            position: relative;
            padding-left: 2rem;
            margin-bottom: 2rem;
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            width: 2px;
            height: 100%;
            background: var(--primary);
        }
        
        .timeline-dot {
            position: absolute;
            left: -8px;
            top: 4px;
            width: 16px;
            height: 16px;
            border-radius: 50%;
            background: var(--primary);
        }
        
        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 0;
            margin-top: 4rem;
            text-align: center;
        }
        
        @media (max-width: 768px) {
            .card-grid {
                grid-template-columns: 1fr;
            }
            
            header {
                padding: 3rem 0 5rem;
                clip-path: polygon(0 0, 100% 0, 100% 90%, 0 100%);
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <img src="https://via.placeholder.com/150" alt="Photo profil" class="profile-img">
            <h1>Yannick Suppirà</h1>
            <h2>Technicien Systèmes & Réseaux</h2>
        </div>
    </header>

    <main class="container">
        <div class="card-grid">
            <div class="card">
                <h3><i class="fas fa-user"></i> Profil</h3>
                <p>Technicien systèmes et réseaux passionné par la résolution de problèmes et l'optimisation des infrastructures IT. Diplômé d'un bac+2 et certifié CCNA.</p>
                <div style="margin-top: 1rem;">
                    <span class="skill-tag"><i class="fas fa-check"></i> Disponible immédiatement</span>
                    <span class="skill-tag"><i class="fas fa-map-marker-alt"></i> Lille, France</span>
                </div>
            </div>

            <div class="card">
                <h3><i class="fas fa-tools"></i> Compétences</h3>
                <div>
                    <span class="skill-tag">Windows</span>
                    <span class="skill-tag">Linux</span>
                    <span class="skill-tag">Routage</span>
                    <span class="skill-tag">Virtualisation</span>
                    <span class="skill-tag">Active Directory</span>
                    <span class="skill-tag">ServiceNow</span>
                    <span class="skill-tag">Sécurité</span>
                    <span class="skill-tag">Cloud</span>
                </div>
            </div>
        </div>

        <div class="card-grid" style="margin-top: 1.5rem;">
            <div class="card">
                <h3><i class="fas fa-briefcase"></i> Expérience</h3>
                
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <h4>Technicien HelpDesk N1</h4>
                    <p><strong>Econocom</strong> | Août 2024 - Fév 2025</p>
                    <ul style="margin-top: 0.5rem; padding-left: 1.2rem;">
                        <li>Identifier et analyser les incidents</li>
                        <li>Résoudre les incidents auprès des utilisateurs</li>
                        <li>Garantir la qualité de service</li>
                    </ul>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <h4>Technicien de configuration</h4>
                    <p><strong>Ingram Micro</strong> | Oct - Déc 2018</p>
                    <ul style="margin-top: 0.5rem; padding-left: 1.2rem;">
                        <li>Déploiement de systèmes d'exploitation</li>
                        <li>Administration systèmes et applications</li>
                    </ul>
                </div>
            </div>

            <div class="card">
                <h3><i class="fas fa-graduation-cap"></i> Formations</h3>
                
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <h4>Titre Professionnel Bac+2</h4>
                    <p><strong>Technicien systèmes réseaux</strong></p>
                    <p>AFC1 Villeneuve d'Ascq | 2023</p>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <h4>CCNA Introduction au réseau</h4>
                    <p><strong>Cisco Network Academy</strong></p>
                    <p>Certifié Février 2024</p>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <h4>Bac Informatique</h4>
                    <p><strong>Apade Kigali, Rwanda</strong></p>
                    <p>2005 - 2008</p>
                </div>
            </div>
        </div>
    </main>

    <footer>
        <div class="container">
            <h3>Contactez-moi</h3>
            <p style="margin: 1rem 0;"><i class="fas fa-phone"></i> 07 44 12 96 70</p>
            <p style="margin: 1rem 0;"><i class="fas fa-envelope"></i> sugirayannick@yahoo.fr</p>
            <p style="margin: 1rem 0;"><i class="fas fa-map-marker-alt"></i> 59000 Lille, France</p>
            
            <div style="margin-top: 2rem;">
                <a href="#" style="color: white; margin: 0 10px; font-size: 1.2rem;"><i class="fab fa-linkedin"></i></a>
                <a href="#" style="color: white; margin: 0 10px; font-size: 1.2rem;"><i class="fab fa-github"></i></a>
                <a href="#" style="color: white; margin: 0 10px; font-size: 1.2rem;"><i class="fas fa-file-pdf"></i></a>
            </div>
        </div>
    </footer>
</body>
</html>
