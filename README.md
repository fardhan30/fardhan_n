# fardhan_n
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Profil Lucu dengan Animasi & Teks Berjalan</title>
  <style>
    :root {
      --blue-light: #b3e5fc;
      --blue-dark: #0288d1;
      --orange: #ff6f00;
      --white: #fff;
      --text-color: #333;
      --bg-color: #e0f7fa;
    }

    * {
      margin: 0; padding: 0; box-sizing: border-box;
      font-family: 'Comic Sans MS', cursive, sans-serif;
    }

    body {
      background: var(--bg-color);
      color: var(--text-color);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 2rem;
      flex-direction: column;
      gap: 1.5rem;
    }

    /* Teks berjalan */
    .marquee-container {
      width: 100%;
      max-width: 400px;
      overflow: hidden;
      border: 2px solid var(--blue-light);
      background-color: #d0f0ff;
      border-radius: 15px;
      box-shadow: 0 4px 8px rgba(3,169,244,0.3);
      padding: 0.6rem 0;
    }

    .marquee-text {
      display: inline-block;
      white-space: nowrap;
      padding-left: 100%;
      animation: marquee 12s linear infinite;
      font-size: 1.2rem;
      color: var(--blue-dark);
      font-weight: bold;
    }

    @keyframes marquee {
      0% { transform: translateX(0); }
      100% { transform: translateX(-100%); }
    }

    /* Profil card */
    .profile-card {
      background: var(--white);
      border-radius: 20px;
      max-width: 400px;
      width: 100%;
      padding: 2rem;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
      text-align: center;
      animation: slideIn 1s ease forwards;
    }

    @keyframes slideIn {
      from { opacity: 0; transform: translateY(40px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .profile-pic {
      width: 160px;
      height: 160px;
      border-radius: 50%;
      margin: 0 auto 1.5rem;
      border: 5px solid var(--blue-light);
      overflow: hidden;
      animation: pulse 2.5s infinite;
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); box-shadow: 0 0 0 0 rgba(3,169,244, 0.7);}
      50% { transform: scale(1.05); box-shadow: 0 0 15px 10px rgba(3,169,244, 0.3);}
    }

    .profile-pic img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    h1 {
      color: var(--blue-dark);
      font-size: 2.5rem;
      margin-bottom: 1rem;
      opacity: 0;
      animation: slideUp 0.8s ease forwards;
      animation-delay: 1s;
    }

    @keyframes slideUp {
      to { opacity: 1; transform: translateY(0); }
      from { opacity: 0; transform: translateY(20px); }
    }

    p.bio {
      font-size: 1.1rem;
      margin-bottom: 1.8rem;
      color: #555;
      line-height: 1.5;
    }

    .hobbies {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin-bottom: 2rem;
    }

    .hobby {
      background: var(--orange);
      color: var(--white);
      padding: 0.5rem 1rem;
      border-radius: 50px;
      font-weight: bold;
      font-size: 0.95rem;
      opacity: 0;
      animation: fadeIn 0.6s forwards;
    }

    .hobby:nth-child(1) { animation-delay: 1.5s; }
    .hobby:nth-child(2) { animation-delay: 1.8s; }
    .hobby:nth-child(3) { animation-delay: 2.1s; }
    .hobby:nth-child(4) { animation-delay: 2.4s; }
    .hobby:nth-child(5) { animation-delay: 2.7s; }

    @keyframes fadeIn {
      to { opacity: 1; transform: translateY(0); }
      from { opacity: 0; transform: translateY(15px); }
    }

    .contacts {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .contact-btn {
      display: block;
      text-align: center;
      background: var(--blue-dark);
      color: var(--white);
      padding: 0.75rem;
      border-radius: 50px;
      font-size: 1.1rem;
      text-decoration: none;
      transition: background 0.3s ease;
    }

    .contact-btn:hover {
      background: var(--orange);
    }
  </style>
</head>
<body>

  <div class="marquee-container">
    <div class="marquee-text">🎉 Selamat datang di profil saya! Semoga harimu menyenangkan! 🐱✨</div>
  </div>

  <div class="profile-card">
    <div class="profile-pic">
      <img src="https://i.pinimg.com/originals/fc/33/08/fc3308e1c6892d6468dca5ae49b30126.jpg" alt="Kucing Gemas" />
    </div>

    <h1>Anggun Permata Sari D.</h1>
    <p class="bio">Pelajar SMA yang menyukai seni, teknologi, dan tentu saja kucing! Selalu bersemangat belajar hal baru dan berbagi kebaikan.</p>

    <div class="hobbies">
      <span class="hobby">Menggambar</span>
      <span class="hobby">Musik</span>
      <span class="hobby">Membaca</span>
      <span class="hobby">Badminton</span>
      <span class="hobby">Berenang</span>
    </div>

    <div class="contacts">
      <a class="contact-btn" href="tel:+6289673305966">📞 0896-7330-5966</a>
      <a class="contact-btn" href="mailto:anggunpermatasarid@gmail.com">✉ anggunpermatasarid@gmail.com</a>
      <a class="contact-btn" href="https://www.instagram.com/beries_03?igsh=djFuNjhubnR5NXZ0" target="_blank">📷 Instagram</a>
    </div>
  </div>

</body>
</html>
