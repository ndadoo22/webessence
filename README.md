<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Webessence - Création de sites web rapides et sur mesure. Design moderne, référencement optimisé et satisfaction garantie.">
    <title>Webessence - Création de Sites Web sur Mesure | Rapide & Professionnel</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f0abfc 0%, #a5b4fc 50%, #67e8f9 100%);
            min-height: 100vh;
            padding: 20px;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 50%, #ec4899 100%);
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #6366f1, #ec4899);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .gradient-border {
            border: 3px solid transparent;
            border-image: linear-gradient(135deg, #6366f1, #8b5cf6, #ec4899) 1;
        }
        
        .pulse-animation {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% {
                transform: scale(1);
                box-shadow: 0 0 0 0 rgba(99, 102, 241, 0.7);
            }
            70% {
                transform: scale(1.05);
                box-shadow: 0 0 0 10px rgba(99, 102, 241, 0);
            }
            100% {
                transform: scale(1);
                box-shadow: 0 0 0 0 rgba(99, 102, 241, 0);
            }
        }
        
        .floating {
            animation: floating 3s ease-in-out infinite;
        }
        
        @keyframes floating {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        
        .color-dots {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: 0;
        }
        
        .color-dot {
            position: absolute;
            border-radius: 50%;
            opacity: 0.3;
            filter: blur(40px);
        }
        
        .card-bg {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
        }
        
        .section-title {
            position: relative;
            display: inline-block;
            margin-bottom: 2rem;
        }
        
        .section-title:after {
            content: '';
            position: absolute;
            width: 60%;
            height: 4px;
            bottom: -10px;
            left: 20%;
            background: linear-gradient(90deg, #6366f1, #ec4899);
            border-radius: 2px;
        }
        
        .logo-container {
            position: relative;
            width: 120px;
            height: 120px;
            margin: 0 auto;
        }
        
        .logo-symbol {
            position: relative;
            width: 100%;
            height: 100%;
        }
        
        .logo-base {
            position: absolute;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 50%, #ec4899 100%);
            border-radius: 50%;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            transform: rotate(15deg);
        }
        
        .logo-globe {
            position: absolute;
            font-size: 70px;
            color: white;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-15deg);
            z-index: 1;
            text-shadow: 0 0 15px rgba(0,0,0,0.3);
            animation: spin 20s linear infinite;
        }
        
        @keyframes spin {
            0% { transform: translate(-50%, -50%) rotate(-15deg); }
            100% { transform: translate(-50%, -50%) rotate(345deg); }
        }
        
        .logo-w {
            position: absolute;
            font-size: 60px;
            font-weight: 900;
            color: white;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-15deg);
            z-index: 2;
            text-shadow: 0 0 10px rgba(0,0,0,0.2);
        }
        
        .logo-ring {
            position: absolute;
            width: 100%;
            height: 100%;
            border: 3px dashed rgba(255,255,255,0.5);
            border-radius: 50%;
            z-index: 3;
            animation: pulse-ring 3s ease-in-out infinite;
        }
        
        @keyframes pulse-ring {
            0% { transform: scale(1); opacity: 0.7; }
            50% { transform: scale(1.05); opacity: 0.3; }
            100% { transform: scale(1); opacity: 0.7; }
        }
        
        .logo-dots {
            position: absolute;
            width: 100%;
            height: 100%;
            z-index: 4;
        }
        
        .logo-dot {
            position: absolute;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: white;
            box-shadow: 0 0 10px rgba(255,255,255,0.8);
        }
        
        .logo-dot:nth-child(1) {
            top: 10%;
            left: 25%;
            animation: float-dot 4s ease-in-out infinite;
        }
        
        .logo-dot:nth-child(2) {
            top: 20%;
            right: 15%;
            animation: float-dot 5s ease-in-out infinite 0.5s;
        }
        
        .logo-dot:nth-child(3) {
            bottom: 15%;
            left: 30%;
            animation: float-dot 6s ease-in-out infinite 1s;
        }
        
        .logo-dot:nth-child(4) {
            bottom: 10%;
            right: 20%;
            animation: float-dot 5.5s ease-in-out infinite 1.5s;
        }
        
        @keyframes float-dot {
            0%, 100% { transform: translateY(0) translateX(0); }
            25% { transform: translateY(-5px) translateX(5px); }
            50% { transform: translateY(5px) translateX(-5px); }
            75% { transform: translateY(-3px) translateX(-3px); }
        }
        
        .feature-card {
            transition: all 0.3s ease;
            min-height: 220px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1) !important;
        }
        
        .guarantee-icon {
            position: relative;
            width: 50px;
            height: 50px;
            margin: 0 auto 15px;
        }
        
        .guarantee-badge {
            position: absolute;
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, #6366f1, #8b5cf6);
            border-radius: 50%;
            z-index: 1;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .guarantee-check {
            position: absolute;
            font-size: 25px;
            color: white;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 2;
        }
        
        .guarantee-money {
            position: absolute;
            font-size: 20px;
            color white;
            top: 65%;
            left: 65%;
            transform: translate(-50%, -50%);
            z-index: 3;
        }
        
        .delivery-time {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 20px;
            color: #4f46e5;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="max-w-4xl mx-auto bg-white/90 rounded-2xl overflow-hidden shadow-2xl relative card-bg">
        <!-- Colorful background dots -->
        <div class="color-dots">
            <div class="color-dot bg-indigo-400 w-60 h-60 top-10 -left-20"></div>
            <div class="color-dot bg-purple-400 w-80 h-80 -bottom-20 -right-20"></div>
            <div class="color-dot bg-pink-400 w-40 h-40 top-1/2 left-1/4"></div>
        </div>
        
        <!-- Header -->
        <header class="gradient-bg text-white p-8 text-center relative z-10">
            <div class="flex justify-center mb-6">
                <div class="logo-container">
                    <div class="logo-symbol">
                        <div class="logo-base"></div>
                        <div class="logo-globe">
                            <i class="fas fa-globe"></i>
                        </div>
                        <div class="logo-w">W</div>
                        <div class="logo-ring"></div>
                        <div class="logo-dots">
                            <div class="logo-dot"></div>
                            <div class="logo-dot"></div>
                            <div class="logo-dot"></div>
                            <div class="logo-dot"></div>
                        </div>
                    </div>
                </div>
            </div>
            <h1 class="text-5xl font-extrabold mb-2 text-white">WEBESSENCE</h1>
            <div class="w-24 h-1 bg-white/80 mx-auto my-4 rounded-full"></div>
            <h2 class="text-2xl md:text-3xl font-semibold text-white/90 mb-4">VOTRE SITE WEB PROFESSIONNEL EN 48H</h2>
        </header>
        
        <!-- Main Content -->
        <main class="p-8 md:p-12 relative z-10">
            <h2 class="text-3xl font-bold text-center mb-4 section-title gradient-text">CRÉATION DE SITE WEB SUR MESURE</h2>
            
            <section class="flex flex-col md:flex-row items-center mb-10">
                <div class="md:w-1/2 mb-8 md:mb-0 md:pr-8">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Votre site web clé en main</h3>
                    <ul class="space-y-4 text-gray-700">
                        <li class="flex items-start bg-white/50 p-3 rounded-lg shadow-sm">
                            <div class="w-8 h-8 rounded-full bg-indigo-500 flex items-center justify-center text-white mr-3">
                                <i class="fas fa-check text-sm"></i>
                            </div>
                            <span class="font-medium">Sites vitrines professionnels</span>
                        </li>
                        <li class="flex items-start bg-white/50 p-3 rounded-lg shadow-sm">
                            <div class="w-8 h-8 rounded-full bg-purple-500 flex items-center justify-center text-white mr-3">
                                <i class="fas fa-check text-sm"></i>
                            </div>
                            <span class="font-medium">Sites complets pour commerçants, restaurants et artisans</span>
                        </li>
                        <li class="flex items-start bg-white/50 p-3 rounded-lg shadow-sm">
                            <div class="w-8 h-8 rounded-full bg-pink-500 flex items-center justify-center text-white mr-3">
                                <i class="fas fa-check text-sm"></i>
                            </div>
                            <span class="font-medium">Solutions pour entreprises de services</span>
                        </li>
                        <li class="flex items-start bg-white/50 p-3 rounded-lg shadow-sm">
                            <div class="w-8 h-8 rounded-full bg-blue-400 flex items-center justify-center text-white mr-3">
                                <i class="fas fa-check text-sm"></i>
                            </div>
                            <span class="font-medium">Design moderne et responsive</span>
                        </li>
                        <li class="flex items-start bg-white/50 p-3 rounded-lg shadow-sm">
                            <div class="w-8 h-8 rounded-full bg-purple-400 flex items-center justify-center text-white mr-3">
                                <i class="fas fa-check text-sm"></i>
                            </div>
                            <span class="font-medium">Optimisé pour le référencement</span>
                        </li>
                    </ul>
                </div>
                
                <div class="md:w-1/2 relative">
                    <div class="bg-gradient-to-br from-indigo-50 to-purple-50 p-6 rounded-xl shadow-lg floating gradient-border">
                        <div class="flex items-center mb-4">
                            <div class="w-14 h-14 gradient-bg rounded-full flex items-center justify-center text-white mr-4 shadow-lg">
                                <i class="fas fa-bolt text-2xl"></i>
                            </div>
                            <h4 class="text-2xl font-bold text-gray-800">Délai express</h4>
                        </div>
                        <p class="text-gray-700 mb-4 text-lg">Livraison en <span class="font-bold gradient-text">24h à 48h</span> selon la complexité de votre projet.</p>
                        <div class="bg-white p-4 rounded-lg border border-gray-200 shadow-sm">
                            <p class="text-gray-700 text-center font-medium">Nous comprenons l'urgence d'avoir une présence en ligne rapide et efficace pour votre activité.</p>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Features -->
            <section>
                <h2 class="text-3xl font-bold text-center mb-10 section-title gradient-text">NOS GARANTIES</h2>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-10">
                    <div class="bg-gradient-to-br from-indigo-50 to-purple-50 p-6 rounded-xl gradient-border shadow-lg feature-card">
                        <div class="w-16 h-16 gradient-bg rounded-full flex items-center justify-center text-white mb-4 mx-auto shadow-lg">
                            <i class="fas fa-mobile-alt text-2xl"></i>
                        </div>
                        <h4 class="text-center font-bold text-gray-800 mb-2 text-xl">Responsive Design</h4>
                        <p class="text-center text-gray-600">Adapté à tous les appareils : mobile, tablette et ordinateur</p>
                    </div>
                    
                    <div class="bg-gradient-to-br from-purple-50 to-pink-50 p-6 rounded-xl gradient-border shadow-lg feature-card">
                        <div class="w-16 h-16 gradient-bg rounded-full flex items-center justify-center text-white mb-4 mx-auto shadow-lg">
                            <i class="fas fa-chart-line text-2xl"></i>
                        </div>
                        <h4 class="text-center font-bold text-gray-800 mb-2 text-xl">SEO Optimisé</h4>
                        <p class="text-center text-gray-600">Meilleure visibilité sur les moteurs de recherche</p>
                    </div>
                    
                    <div class="bg-gradient-to-br from-pink-50 to-blue-50 p-6 rounded-xl gradient-border shadow-lg feature-card">
                        <div class="guarantee-icon">
                            <div class="guarantee-badge"></div>
                            <div class="guarantee-check">
                                <i class="fas fa-check"></i>
                            </div>
                            <div class="guarantee-money">
                                <i class="fas fa-euro-sign"></i>
                            </div>
                        </div>
                        <h4 class="text-center font-bold text-gray-800 mb-2 text-xl">Satisfait ou remboursé</h4>
                        <p class="text-center text-gray-600">7 jours pour valider votre satisfaction</p>
                    </div>
                </div>
            </section>
            
            <!-- CTA -->
            <section class="gradient-bg rounded-xl p-8 text-center pulse-animation shadow-lg">
                <h3 class="text-2xl font-bold text-white mb-4">PRÊT À BOOSTER VOTRE PRÉSENCE EN LIGNE ?</h3>
                <p class="text-white/90 mb-6 text-lg">Contactez-nous dès maintenant pour discuter de votre projet</p>
                <a href="mailto:contact.webessence@gmail.com" class="inline-block bg-white text-transparent bg-clip-text font-bold py-4 px-10 rounded-full hover:bg-gray-100 transition duration-300 gradient-border text-xl">
                    <i class="fas fa-globe mr-2"></i> DEMANDER UN DEVIS
                </a>
            </section>
        </main>
        
        <!-- Footer -->
        <footer class="bg-gray-100/80 p-6 text-center relative z-10">
            <div class="mb-4">
                <a href="mailto:contact.webessence@gmail.com" class="inline-block bg-white/90 hover:bg-white transition duration-300 text-gray-800 font-medium py-3 px-6 rounded-full shadow-md">
                    <i class="fas fa-envelope mr-2"></i> CONTACTEZ-NOUS
                </a>
            </div>
            <p class="text-gray-600">© 2025 <span class="font-bold gradient-text">WEBESSENCE</span> - Création de sites web sur mesure</p>
            <p class="text-gray-500 text-sm mt-2">Tous droits réservés</p>
        </footer>
    </div>
</body>
</html>
