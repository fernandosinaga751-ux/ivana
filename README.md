# Dearmatrip Website

## 📁 Struktur Folder (WAJIB seperti ini)

```
dearmatrip/          ← folder ini yang di-push ke GitHub
├── package.json
├── .gitignore
├── public/
│   └── index.html
└── src/
    ├── index.js
    └── App.js       ← file utama website
```

## ⚙️ Konfigurasi (Edit di src/App.js baris atas)

```js
const CFG = {
  CLOUD_NAME:    "your_cloud_name",       // dari Cloudinary dashboard
  UPLOAD_PRESET: "dearmatrip_unsigned",   // preset unsigned di Cloudinary
  SUPABASE_URL:  "https://xxxx.supabase.co",
  SUPABASE_ANON: "eyJ...",               // anon key dari Supabase
  ADMIN_PASS:    "password_anda",
  WA_NUM:        "6281234567890",
};
```

## 🚀 Deploy ke Vercel

### Cara 1 — Lewat GitHub (Recommended)

```bash
# Di dalam folder dearmatrip/
git init
git add .
git commit -m "first commit"

# Buat repo baru di github.com dulu, lalu:
git remote add origin https://github.com/USERNAME/dearmatrip.git
git branch -M main
git push -u origin main
```

Lalu di **vercel.com**:
1. New Project → Import dari GitHub
2. Pilih repo `dearmatrip`
3. Framework: **Create React App** (otomatis terdeteksi)
4. Klik **Deploy** ✅

### Cara 2 — Vercel CLI (Lebih Cepat)

```bash
npm install -g vercel
cd dearmatrip
vercel
# Ikuti instruksi, pilih defaults semua
```

## 🛠 Jalankan Lokal

```bash
cd dearmatrip
npm install
npm start
# Buka http://localhost:3000
```
