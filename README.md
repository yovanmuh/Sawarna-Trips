<!DOCTYPE html>
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

        /* --- WADAH FOTO KEBERSAMAAN --- */
        .bike-animation-container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 180px;
            margin-top: 1rem;
            position: relative;
        }

        .couple-photo {
            width: 160px;
            height: 160px;
            object-fit: cover;
            border-radius: 50%;
            border: 3px solid #ffffff;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
            animation: floatEffect 3s infinite ease-in-out;
        }
       <!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sawarna Trip — Special Journey</title>
  
  <!-- Font Google untuk kesan estetis & elegan -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,600;1,400&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

  <style>
    :root {
      --primary-color: #8e7dbe;
      --text-dark: #2c3e50;
      --bg-gradient: linear-gradient(135deg, #f0eff8 0%, #e5e9f0 100%);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: var(--bg-gradient);
      color: var(--text-dark);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }

    .hero-card {
      background: rgba(255, 255, 255, 0.65);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      border: 1px solid rgba(255, 255, 255, 0.8);
      border-radius: 28px;
      padding: 40px 28px;
      text-align: center;
      max-width: 500px;
      width: 100%;
      box-shadow: 0 20px 50px rgba(142, 125, 190, 0.12);
    }

    .tagline {
      font-family: 'Playfair Display', serif;
      font-style: italic;
      font-size: 1.1rem;
      color: var(--primary-color);
      margin-bottom: 8px;
    }

    .main-title {
      font-family: 'Playfair Display', serif;
      font-size: 2.2rem;
      color: var(--text-dark);
      margin-bottom: 24px;
      letter-spacing: 0.5px;
    }

    /* Grid Countdown */
    .timer-grid {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 10px;
      margin-top: 10px;
    }

    .time-box {
      background: #ffffff;
      padding: 14px 12px;
      border-radius: 18px;
      flex: 1;
      max-width: 80px;
      box-shadow: 0 10px 20px rgba(142, 125, 190, 0.08);
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .time-number {
      font-size: 1.8rem;
      font-weight: 600;
      color: var(--text-dark);
      line-height: 1.1;
    }

    .time-label {
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: #95a5a6;
      margin-top: 6px;
    }

    .time-separator {
      font-size: 1.4rem;
      font-weight: 400;
      color: var(--primary-color);
      margin-bottom: 16px;
    }

    .footer-note {
      margin-top: 28px;
      font-size: 0.88rem;
      color: #7f8c8d;
      line-height: 1.5;
    }
  </style>
</head>
    
<body>

    <!-- Header Banner dengan Gambar Pilihan Sendiri -->
    <header>
        <h1>Itinerary Ke Sawarna</h1>
        <p>Tak peduli seberapa jauh jalannya, asal tujuannya bersamamu, aku pasti bahagia❤️</p>
        
        <!-- Wadah Foto Profil -->
            <img src="motor.png" alt="Foto Tanjung Layar" class="couple-photo">
        </div>
    </header>
