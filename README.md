<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kopi Kenangan Senja - Coffee Shop</title>
    <style>
:root {
        --primary-color: #6f4e37;
        --secondary-color: #d7ccc8;
        --accent-color: #3e2723;
        --bg-color: #fdfbf7;
        --text-color: #4e342e;
    }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        header {
            background-color: var(--accent-color);
            color: white;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 1.5rem;
            font-weight: 500;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--secondary-color);
        }

        .hero {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1495474472287-4d71bcdd2085?auto=format&fit=crop&w=1200&q=80') no-repeat center center/cover;
            height: 70vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            padding: 0 1rem;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 0.5rem;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
        }

        .btn {
            background-color: var(--primary-color);
            color: white;
            padding: 0.75rem 1.5rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            text-decoration: none;
            transition: background 0.3s;
        }

        .btn:hover {
            background-color: var(--accent-color);
        }

        .container {
            max-width: 1100px;
            margin: 2rem auto;
            padding: 0 1rem;
        }

        section {
            padding: 3rem 0;
        }

        h2 {
            text-align: center;
            margin-bottom: 2rem;
            font-size: 2rem;
            color: var(--accent-color);
        }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .menu-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            text-align: center;
            padding-bottom: 1rem;
            transition: transform 0.3s;
        }

        .menu-card:hover {
            transform: translateY(-5px);
        }

        .menu-card img {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }

        .menu-card h3 {
            margin: 1rem 0 0.5rem;
        }

        .menu-card p {
            color: #777;
            font-size: 0.9rem;
            padding: 0 1rem;
            margin-bottom: 1rem;
        }

        .price {
            font-weight: bold;
            color: var(--primary-color);
            margin-bottom: 1rem;
            display: block;
        }

        /* Order Form Section */
        .order-section {
            background: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            max-width: 600px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 1.2rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 1rem;
        }

        footer {
            background-color: var(--accent-color);
            color: white;
            text-align: center;
            padding: 1.5rem;
            margin-top: 3rem;
        }
    </style>
</head>
<body>

    <!-- Header & Nav -->
    <header>
        <div class="logo">
            ☕ Kopi Senja
        </div>
        <nav>
            <a href="#home">Beranda</a>
            <a href="#menu">Menu</a>
            <a href="#order">Pesan Sekarang</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <h1>Nikmati Hari dengan Secangkir Kopi</h1>
        <p>
            Kopi pilihan berkualitas tinggi disajikan dengan penuh cinta setiap hari.
        </p>
        <a href="#order" class="btn">Pesan Sekarang</a>
    </section>

    <div class="container">
        <!-- Menu Section -->
        <section id="menu">
            <h2>Menu Favorit Kami</h2>
            <div class="menu-grid">
                <div class="menu-card">
                    <img src="https://images.unsplash.com/photo-1541167760496-1628856ab772?auto=format&fit=crop&w=500&q=80" alt="Espresso">
                    <h3>Caffè Latte</h3>
                    <p>
                        Perpaduan sempurna espresso kaya rasa dan susu蒸 yang lembut.
                    </p>
                    <span class="price">Rp 28.000</span>
                    <button class="btn" onclick="pilihMenu('Caffè Latte')">Pilih Menu</button>
                </div>
                <div class="menu-card">
                    <img src="https://images.unsplash.com/photo-1514432324607-a09d9b4aefdd?auto=format&fit=crop&w=500&q=80" alt="Cappuccino">
                    <h3>Cappuccino</h3>
                    <p>
                        Kombinasi klasik espresso, steamed milk, dan busa susu tebal di atasnya.
                    </p>
                    <span class="price">Rp 28.000</span>
                    <button class="btn" onclick="pilihMenu('Cappuccino')">Pilih Menu</button>
                </div>
                <div class="menu-card">
                    <img src="https://images.unsplash.com/photo-1517701550927-30cf4ba1dba5?auto=format&fit=crop&w=500&q=80" alt="Americano">
                    <h3>Americano</h3>
                    <p>
                        Espresso berkualitas dengan tambahan air panas untuk rasa yang bersih.
                    </p>
                    <span class="price">Rp 22.000</span>
                    <button class="btn" onclick="pilihMenu('Americano')">Pilih Menu</button>
                </div>
            </div>
        </section>

        <!-- Order Section -->
        <section id="order">
            <h2>Formulir Pemesanan</h2>
            <div class="order-section">
                <form id="orderForm" onsubmit="kirimPesanan(event)">
                    <div class="form-group">
                        <label for="nama">Nama Pemesan</label>
                        <input type="text" id="nama" required placeholder="Masukkan nama Anda">
                    </div>
                    <div class="form-group">
                        <label for="pilihanMenu">Pilihan Menu</label>
                        <select id="pilihanMenu" required>
                            <option value="">-- Pilih Menu --</option>
                            <option value="Caffè Latte">Caffè Latte - Rp 28.000</option>
                            <option value="Cappuccino">Cappuccino - Rp 28.000</option>
                            <option value="Americano">Americano - Rp 22.000</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="jumlah">Jumlah</label>
                        <input type="number" id="jumlah" min="1" value="1" required>
                    </div>
                    <div class="form-group">
                        <label for="catatan">Catatan Tambahan (Opsional)</label>
                        <textarea id="catatan" rows="3" placeholder="Contoh: Kurang manis, es sedikit"></textarea>
                    </div>
                    <button type="submit" class="btn" style="width: 100%;">Kirim Pesanan</button>
                </form>
            </div>
        </section>
    </div>

    <!-- Footer -->
    <footer>
        <p>
            &copy; 2026 Kopi Kenangan Senja. All Rights Reserved.
        </p>
    </footer>

    <!-- JavaScript Sederhana untuk Interaksi -->
    <script>
        function pilihMenu(namaMenu) {
            // Mengarahkan pilihan dropdown ke menu yang diklik
            const selectMenu = document.getElementById('pilihanMenu');
            selectMenu.value = namaMenu;

            // Gulir otomatis ke bagian formulir pemesanan
            document.getElementById('order').scrollIntoView({
                behavior: 'smooth'
            });
        }

        function kirimPesanan(event) {
            event.preventDefault();
            const nama = document.getElementById('nama').value;
            const menu = document.getElementById('pilihanMenu').value;
            const jumlah = document.getElementById('jumlah').value;

            alert(`Terima kasih, ${nama}! Pesanan ${jumlah} ${menu} Anda berhasil dikirim dan sedang diproses.`);
            document.getElementById('orderForm').reset();
        }
    </script>
</body>
</html>
