# 🎲 Mesin Pengacak Kelompok Mahasiswa (Retro Classic Edition)

Aplikasi berbasis web interaktif dengan antarmuka **Light Retro / Vintage** yang dirancang untuk mempermudah pembagian kelompok mahasiswa atau siswa secara acak, fleksibel, dan transparan.

![Retro Group Generator](https://img.shields.io/badge/Style-Light_Retro-c85a32?style=for-the-badge)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## 🌟 Fitur Utama

- **🎨 Desain Light Retro Classic / Vintage**: Visual estetik terinspirasi dari gaya arsip dan koran cetak klasik dengan perpaduan warna hangat (*terracotta, mustard, sage green, cream*), font retro, serta bayangan tegas (*hard shadow*).
- **📝 Input Manual Tanpa Batasan**: Bebas memasukkan daftar nama mahasiswa dalam jumlah berapa pun (tidak terbatas).
- **⚙️ Kustomisasi Mode Pembagian Flexible**:
  - **Berdasarkan Jumlah Kelompok**: Menentukan berapa banyak kelompok yang ingin dibuat (misal: 7 kelompok).
  - **Berdasarkan Kapasitas Maksimal**: Menentukan jumlah maksimal anggota per kelompok (misal: 5 orang/tim).
- **📊 Kalkulasi & Distribuasi Otomatis**: Secara cerdas membagi sisa anggota (*remainder*) secara merata ke dalam kelompok-kelompok yang ada sehingga tidak ada anggota yang tertinggal.
- **⚡ Fitur Sampel Instan**: Tombol cepat untuk mengisi 36 nama sampel mahasiswa guna pengujian aplikasi.
- **💾 Auto-Save (Local Storage)**: Daftar nama yang dimasukkan akan tersimpan secara otomatis di browser sehingga aman dari ketidaksengajaan *refresh* halaman.
- **📋 Salin Hasil Satu Klik**: Menyalin teks hasil pembagian kelompok dengan rapi ke papan klip (*clipboard*) untuk dibagikan ke grup percakapan (WhatsApp/Telegram).

---

## 🛠️ Teknologi yang Digunakan

1. **HTML5**: Struktur dokumen web utama.
2. **Tailwind CSS (v3 CDN)**: *Styling* utility-first untuk membangun tema retro yang konsisten dan responsif.
3. **Vanilla JavaScript (ES6+)**: Logika pengacakan (Algoritma *Fisher-Yates*), kalkulasi kapasitas dinamis, pengelolaan DOM, dan integrasi Local Storage.
4. **Lucide Icons**: Ikon vektor minimalis modern.
5. **Google Fonts**:
   - `Space Grotesk` (Teks Utama/Sans-serif)
   - `Playfair Display` (Judul Klasik/Serif)
   - `Courier Prime` (Sentuhan Mesin Ketik/Monospace)

---

## 🚀 Cara Menggunakan

1. **Buka Aplikasi**: Jalankan file `index.html` langsung di browser web Anda.
2. **Input Daftar Mahasiswa**:
   - Masukkan nama-nama mahasiswa pada area teks yang disediakan (satu nama per baris atau dipisahkan koma).
   - Atau klik tombol **"Sampel (36 Nama)"** untuk menguji secara otomatis.
3. **Atur Pembagian**:
   - Pilih metode pembagian yang diinginkan (**Jumlah Kelompok** atau **Maks Anggota / Tim**).
   - Geser slider sesuai kebutuhan Anda.
4. **Mulai Pengacakan**:
   - Klik tombol **"MULAI ACAK KELOMPOK"**.
   - Sistem akan mengacak nama dan menampilkan hasilnya dengan animasi pengisian bertahap.
5. **Salin / Bagikan**:
   - Klik tombol **"SALIN TEKS"** untuk menyimpan hasil pembagian ke *clipboard*.

---

## 📐 Logika Pembagian Kelompok

Aplikasi menggunakan pendekatan matematika adil (*balanced distribution*):
$$\text{Kapasitas Dasar} = \lfloor \frac{N}{K} \rfloor$$
$$\text{Sisa Mahasiswa} = N \bmod K$$

Di mana $N$ adalah total mahasiswa dan $K$ adalah target jumlah kelompok. $Sisa Mahasiswa$ akan didistribusikan $1$ per $1$ ke kelompok awal hingga seluruh mahasiswa terbagi habis.

---

## 📄 Lisensi

Proyek ini bersifat *Open Source* dan bebas digunakan untuk keperluan akademis, sekolah, maupun personal.