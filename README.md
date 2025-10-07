<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Website Zahra</title>
  <!-- Import Font -->
  <link href="https://fonts.googleapis.com/css2?family=Super+Sunkissed&family=Super+Vanilla&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #ffe6f0, #ffffff);
      font-family: 'Super Vanilla', cursive;
      color: #3e2f2f;
    }

    header {
      text-align: center;
      padding: 30px 20px;
      background: linear-gradient(135deg, #e8a7c0, #f5d2e1);
      border-bottom-left-radius: 40px;
      border-bottom-right-radius: 40px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.15);
    }

    header h1 {
      font-family: "Super Sunkissed", cursive;
      font-size: 48px;
      color: #fff;
      margin: 0;
      text-shadow: 2px 2px 6px rgba(0,0,0,0.25);
    }

    nav {
      background:#f3dbe4;
      padding:10px;
      text-align:center;
    }
    nav a {
      margin:0 15px;
      text-decoration:none;
      color:#3e3e3e;
      font-weight:bold;
      cursor:pointer;
    }
    nav a:hover {color:#d63384;}

    /* Dropdown */
    .dropdown {
      display:inline-block;
      position:relative;
    }
    .dropdown-content {
      display:none;
      position:absolute;
      background:#fff;
      min-width:160px;
      box-shadow:0 4px 12px rgba(0,0,0,0.15);
      border-radius:8px;
      overflow:hidden;
      z-index:10;
    }
    .dropdown-content a {
      display:block;
      padding:10px;
      color:#3e3e3e;
      text-decoration:none;
      font-weight:normal;
    }
    .dropdown-content a:hover {
      background:#f3dbe4;
      color:#d63384;
    }
    .dropdown:hover .dropdown-content {
      display:block;
    }

    main {padding: 30px; text-align:center;}
    section {display:none;}
    section.active {display:block;}

    /* Konten About */
    .content {
      display: flex;
      max-width: 1000px;
      background: #fff;
      margin: 40px auto;
      border-radius: 25px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      overflow: hidden;
      padding: 30px;
      gap: 30px;
      text-align:left;
    }
    .left {flex:1; display:flex; justify-content:center;}
    .left img {
      width: 250px; height: 250px;
      object-fit: cover;
      border-radius: 30px;
      border: 6px solid #e99cb9;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
    }
    .right {flex:2;}
    h2 {color:#b35679; margin-top:0;}
    .intro {font-size:18px; line-height:1.8;}
    .biodata p {font-size:16px; margin:4px 0;}

    .organization {
      max-width: 950px;
      margin: 20px auto 40px;
      background: #fff;
      padding: 25px;
      border-radius: 20px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      text-align:left;
    }

    .gallery {
      display:flex; justify-content:center; gap:20px;
      margin:0 auto 50px; max-width:1000px;
    }
    .gallery img {
      width:280px; height:200px; object-fit:cover;
      border-radius:20px; border:4px solid #e99cb9;
      box-shadow:0 4px 10px rgba(0,0,0,0.2);
      transition:transform 0.3s;
    }
    .gallery img:hover {transform:scale(1.05);}

    /* Jadwal */
    table {
      margin: auto;
      border-collapse: collapse;
      width: 95%;
      background: #ffffff;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }
    th, td {
      border: 1px solid #ddd;
      padding: 10px;
      text-align: center;
      font-size: 15px;
    }
    th {
      background: #e8b7c8;
      color: #ffffff;
      font-size: 16px;
    }
    td:first-child {
      background: #f3dbe4;
      font-weight: bold;
    }
    tr:nth-child(even) td {background:#fff7fa;}

    /* Lirik Lagu */
    .lyrics {
      max-width: 800px;
      margin: 30px auto;
      background: #fff;
      padding: 25px;
      border-radius: 20px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      text-align:left;
      font-family: "Courier New", monospace;
      font-size: 20px;
      line-height: 1.8;
    }
    .lyrics .chord {
      color: #b35679;
      font-weight: bold;
    }

    footer {
      background:#e8b7c0;
      color:white;
      text-align:center;
      padding:15px;
      margin-top:20px;
      border-top-left-radius:40px;
      border-top-right-radius:40px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Website Zahra XII DKV 2</h1>
  </header>

  <nav>
    <a onclick="showPage('home')">Beranda</a>
    <a onclick="showPage('about')">About Me Zahra</a>
    <a onclick="showPage('jadwal')">Jadwal Mapel</a>
    <a onclick="showPage('lirik')">Lirik Lagu</a>
    <!-- Tambahan menu dropdown Menghitung -->
    <div class="dropdown">
      <a>Menghitung ▼</a>
      <div class="dropdown-content">
        <a onclick="showPage('persegi')">Luas Persegi</a>
        <a onclick="showPage('volume')">Volume Kotak</a>
      </div>
    </div>
  </nav>

  <main>
    <!-- Beranda -->
    <section id="home" class="active">
      <h2> Halo, Welcome to website 👀</h2>
      <p>Pilih menu di atas untuk melihat halaman <b>About Me Zahra</b>, <b>Jadwal Pelajaran</b>, <b>Lirik Lagu</b>, <b>Menghitung</b>.</p>

    </section>

     <!-- About Me -->
    <section id="about">
      <div class="content">
        <div class="left">
           <img src="C:\Users\NESTA LKS\Downloads\gyejh.jfif" alt="gyejh">
        </div>
        <div class="right">
          <h2>Perkenalan Diri 👋🏻</h2>
          <p class="intro">
            hayyiee! Nama saya <b>Zahra</b>, saya adalah siswi dari <b>SMKN 1 Tangerang</b>.  
            Saya punya banyak mimpi besar, tetapi prosesnya harus saya mulai dari hal-hal kecil terlebih dahulu.  
            Saya percaya, usaha kecil yang saya tekuni akan membawakan hasil besar di masa depan.
          </p>

          <h2>Biodata Zahra 🫣</h2>
          <div class="biodata">
            <p><b>Nama:</b> Zahra</p>
            <p><b>TTL:</b> Jakarta, 27 Juni 2008</p>
            <p><b>Hobi:</b> Bermain game & memasak</p>
            <p><b>Makanan Kesukaan:</b> Kentang, Sosis, Indomie, Ayam</p>
            <p><b>Warna Kesukaan:</b> Hijau, Pink, Warna Soft</p>
            <p><b>Cita-cita:</b> Mempunyai Coffee & Bake Shop</p>
          </div>
        </div>
      </div>

      <div class="organization">
        <h2>Organisasi & Kegiatan ✨</h2>
        <p>
          Selain belajar di sekolah, saya juga aktif mengikuti beberapa kegiatan organisasi.  
          Saya pernah bergabung dalam <b>OSIS</b> dan ekstrakurikuler <b>Basket</b> yang mengajarkan saya tentang kepemimpinan,  
          kerja sama, tanggung jawab, dan menjaga ketahanan tubuh.  
          Saya juga suka mengikuti perlombaan untuk menambah pengalaman baru.
        </p>
      </div>

      <!-- Gallery Foto -->
      <div class="gallery">
        <img src="C:\Users\NESTA LKS\Downloads\sekbid.jfif" alt="Foto Kegiatan 1">
        <img src="C:\Users\NESTA LKS\Downloads\osis.jfif"  alt="Foto Kegiatan 2">
        <img src="C:\Users\NESTA LKS\Downloads\basket.jfif" alt="Foto Kegiatan 3">
      </div>
    </section>

    <!-- Jadwal -->
    <section id="jadwal">
      <h2>Jadwal Pelajaran</h2>
      <table>
        <tr>
          <th>Waktu</th>
          <th>Senin</th>
          <th>Selasa</th>
          <th>Rabu</th>
          <th>Kamis</th>
          <th>Jumat</th>
        </tr>
        <tr><td>07.00 - 07.40</td><td>Upacara</td><td>PPKN</td><td>Bhs Inggris</td><td>Kejuruan 3</td><td>Pengajian</td></tr>
        <tr><td>07.40 - 08.20</td><td>Kejuruan 1</td><td>PPKN</td><td>Bhs Inggris</td><td>Kejuruan 3</td><td>PKWH</td></tr>
        <tr><td>08.20 - 09.00</td><td>Kejuruan 1</td><td>Kejuruan 2</td><td>Bhs Inggris</td><td>Kejuruan 3</td><td>PKWH</td></tr>
        <tr><td>09.00 - 09.40</td><td>Kejuruan 1</td><td>Kejuruan 2</td><td>Bhs Inggris</td><td>Bahasa Indonesia</td><td>PKWH</td></tr>
        <tr><td>09.40 - 10.00</td><td>Istirahat</td><td>Istirahat</td><td>Istirahat</td><td>Istirahat</td><td>Istirahat</td></tr>
        <tr><td>10.00 - 10.40</td><td>Kejuruan 1</td><td>Matematika</td><td>Kejuruan 3</td><td>Agama Islam</td><td>Bahasa Indonesia</td></tr>
        <tr><td>10.40 - 11.20</td><td>Kejuruan 2</td><td>Matematika</td><td>Kejuruan 3</td><td>Agama Islam</td><td>Bahasa Indonesia</td></tr>
        <tr><td>11.20 - 12.00</td><td>Kejuruan 2</td><td>Matematika</td><td>Kejuruan 3</td><td>Agama Islam</td><td>Jumsih</td></tr>
        <tr><td>12.00 - 12.45</td><td>Istirahat</td><td>Istirahat</td><td>Istirahat</td><td>Istirahat</td><td>Istirahat</td></tr>
        <tr><td>12.45 - 13.25</td><td>Kejuruan 2</td><td>Mapel Pilihan DKV</td><td>Kejuruan 1</td><td>Kejuruan 1</td><td>Istirahat</td></tr>
        <tr><td>13.25 - 14.05</td><td>Kejuruan 2</td><td>Mapel Pilihan DKV</td><td>Kejuruan 1</td><td>Kejuruan 1</td><td>Estrakulikuler</td></tr>
        <tr><td>14.05 - 14.45</td><td>Kejuruan 2</td><td>Mapel Pilihan DKV</td><td>PKWH</td><td>Bahasa Korea</td><td>Estrakulikuler</td></tr>
        <tr><td>14.45 - 15.25</td><td>Kejuruan 2</td><td>Mapel Pilihan DKV</td><td>PKWH</td><td>Bahasa Korea</td><td>Estrakulikuler</td></tr>
      </table>
    </section>

    <!-- Lirik Lagu -->
    <section id="lirik">
      <h2>Lirik Lagu 🎶</h2>
      <div class="lyrics">
        <h3>A Thousand Years - Christina Perri</h3>
        <p><span class="chord">G       Em</span><br>Heart beats fast</p>
        <p><span class="chord">C             D</span><br>Colors and promises</p>
        <p><span class="chord">G       Em</span><br>How to be brave</p>
        <p><span class="chord">C                D</span><br>How can I love when I'm afraid to fall</p>

        <p><span class="chord">G           Em</span><br>But watching you stand alone</p>
        <p><span class="chord">C                   D</span><br>All of my doubt suddenly goes away somehow</p>

        <p><span class="chord">Am  G   D</span><br>One step closer</p>

        <p><span class="chord">G             Em</span><br>I have died everyday, waiting for you</p>
        <p><span class="chord">C                     D</span><br>Darling, don't be afraid, I have loved you</p>
        <p><span class="chord">Em      C          G    D</span><br>For a thousand years, I'll love you for a thousand more</p>

        <p><span class="chord">G       Em</span><br>Time stands still</p>
        <p><span class="chord">C              D</span><br>Beauty in all she is</p>
        <p><span class="chord">G        Em</span><br>I will be brave</p>
        <p><span class="chord">C                D</span><br>I will not let anything take away</p>

        <p><span class="chord">G           Em</span><br>What's standing in front of me</p>
        <p><span class="chord">C                D</span><br>Every breath, every hour has come to this</p>
      </div>
    </section>
  </main>


    <!-- Tambahan Section Luas Persegi -->
    <section id="persegi">
      <h2>Menghitung Luas Persegi</h2>
      <p>Masukkan panjang sisi:</p>
      <input type="number" id="sisi" placeholder="Sisi">
      <button onclick="hitungLuas()">Hitung</button>
      <p id="hasilLuas"></p>
    </section>

    <!-- Tambahan Section Volume Kotak -->
    <section id="volume">
      <h2>Menghitung Volume Kotak</h2>
      <p>Masukkan panjang, lebar, dan tinggi:</p>
      <input type="number" id="panjang" placeholder="Panjang">
      <input type="number" id="lebar" placeholder="Lebar">
      <input type="number" id="tinggi" placeholder="Tinggi">
      <button onclick="hitungVolume()">Hitung</button>
      <p id="hasilVolume"></p>
    </section>
  </main>

  <footer>
    &copy; 2025 Zahra - XII DKV 2
  </footer>

  <script>
    function showPage(pageId) {
      document.querySelectorAll("section").forEach(sec => sec.classList.remove("active"));
      document.getElementById(pageId).classList.add("active");
    }

    function hitungLuas() {
      let sisi = document.getElementById("sisi").value;
      if (sisi) {
        let luas = sisi * sisi;
        document.getElementById("hasilLuas").innerText = "Luas persegi = " + luas;
      }
    }

    function hitungVolume() {
      let p = document.getElementById("panjang").value;
      let l = document.getElementById("lebar").value;
      let t = document.getElementById("tinggi").value;
      if (p && l && t) {
        let volume = p * l * t;
        document.getElementById("hasilVolume").innerText = "Volume kotak = " + volume;
      }
    }
  </script>
</body>
</html>

