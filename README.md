# 📋 CV Recruitment Analyzer — Full Stack

Aplikasi analisa CV berbasis AI dengan autentikasi user dan penyimpanan riwayat.

**Stack:** Next.js 14 · Supabase (Auth + DB) · Vercel (Deploy) · Anthropic Claude API

---

## ✨ Fitur

- 🔐 **Auth** — Login & register HR via Supabase
- 🤖 **Analisa AI** — 10 dimensi penilaian lengkap (Executive Summary, Skill Gap, Red Flags, Score, dll)
- 💾 **Simpan otomatis** — Setiap hasil analisa tersimpan ke database
- 📁 **Riwayat** — Lihat & hapus semua analisa sebelumnya
- 🌙 **Dark mode** otomatis

---

## 🚀 Setup & Deploy

### 1. Clone repo

```bash
git clone https://github.com/workimamaldiainulyaqin/Analisa-CV.git
cd Analisa-CV
npm install
```

### 2. Setup Supabase

1. Buat project baru di [supabase.com](https://supabase.com)
2. Buka **SQL Editor**, jalankan isi file `lib/schema.sql`
3. Copy **Project URL** dan **Anon Key** dari Settings → API

### 3. Setup environment variables

Buat file `.env.local`:

```env
ANTHROPIC_API_KEY=sk-ant-api03-...
NEXT_PUBLIC_SUPABASE_URL=https://xxxx.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=eyJhbGci...
```

### 4. Jalankan lokal

```bash
npm run dev
# buka http://localhost:3000
```

### 5. Deploy ke Vercel

1. Push ke GitHub
2. Buka [vercel.com](https://vercel.com) → **Add New Project** → import repo ini
3. Tambahkan 3 environment variables di Vercel dashboard:
   - `ANTHROPIC_API_KEY`
   - `NEXT_PUBLIC_SUPABASE_URL`
   - `NEXT_PUBLIC_SUPABASE_ANON_KEY`
4. Klik **Deploy**

---

## 📁 Struktur Project

```
analisa-cv/
├── app/
│   ├── api/analyze/route.ts   # API route — proxy ke Anthropic (API key aman di server)
│   ├── dashboard/page.tsx     # Halaman utama analisa
│   ├── history/page.tsx       # Riwayat analisa
│   ├── login/page.tsx         # Login & register
│   ├── layout.tsx
│   ├── globals.css
│   └── page.tsx               # Redirect otomatis
├── lib/
│   ├── supabase.ts            # Supabase browser client
│   ├── supabase-server.ts     # Supabase server client
│   └── schema.sql             # SQL untuk setup database
├── .env.local.example
├── next.config.js
├── package.json
└── tsconfig.json
```

---

## 🔒 Keamanan

- **Anthropic API key** hanya ada di server (Vercel environment variable) — tidak pernah dikirim ke browser
- **Row Level Security** aktif di Supabase — setiap user hanya bisa lihat data miliknya sendiri
- Auth session dikelola oleh Supabase SSR

---

## 📄 Lisensi

MIT License
