<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Itinerary Liburan Sawarna (Slow Morning Fit)</title>
    <style>
        /* --- RESET & VARIABLE UTAMA --- */
        :root {
            --bg-main: #f8fafc;
            --text-main: #1e293b;
            --text-muted: #64748b;
            --accent-h1: #2563eb;
            --accent-h2: #0d9488;
            --accent-h3: #d97706;
            --card-bg: #ffffff;
            --border-color: #e2e8f0;
            --shadow-sm: 0 1px 3px rgba(0,0,0,0.05), 0 1px 2px rgba(0,0,0,0.03);
            --shadow-md: 0 4px 6px -1px rgba(0,0,0,0.05), 0 2px 4px -1px rgba(0,0,0,0.03);
            --transition-fast: all 0.2s ease;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: var(--bg-main);
            color: var(--text-main);
            line-height: 1.6;
            padding-bottom: 4rem;
        }

        /* --- HEADER --- */
        header {
            background: linear-gradient(135deg, #1e3a8a 0%, #0d9488 100%);
            color: #ffffff;
            padding: 3rem 1.5rem 2rem 1.5rem;
            text-align: center;
            position: relative;
            box-shadow: var(--shadow-md);
            margin-bottom: 2rem;
            overflow: hidden;
        }

        header h1 {
            font-size: 2.25rem;
            font-weight: 800;
            letter-spacing: -0.025em;
            margin-bottom: 0.5rem;
            animation: fadeInDown 0.6s ease-out;
        }

        header p {
            color: #ccfbf1;
            font-size: 1rem;
            font-weight: 500;
            animation: fadeInUp 0.6s ease-out 0.2s both;
            margin-bottom: 1.5rem;
        }

        /* --- WADAH FOTO/GIF MOTOR PILIHAN SENDIRI --- */
        .bike-animation-container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 80px;
            margin-top: 1.5rem;
            position: relative;
        }

        /* --- CONTAINER UTAMA --- */
        main {
            max-width: 800px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        /* --- CARD SEKSI HARI --- */
        .day-section {
            background-color: var(--card-bg);
            border-radius: 1rem;
            border: 1px solid var(--border-color);
            box-shadow: var(--shadow-sm);
            margin-bottom: 2.5rem;
            overflow: hidden;
            transition: var(--transition-fast);
        }

        .day-section:hover {
            box-shadow: var(--shadow-md);
            transform: translateY(-2px);
        }

        .day-header {
            padding: 1.25rem 1.5rem;
            color: #ffffff;
            font-size: 1.25rem;
            font-weight: 700;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .day-1 .day-header { background: linear-gradient(90deg, #2563eb, #3b82f6); }
        .day-2 .day-header { background: linear-gradient(90deg, #0d9488, #14b8a6); }
        .day-3 .day-header { background: linear-gradient(90deg, #d97706, #f59e0b); }

        .day-badge {
            background-color: rgba(255, 255, 255, 0.2);
            padding: 0.25rem 0.75rem;
            border-radius: 9999px;
            font-size: 0.75rem;
            font-weight: 600;
            letter-spacing: 0.05em;
        }

        /* --- TIMELINE CONTAINER --- */
        .timeline {
            padding: 1.5rem;
            position: relative;
        }

        .timeline::before {
            content: '';
            position: absolute;
            top: 1.5rem;
            bottom: 1.5rem;
            left: 2.25rem;
            width: 2px;
        }

        .day-1 .timeline::before { background-color: #dbeafe; }
        .day-2 .timeline::before { background-color: #ccfbf1; }
        .day-3 .timeline::before { background-color: #fef3c7; }

        /* --- TIMELINE ITEM / ROW --- */
        .timeline-item {
            position: relative;
            padding-left: 3.5rem;
            margin-bottom: 2rem;
            cursor: pointer;
            user-select: none;
        }

        .timeline-item:last-child {
            margin-bottom: 0;
        }

        .timeline-node {
            position: absolute;
            left: 1.75rem;
            top: 0.25rem;
            width: 1rem;
            height: 1rem;
            border-radius: 50%;
            background-color: #ffffff;
            border: 3px solid var(--border-color);
            transform: translateX(-50%);
            transition: var(--transition-fast);
            z-index: 2;
        }

        .day-1 .timeline-item:hover .timeline-node { border-color: #2563eb; background-color: #2563eb; }
        .day-2 .timeline-item:hover .timeline-node { border-color: #0d9488; background-color: #0d9488; }
        .day-3 .timeline-item:hover .timeline-node { border-color: #d97706; background-color: #d97706; }

        .time-badge {
            display: inline-block;
            font-size: 0.75rem;
            font-weight: 700;
            background-color: #f1f5f9;
            color: var(--text-main);
            padding: 0.15rem 0.5rem;
            border-radius: 4px;
            margin-bottom: 0.25rem;
            transition: var(--transition-fast);
        }

        .activity-title {
            font-size: 1rem;
            font-weight: 600;
            color: #0f172a;
            margin-bottom: 0.15rem;
            transition: var(--transition-fast);
        }

        .activity-desc {
            font-size: 0.875rem;
            color: var(--text-muted);
            transition: var(--transition-fast);
        }

        /* --- STATE DONE --- */
        .timeline-item.done .timeline-node {
            background-color: #10b981 !important;
            border-color: #10b981 !important;
            transform: scale(1.2) translateX(-40%);
        }

        .timeline-item.done .time-badge {
            background-color: #d1fae5;
            color: #065f46;
        }

        .timeline-item.done .activity-title {
            color: var(--text-muted);
            text-decoration: line-through;
        }

        .timeline-item.done .activity-desc {
            color: #cbd5e1;
            text-decoration: line-through;
        }

        /* --- FOOTER --- */
        footer {
            text-align: center;
            padding: 2rem 1rem;
            font-size: 0.75rem;
            color: var(--text-muted);
            border-top: 1px solid var(--border-color);
            margin-top: 4rem;
            background-color: #ffffff;
        }

        /* --- ANIMASI KEYFRAMES --- */
        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes rideEffect {
            0%, 100% { transform: translateY(0) translateX(-8px); }
            50% { transform: translateY(-4px) translateX(8px); }
        }

        /* --- RESPONSIF LAYAR --- */
        @media (max-width: 640px) {
            header { padding: 2rem 1rem 1.5rem 1rem; }
            header h1 { font-size: 1.75rem; }
            .timeline { padding: 1.25rem 1rem; }
            .timeline::before { left: 1.5rem; }
            .timeline-item { padding-left: 2.5rem; }
            .timeline-node { left: 1.05rem; }
        }
    </style>
</head>
<body>

    <!-- Header Banner dengan Gambar/GIF Pilihan Sendiri -->
    <header>
        <h1>Itinerary Ke Sawarna</h1>
        <p>Gunakan halaman ini sebagai panduan interaktif selama perjalanan motor Anda</p>
        
        <!-- Wadah Animasi Motor -->
        <div class="bike-animation-container">
            <img src="motor.gif" alt="Motor Nyata" style="height: 70px; animation: rideEffect 2.5s infinite ease-in-out;">
        </div>
    </header>

    <!-- Konten Utama -->
    <main>

        <!-- HARI 1 -->
        <section class="day-section day-1">
            <div class="day-header">
                <h2>Hari 1: Karang Bokor & Ikon Tanjung Layar</h2>
                <span class="day-badge">EKSPLORASI</span>
            </div>
            <div class="timeline">
                
                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">05.00 – 09.30</div>
                    <div class="activity-title">Berangkat Motoran</div>
                    <div class="activity-desc">Jalur Serang – Pandeglang – Gunung Kencana – Malingping – Bayah – Sawarna.</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">09.30 – 11.30</div>
                    <div class="activity-title">Masuk dan Wisata di Karang Bokor Sawarna</div>
                    <div class="activity-desc">(Foto di jembatan tebing).</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">11.30 – 12.30</div>
                    <div class="activity-title">Makan Siang</div>
                    <div class="activity-desc">Di area luar/sekitar Sawarna.</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">12.30 – 13.00</div>
                    <div class="activity-title">Menuju Penginapan Pertama</div>
                    <div class="activity-desc">(Area Ciantir/Tanjung Layar), check-in, mandi, dan istirahat.</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">15.30 – 18.00</div>
                    <div class="activity-title">Ke Pantai Tanjung Layar</div>
                    <div class="activity-desc">(Berjalan kaki/motor ke area karang saat air surut untuk foto berdua & menikmati sunset).</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">19.00 – Selesai</div>
                    <div class="activity-title">Makan Malam & Istirahat Total</div>
                    <div class="activity-desc">Di sekitar penginapan.</div>
                </div>

            </div>
        </section>

        <!-- HARI 2 -->
        <section class="day-section day-2">
            <div class="day-header">
                <h2>Hari 2: Karang Taraje & Pindah Cabin Legon Pari</h2>
                <span class="day-badge">PINDAH SPOT</span>
            </div>
            <div class="timeline">

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">05.30 – 06.00</div>
                    <div class="activity-title">Bangun Pagi dan Bersiap</div>
                    <div class="activity-desc">Persiapan agenda pagi hari.</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">06.00 – 08.00</div>
                    <div class="activity-title">Berkendara ke Pantai Karang Taraje</div>
                    <div class="activity-desc">(Melihat ombak air terjun karang saat pagi).</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">08.00 – 09.30</div>
                    <div class="activity-title">"Slow Morning" & Ngopi</div>
                    <div class="activity-desc">Menikmati pagi yang santai di teras penginapan pertama sembari menyeduh kopi/teh sachet bawaan sendiri dan menyortir foto-foto kemarin.</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">10.00 – 11.30</div>
                    <div class="activity-title">Kembali ke Penginapan Pertama</div>
                    <div class="activity-desc">Bersiap, packing, dan check-out.</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">11.30 – 12.30</div>
                    <div class="activity-title">Perjalanan dan Check-in</div>
                    <div class="activity-desc">Menuju ke Cabin Legon Pari.</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">12.30 – 15.30</div>
                    <div class="activity-title">Makan Siang dan Istirahat Siang</div>
                    <div class="activity-desc">Di area Legon Pari.</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">16.00 – 18.00</div>
                    <div class="activity-title">Menuju Pantai Ciantir</div>
                    <div class="activity-desc">Untuk menikmati sunset terakhir di hamparan pasir putih yang luas.</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">18.30 – Selesai</div>
                    <div class="activity-title">Kembali ke Legon Pari</div>
                    <div class="activity-desc">Makan malam dan istirahat.</div>
                </div>

            </div>
        </section>

        <!-- HARI 3 -->
        <section class="day-section day-3">
            <div class="day-header">
                <h2>Hari ke 3: Sunrise Legon Pari & Pulang</h2>
                <span class="day-badge">RUTE PULANG</span>
            </div>
            <div class="timeline">

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">05.00 – 07.00</div>
                    <div class="activity-title">Pantai Legon Pari</div>
                    <div class="activity-desc">(Cukup jalan kaki dari cabin untuk mengejar sunrise dan menikmati pantai teluk yang tenang).</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">07.30 – 09.00</div>
                    <div class="activity-title">Sarapan dan Mandi</div>
                    <div class="activity-desc">Persiapan sebelum check-out.</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">09.00 – 11.00</div>
                    <div class="activity-title">Aktivitas Opsional</div>
                    <div class="activity-desc">Jalan kaki ke area Karang Warna (sebelah Legon Pari) untuk foto-foto tambahan, atau sekadar bersantai di depan cabin.</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">11.00 – 12.00</div>
                    <div class="activity-title">Packing dan Check-out</div>
                    <div class="activity-desc">Meninggalkan Cabin Legon Pari.</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">12.00 – 13.00</div>
                    <div class="activity-title">Makan Siang</div>
                    <div class="activity-desc">Dilakukan sebelum memulai perjalanan jauh.</div>
                </div>

                <div class="timeline-item" onclick="toggleTask(this)">
                    <div class="timeline-node"></div>
                    <div class="time-badge">13.00 – 17.30</div>
                    <div class="activity-title">Perjalanan Naik Motor Kembali ke Serang</div>
                    <div class="activity-desc">(Lebih aman jalan siang agar melewati jalur Gunung Kencana/Pandeglang sebelum gelap).</div>
                </div>

            </div>
        </section>

    </main>

    <!-- Footer Peta Panduan -->
    <footer>
        <p>Tip: Ketuk pada baris kegiatan untuk menandai jadwal yang sudah selesai dilakukan.</p>
        <p style="margin-top: 0.5rem; color: #94a3b8;">© 2026 Sawarna Road Trip Guide • Clean Responsive Design</p>
    </footer>

    <!-- --- JAVASCRIPT INTERNAL --- -->
    <script>
        function toggleTask(element) {
            element.classList.toggle('done');
        }
    </script>
</body>
</html>
