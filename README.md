<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Will You Be My Girlfriend? 💖</title>
  <style>
    :root {
      --bg1: #fff7fb;
      --bg2: #ffe4f1;
      --pink: #ff5fa2;
      --pink-dark: #e8488d;
      --soft-pink: #ffd3e6;
      --cream: #fffdf8;
      --text: #5d3552;
      --text-soft: #8b5c78;
      --white: #ffffff;
      --shadow: 0 16px 40px rgba(255, 95, 162, 0.18);
      --radius-xl: 28px;
      --radius-lg: 20px;
      --radius-md: 14px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      color: var(--text);
      background:
        radial-gradient(circle at top left, rgba(255,255,255,0.92), rgba(255,255,255,0) 30%),
        radial-gradient(circle at right, rgba(255,195,224,0.45), rgba(255,255,255,0) 35%),
        linear-gradient(135deg, var(--bg1), var(--bg2));
      min-height: 100vh;
      overflow-x: hidden;
      position: relative;
    }

    .floating-hearts {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 0;
      overflow: hidden;
    }

    .heart {
      position: absolute;
      bottom: -40px;
      font-size: 18px;
      opacity: 0.35;
      animation: floatUp linear infinite;
      filter: drop-shadow(0 6px 10px rgba(255,95,162,0.12));
    }

    @keyframes floatUp {
      0% {
        transform: translateY(0) translateX(0) rotate(0deg);
        opacity: 0;
      }
      12% {
        opacity: 0.45;
      }
      100% {
        transform: translateY(-110vh) translateX(40px) rotate(15deg);
        opacity: 0;
      }
    }

    .container {
      position: relative;
      z-index: 1;
      width: min(1100px, calc(100% - 32px));
      margin: 0 auto;
    }

    .hero {
      min-height: 100vh;
      display: grid;
      place-items: center;
      padding: 48px 0 24px;
    }

    .hero-card {
      background: rgba(255, 255, 255, 0.75);
      backdrop-filter: blur(12px);
      border: 1px solid rgba(255, 255, 255, 0.85);
      box-shadow: var(--shadow);
      border-radius: 34px;
      padding: 34px;
      width: 100%;
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap: 28px;
      align-items: center;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 10px 16px;
      background: rgba(255, 95, 162, 0.12);
      border: 1px solid rgba(255, 95, 162, 0.14);
      color: var(--pink-dark);
      border-radius: 999px;
      font-size: 0.95rem;
      font-weight: 700;
      margin-bottom: 18px;
    }

    .hero h1 {
      font-size: clamp(2.2rem, 4vw, 4.2rem);
      line-height: 1.05;
      margin-bottom: 16px;
    }

    .hero h1 .cute {
      color: var(--pink);
      text-shadow: 0 8px 18px rgba(255,95,162,0.15);
    }

    .hero p {
      font-size: 1.08rem;
      color: var(--text-soft);
      line-height: 1.8;
      max-width: 600px;
      margin-bottom: 24px;
    }

    .cta-row {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
      margin-bottom: 18px;
    }

    .btn {
      appearance: none;
      border: none;
      outline: none;
      cursor: pointer;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      min-height: 52px;
      padding: 0 22px;
      border-radius: 999px;
      font-weight: 700;
      transition: transform 0.2s ease, box-shadow 0.2s ease, opacity 0.2s ease;
    }

    .btn:hover {
      transform: translateY(-2px);
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--pink), #ff86b9);
      color: white;
      box-shadow: 0 16px 24px rgba(255,95,162,0.22);
    }

    .btn-secondary {
      background: var(--white);
      color: var(--pink-dark);
      border: 1px solid rgba(255, 95, 162, 0.18);
      box-shadow: 0 10px 20px rgba(255,95,162,0.08);
    }

    .tiny-note {
      font-size: 0.95rem;
      color: var(--text-soft);
    }

    .visual-wrap {
      position: relative;
      min-height: 420px;
      display: grid;
      place-items: center;
    }

    .main-bubble {
      width: min(380px, 100%);
      aspect-ratio: 1 / 1;
      background: linear-gradient(145deg, rgba(255,255,255,0.95), rgba(255,231,241,0.9));
      border-radius: 32px;
      box-shadow: var(--shadow);
      border: 1px solid rgba(255,255,255,0.85);
      display: grid;
      place-items: center;
      text-align: center;
      padding: 30px;
      position: relative;
      overflow: hidden;
    }

    .main-bubble::before,
    .main-bubble::after {
      content: "";
      position: absolute;
      border-radius: 50%;
      background: rgba(255, 123, 178, 0.12);
      z-index: 0;
    }

    .main-bubble::before {
      width: 160px;
      height: 160px;
      top: -40px;
      right: -30px;
    }

    .main-bubble::after {
      width: 120px;
      height: 120px;
      bottom: -25px;
      left: -20px;
    }

    .bubble-content {
      position: relative;
      z-index: 1;
    }

    .emoji-big {
      font-size: 4.5rem;
      display: block;
      margin-bottom: 14px;
      animation: pulse 1.8s infinite ease-in-out;
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.08); }
    }

    .bubble-title {
      font-size: 1.5rem;
      font-weight: 800;
      color: var(--pink-dark);
      margin-bottom: 10px;
    }

    .bubble-text {
      line-height: 1.7;
      color: var(--text-soft);
    }

    .mini-card {
      position: absolute;
      background: rgba(255,255,255,0.92);
      border: 1px solid rgba(255,255,255,0.85);
      box-shadow: 0 14px 28px rgba(255,95,162,0.13);
      border-radius: 20px;
      padding: 14px 16px;
      font-size: 0.95rem;
      font-weight: 700;
      color: var(--pink-dark);
    }

    .mini-card.one {
      top: 24px;
      left: 0;
      transform: rotate(-8deg);
    }

    .mini-card.two {
      right: 6px;
      bottom: 30px;
      transform: rotate(8deg);
    }

    .mini-card.three {
      right: 10px;
      top: 28px;
      transform: rotate(-4deg);
    }

    section {
      padding: 30px 0 60px;
    }

    .section-card {
      background: rgba(255,255,255,0.78);
      border: 1px solid rgba(255,255,255,0.88);
      border-radius: 32px;
      box-shadow: var(--shadow);
      padding: 30px;
    }

    .section-head {
      text-align: center;
      margin-bottom: 28px;
    }

    .section-head h2 {
      font-size: clamp(1.6rem, 3vw, 2.5rem);
      color: var(--pink-dark);
      margin-bottom: 10px;
    }

    .section-head p {
      color: var(--text-soft);
      max-width: 700px;
      margin: 0 auto;
      line-height: 1.8;
    }

    .form-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 16px;
    }

    .field {
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    .field.full {
      grid-column: 1 / -1;
    }

    label {
      font-weight: 700;
      color: var(--text);
    }

    input,
    textarea,
    select {
      width: 100%;
      border: 1.5px solid rgba(255,95,162,0.18);
      background: rgba(255,255,255,0.92);
      border-radius: 16px;
      padding: 14px 16px;
      font-size: 1rem;
      color: var(--text);
      outline: none;
      transition: border-color 0.2s ease, box-shadow 0.2s ease;
    }

    input:focus,
    textarea:focus,
    select:focus {
      border-color: rgba(255,95,162,0.6);
      box-shadow: 0 0 0 4px rgba(255,95,162,0.08);
    }

    textarea {
      resize: vertical;
      min-height: 110px;
    }

    .helper {
      font-size: 0.9rem;
      color: var(--text-soft);
    }

    .form-actions {
      display: flex;
      justify-content: center;
      margin-top: 20px;
    }

    .reveal-wrap {
      display: none;
      margin-top: 26px;
      animation: fadeUp 0.5s ease;
    }

    .reveal-wrap.show {
      display: block;
    }

    @keyframes fadeUp {
      from {
        opacity: 0;
        transform: translateY(16px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .love-letter {
      background: linear-gradient(180deg, rgba(255,255,255,0.96), rgba(255,240,247,0.96));
      border: 1px solid rgba(255,95,162,0.18);
      border-radius: 28px;
      padding: 28px;
      box-shadow: 0 18px 36px rgba(255,95,162,0.14);
      position: relative;
      overflow: hidden;
    }

    .love-letter::before {
      content: "💌";
      position: absolute;
      top: 16px;
      right: 18px;
      font-size: 2.1rem;
      opacity: 0.18;
    }

    .letter-tag {
      display: inline-block;
      padding: 8px 14px;
      border-radius: 999px;
      background: rgba(255,95,162,0.1);
      color: var(--pink-dark);
      font-weight: 700;
      margin-bottom: 14px;
    }

    .letter-title {
      font-size: clamp(1.5rem, 3vw, 2.4rem);
      color: var(--pink-dark);
      margin-bottom: 14px;
      font-weight: 900;
    }

    .letter-body {
      line-height: 1.95;
      color: var(--text);
      margin-bottom: 24px;
      font-size: 1.03rem;
      white-space: pre-line;
    }

    .answer-box {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
      align-items: center;
    }

    .btn-yes {
      background: linear-gradient(135deg, #ff5fa2, #ff7db6);
      color: white;
      min-width: 200px;
      box-shadow: 0 16px 24px rgba(255,95,162,0.24);
    }

    .btn-maybe {
      background: white;
      color: var(--pink-dark);
      border: 1px solid rgba(255,95,162,0.2);
      min-width: 160px;
      position: relative;
    }

    .result-card {
      display: none;
      margin-top: 18px;
      padding: 18px 20px;
      border-radius: 20px;
      background: rgba(255,95,162,0.08);
      border: 1px dashed rgba(255,95,162,0.28);
      color: var(--pink-dark);
      font-weight: 700;
      line-height: 1.7;
    }

    .result-card.show {
      display: block;
    }

    .moments {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 18px;
      margin-top: 10px;
    }

    .moment-card {
      background: rgba(255,255,255,0.88);
      border: 1px solid rgba(255,255,255,0.9);
      border-radius: 24px;
      padding: 22px;
      box-shadow: 0 14px 24px rgba(255,95,162,0.1);
    }

    .moment-icon {
      font-size: 2rem;
      margin-bottom: 12px;
    }

    .moment-title {
      font-size: 1.15rem;
      color: var(--pink-dark);
      font-weight: 800;
      margin-bottom: 8px;
    }

    .moment-text {
      color: var(--text-soft);
      line-height: 1.75;
      font-size: 0.98rem;
    }

    .footer {
      text-align: center;
      padding: 20px 0 40px;
      color: var(--text-soft);
      font-size: 0.95rem;
    }

    .footer strong {
      color: var(--pink-dark);
    }

    .music-toggle {
      position: fixed;
      right: 18px;
      bottom: 18px;
      z-index: 5;
      width: 58px;
      height: 58px;
      border-radius: 50%;
      border: none;
      background: linear-gradient(135deg, var(--pink), #ff7bb5);
      color: white;
      font-size: 1.3rem;
      cursor: pointer;
      box-shadow: 0 14px 24px rgba(255,95,162,0.28);
      transition: transform 0.2s ease;
    }

    .music-toggle:hover {
      transform: scale(1.06);
    }

    .credit-note {
      margin-top: 16px;
      font-size: 0.88rem;
      color: var(--text-soft);
      text-align: center;
    }

    @media (max-width: 920px) {
      .hero-card {
        grid-template-columns: 1fr;
      }

      .visual-wrap {
        min-height: auto;
      }

      .moments {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 700px) {
      .hero-card,
      .section-card {
        padding: 22px;
        border-radius: 24px;
      }

      .form-grid {
        grid-template-columns: 1fr;
      }

      .answer-box {
        flex-direction: column;
        align-items: stretch;
      }

      .btn-yes,
      .btn-maybe {
        width: 100%;
      }

      .mini-card {
        display: none;
      }
    }
  </style>
</head>
<body>
  <div class="floating-hearts" id="floatingHearts"></div>

  <button class="music-toggle" id="musicToggle" aria-label="Toggle music">🎵</button>

  <main>
    <section class="hero">
      <div class="container">
        <div class="hero-card">
          <div>
            <div class="badge">🌷 Website Nembak Pacar Imut</div>
            <h1>
              Hai kamu yang <span class="cute">manis banget</span>,
              ada sesuatu yang pengin aku bilang... 💗
            </h1>
            <p>
              Ini bukan website biasa. Ini website spesial buat satu cewek spesial.
              Ada form daftar kecil dulu, terus di bawah ada pesan rahasia yang isinya
              perasaan manis dan pertanyaan paling penting hari ini.
            </p>

            <div class="cta-row">
              <a href="#daftar" class="btn btn-primary">Mulai dari sini 💌</a>
              <a href="#kenapa-kamu" class="btn btn-secondary">Lihat dulu alasannya ✨</a>
            </div>

            <div class="tiny-note">
              Tip: ganti nama, username IG, dan isi pesannya sesuai cerita kalian yaa.
            </div>
          </div>

          <div class="visual-wrap">
            <div class="main-bubble">
              <div class="bubble-content">
                <span class="emoji-big">🐻💞🐰</span>
                <div class="bubble-title">Special page for special girl</div>
                <div class="bubble-text">
                  Dibuat dengan rasa deg-degan, niat, dan sedikit overthinking lucu.
                </div>
              </div>
            </div>
            <div class="mini-card one">manis + lucu = kamu</div>
            <div class="mini-card two">klik “iya” nanti ya 😳</div>
            <div class="mini-card three">100% dibuat spesial</div>
          </div>
        </div>
      </div>
    </section>

    <section id="kenapa-kamu">
      <div class="container">
        <div class="section-card">
          <div class="section-head">
            <h2>Kenapa harus kamu? 💖</h2>
            <p>
              Karena dari sekian banyak orang, ada satu orang yang bikin hari biasa jadi terasa lebih hangat.
              Kamu mungkin nggak sadar, tapi senyum kamu itu berisik di hati aku.
            </p>
          </div>

          <div class="moments">
            <article class="moment-card">
              <div class="moment-icon">🌸</div>
              <div class="moment-title">Bikin nyaman</div>
              <div class="moment-text">
                Cara kamu ngobrol, bercanda, dan jadi diri sendiri itu bikin aku ngerasa tenang banget.
              </div>
            </article>

            <article class="moment-card">
              <div class="moment-icon">✨</div>
              <div class="moment-title">Bikin hari seru</div>
              <div class="moment-text">
                Hal kecil pun jadi menyenangkan kalau ada kamu. Bahkan chat sederhana bisa bikin senyum sendiri.
              </div>
            </article>

            <article class="moment-card">
              <div class="moment-icon">💗</div>
              <div class="moment-title">Bikin yakin</div>
              <div class="moment-text">
                Aku nggak cari yang sempurna. Aku cuma merasa, versi nyaman dan tulus itu ada di kamu.
              </div>
            </article>
          </div>
        </div>
      </div>
    </section>

    <section id="daftar">
      <div class="container">
        <div class="section-card">
          <div class="section-head">
            <h2>Daftar Dulu, Cantik 🌷</h2>
            <p>
              Biar makin personal, isi dulu form kecil ini. Ada kolom akun Instagram juga biar makin berasa dibuat khusus.
            </p>
          </div>

          <form id="loveForm">
            <div class="form-grid">
              <div class="field">
                <label for="namaCewek">Nama kamu</label>
                <input type="text" id="namaCewek" placeholder="Contoh: Aisyah" required />
              </div>

              <div class="field">
                <label for="igCewek">Akun Instagram</label>
                <input type="text" id="igCewek" placeholder="Contoh: @aisyahmanis" required />
              </div>

              <div class="field">
                <label for="namaKamu">Nama aku</label>
                <input type="text" id="namaKamu" placeholder="Contoh: Fajar" required />
              </div>

              <div class="field">
                <label for="panggilan">Panggilan sayang</label>
                <input type="text" id="panggilan" placeholder="Contoh: cantik, bub, ayang" />
              </div>

              <div class="field full">
                <label for="pesanCustom">Pesan manis tambahan</label>
                <textarea id="pesanCustom" placeholder="Contoh: Aku suka cara kamu ketawa, cara kamu perhatian, dan cara kamu bikin aku nyaman..."></textarea>
                <div class="helper">Kosongkan kalau mau pakai teks default.</div>
              </div>
            </div>

            <div class="form-actions">
              <button type="submit" class="btn btn-primary">Buka pesan rahasia 💌</button>
            </div>
          </form>

          <div class="reveal-wrap" id="revealWrap">
            <div class="love-letter">
              <div class="letter-tag">Pesan spesial buat <span id="targetNama">kamu</span> ✨</div>
              <div class="letter-title">Aku mau bilang sesuatu yang penting...</div>
              <div class="letter-body" id="letterBody"></div>

              <div class="answer-box">
                <button class="btn btn-yes" id="yesBtn" type="button">Iya, aku mau jadi pacarmu 💞</button>
                <button class="btn btn-maybe" id="maybeBtn" type="button">Malu jawab 🙈</button>
              </div>

              <div class="result-card" id="resultCard"></div>
            </div>

            <div class="credit-note">
              Akun IG yang didaftarkan: <strong id="showIg">@username</strong>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <div class="footer">
    Dibuat dengan rasa sayang, effort, dan sedikit gemetar oleh <strong id="footerName">seseorang yang lagi jatuh hati</strong> 💗
  </div>

  <audio id="bgMusic" loop>
    <source src="" type="audio/mpeg" />
  </audio>

  <script>
    const heartsContainer = document.getElementById('floatingHearts');
    const loveForm = document.getElementById('loveForm');
    const revealWrap = document.getElementById('revealWrap');
    const targetNama = document.getElementById('targetNama');
    const letterBody = document.getElementById('letterBody');
    const showIg = document.getElementById('showIg');
    const footerName = document.getElementById('footerName');
    const yesBtn = document.getElementById('yesBtn');
    const maybeBtn = document.getElementById('maybeBtn');
    const resultCard = document.getElementById('resultCard');
    const musicToggle = document.getElementById('musicToggle');
    const bgMusic = document.getElementById('bgMusic');

    function createHeart() {
      const heart = document.createElement('div');
      const icons = ['💗', '💕', '💖', '💘', '🌸', '✨'];
      heart.className = 'heart';
      heart.textContent = icons[Math.floor(Math.random() * icons.length)];
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (8 + Math.random() * 8) + 's';
      heart.style.fontSize = (16 + Math.random() * 16) + 'px';
      heartsContainer.appendChild(heart);
      setTimeout(() => heart.remove(), 17000);
    }

    setInterval(createHeart, 700);
    for (let i = 0; i < 16; i++) {
      setTimeout(createHeart, i * 250);
    }

    loveForm.addEventListener('submit', function (e) {
      e.preventDefault();

      const namaCewek = document.getElementById('namaCewek').value.trim();
      const igCewek = document.getElementById('igCewek').value.trim();
      const namaKamu = document.getElementById('namaKamu').value.trim();
      const panggilan = document.getElementById('panggilan').value.trim();
      const pesanCustom = document.getElementById('pesanCustom').value.trim();

      const sapaan = panggilan ? panggilan : namaCewek;

      const defaultMessage = `Hai ${sapaan},\n\nAku bikin halaman ini khusus buat kamu karena aku pengin nyampein sesuatu dengan cara yang manis dan beda dari biasanya. Jujur, aku nyaman banget sama kamu. Kehadiran kamu bikin hari-hari aku terasa lebih seru, lebih hangat, dan entah kenapa selalu bikin aku pengin ngobrol lebih lama.\n\nAku suka cara kamu jadi diri sendiri. Aku suka hal-hal kecil tentang kamu yang mungkin kelihatannya sederhana, tapi buat aku itu berkesan. Dan dari semua rasa nyaman itu, aku sadar... aku nggak cuma suka ngobrol sama kamu. Aku suka kamu.\n\nJadi hari ini aku mau tanya, dengan versi paling tulus dari hati aku:\n\nMau nggak kamu jadi pacar aku? 💖\n\n- ${namaKamu}`;

      const customMessage = `Hai ${sapaan},\n\n${pesanCustom}\n\nJadi... setelah semua rasa nyaman ini, aku cuma mau bilang satu hal yang paling jujur dari hati aku:\n\nMau nggak kamu jadi pacar aku? 💖\n\n- ${namaKamu}`;

      targetNama.textContent = namaCewek;
      showIg.textContent = igCewek;
      footerName.textContent = namaKamu;
      letterBody.textContent = pesanCustom ? customMessage : defaultMessage;

      revealWrap.classList.add('show');
      revealWrap.scrollIntoView({ behavior: 'smooth', block: 'start' });

      localStorage.setItem('proposalData', JSON.stringify({
        namaCewek,
        igCewek,
        namaKamu,
        panggilan,
        pesanCustom
      }));
    });

    yesBtn.addEventListener('click', function () {
      resultCard.classList.add('show');
      resultCard.innerHTML = 'YAYYY 🥹💞<br>Jawaban kamu bikin aku senyum sendiri. Makasih udah mau nerima perasaan aku. Mulai sekarang, semoga kita bisa sama-sama bikin banyak cerita manis yaa ✨';
      burstHearts();
    });

    function moveMaybeButton() {
      const isMobile = window.innerWidth < 700;
      if (isMobile) {
        maybeBtn.textContent = 'Masih malu yaa? 🙈';
        resultCard.classList.add('show');
        resultCard.innerHTML = 'Gapapa kalau masih malu jawab 😆 Tapi aku bakal tetap nunggu jawaban manis dari kamu yaa 💗';
        return;
      }

      const parent = maybeBtn.parentElement;
      const maxX = Math.max(0, parent.clientWidth - maybeBtn.offsetWidth - 10);
      const randomX = Math.floor(Math.random() * maxX);
      maybeBtn.style.transform = `translateX(${randomX}px)`;
      maybeBtn.textContent = 'eh jangan yang ini 😝';
    }

    maybeBtn.addEventListener('mouseenter', moveMaybeButton);
    maybeBtn.addEventListener('click', moveMaybeButton);

    function burstHearts() {
      for (let i = 0; i < 30; i++) {
        setTimeout(createHeart, i * 100);
      }
    }

    let musicOn = false;
    musicToggle.addEventListener('click', () => {
      musicOn = !musicOn;
      musicToggle.textContent = musicOn ? '🔇' : '🎵';
      if (musicOn) {
        musicToggle.title = 'Matikan musik';
      } else {
        musicToggle.title = 'Nyalakan musik';
      }
    });

    window.addEventListener('DOMContentLoaded', () => {
      const saved = localStorage.getItem('proposalData');
      if (!saved) return;

      try {
        const data = JSON.parse(saved);
        document.getElementById('namaCewek').value = data.namaCewek || '';
        document.getElementById('igCewek').value = data.igCewek || '';
        document.getElementById('namaKamu').value = data.namaKamu || '';
        document.getElementById('panggilan').value = data.panggilan || '';
        document.getElementById('pesanCustom').value = data.pesanCustom || '';
      } catch (err) {
        console.error('Gagal membaca data lokal:', err);
      }
    });
  </script>
</body>
</html>
