<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GathannErlangga</title>
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to bottom, #1c1c1c, #383838);
            color: #f5f5f5;
            overflow-x: hidden;
        }
        header {
            background-color: #222;
            color: #fff;
            padding: 20px 40px;
            text-align: center;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        header h1 {
            margin: 0;
            font-size: 32px;
            font-weight: 600;
        }
        .hero {
            height: 100vh;
            background: url('https://images.wallpapersden.com/image/download/dark-natural-landscape-hd-black-aesthetic_bmZmbGuUmZqaraWkpJRnamtorWZpaGs.jpg') no-repeat center center/cover;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #fff;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7);
        }
        .hero h2 {
            font-size: 56px;
            margin: 0;
            animation: glowText 2s infinite alternate;
        }
        @keyframes glowText {
            from {
                text-shadow: 0 0 10px #fff, 0 0 20px #ff00ff, 0 0 30px #ff00ff;
            }
            to {
                text-shadow: 0 0 20px #00ffff, 0 0 30px #00ffff, 0 0 40px #00ffff;
            }
        }
        .ErlaaNEWS {
            padding: 60px 20px;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin-top: 80px;
        }
        .ErlaaNEWS-item {
            width: 300px;
            height: 200px;
            background: #444;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transform: scale(1);
            transition: transform 0.5s, box-shadow 0.5s;
        }
        .ErlaaNEWS-item:hover {
            transform: scale(1.1);
            box-shadow: 0 8px 16px rgba(255, 255, 255, 0.3);
        }
        .ErlaaNEWS-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        footer {
            background-color: #222;
            color: #fff;
            text-align: center;
            padding: 20px;
            position: relative;
            bottom: 0;
            width: 100%;
            margin-top: 40px;
        }
        footer p {
            margin: 0;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <header>
        <h1>ErlaaNEWS</h1>
    </header>

    <section class="hero">
        <h2>Selamat Datang di ErlaaNEWS</h2>
    </section>

    <section class="ErlaaNEWS">
        <div class="ErlaaNEWS-item">
            <img src="https://pict.sindonews.net/webp/360/salsabila/video/2024/12/20/6/112037/menkomdigi-meutya-hafid-angkat-bicara-terkait-pemeriksaan-budi-arie-di-bareskrim-wyr.webp" alt="Proyek 1">
        </div>
        <div class="ErlaaNEWS-item">
            <img src="https://asset-2.tstatic.net/tribunnews/foto/bank/images2/PDIP-siaga-1-menyusul-munculnya-sejumlah-baliho-dan-spanduk.jpg" alt="Proyek 2">
        </div>
        <div class="ErlaaNEWS-item">
            <img src="https://i1.ytimg.com/vi/pLvv8v2fd3c/hqdefault.jpg" alt="Proyek 3">
        </div>
        <div class="ErlaaNEWS-item">
            <img src="https://asset-2.tstatic.net/tribunnews/foto/bank/images2/Budi-Said-mengklaim-dirinya-merupakan-korban-penipuan-penjualan-emas.jpg" alt="Proyek 4">
        </div>
        <div class="ErlaaNEWS-item">
            <img src="https://statik.tempo.co/data/2024/12/20/id_1363770/1363770_720.jpg" alt="Proyek 5">
        </div>
    </section>

    <footer>
        <p>&copy; 2024 ErlaaNEWS. Semua Hak Dilindungi.</p>
    </footer>

    <script>
        // Animasi teks berganti pada hero
        document.addEventListener('DOMContentLoaded', () => {
            const heroText = document.querySelector('.hero h2');
            const texts = ["Selamat Datang di ErlaaNEWS", "Scroll Ke Bawah ", "Siapa Tau Ada Berita Yang Menarik"];
            let index = 0;

            setInterval(() => {
                heroText.textContent = texts[index];
                index = (index + 1) % texts.length;
            }, 3000);
        });

        // Interaksi hover pada elemen ErlaaNEWS
        document.querySelectorAll('.ErlaaNEWS-item').forEach(item => {
            item.addEventListener('mouseover', () => {
                item.style.transform = "rotate(5deg) scale(1.1)";
                item.style.transition = "transform 0.5s";
            });
            item.addEventListener('mouseout', () => {
                item.style.transform = "rotate(0deg) scale(1)";
            });
        });

        // Scroll animasi untuk menampilkan ErlaaNEWS
        const portfolioItems = document.querySelectorAll('.ErlaaNEWS-item');
        const observer = new IntersectionObserver(entries => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = "translateY(0)";
                    observer.unobserve(entry.target);
                }
            });
        }, { threshold: 0.2 });

        ErlaaNEWSItems.forEach(item => {
            item.style.opacity = 0;
            item.style.transform = "translateY(50px)";
            item.style.transition = "opacity 0.5s, transform 0.5s";
            observer.observe(item);
        });
    </script>
</body>
</html>
