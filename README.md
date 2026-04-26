# Sistem Pakar Rekomendasi Jurusan Kuliah

Sistem rekomendasi jurusan kuliah berbasis **Sistem Pakar (Expert System)** dengan metode **Forward Chaining** dan antarmuka web statis bergaya quiz interaktif.

---

## 🗒️ Identitas

**Nama:** Sani Aprillia Anjani

**NIM:** H1D024011

**Shift Awal:** H

**Shift Akhir:** E

---

## 🧠 Tentang Sistem

Sistem ini menggunakan metode **Forward Chaining** berbasis bobot untuk mencocokkan profil minat & kepribadian pengguna dengan knowledge base jurusan kuliah. Sistem mengajukan 10 pertanyaan adaptif, mengakumulasi skor pada 7 dimensi minat, lalu menghitung persentase kecocokan terhadap setiap jurusan.

### Variabel Dimensi Minat

| Dimensi | Deskripsi |
|---|---|
| 🧮 Matematika & Logika | Kemampuan dan minat pada hitungan, rumus, dan penalaran logis |
| 🔍 Analitik | Kecenderungan menganalisis data, pola, dan informasi |
| 🎨 Kreativitas | Dorongan berkarya, bereksplorasi, dan berinovasi |
| 🖼️ Estetika | Kepekaan terhadap keindahan, desain, dan tampilan visual |
| 💻 Teknologi | Ketertarikan pada sistem digital, pemrograman, dan gadget |
| 🗣️ Komunikasi | Kemampuan dan minat dalam menyampaikan informasi ke orang lain |
| 🤝 Sosial | Orientasi pada interaksi manusia, empati, dan kerja tim |

### Output Rekomendasi

| Jurusan | Ikon |
|---|---|
| Teknik Informatika | 💻 |
| Sistem Informasi | 🖥️ |
| Desain Komunikasi Visual | 🎨 |
| Desain Produk | 🛠️ |
| Manajemen Bisnis | 📊 |
| Ilmu Komunikasi | 🗣️ |
| Psikologi | 🧠 |
| Matematika / Statistika | 📐 |
| Teknik Elektro | ⚡ |
| Hubungan Internasional | 🌍 |

### Mekanisme Inferensi

- Setiap jawaban membawa **bobot pada beberapa dimensi** secara bersamaan (multi-dimensi)
- Metode inferensi: **Forward Chaining** berbasis akumulasi bobot
- Scoring: persentase kecocokan dihitung dari `min(bobot_user, syarat_jurusan) / total_syarat × 100%`
- Output diurutkan dari persentase kecocokan tertinggi

---

## 📁 Struktur Proyek

```
ResponsiSistemPakar/
└── index.html          # Seluruh sistem (HTML + CSS + JS dalam satu file)
```

> Sistem ini adalah **web statis murni** — tidak memerlukan backend, server, atau instalasi apapun. Cukup buka file HTML di browser.

---

## ⚙️ Cara Menjalankan

```bash
# Clone repository
git clone https://github.com/saniaprl/H1D024011-PraktikumKB-ResponsiSistemPakar.git
cd ResponsiSistemPakar
```

1. Buka folder di VS Code
2. Install ekstensi **Live Server**
3. Klik kanan `index.html` → **Open with Live Server**
4. Akses di `http://127.0.0.1:5500`

---

## 🛠️ Teknologi

| Komponen | Teknologi |
|---|---|
| Logika Pakar | Vanilla JavaScript |
| Antarmuka | HTML5, CSS3 |
| Tipografi | Google Fonts |
| Deployment | Web Statis |

---

## 📊 Cara Kerja

1. Pengguna memulai kuis dan menjawab **10 pertanyaan** bergaya pilihan ganda bergambar
2. Setiap jawaban menambah bobot pada **dimensi minat** yang relevan (bisa lebih dari satu dimensi per jawaban)
3. Setelah semua pertanyaan dijawab, **Inference Engine** menghitung skor kecocokan terhadap setiap jurusan di knowledge base
4. Sistem menampilkan **5 rekomendasi terurut** beserta persentase kecocokan, bar chart dimensi, dan profil kepribadian pengguna

```
Input (Jawaban User)
       ↓
Akumulasi Bobot per Dimensi
       ↓
Forward Chaining → Hitung % Kecocokan tiap Jurusan
       ↓
Ranking & Output Rekomendasi
```

---

## 🖼️ Tampilan

| Halaman | Deskripsi |
|---|---|
| Halaman Awal | Penjelasan sistem dan tombol mulai |
| Halaman Quiz | Progress bar, pertanyaan, 4 pilihan bergambar, navigasi |
| Halaman Hasil | Rekomendasi terurut, skor tiap dimensi, profil kepribadian |

---

## ✨ Fitur

- ✅ 10 pertanyaan dengan 4 opsi bergambar per soal
- ✅ Navigasi maju-mundur & opsi lewati pertanyaan
- ✅ Progress bar animasi real-time
- ✅ Ranking 5 rekomendasi jurusan dengan skor kecocokan
- ✅ Visualisasi bar chart dimensi minat
- ✅ Profil kepribadian otomatis berdasarkan jawaban
- ✅ Tampilan responsif (mobile & desktop)
- ✅ Tidak perlu instalasi — satu file HTML langsung jalan

---
