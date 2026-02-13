<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi San Valentín</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&family=Quicksand:wght@300;500&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: 'Quicksand', sans-serif;
            /* Fondo con imagen de tulipanes rosas */
            background-image: linear-gradient(rgba(255, 192, 203, 0.4), rgba(255, 192, 203, 0.4)), 
                              url('https://images.unsplash.com/photo-1526047932273-341f2a7631f9?q=80&w=1480&auto=format&fit=crop');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            min-height: 100vh;
        }

        .glass-panel {
            background: rgba(255, 255, 255, 0.7);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.3);
            border-radius: 20px;
        }

        .gradient-text {
            background: linear-gradient(45deg, #ff4d6d, #ff85a1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-family: 'Dancing Script', cursive;
        }

        .editable-area:focus {
            outline: none;
            border-bottom: 2px dashed #ff4d6d;
        }

        .photo-frame {
            transition: transform 0.3s ease;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .photo-frame:hover {
            transform: rotate(2deg) scale(1.05);
        }

        /* Difuminados en los bordes */
        .edge-glow {
            box-shadow: 0 0 50px rgba(255, 182, 193, 0.6);
        }
    </style>
</head>
<body class="flex items-center justify-center p-4">

    <div class="max-w-6xl w-full grid grid-cols-1 md:grid-cols-4 gap-8 items-center">
        
        <!-- Lateral Izquierdo: Fotos -->
        <div class="flex flex-col gap-6 order-2 md:order-1">
            <div class="photo-frame bg-white p-2 rounded-lg edge-glow">
                <img src="img/arbol.jpeg" 
                     alt="Amor 1" class="rounded w-full h-48 object-cover">
                <p class="text-center text-pink-500 mt-2 text-sm italic">Te quiero Mucho</p>
            </div>
            <div class="photo-frame bg-white p-2 rounded-lg edge-glow">
                <img src="img/I.jpeg" 
                     alt="Amor 2" class="rounded w-full h-48 object-cover">
                <p class="text-center text-pink-500 mt-2 text-sm italic">Mi amor</p>
            </div>
        </div>

        <!-- Centro: Texto Editable -->
        <div class="md:col-span-2 order-1 md:order-2">
            <div class="glass-panel p-8 md:p-12 text-center shadow-2xl">
                <h1 class="text-5xl md:text-6xl mb-6 gradient-text">¡Feliz San Valentín!</h1>
                
                <div class="space-y-4 text-gray-700 leading-relaxed text-lg">
                    <p class="editable-area" contenteditable="true">
                        Para mi niña hermosa, cada día a tu lado es un regalo que atesoro. Eres la luz que ilumina mi vida y el motivo de mi sonrisa. En este día especial, quiero recordarte lo mucho que te amo y lo agradecido que estoy por tenerte en mi vida.
                    </p>
                    <p class="editable-area" contenteditable="true">
                        Eres la persona más especial en mi vida. Gracias por cada sonrisa y por cada momento compartido. Unque no sea por una pantalla por el momento te quiero mucho y gracias por estar en mi vida.
                    </p>
                    <p class="editable-area font-bold text-pink-600" contenteditable="true">
                        Con todo mi amor, Yojan
                    </p>
                </div>

                <div class="mt-8 flex justify-center gap-4">
                    <span class="text-pink-400 text-3xl animate-bounce">❤️</span>
                    <span class="text-pink-400 text-3xl animate-bounce" style="animation-delay: 0.2s">🌸</span>
                    <span class="text-pink-400 text-3xl animate-bounce" style="animation-delay: 0.4s">❤️</span>
                </div>
            </div>
        </div>

        <!-- Lateral Derecho: Fotos -->
        <div class="flex flex-col gap-6 order-3">
            <div class="photo-frame bg-white p-2 rounded-lg edge-glow">
                <img src="img/M.jpeg" 
                     alt="Amor 3" class="rounded w-full h-48 object-cover">
                <p class="text-center text-pink-500 mt-2 text-sm italic">Te amo</p>
            </div>
            <div class="photo-frame bg-white p-2 rounded-lg edge-glow">
                <img src="img/Ñ.jpeg" 
                     alt="Amor 4" class="rounded w-full h-48 object-cover">
                <p class="text-center text-pink-500 mt-2 text-sm italic">Tú y yo</p>
            </div>
        </div>

    </div>

    <!-- Música de fondo (opcional/decorativo) -->
    <div class="fixed bottom-4 right-4 bg-white/50 backdrop-blur rounded-full p-3 shadow-lg">
        <button onclick="toggleMusic()" class="text-pink-600">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19V6l12-3v13M9 19c0 1.105-1.343 2-3 2s-3-.895-3-2 1.343-2 3-2 3 .895 3 2zm12-3c0 1.105-1.343 2-3 2s-3-.895-3-2 1.343-2 3-2 3 .895 3 2zM9 10l12-3" />
            </svg>
        </button>
    </div>

    <script>
        function toggleMusic() {
            // Aquí podrías añadir lógica para reproducir un audio
            console.log("Música activada/desactivada");
        }
    </script>
</body>
</html>
