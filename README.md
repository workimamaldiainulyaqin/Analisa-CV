# 🧠 CV Recruitment Analyzer — AI-Powered

Alat analisa CV berbasis AI yang membantu HR & Rekruter menilai kesesuaian kandidat dengan posisi yang dibutuhkan secara **cepat, detail, dan objektif**.

Built with **Claude AI (Anthropic)** — tidak memerlukan backend, server, atau database. Cukup satu file HTML.

---

## ✨ Fitur Utama

- 📋 **Input Job Description & Kualifikasi** — tempel langsung dari sistem HR
- 📄 **Upload CV** — support PDF & TXT, atau copy-paste teks CV
- 🤖 **Analisa AI 10 Dimensi** meliputi:
  - Executive Summary kandidat
  - Tabel pencocokan setiap requirement (Match / Partial / No Match + Score)
  - Analisa pengalaman & skill gap
  - Achievement analysis
  - Red flag & risiko rekrutmen
  - Probabilitas lolos tiap tahap seleksi
  - 10 pertanyaan interview yang tepat sasaran
  - Estimasi range kompensasi (konteks Indonesia)
  - Rekomendasi final dengan skor keseluruhan (A+ → E)
- 💾 **Unduh hasil** analisa sebagai file teks
- 🌙 **Dark mode** otomatis
- 📱 **Responsive** — bisa dipakai di mobile

---

## 🚀 Cara Menggunakan

### 1. Clone repo ini

```bash
git clone https://github.com/username/cv-recruitment-analyzer.git
cd cv-recruitment-analyzer
```

### 2. Buka `index.html` di browser

Tidak perlu install apapun. Langsung buka file-nya:

```bash
open index.html
# atau drag-and-drop ke browser
```

### 3. Dapatkan Anthropic API Key

Daftar dan dapatkan API key di [console.anthropic.com](https://console.anthropic.com).

> API key hanya tersimpan di browser kamu selama sesi berlangsung — tidak dikirim ke server manapun selain Anthropic.

### 4. Isi form & analisa

1. Masukkan API key, nama posisi, job description, dan kualifikasi
2. Upload file CV kandidat (PDF/TXT) atau tempel teks CV
3. Klik **Mulai Analisa CV**
4. Hasil lengkap tampil dalam beberapa detik

---

## 📁 Struktur Repo

```
cv-recruitment-analyzer/
├── index.html      # Seluruh aplikasi dalam satu file
└── README.md       # Dokumentasi ini
```

---

## 🔧 Kustomisasi

Semua kode ada dalam `index.html`. Kamu bisa edit:

- **System prompt** — ubah gaya analisa atau bahasa output (cari `systemPrompt`)
- **Model AI** — ganti `claude-sonnet-4-6` ke model lain jika diperlukan
- **Warna & tampilan** — edit CSS variables di bagian `:root`
- **Format output** — ubah template prompt di bagian `textPrompt`

---

## 💡 Tips Penggunaan

- Semakin **lengkap job description & kualifikasi**, semakin akurat hasil analisa
- Untuk CV PDF, gunakan PDF yang berisi **teks asli** (bukan scan/gambar) agar bisa dibaca AI
- Hasil analisa bisa **diunduh** sebagai file `.txt` untuk disimpan atau dishare ke hiring manager

---

## ⚠️ Catatan Penting

- Tools ini menggunakan **Anthropic API** yang berbayar berdasarkan token penggunaan
- Estimasi biaya per analisa: sekitar **$0.01–0.03 USD** (tergantung panjang CV & JD)
- API key **tidak disimpan** di localStorage maupun server — hanya ada di memori browser selama tab terbuka

---

## 📄 Lisensi

MIT License — bebas digunakan, dimodifikasi, dan didistribusikan.

---

## 🙌 Dibuat dengan

- [Claude API — Anthropic](https://anthropic.com)
- [Font Awesome](https://fontawesome.com) untuk ikon
- Vanilla HTML, CSS, JavaScript — tanpa framework
