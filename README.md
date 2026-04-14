<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rangkuman Sejarah Indonesia</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Source+Serif+4:ital,wght@0,300;0,400;0,600;1,400&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #1a1209;
    --paper: #fdf6e3;
    --parchment: #f5e9c8;
    --gold: #c8902a;
    --gold-light: #e8b84b;
    --rust: #8b3a1a;
    --deep: #2c1a0e;
    --muted: #6b5533;
    --accent: #4a7c59;
    --accent2: #2d5a8e;
    --line: rgba(200,144,42,0.25);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--paper);
    color: var(--ink);
    font-family: 'Source Serif 4', Georgia, serif;
    font-size: 15px;
    line-height: 1.8;
    min-height: 100vh;
  }

  /* Decorative background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background:
      radial-gradient(ellipse at 10% 20%, rgba(200,144,42,0.06) 0%, transparent 50%),
      radial-gradient(ellipse at 90% 80%, rgba(139,58,26,0.05) 0%, transparent 50%);
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 860px;
    margin: 0 auto;
    padding: 40px 24px 80px;
    position: relative;
    z-index: 1;
  }

  /* HEADER */
  .hero {
    text-align: center;
    padding: 60px 20px 50px;
    border-bottom: 2px solid var(--gold);
    margin-bottom: 60px;
    position: relative;
  }
  .hero::before, .hero::after {
    content: '◆';
    color: var(--gold);
    font-size: 10px;
    position: absolute;
    bottom: -6px;
    left: 50%;
  }
  .hero::before { transform: translateX(-30px); }
  .hero::after  { transform: translateX(20px);  }

  .hero-kecil {
    font-family: 'Source Serif 4', serif;
    font-size: 11px;
    letter-spacing: 5px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 14px;
    font-weight: 600;
  }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.2rem, 6vw, 3.6rem);
    font-weight: 900;
    color: var(--deep);
    line-height: 1.15;
    margin-bottom: 18px;
  }
  .hero h1 span { color: var(--gold); }
  .hero-sub {
    font-size: 14px;
    color: var(--muted);
    font-style: italic;
    max-width: 500px;
    margin: 0 auto;
  }

  /* TIMELINE CONNECTOR */
  .timeline-track {
    position: relative;
    padding-left: 36px;
  }
  .timeline-track::before {
    content: '';
    position: absolute;
    left: 10px;
    top: 0;
    bottom: 0;
    width: 2px;
    background: linear-gradient(to bottom,
      transparent 0%,
      var(--gold) 5%,
      var(--gold) 95%,
      transparent 100%
    );
  }

  /* CHAPTER */
  .chapter {
    margin-bottom: 56px;
    position: relative;
    animation: fadeUp 0.5s ease both;
  }

  .chapter-dot {
    position: absolute;
    left: -30px;
    top: 8px;
    width: 18px;
    height: 18px;
    background: var(--paper);
    border: 2.5px solid var(--gold);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .chapter-dot::after {
    content: '';
    width: 7px;
    height: 7px;
    background: var(--gold);
    border-radius: 50%;
  }

  .chapter-header {
    display: flex;
    align-items: flex-start;
    gap: 14px;
    margin-bottom: 18px;
  }
  .chapter-num {
    font-family: 'Playfair Display', serif;
    font-size: 11px;
    font-weight: 700;
    color: var(--paper);
    background: var(--gold);
    padding: 3px 9px;
    border-radius: 3px;
    letter-spacing: 1px;
    white-space: nowrap;
    margin-top: 4px;
  }
  .chapter-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.35rem;
    font-weight: 700;
    color: var(--deep);
    line-height: 1.3;
  }
  .chapter-era {
    font-size: 11px;
    color: var(--gold);
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-top: 2px;
  }

  .chapter-body {
    background: var(--parchment);
    border-left: 3px solid var(--gold-light);
    border-radius: 0 8px 8px 0;
    padding: 20px 22px;
  }

  .chapter-body p {
    color: #3a2a14;
    margin-bottom: 10px;
    font-size: 14.5px;
  }
  .chapter-body p:last-child { margin-bottom: 0; }

  /* Highlight box */
  .highlight {
    background: rgba(200,144,42,0.12);
    border: 1px solid rgba(200,144,42,0.35);
    border-radius: 6px;
    padding: 12px 16px;
    margin: 12px 0;
    font-size: 14px;
  }
  .highlight strong { color: var(--rust); }

  /* Mini table */
  .mini-table {
    width: 100%;
    border-collapse: collapse;
    margin: 12px 0;
    font-size: 13.5px;
  }
  .mini-table th {
    background: var(--gold);
    color: var(--paper);
    padding: 7px 12px;
    text-align: left;
    font-weight: 600;
    font-family: 'Playfair Display', serif;
  }
  .mini-table td {
    padding: 7px 12px;
    border-bottom: 1px solid rgba(200,144,42,0.2);
    vertical-align: top;
  }
  .mini-table tr:nth-child(even) td { background: rgba(255,255,255,0.4); }
  .mini-table td strong { color: var(--rust); }

  /* Tag pills */
  .tags {
    display: flex;
    flex-wrap: wrap;
    gap: 7px;
    margin: 10px 0;
  }
  .tag {
    background: white;
    border: 1px solid var(--gold-light);
    color: var(--deep);
    padding: 3px 11px;
    border-radius: 20px;
    font-size: 12.5px;
    font-weight: 600;
  }
  .tag.green { border-color: var(--accent); color: var(--accent); }
  .tag.blue  { border-color: var(--accent2); color: var(--accent2); }
  .tag.red   { border-color: var(--rust); color: var(--rust); }

  /* Connection arrow between chapters */
  .bridge {
    display: flex;
    align-items: center;
    gap: 10px;
    margin: -30px 0 10px 0;
    padding-left: 0;
    font-size: 12px;
    color: var(--muted);
    font-style: italic;
  }
  .bridge::before {
    content: '↓';
    color: var(--gold);
    font-size: 16px;
    font-style: normal;
  }

  /* Divider */
  .ornament {
    text-align: center;
    color: var(--gold);
    font-size: 12px;
    letter-spacing: 8px;
    margin: 8px 0 20px;
    opacity: 0.6;
  }

  /* Section dividers */
  .section-label {
    font-size: 10px;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--muted);
    font-weight: 600;
    text-align: center;
    margin: 50px 0 30px;
    display: flex;
    align-items: center;
    gap: 14px;
  }
  .section-label::before, .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(to right, transparent, var(--gold), transparent);
  }

  /* Key figure box */
  .key-box {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(170px, 1fr));
    gap: 8px;
    margin: 12px 0;
  }
  .key-item {
    background: white;
    border-radius: 6px;
    padding: 10px 12px;
    border-top: 3px solid var(--gold);
    font-size: 13px;
  }
  .key-item .ki-title { font-weight: 700; color: var(--deep); font-size: 13px; }
  .key-item .ki-sub   { color: var(--muted); font-size: 12px; margin-top: 2px; }

  /* Footer */
  footer {
    text-align: center;
    margin-top: 70px;
    padding-top: 30px;
    border-top: 1px solid var(--line);
    color: var(--muted);
    font-size: 12px;
    font-style: italic;
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @media (max-width: 600px) {
    .timeline-track { padding-left: 26px; }
    .chapter-dot { left: -22px; width: 14px; height: 14px; }
    .mini-table { font-size: 12px; }
    .key-box { grid-template-columns: 1fr 1fr; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-kecil">Rangkuman Lengkap & Runtut</div>
    <h1>Sejarah <span>Indonesia</span></h1>
    <p class="hero-sub">Dari Masa Pra-Aksara hingga Era Reformasi — disusun secara kronologis dan berkesinambungan</p>
  </div>

  <!-- TIMELINE -->
  <div class="timeline-track">

    <!-- ══════════════════ BAB 1 ══════════════════ -->
    <div class="chapter" style="animation-delay:0.05s">
      <div class="chapter-dot"></div>
      <div class="chapter-header">
        <div>
          <div class="chapter-num">BAB 1</div>
          <div class="chapter-era">Fondasi Ilmu</div>
        </div>
        <div>
          <div class="chapter-title">Konsep Dasar &amp; Metodologi Sejarah</div>
        </div>
      </div>
      <div class="chapter-body">
        <p>Sebelum mempelajari peristiwa sejarah, kita harus memahami <strong>cara berpikir sejarawan</strong>. Sejarah bukan sekadar hafalan, melainkan cara memahami mengapa sesuatu terjadi dan bagaimana peristiwa masa lalu membentuk masa kini.</p>

        <div class="highlight">
          <strong>5 Konsep Kunci:</strong><br>
          • <strong>Kronologis</strong> — Berpikir urut dari masa lalu ke masa kini<br>
          • <strong>Diakronik</strong> — Memanjang dalam waktu (menelusuri perkembangan suatu hal)<br>
          • <strong>Sinkronik</strong> — Melebar dalam ruang (mengkaji satu kurun waktu secara mendalam)<br>
          • <strong>Ruang &amp; Waktu</strong> — Di mana dan kapan peristiwa terjadi<br>
          • <strong>Perubahan &amp; Keberlanjutan</strong> — Ada yang berubah, ada yang bertahan lintas zaman
        </div>

        <p>Untuk meneliti sejarah, digunakan <strong>4 langkah metodologi</strong>: <em>Heuristik</em> (mengumpulkan sumber) → <em>Verifikasi</em> (menguji kebenaran) → <em>Interpretasi</em> (menafsirkan fakta) → <em>Historiografi</em> (penulisan sejarah). <strong>Sejarah Lokal</strong> mengkaji kejadian di tingkat daerah untuk memahami keunikan identitas suatu wilayah.</p>
      </div>
    </div>

    <div class="bridge">Dengan bekal cara berpikir ini, kita mulai perjalanan dari awal mula peradaban Indonesia…</div>

    <!-- ══════════════════ BAB 2 ══════════════════ -->
    <div class="chapter" style="animation-delay:0.1s">
      <div class="chapter-dot"></div>
      <div class="chapter-header">
        <div>
          <div class="chapter-num">BAB 2</div>
          <div class="chapter-era">± 2 Juta — 500 SM</div>
        </div>
        <div>
          <div class="chapter-title">Kehidupan Masyarakat Pra-Aksara</div>
        </div>
      </div>
      <div class="chapter-body">
        <p>Sebelum mengenal tulisan, manusia Nusantara hidup berpindah-pindah (nomaden), lalu secara bertahap menetap dan bercocok tanam. Periode ini terbagi menurut perkembangan teknologi:</p>

        <table class="mini-table">
          <tr><th>Zaman</th><th>Ciri Utama</th><th>Peninggalan</th></tr>
          <tr><td><strong>Paleolitikum</strong></td><td>Berburu & meramu, nomaden</td><td>Kapak perimbas, kapak genggam</td></tr>
          <tr><td><strong>Mesolitikum</strong></td><td>Mulai menetap di gua</td><td>Kjokkenmodding (tumpukan kerang), lukisan gua</td></tr>
          <tr><td><strong>Neolitikum</strong></td><td>Bercocok tanam, membuat gerabah</td><td>Beliung persegi, kapak lonjong, gerabah</td></tr>
          <tr><td><strong>Megalitikum</strong></td><td>Kepercayaan animisme-dinamisme</td><td>Menhir, dolmen, sarkofagus, punden berundak</td></tr>
          <tr><td><strong>Zaman Logam</strong></td><td>Teknologi perunggu & besi</td><td>Nekara, kapak corong, bejana perunggu</td></tr>
        </table>

        <p>Nilai penting dari masa ini: <strong>gotong royong, kepercayaan spiritual, dan kemampuan beradaptasi</strong> — nilai-nilai yang terus diwariskan hingga Indonesia modern.</p>
      </div>
    </div>

    <div class="bridge">Kemampuan berlayar membuka kontak dengan India, membawa pengaruh besar yang mengubah wajah Nusantara…</div>

    <!-- ══════════════════ BAB 3 ══════════════════ -->
    <div class="chapter" style="animation-delay:0.15s">
      <div class="chapter-dot"></div>
      <div class="chapter-header">
        <div>
          <div class="chapter-num">BAB 3</div>
          <div class="chapter-era">Abad 1 — 15 M</div>
        </div>
        <div>
          <div class="chapter-title">Era Hindu-Buddha: Lahirnya Kerajaan-Kerajaan Besar</div>
        </div>
      </div>
      <div class="chapter-body">
        <p>Masuknya pengaruh Hindu-Buddha dari India melahirkan sistem kerajaan, tulisan, seni arsitektur, dan sastra di Nusantara. Ada 4 teori cara masuknya:</p>

        <div class="tags">
          <span class="tag">🏛 Brahmana — Pendeta diundang raja</span>
          <span class="tag">⚔️ Ksatria — Prajurit mendirikan kerajaan</span>
          <span class="tag">🛒 Waisya — Pedagang menyebarkan budaya</span>
          <span class="tag">👷 Sudra — Kaum pekerja yang berpindah</span>
        </div>

        <p><strong>Perkembangan kerajaan berjalan secara berkesinambungan:</strong></p>

        <table class="mini-table">
          <tr><th>Kerajaan</th><th>Lokasi & Waktu</th><th>Peran Bersejarah</th></tr>
          <tr><td><strong>Kutai</strong></td><td>Kaltim, Abad ke-4</td><td>Kerajaan Hindu <em>tertua</em> di Indonesia — Prasasti Yupa</td></tr>
          <tr><td><strong>Tarumanegara</strong></td><td>Jawa Barat, Abad ke-5</td><td>Raja Purnawarman — Prasasti Ciaruteun, irigasi pertanian</td></tr>
          <tr><td><strong>Sriwijaya</strong></td><td>Sumatera, Abad ke-7</td><td>Kerajaan maritim terkuat, pusat agama Buddha, kuasai perdagangan Selat Malaka</td></tr>
          <tr><td><strong>Mataram Kuno</strong></td><td>Jawa Tengah, Abad ke-8–9</td><td>Candi Borobudur (Buddha) & Prambanan (Hindu) — warisan dunia UNESCO</td></tr>
          <tr><td><strong>Kediri</strong></td><td>Jawa Timur, Abad ke-11</td><td>Pusat sastra — Kitab Bharatayuda, Arjunawiwaha</td></tr>
          <tr><td><strong>Singhasari</strong></td><td>Jawa Timur, 1222–1292</td><td>Raja Kertanegara, ekspansi ke luar Jawa — cikal bakal Majapahit</td></tr>
          <tr><td><strong>Majapahit</strong></td><td>Jawa Timur, 1293–1527</td><td>Kerajaan terbesar Nusantara — Gajah Mada & Sumpah Palapa, embrio NKRI</td></tr>
        </table>

        <div class="highlight">
          <strong>Peninggalan yang masih dapat kita lihat:</strong> Candi Borobudur, Candi Prambanan, Prasasti Yupa, Kitab Negarakertagama, Kitab Sutasoma ("Bhinneka Tunggal Ika" pertama kali muncul di sini).
        </div>
      </div>
    </div>

    <div class="bridge">Ketika Majapahit mulai melemah, pedagang Muslim mulai membawa pengaruh baru yang mengubah peta kekuasaan Nusantara…</div>

    <!-- ══════════════════ BAB 4 ══════════════════ -->
    <div class="chapter" style="animation-delay:0.2s">
      <div class="chapter-dot"></div>
      <div class="chapter-header">
        <div>
          <div class="chapter-num">BAB 4</div>
          <div class="chapter-era">Abad 13 — 17 M</div>
        </div>
        <div>
          <div class="chapter-title">Era Islam: Gelombang Peradaban Baru</div>
        </div>
      </div>
      <div class="chapter-body">
        <p>Islam masuk ke Nusantara melalui jalur perdagangan, tanpa kekerasan, dan menyesuaikan diri dengan budaya lokal. Terdapat beberapa teori asal-usulnya: <strong>Gujarat</strong> (India), <strong>Arab</strong> (langsung dari Mekah), <strong>Persia</strong>, dan <strong>Cina</strong>.</p>

        <table class="mini-table">
          <tr><th>Kerajaan</th><th>Lokasi</th><th>Keunggulan</th></tr>
          <tr><td><strong>Demak</strong></td><td>Jawa Tengah</td><td>Kerajaan Islam pertama di Jawa, Raden Patah — pewaris legitimasi Majapahit</td></tr>
          <tr><td><strong>Aceh</strong></td><td>Ujung Sumatera</td><td>"Serambi Mekah", Sultan Iskandar Muda — perlawanan sengit terhadap Portugis &amp; Belanda</td></tr>
          <tr><td><strong>Banten</strong></td><td>Jawa Barat</td><td>Pusat perdagangan lada, Sultan Ageng Tirtayasa — anti-VOC</td></tr>
          <tr><td><strong>Mataram Islam</strong></td><td>Jawa Tengah</td><td>Sultan Agung — dua kali menyerang Batavia (markas VOC)</td></tr>
          <tr><td><strong>Bone</strong></td><td>Sulawesi Selatan</td><td>Kerajaan Bugis yang kuat, budaya maritim dan pelayaran</td></tr>
          <tr><td><strong>Ternate &amp; Tidore</strong></td><td>Maluku</td><td>Pusat rempah dunia (cengkih &amp; pala) — rebutan bangsa Eropa</td></tr>
        </table>

        <p><strong>Hasil kebudayaan Islam</strong> meresap ke kehidupan sehari-hari: masjid (Masjid Agung Demak, Banten), pesantren, aksara Arab-Melayu, tradisi sekaten, seni kaligrafi, dan wayang yang dimodifikasi oleh Wali Songo untuk dakwah.</p>
      </div>
    </div>

    <div class="bridge">Kekayaan rempah-rempah justru menarik perhatian bangsa Eropa — dan babak yang paling menyakitkan dalam sejarah Indonesia pun dimulai…</div>

    <!-- ══════════════════ BAB 5 ══════════════════ -->
    <div class="chapter" style="animation-delay:0.25s">
      <div class="chapter-dot"></div>
      <div class="chapter-header">
        <div>
          <div class="chapter-num">BAB 5</div>
          <div class="chapter-era">Abad 16 — 1942</div>
        </div>
        <div>
          <div class="chapter-title">Kolonialisme &amp; Imperialisme Eropa</div>
        </div>
      </div>
      <div class="chapter-body">
        <p>Bangsa Eropa datang dengan misi <strong>"3G": Gold</strong> (kekayaan), <strong>Glory</strong> (kejayaan), <strong>Gospel</strong> (penyebaran agama). Nusantara yang kaya rempah menjadi incaran utama.</p>

        <table class="mini-table">
          <tr><th>Bangsa</th><th>Periode</th><th>Jejak di Indonesia</th></tr>
          <tr><td><strong>Portugis</strong></td><td>1511–1605</td><td>Pertama masuk Maluku, monopoli rempah di Ternate</td></tr>
          <tr><td><strong>Spanyol</strong></td><td>1521–1663</td><td>Masuk dari timur, bersaing dengan Portugis di Maluku</td></tr>
          <tr><td><strong>Belanda (VOC)</strong></td><td>1602–1942</td><td>Paling lama dan paling dalam menjajah — mendirikan VOC 1602, Batavia 1619</td></tr>
          <tr><td><strong>Prancis</strong></td><td>1806–1811</td><td>Melalui penguasaan Belanda era Napoleon, pengaruh terbatas</td></tr>
          <tr><td><strong>Inggris</strong></td><td>1811–1816</td><td>Thomas Raffles — menghapus kerja paksa, memperkenalkan land rent</td></tr>
        </table>

        <div class="highlight">
          <strong>Dampak Penjajahan (khususnya Belanda):</strong><br>
          • <strong>Ekonomi:</strong> Tanam Paksa (Cultuurstelsel, 1830) — rakyat dipaksa menanam tanaman ekspor<br>
          • <strong>Sosial:</strong> Diskriminasi ras, kemiskinan, stratifikasi sosial yang kaku<br>
          • <strong>Politik:</strong> Kerajaan lokal dihancurkan atau dilemahkan<br>
          • <strong>Budaya:</strong> Masuknya budaya Barat, perubahan pola hidup<br>
          • <strong>Pendidikan:</strong> Lahirnya kaum terpelajar pribumi — bibit pergerakan nasional
        </div>

        <p><em>Sisi positif:</em> pembangunan infrastruktur (jalan raya Anyer–Panarukan oleh Daendels), sistem hukum modern, dan masuknya teknologi — meski semua itu lebih untuk kepentingan penjajah.</p>
      </div>
    </div>

    <div class="bridge">Penderitaan panjang itu melahirkan kesadaran: rakyat Nusantara harus bersatu untuk merdeka…</div>

    <!-- ══════════════════ BAB 6 ══════════════════ -->
    <div class="chapter" style="animation-delay:0.3s">
      <div class="chapter-dot"></div>
      <div class="chapter-header">
        <div>
          <div class="chapter-num">BAB 6</div>
          <div class="chapter-era">1908 — 1945</div>
        </div>
        <div>
          <div class="chapter-title">Kebangkitan Nasional, Sumpah Pemuda &amp; Proklamasi</div>
        </div>
      </div>
      <div class="chapter-body">
        <p>Pendidikan ala Barat yang terbatas justru melahirkan kaum terpelajar yang kemudian memimpin perlawanan. Ini adalah periode lahirnya rasa kebangsaan Indonesia.</p>

        <div class="key-box">
          <div class="key-item">
            <div class="ki-title">Budi Utomo (1908)</div>
            <div class="ki-sub">Organisasi modern pertama — "Hari Kebangkitan Nasional"</div>
          </div>
          
