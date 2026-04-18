
<!DOCTYPE html> 
<html lang="fr" dir="ltr">
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>BinYdik بين يديك .. Sécurité pour chaque femme </title>
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,opsz,wght@0,9..40,400;09..40,500;1,9..40,300&display=swap" rel="stylesheet">
        <style>
            *, *::before, *::after {
                box-sizing: border-box;
                margin: 0;
                padding: 0;
            }
            :root {
                --purple-950: #1a0533;
                --purple-900: #2d0a5c;
                --purple-800: #4a1578;
                --purple-600: #7c3aed;
                --purple-400: #a78bfa; 
                --purple-300: #c4b5fd;
                --purple-100: #ede9fe;
                --pink-400: #f472b6;
                --pink-500: #ec4899;
                --rose-400: #fb7185;
                --white: #ffffff;
                --gray-100: #f3f4f6;
                --gray-400: #9ca3af;
                --gray-600: #4b5563;

            }
            html { scroll-behavior: smooth; 
            body {
                font-family: 'DM Sans', sans-serif;
                background : var(--purple-950);
                color: var(--white);
                overflow-x: hidden; 
            }

            body::before {
                content: ' ';
                position: fixed;
                inset: 0;
                background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmls='http://www.w3.org/2000/svg'%3E%3Cfilter id= 'noise' %3E%3CfeTurbulence type= 'fractalNoise' baseFrequency= '0.9' numOctaves= '4' stitchTiles= 'stitch' /%3E%3C/filter%3E%3Crect width= '100%25' height= '100%25' filter= 'url(%23noise)' opacity= '0.04' /%3E%3C/svg%3E");
                pointer-events: none;
                z-index: 0; 
            }

            nav {
                position: fixed; top: 0; left: 0; right: 0; z-index: 100;
                display: flex; align-items: center; justify-content: space-between;
                padding: 1.2rem 5%;
                background: rgba(26, 5, 51, 0.85);
                backdrop-filter: blur(20px);
                border-bottom: 1px solid rgba(167,139,250,0,15);
            }

            .nav-logo {
                display: flex; align-items: center; gap: 0.7rem;
                font-family: 'Syne', sans-serif; font-weight: 800; font-size: 1.4rem;
                color: var(--white); text-decoration: none
            }
            .nav-logo .shield {font-size:1.6rem;}

            .nav-links{display: flex; gap: 2rem; list-style: none;   }
            .nav-links a {
                color: var(--purple-300); text-decoration: none; font-size: 0.9rem; font-weight: 500;
                transition: color 0.2s;
            }
            .nav-links a:hover {
                color: var(--white);}
            
            .nav-cta {
                background: linear-gradient(135deg, var(--purple-600), var(--pink-500));
                color: white; border: none; padding: 0.6rem 1.4rem;
                border-radius: 50px; font-family: 'DM Sans', sans-serif;
                font-size: 0.9rem; font-weight:600; cursor: pointer;
                transition: transform 0.2s, box-shadow 0.2s;
                text-decoration: none;
            }
            .nav-cta:hover {
                transform: translateY(-1px);
                box-shadow: 0 8px 25px rgba(139, 92, 246 , 0.4);}

            .hero {
                min-height: 100vh; display: flex; align-items: center; justify-content: center; text-align: center;
                padding: 7rem 5% 4rem;
                position: relative; 
                overflow: hidden;
            }

            .hero::after{
                content: '';
                position: absolute;
                width: 700px; height: 700px;
                background: radial-gradient(circle, rgba(124,58,237,035) 0%, transaprent 70%);
                top: 50%; left: 50%; transform: translate(-50%, -60%);
                pointer-events: none;
            }

            .orb1 {
                position: absolute; width: 200px; height: 400px; border-radius: 50%; background: radial-gradient(circle, rgba(236, 72, 153, 0.2) 0%, transparent 70%);
                top: 20%; right: 10%; animation: float1 8s ease-in-out infinite;
            }
            .orb2 {
                position: absolute; width: 300px; height: 300px; border-radius: 50%; background: radial-gradient(circle, rgba(167, 139, 250, 0.15) 0%, transparent 70%);
                bottom: 20%; left: 5%; animation: float 6s ease-in-out infinite reverse;
            }
            @keyframes float {
                0%, 100% { transform: translateY(0)}
                50% { transform: translateY(-30px)} }
                
                      
                     .hero-badge {
                display: inline-flex; align-items: center; gap: 0.5rem;
                background: rgba(167, 139, 250, 0.15);
                border: 1px solid rgba(167, 139, 250, 0.3);
                color: var(--purple-300); font-size: 0.85rem; font-weight: 500; padding: 0.4rem 1rem; border-radius: 50px;
                margin-bottom: 2rem;
                        animation: fadeUp 0.8s ease both;
                     }
                .hero-badge .dot {
                    width: 7px; height: 7px; border-radius: 50%; background: var(--pink-400); animation: pulse 2s infinite;
                }
                @keyframes pulse { 0%, 100% { opacity:1;transform: scale(1)} 50% { opacity: 0.6; transform: scale(1.3) } }

                .hero-arabic {
                    font-family: 'Syne', sans-serif; font-weight: 600; font-size: 1.1rem; color: var(--purple-400); margin-bottom: 0.5rem;
                    animation: fadeUp 0.9s 0.1s ease both;
                }
                .hero-title {
                    font-family: 'Syne', sans-serif;
                    font-size: clamp(3.5rem, 8vw, 6.5rem);
                    font-weight: 800; line-height: 1;
                    background: linear-gradient(135deg, #fff 0%, var(--purple-300) 50%, var(--pink-400) 100%);
                        -webkit-background-clib: text; -webkit-text-fill-color: transparent; background-clip: text;
                        margin-bottom: 1.5rem;
                        animation: fadeUp 1s 0.2s ease both;
                }

                .hero-sub {
                    font-size: 1.2rem; color: var(--purple-300); line-height: 1.7;
                    max-width: 580px; margin: 0 auto 3rem;
                    font-weight: 300;
                    animation: fadeUp 1s 0.3s ease both;
                }

                .hero-buttons {
                    display: flex; gap: 1rem; justify-content: center;
                    flex-wrap: wrap;
                    animation: fadeUp 1s 0.4s ease both;
                }

                .btn-primary {
                    display: inline-flex; align-items: center; gap: 0.6rem;
                    background: linear-gradient(135deg, var(--purple-600), var(--pink-500));
                    color: white; border: none; padding: 1rem 2rem;
                    border-radius: 50px; font-family: 'DM Sans', sans-serif;
                    font-size: 1rem; font-weight:600; cursor: pointer;
                    text-decoration: none;
                    box-shadow: 0 0 40px rgba(124, 58, 237, 0.5);
                    transition: transform 0.2s, box-shadow 0.2s;
                }
                .btn-primary:hover {
                    transform: translateY(-3px);
                    box-shadow: 0 15px 50px rgba(124, 58, 237, 0.6); }

                .btn-secondary {
                    display: inline-flex; align-items: center; gap: 0.6rem;
                    background: transparent; color: var(--purple-300);
                    border: 1px solid rgba(167, 139, 250, 0.4); padding: 1rem 2rem; border-radius: 50px; font-family: 'DM Sans', sans-serif;
                    font-size: 1rem; font-weight: 500; cursor: pointer;
                    text-decoration: none;
                    transition: border-color 0.2s, color 0.2s, background 0.2s;
                }
                .btn-secondary:hover {
                    border-color: var(--purple-400);
                    color: white;
                    background: rgba(167, 139, 250, 0.1); 

                }

                @keyframes fadeUp {
                    from { opacity: 0; transform: translateY(30px) }
                    to { opacity: 1; transform: translateY(0) }

                    .scroll-hint {
                        position: absolute; bottom: 2rem; left: 50%; transform: translateX(-50%);
                        display: flex; flex-direction: column; align-items: center; gap: 0.4rem;
                        font-size: 0.75rem; color: var(--purple-400); animation:fadeUp 1s 1s ease both;
                    }

                    .scroll-hint-line {
                        width: 1px; height: 40px; background: linear-gradient(to bottom, var(--purple-500), transparent);
                        animation: lineDown 2s   ease-in-out infinite;
                    }
                    @keyframes lineDown {
                        0% { height: 0; opacity:0}
                         50% { height: 40px; opacity: 1 }
                        100% { height: 40px; opacity: 0 }
                    }

                    .stats-bar {
                        background: rgba(45,10,92,0.6);
                        border-top: 1px solid rgba(167, 139, 250, 0.2);
                        border-bottom: 1px solid rgba(167, 139, 250, 0.2);
                        padding: 2rem 5%;
                        display: flex; justify-content: center; gap: 5rem; flex-wrap: wrap;    
                    }
                    .stat {
                        text-align: center;
                    }
                    .stat-number {
                        font-family: 'Syne', sans-serif; font-weight: 800; font-size: 2.2rem; 
                        background: linear-gradient(135deg, var(--purple-300), var(--pink-400));
                        -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
                               }
                    .stat-label {
                        font-size: 0.85rem; color: var(--purple-400); margin-top: 0.2rem;}

                        .section {
                            padding: 5rem 5%;
                            max-width: 1200px; margin: 0 auto;
                        }

                        .section-tag {
                            display: inline-block; color: var(--pink-400);
                            font-size: 0.75rem; font-weight: 700; margin-bottom: 0.8rem;
                            
                        }
                        .section-title {
                            font-family: 'Syne', sans-serif; 
                            font-weight: 800;
                            font-size: clamp(2rem, 4vw, 3rem);
                            margin-bottom: 1rem; line-height: 1.1;
                        }

                        .section-sub {
                            font-size: 1.05rem; 
                            color: var(--purple-300); 
                            line-height: 1.7;
                            max-width: 600px; 
                        }

                        .problem-grid{
                            display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; margin-top: 3rem;
                        }

                        .problem-card{
                            background: rgba(74, 16, 128, 0.2);
                            border: 1px solid rgba(167, 139, 250, 0.2);
                            border-radius: 20px; padding: 2rem;
                            position: relative; overflow: hidden;
                            transition: border-color 0.3s, transform 0.3s;
                        }

                        .problem-card:hover {
                            border-color: rgba(167, 139, 250, 0.5);
                            transform: translateY(-4px);}

                            .problem-card .big-num {
                                font-family: 'Syne', sans-serif; font-weight: 800; font-size: 3.5rem}
                                background: linear-gradient(135deg, var(--purple-300), var(--pink-400));
                                -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
                                line-height: 1;
                            }

                        .problem-card p { color: var(--purple-300); font-size: 0.95rem; margin-top: 0.5rem; line-height: 1.5;}
                        
                        
                        .features-wrap {padding: 5rem 5%;}
                        .features-inner {max-width: 1200px; margin: 0 auto; }

                        .features-grid {
                            display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; margin-top: 3rem;
                        }
                        .feature-card {
                            background: rgba(45, 10, 92, 0.4);
                            border: 1px solid rgba(167, 139, 250, 0.15);
                            border-radius: 24px; padding: 2rem;
                            transition: all 0.3s;
                            position: relative; overflow: hidden;
                        }

                        .feature-card::before {
                            content: '';
                            position: absolute; inset: 0; background: linear-gradiant(135deg, rgba(124,58,237,0.1) 0%, transparent 6...
                            
                        }
        </style>
    </head>
    <body>
        ::before
        <!--NAV -->
        <nav>
            <a href="#" class="nav-logo"><span class="shield">🛡️</span>
                "Bin"
                <span>Ydik</span>
            </a>
            <ul class="nav-links">
                <li><a href="#features">Fonctionnalités </a>
                </li>
                <li><a href="#demo">Comment ça marche</a>
                </li>
                    <li><a href="#bmc">Business Model</a>
                  </li> 
                  <li><a href="team">Notre Équipe</a>
                  </li>
            </ul>
            <a href="#cta" class="nav-cta">Télécharger</a>
        </nav>
        <!-- HERO -->
         <section class="hero">
            <div class="orb1"></div>
            <div class="orb2"></div>
            <div class="hero-content">
                <div class="hero-badge">
                    <span class="dot"></span>
                    "Projet Entrepreneuriat 2ème année BI FSEGT 2025-2026"
                </div>
                <p class="hero-arabic"> بين يديك  - Entre tes mains  </p>
                <h1 class="hero-title">BinYdik</h1>
                <p class="hero-sub">"BinYdik est une application mobile innovante conçue pour renforcer la sécurité des femmes dans les espaces publics. Grâce à une interface intuitive et des fonctionnalités avancées, BinYdik offre une protection proactive en permettant aux utilisatrices de signaler rapidement les incidents, d'envoyer des alertes à leurs contacts de confiance et de partager leur localisation en temps réel. Notre mission est de créer un environnement plus sûr pour toutes les femmes, en leur donnant les outils nécessaires pour se sentir protégées et autonomes dans leurs déplacements quotidiens. Par un seul bouton.. une vie protégée."</p>
                <div class="hero-buttons">
                    <a href="#features" class="btn-primary">Découvrir l'app</a>
                    <a href="#demo" class="btn-secondary">Voir la démo</a>
                </div>
            </div>
            <div class="scroll-hint">
                <span>Faites défiler pour en savoir plus</span>
                <div class="line"></div>
            </div>
            ::after
         </section>
         <!-- STATS -->
          <div class="stats-bar">
            <div class="stat">
                <div class="stat-number">78%</div>
                <div class="stat-label">des femmes se sentent en insécurité dans les espaces publics à cause des harcelements</div>
            </div>
            <div class="stat">
                <div class="stat-number">2.5M</div>
                <div class="stat-label">femmes actives & étudiantes en Tunisie</div>
            </div>
        </div>
        <div class="stat">
            <div class="stat-number">0</div>
            <div class="stat-label">application locale dédiée à ce jour </div>
        </div>
        <div class="stat">
            <div class="stat-number">2s</div>
            <div class="stat-label">pour déclencher une alerte SOS </div>
        </div>
    </div>
    <!-- PROBLEMS -->
<div style="background: rgba(26,5,51,0.5);">
    <div class=""section">
        <p class="section-tag">Le Problème</p>
        <h2 class="section-title">Pourquoi BinYdik ?</h2>
        <p class="section-sub">Malgré les avancées technologiques, aucune solution technologique locale n'existe pour garantir la sécurité des femmes dans les espaces publics en Tunisie. Les femmes font face à des risques quotidiens de harcèlement et d'agression, ce qui limite leur liberté de mouvement et affecte leur qualité de vie. BinYdik vise à combler ce vide en offrant une application mobile dédiée qui permet aux femmes de se sentir plus en sécurité et autonomes dans leurs déplacements.</p>
        <div class="problem-grid">
            <div class="problem-card">
                <div class="big-num">78%</div>
                <p>"des femmes tunisiennes ont subi d'harcélement en espace public (Source: étude nationale 2023)"</p>
    </div>
            <div class="problem-card">
                <div class="big-num">94%</div>
                <p>"beaucoup des femmes disent qu'elles ont peur de sortir seules la nuit. Elles déclarent aussi que ces comprtements sont un "cauchemar qutidien". (Source: LaPresse.tn en 2022)"</p>
            </div>
            <div class="problem-card">
                <div class="big-num">0</div>
                <p>"application locale dédiée à ce jour pour garantir la sécurité des femmes dans les espaces publics en Tunisie. un marché 100% vierge"</p>
            </div>
        </div>
    </div>
</div>

<!-- FEATURES -->
<div class="features-wrap" id="features">
    <div class="features-inner">
        <p class="section-tag">Fonctionnalités</p>
        <h2 class="section-title">Tout ce dont tu as besoin." <br> "dans un seul clic"</h2>
        <div class="features-grid">
            <div class="feature-card">
                ::before
                <div class="feature-icon">🆘</div>
                <div class="features-title">Bouton SOS</div>
                <div class="feature-desc">
                    "Alerte instantanée envoyée à tes contacts proches avec ta localisation GPS précise. Activable en moins de 2 secondes, même écran verrouillé."
                </div>
                <span class="feature-tag tag-free">Gratuit</span>
            </div>
            <div class="feature-card">
                ::before
                <div class="feature-icon">📍</div>
                    <div class="features-title">Partage de localisation</div>
                    <div class="feature-desc">
                        "Partage ta localisation en temps réel avec tes contacts de confiance pendant tes déplacements. Idéal pour les trajets nocturnes ou dans des zones peu fréquentées."
                        </div>
                        <span class="feature-tag tag-free">Gratuit</span>
            </div>
            <div class="feature-card">
                        <div class="feature-icon">🔔</div>
                        <div class="features-title">Alerte contacts proches </div>
                        <div class="feature-desc">
                            "SMS + notifications push automatiques à toute ta liste d'urgence simultanément. Tes proches sont alertés immédiatement en moins de 5 secondes."
                        </div>
                        <span class="feature-tag tag-free">Gratuit</span>
            </div>
            <div class="feature-card">
                ::before
                <div class="feature-icon">🔒</div>
                <div class="features-title">Mode discret</div>
                <div class="feature-desc">
                    "Activation silencieuse de l'alerte SOS. Pas de son, pas de vibration visible. L'agresseur ne voit rien. Tes proches sont alertés en toute discrétion."
                </div>
                <span class="feature-tag tag-premium">Premium</span>
            </div>
            <div class="feature-card">
                ::before
                <div class="feature-icon">🎙️</div>
                <div class="features-title">Enregistrement audio</div>
                <div class="feature-desc">
                    "Enregistre automatiquement les sons ambiants pendant une alerte SOS. Utile pour fournir des preuves audio en cas d'incident."
                </div>
                <span class="feature-tag tag-premium">Premium</span>
            </div>
            <span class="feature-tag tag-premium">Premium</span>
            <div class="feature-card">
                ::before
                <div class="feature-icon">👥</div>
                <div class="features-title">Carte Communautaire</div>
                <div class="feature-desc">
                    "Signale et consulte les zones dangereuses reportées par d'autres utilisatrices. Une intelligence collective au service de ta sécurité."
                </div>
                <span class="feature-tag tag-free">Gratuit</span>
            </div> 
        </div>
    </div>
</div>

<!-- DEMO -->
<div class="demo-wrap" id="demo">
    <div class="demo-inner">
        <div class="phone mockup">
            <div class="phone">
                <div class="phone-notch"></div>
                <div class="phone-screen">
                    <div class="loc">📍 Localisation active : Tunis, Lac II </div>
                    <div class="sos-btn"onclick=this.style.transform = 'scale(0.9)'; setTimeout(() =>this.style.transform = '',200)">
                        "SOS"
                        <span class="sos-text">Maintenir 2s</span>
                    </div>
                    <div class="phone-info">
                        <div style="color: var(--purple-400); font-size: 0.72rem; margin-bottom: 0.5rem;">Contacts d'urgence : </div>
                    </div>
           <div class="contact-list">
                <div class="contact-chip">
                    <span class="dot-green"></span>
                    "Mama"
                </div>
                <div class="contact-chip">
                    <span class="dot-green"></span>
                    "Eya" (amie)
                </div>
                <div class="contact-chip">
                    <span class="dot-green"></span>
                    "Salim" (frère)
                </div>
                <div class="contact-chip">
                    <span class="dot-green"></span>
                    "Papa"
                </div>
           </div>
                </div>
            </div>
        </div>
        </div>  

        <div class="demo-text">
            <p class="section-tag">Comment ça marche ?</p>
            <h2>"Simple. Rapide. Sûr."</h2>
            <br>
            "Efficace."
            </h2>
            <p>"En situation de danger, chaque seconde compte. BinYdik est conçue pour te protéger en toute simplicité."</p>
            <div class="steps">
                <div class="step">
                    <div class="step-num">1</div>
                    <div class="step-info">
                        <strong> Tu te sens en danger</strong>
                        <span>Appuie sur le bouton SOS rouge (2 secondes)</span>
                    </div>
                </div>
                <div class="step">
                    <div class="step-num">2</div>
                    <div class="step-info">
                        <strong> Alerte instantanée</strong>
                        <span>SMS + notifications envoyées à tous tes contacts d'urgence avec ta localisation GPS exacte"</span>
                    </div>
                </div>
                <div class="step">
                    <div class="step-num">3</div>
                    <div class="step-info">
                        <strong> Tes proches réagissent</strong>
                        <span>Ils suivent ta position en temps réel et peuvent t'aider immédiatement en savant ta localisation exacte.</span>
                    </div>
                </div>
                <div class="step">
                    <div class="step-num">4</div>
                    <div class="step-info">
                        <strong> Enregistrement audio (Premium)</strong>
                        <span>L'application enregistre le son ambiant automatiquement ; Preuve concervée en sécurité.</span>
                    </div>
                 </div>
            </div>
        </div>
    </div>
</div>

<!-- BMC -->
 <div class="bmc-wrap" id="bmc">
    <div class="bmc-inner">
        <p class="section-tag">Business Model Canvas</p>
        <h2 class="section-title">Comment BinYdik génère de la valeur ?</h2>
        <div class="bmc-grid">
            <div class="bmc-card">
                <h4>Partenaires clés</h4>
                <ul>
                    <li>
                        ::before
                        "Universités et écoles pour la sensibilisation et le recrutement d'utilisatrices pilotes."
                    </li>
                <li>
                    ::before
                    "ATFD (Association Tunisienne des Femmes Démocrates) pour le soutien communautaire et la légitimité sociale."
                </li>
                <li>
                    ::before
                    "Ooredoo, Orange, Tunisie Telecom pour l'intégration de services SMS et la distribution."
                </li>
                <li>
                    ::before
                    "Google Firebase/Maps pour l'infrastructure technique et les services de localisation."
                </li>
                <li>
                    ::before
                    "Ministère de la Femme pour le soutien institutionnel et les campagnes de sensibilisation."
                </li>
                <li>
                    ::before
                    "Ministère de l'Intérieur pour la coordination en cas d'incidents signalés via l'app."
                </li>
                </ul>
            </div>
            <div class="bmc-card center" style="border-color:rgba(167,139,250,00.4); background: rgba(74,16,128,0.5);">
                <h4>Proposition de valeur</h4>
                <p style="color: white; font-family: 'Syne', sans-serif; font-size: 1.3rem; font-weight: 700; margin-bottom : 1rem;">La sécurité bin ydik</p>
                <ul>
                    <li>
                        ::before
                        "SOS en 2 secondes"
                    </li>
                    <li>
                        ::before
                        "Partage de localisation en temps réel"
                    </li>
                    <li>
                        ::before
                        "Adapté au contexte tunisien"
                    </li>
                    <li>
                        ::before
                        "Interface arabe + français"
                    </li>
                    <li>
                        ::before
                        "Fonctionne sans internet (SMS)"
                    </li>
                    <li>
                        ::before
                        "Gratuit dans sa version de base"
                    </li>
                </ul>
            </div>"
            <div class="bmc-card">
                <h4>Segments de clients</h4>
                <ul>
                    <li>
                        ::before
                        "Etudiantes 18-25 ans "
                    </li>
                    <li>
                        ::before
                        "Femmes actives 25-55 ans"
                    </li>
                    <li>
                        ::before
                        "Parents(surtout mères) de jeunes filles"
                    </li>
                    <li>
                        ::before
                        "Entreprise (pour la sécurité de leurs employées)"
                    </li>
                    <li>
                        ::before
                        "Institutions éducatives (universités, écoles)"
                    </li>
                    <li>
                        ::before
                        "Associations féminines"
                    </li>
                </ul>
                </div>
                <div class="bmc-card">
                    <h4>Activités clés</h4>
                    <ul>
                        <li>
                            ::before
                            "Développement de l'application"
                        </li>
                        <li>
                            ::before
                            "Maintenance serveurs"
                        </li>
                        <li>
                            ::before
                            "Marketing digital"
                        </li>
                        <li>
                            ::before
                            "Partenariats avec institutionnels et associations"
                        </li>
                        <li>
                            ::before
                            "Support client et gestion de la communauté"
                        </li>
                    </ul>
                </div>
                <div class="bmc-card">
                    <h4>Canaux </h4>
                    <ul>
                        <li>
                            ::before
                            "App Store & Google Play"
                        </li>
                        <li>
                            ::before
                            "Réseaux sociaux (Instagram, Facebook, TikTok)"
                        </li>
                        <li>
                            ::before
                            "Partenariats avec universités et écoles"
                        </li>
                        <li>
                            ::before
                            "Campagnes de sensibilisation en ligne et hors ligne"
                        </li>
                        <li>
                            ::before
                            "Relations presse et médias"
                        </li>
                    </ul>
                </div>
                <div class="bmc-bottom">
                    <div class="bmc-card">
                        <h4>Structure de coûts</h4>
                        <ul>
                            <li>
                                ::before
                                "Développement MVP : 3 500 TND (développeur freelance)"
                            </li>
                            <li>
                                ::before
                                APIs & hébergement : 1 300 TND"
                            </li>
                            <li>
                                ::before
                                "Marketing lancement : 2 000 TND"
                            </li>
                            <li>
                                ::before
                                "Frais juridiques : 3000 TND"
                            </li>
                            <li>
                                ::before
                                "Fonds de roulement : 7 000 TND"
                            </li>
                            <li>
                                ::before
                                <strong style="color:white">TOTAL : 16 800 TND </strong>
                            </li>
                        </ul>
                    </div>
                    <div class="bmc-card">
                        <h4>Sources de revenus</h4>
                        <ul>
                            <li>
                                ::before
                                "Premium 3.5 TND/mois (abonnement mensuel)"

                            </li>
                            <li>
                                ::before
                                "Partenariats universités / entreprises pour la sécurité de leurs employées"
                            </li>
                            <li>
                                ::before
                                "Publicité partenaires engagés (ex: compagnies d'assurance, services de taxi sécurisés)"
                            </li>
                            <li>
                                ::before
                                <strong style="color: #4ade80">An 1 : 6 400 TND</strong>
                            </li>
                            <li>
                                ::before
                                <strong style="color: #fbbf24">An 2 : 28 000 TND</strong>
                            </li>
                            <li>
                                ::before
                                <strong style="color: #a78bfa">An 3 : 48 000 TND</strong>
                            </li>
                        </ul>
                    </div>
                </div>
                </div>  
                </div>
                </div>  
                <!--TEAM-->
                <div class="team-wrap" id="team">
                    <div class="team-inner
                    <p class="section-tag">Notre Équipe</p>
                    <h2 class="section-title">5 étudiantes.. une mission</h2>
                    <p class="section-sub"style="margin: 0.5rem auto 0; max-width: 500px">2BI  FSEGT 2025-2026</p>
                    <div class="team-grid">
                        <div class="team-card">
                            <div class="team-avatar">👨‍💻</div>
                            <div class="team-role">Chef de projet</div>
                            <div class="team-name">Malek HOMRI</div>
                            <div class="team-card">
                                <div class="team-avatar">💻</div>
                                <div class="team-name">Eya SELLINI </div>
                                <div class="team-role">Développeuse</div>
                                <div class="team-card">
                                    <div class="team-avatar">🔍</div>
                                    <div class="team-name">Eya KHAZRI</div>
                                    <div class="team-role">Analyste</div>
                                    <div class="team-card">
                                        <div class="team-avatar">📊</div>
                                        <div class="team-name">Maram JBELI</div>
                                        <div class="team-role">Marketing & Business Dev</div>
                                        <div class="team-card">
                                            <div class="team-avatar">🎨</div>
                                            <div class="team-name">Ines </div>
                                            <div class="team-role">Designer</div>
                                        </div>
                                    </div>
                            </div>
                        </div>
                    </div>
                </div>
                <!--CTA-->
                <div class="cta-wrap" id="cta">
                    ::before
                    <h2>بين يديك
                    <br>
                    BinYdik
                    </h2>
                    <p>La sécurité n'est pas un luxe, c'est un droit</p>
                    <div class="hero-buttons"style="position:relative;">
                        <a href="#" class="btn-primary">📱 Télécharger BinYdik</a>
                        <a href="#bmc" class="btn-secondary">📊Voir le Business Plan</a>
                    </div>
                </div>
                <!--FOOTER-->
                <footer>
                    <p>
                        <strong>BinYdik</strong>
                            - Projet Entrepreneuriat 2ème année BI FSEGT 2025-2026
                            <br>
                            "Entre tes mains, la sécurité de demain"
                    </p>
                    <p style="margin-top: 0.4rem;">
                        "Dr. Samah Chemli Horchani - Professeur d'Entrepreneuriat"

