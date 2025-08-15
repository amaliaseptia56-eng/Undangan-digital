# Undangan-digital
UndanganDigitalRianRini
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Undangan Pernikahan Digital</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            overflow: hidden;
        }
        .slide {
            height: 100vh;
            width: 100vw;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            scroll-snap-align: start;
            background-size: cover;
            background-position: center;
        }
        .carousel {
            scroll-snap-type: y mandatory;
            overflow-y: scroll;
            height: 100vh;
        }
        .hidden {
            display: none;
        }
        #music-control {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 100;
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Music Control -->
    <div id="music-control" class="bg-white p-3 rounded-full shadow-lg">
        <button id="playBtn" onclick="toggleMusic()" class="bg-black text-white rounded-full w-10 h-10 flex items-center justify-center">
            ♫
        </button>
        <!-- Audio can be changed by replacing URL below -->
        <audio id="bgMusic" loop>
            <source src="[URL_LAGU_ANDA.mp3]" type="audio/mpeg">
        </audio>
    </div>

    <!-- Carousel Slides -->
    <div class="carousel">
        <!-- Slide 1: Cover -->
        <div class="slide" style="background-image: url('[URL_BACKGROUND_SLIDE_1]');">
            <div class="text-center">
                <h1 class="text-4xl md:text-6xl font-bold mb-4">The Wedding Of</h1>
                <div id="Rian & Rini" class="text-4xl md:text-5xl font-bold mb-8">[Rian Hardiansyah] & [Amalia septiarini]</div>
                <div class="text-xl mb-12">Kepada Yth: <span id="guestName">Bapak/Ibu/Saudara/i</span></div>
                <button onclick="scrollToNext()" class="bg-black text-white px-6 py-2 rounded-full animate-bounce mt-8">Buka Undangan</button>
            </div>
        </div>

        <!-- Slide 2: Verse -->
        <div class="slide" style="background-image: url('https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/6471b091-6aa5-40d8-bf0e-c2fe329f0397.png');">
            <div class="text-center">
                <h2 class="text-3xl md:text-4xl font-bold mb-12">Rian & Amalia</h2>
                <div id="verseText" class="text-xl md:text-2xl text-gray-700 mb-12 leading-relaxed">
                    "[Ayat Al-Quran/Q.S. Ar-Rum:21]"
                </div>
                <button onclick="scrollToNext()" class="bg-black text-white px-6 py-2 rounded-full">Lanjut</button>
            </div>
        </div>

        <!-- Slide 3: Couple -->
        <div class="slide" style="background-image: url('https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/753fc73c-3a0b-4bfe-b835-afaad4bf7efd.png');">
            <div class="flex flex-col md:flex-row items-center justify-center p-8">
                <div class="md:w-1/2 mb-8 md:mb-0 md:pr-8">
                    <img id="couplePhoto" src="[URL_FOTO_PENGANTIN]" alt="Foto pasangan pengantin" class="w-full h-auto max-h-96 md:max-h-full object-cover rounded-lg shadow-lg">
                </div>
                <div class="md:w-1/2 text-center md:text-left">
                    <h2 class="text-3xl md:text-4xl font-bold mb-8">John & Jane</h2>
                    <div class="mb-8">
                        <h3 class="text-xl font-semibold mb-2">Mempelai Pria</h3>
                        <div id="groomName" class="text-2xl mb-1">Rian Hardiansyah</div>
                        <div id="groomParents" class="text-gray-600">Putra dari Bpk. Sugeng Widodo & Ibu Sulasmi</div>
                    </div>
                    <div class="mb-8">
                        <h3 class="text-xl font-semibold mb-2">Mempelai Wanita</h3>
                        <div id="brideName" class="text-2xl mb-1">Amalia Septiarini</div>
                        <div id="brideParents" class="text-gray-600">Putri dari Bpk. Kliwon & Ibu Murniati</div>
                    </div>
                    <button onclick="scrollToNext()" class="bg-black text-white px-6 py-2 rounded-full">Lanjut</button>
                </div>
            </div>
        </div>

        <!-- Slide 4: Event -->
        <div class="slide" style="background-image: url('https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/b3badb4b-6c93-402f-8772-c2cc12ec7d41.png');">
            <div class="text-center max-w-3xl">
                <h2 class="text-3xl md:text-4xl font-bold mb-12">Acara Pernikahan</h2>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
                    <div class="bg-gray-50 p-6 rounded-lg">
                        <h3 class="text-2xl font-bold mb-4">Akad Nikah</h3>
                        <div id="akadDetails" class="text-lg space-y-2">
                            <p>📅 Sabtu, 24 Juni 2023</p>
                            <p>⏰ 08.00 - 10.00 WIB</p>
                            <p>📍 Gedung Serbaguna</p>
                            <p>🏠 Jl. Contoh No. 123, Jakarta</p>
                        </div>
                    </div>
                    <div class="bg-gray-50 p-6 rounded-lg">
                        <h3 class="text-2xl font-bold mb-4">Resepsi</h3>
                        <div id="receptionDetails" class="text-lg space-y-2">
                            <p>📅 Sabtu, 24 Juni 2023</p>
                            <p>⏰ 11.00 - 14.00 WIB</p>
                            <p>📍 Gedung Serbaguna</p>
                            <p>🏠 Jl. Contoh No. 123, Jakarta</p>
                            <p>🎶 Live Music</p>
                        </div>
                    </div>
                </div>
                <button onclick="scrollToNext()" class="bg-black text-white px-6 py-2 rounded-full">Lanjut</button>
            </div>
        </div>

        <!-- Slide 5: Gift -->
        <div class="slide" style="background-image: url('https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/53b86328-c6de-44a4-a136-242b0af9a686.png');">
            <div class="text-center max-w-2xl">
                <h2 class="text-3xl md:text-4xl font-bold mb-12">Konfirmasi & Hadiah</h2>
                <div class="bg-white p-6 rounded-lg shadow-sm mb-8">
                    <h3 class="text-2xl font-bold mb-4">Kirim Hadiah</h3>
                    <div id="giftInfo" class="text-lg space-y-3 mb-6">
                        <p>Untuk yang ingin memberikan hadiah:</p>
                        <div class="bg-gray-50 p-4 rounded-lg">
                            <p>💳 Transfer Bank</p>
                            <p>BCA: 1234567890</p>
                            <p>a.n. John Doe</p>
                        </div>
                        <div class="bg-gray-50 p-4 rounded-lg">
                            <p>📱 E-Wallet</p>
                            <p>DANA/OVO: 08123456789</p>
                            <p>a.n. Jane Smith</p>
                        </div>
                    </div>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-sm mb-8">
                    <h3 class="text-2xl font-bold mb-4">Ucapan & Doa</h3>
                    <textarea id="guestMessage" class="w-full p-4 border rounded-lg mb-4" rows="4" placeholder="Tulis ucapan dan doa untuk mempelai..."></textarea>
                    <button onclick="sendWishes()" class="bg-black text-white px-6 py-2 rounded-full">Kirim Ucapan</button>
                </div>
                <div class="text-center mt-8">
                    <p class="text-xl mb-4">Terima kasih atas doa dan kehadirannya</p>
                    <p class="text-2xl">Rian & Amalia</p>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Global variables
        let currentSlide = 0;

        // Initialize
        document.addEventListener('DOMContentLoaded', function() {
            updateActiveSlide();
        });

        // Navigation functions
        function scrollToNext() {
            currentSlide = (currentSlide + 1) % 5; // 5 slides
            updateActiveSlide();
        }

        function updateActiveSlide() {
            const slides = document.querySelectorAll('.slide');
            slides.forEach((slide, index) => {
                slide.style.transform = `translateY(-${currentSlide * 100}vh)`;
            });
        }

        // Music control
        function toggleMusic() {
            const music = document.getElementById('bgMusic');
            const btn = document.getElementById('playBtn');

            if (music.paused) {
                music.play();
                btn.innerHTML = '❚❚';
            } else {
                music.pause();
                btn.innerHTML = '♫';
            }
        }

        // Send wishes
        function sendWishes() {
            const message = document.getElementById('guestMessage').value;
            if (message.trim() !== '') {
                alert('Terima kasih atas ucapan dan doanya! Pesan Anda: ' + message);
                document.getElementById('guestMessage').value = '';
                // In a real app, you would send this to a server
            } else {
                alert('Silakan tulis ucapan terlebih dahulu');
            }
        }
    </script>
</body>
</html>
