# 🌐 Bagaimana Internet Bekerja — Edukasi Interaktif

Portal pembelajaran interaktif yang menjelaskan **cara kerja internet**, mulai dari perangkat jaringan lokal hingga infrastruktur kabel serat optik bawah laut. Proyek ini menggabungkan **materi pembelajaran** dengan **kuis evaluasi** dalam satu alur belajar: siswa membaca materi, lalu diarahkan langsung untuk menguji pemahamannya.

---

## 📖 Latar Belakang

Internet sering dianggap sebagai "kotak hitam" yang ajaib — semua orang memakainya setiap hari, tetapi sedikit yang memahami bagaimana data dari perangkat kita bisa sampai ke server di benua lain dalam hitungan milidetik.

Proyek ini lahir dari kebutuhan akan **media pembelajaran yang ringan, visual, dan interaktif** untuk memperkenalkan arsitektur serta cara kerja internet kepada pemula, khususnya siswa sekolah menengah. Alih-alih hanya berisi teks teoretis, setiap konsep dilengkapi **simulasi interaktif** (DNS lookup dan pengiriman paket data) agar siswa dapat "melihat" prosesnya secara langsung.

Selain itu, alur belajar dibuat berjenjang: siswa menyerap materi terlebih dahulu, kemudian diarahkan menuju kuis evaluasi untuk mengukur pemahaman mereka.

---

## ✨ Fitur Utama

- **6 Tab Materi Berjenjang** — Jaringan Lokal, IP & DNS, Pengiriman Paket, Klien & Server, Infrastruktur Global, serta Ringkasan.
- **Simulasi DNS Lookup** — menunjukkan bagaimana nama domain diterjemahkan menjadi Alamat IP.
- **Simulasi Pengiriman Paket Data** — visualisasi animasi paket yang bergerak dari klien menuju server.
- **Tabel Perbandingan** — membedakan Alamat MAC, Alamat IP, dan Nama Domain secara ringkas.
- **Kuis Evaluasi Berjenjang** — 30 bank soal yang dibagi menjadi tingkat Mudah, Sedang, dan Sulit, diacak otomatis oleh sistem (Fisher-Yates Shuffle).
- **Penilaian Otomatis** — bobot poin berbeda per tingkat kesulitan, langsung dihitung saat jawaban dikumpulkan.
- **Laporan Rekapitulasi** — menampilkan nilai akhir, rincian jawaban, dan log aktivitas peserta.
- **Deteksi Switch Tab** — mencatat setiap kali peserta berpindah tab/jendela selama ujian berlangsung.
- **Portal Landing Page** — halaman `index.html` sebagai pintu masuk menuju materi dan kuis.

---

## 🧭 Alur Penggunaan

```
index.html  ──▶  web-page.html  ──▶  quiz.html
 (Portal)         (Materi)            (Kuis Evaluasi)
```

1. Siswa membuka **`index.html`** (Portal Pembelajaran).
2. Membaca **materi** secara lengkap pada `web-page.html`.
3. Pada tab terakhir materi, siswa menekan tombol **"Lanjut ke Kuis Ujian"**.
4. Siswa mengisi formulir identitas, mengerjakan kuis, dan menerima laporan hasil.
5. Tersedia tautan **"Kembali ke Materi"** di halaman kuis.

---

## 🛠️ Teknologi

| Teknologi | Keterangan |
|-----------|------------|
| **HTML5** | Struktur konten dan semantik halaman. |
| **CSS3** | Desain responsif, variabel warna (CSS Custom Properties), animasi, dan gradient. |
| **Vanilla JavaScript (ES6)** | Logika kuis, pengacakan soal, penilaian otomatis, simulasi, dan deteksi switch tab. |

Seluruh proyek dibangun **tanpa framework dan tanpa dependensi eksternal** — murni HTML, CSS, dan JavaScript. Artinya, tidak ada proses build, tidak perlu `npm install`, dan situs dapat dijalankan langsung dari browser maupun hosting statis.

---

## 📂 Struktur Proyek

```
working-the-internet/
├── index.html       # Portal/landing page (entry point GitHub Pages)
├── web-page.html    # Materi pembelajaran interaktif
├── quiz.html        # Kuis evaluasi online
└── README.md        # Dokumentasi proyek ini
```

---

## 🚀 Cara Menjalankan

### Secara Lokal
Cukup unduh repositori ini dan buka file `index.html` di peramban web — tidak diperlukan server khusus.

```bash
git clone https://github.com/<username>/<nama-repo>.git
```

### Deploy ke GitHub Pages
1. Push seluruh file ke repositori GitHub.
2. Buka **Settings → Pages** pada repositori.
3. Pada bagian **Source**, pilih branch `main` dan folder `/ (root)`.
4. Simpan, lalu tunggu beberapa saat. Situs akan tersedia di:
   `https://<username>.github.io/<nama-repo>/`

Karena `index.html` berada di root, GitHub Pages akan otomatis membukanya sebagai halaman utama.

---

## 🎯 Manfaat & Hal Positif

- **Gratis dan Ringan** — Tanpa server, tanpa database, tanpa biaya hosting. Cocok untuk sekolah dengan sumber daya terbatas.
- **Aksesibel** — Cukup browser modern; dapat dibuka di komputer, tablet, maupun ponsel.
- **Mudah Dikustomisasi** — Bank soal, materi, dan tampilan dapat diubah langsung di file HTML tanpa pelatihan khusus.
- **Interaktif & Visual** — Simulasi membuat konsep abstrak (DNS, paket data) menjadi lebih mudah dipahami.
- **Alur Belajar Terarah** — Integrasi materi → kuis memastikan siswa belajar sebelum diuji.
- **Penilaian Objektif & Otomatis** — Mengurangi beban koreksi manual bagi guru.
- **Mendukung Kejujuran Akademik** — Deteksi switch tab mencatat aktivitas mencurigakan saat ujian.
- **Portofolio Pembelajaran** — Fondasi yang baik untuk mempelajari dasar pengembangan web (HTML/CSS/JS) sekaligus literasi jaringan komputer.

---

## 🔮 Pengembangan Selanjutnya (Ide)

- Penyimpanan hasil kuis (mis. `localStorage` atau backend sederhana).
- Ekspor laporan hasil ke PDF.
- Mode bank soal yang lebih besar dan kategori topik.
- Dukungan multi-bahasa.

---

## 📄 Lisensi

Proyek ini dibuat untuk keperluan edukasi dan bebas digunakan serta dimodifikasi untuk pembelajaran.
