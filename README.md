# Bollywood Karaoke Event App 🎤✨

Aplikasi Web premium dan mewah bertema panggung Bollywood untuk mengelola, menampilkan papan peringkat (leaderboard) real-time, dan mencetak piagam otomatis untuk pemenang acara lomba karaoke online Anda.

Aplikasi ini mendukung **penilaian kolaboratif 6 juri** yang masing-masing fokus pada satu kriteria penilaian tertentu.

---

## 🚀 Cara Menjalankan Secara Lokal

### Prasyarat
Pastikan Anda sudah menginstal [Node.js](https://nodejs.org/).

### Langkah-langkah
1. Buka folder projek di terminal / command prompt.
2. Instal dependensi (jika belum):
   ```bash
   npm install
   ```
3. Jalankan server pengembangan lokal:
   ```bash
   npm run dev
   ```
4. Buka peramban (browser) di alamat yang muncul di terminal (biasanya `http://localhost:3000`).

---

## 📊 Cara Menghubungkan ke Google Sheets

Anda dapat memasukkan data secara manual di tab **Admin & Sheets (Input Lokal)** atau menghubungkannya ke **Google Sheets** agar terintegrasi real-time.

### Langkah-langkah Pembuatan Sheet:
1. Buat spreadsheet baru di Google Sheets.
2. Buat header kolom pada baris pertama persis seperti berikut (pastikan penulisan kata kunci ini ada):
   - **Nama Peserta** (Kolom A)
   - **Lagu Bollywood** (Kolom B)
   - **Kualitas Vocal** (Kolom C) - *Dinilai oleh Juri 1*
   - **Artikulasi** (Kolom D) - *Dinilai oleh Juri 2*
   - **Pronounce** (Kolom E) - *Dinilai oleh Juri 3*
   - **Pitch Kontrol** (Kolom F) - *Dinilai oleh Juri 4*
   - **Tempo** (Kolom G) - *Dinilai oleh Juri 5*
   - **Penghayatan** (Kolom H) - *Dinilai oleh Juri 6*

3. Setiap juri hanya perlu fokus mengisi kolom kriteria masing-masing (rentang nilai `0 - 100`).

### Langkah-langkah Publikasi CSV:
1. Di Google Sheets Anda, klik **File** > **Bagikan** > **Publikasikan ke web**.
2. Di dropdown pilihan, pilih **Nilai Terpisah Koma (.csv)** (bukan *Halaman Web*).
3. Klik tombol **Publikasikan** dan konfirmasi.
4. Salin (copy) tautan URL yang dihasilkan.
5. Tempel (paste) tautan tersebut ke tab **Admin & Sheets** di Webapp, lalu klik **Hubungkan Sheet**.

---

## 🏆 Fitur Utama Aplikasi

- **Leaderboard Real-Time**: Otomatis menghitung akumulasi total nilai juri dan mengurutkan peringkat peserta dari yang tertinggi. Kartu ranking 3 teratas didesain ala podium Bollywood mewah.
- **Radar Chart Analisis**: Klik pada nama peserta di papan peringkat untuk melihat analisis grafik jaring laba-laba Chart.js dari performa kriteria mereka.
- **Layar Penuh "Live Stage Mode"**: Mode proyektor/layar penuh khusus untuk ditayangkan pada saat pengumuman lomba, lengkap dengan running text (marquee) dan efek pesta konfeti perayaan kemenangan.
- **Generator Piagam Otomatis**: Pilih nama pemenang, tentukan predikat gelar juara (Juara 1, Best Vocal, dll.), pilih tema piagam (Gold, Royal, Emerald), dan unduh instan sebagai file **PNG berkualitas tinggi** atau langsung cetak ke **PDF**.
