# PAGASKA Birthday Card Generator

Generator kartu ulang tahun digital untuk anggota **Paskibra Gala Taksaka (PAGASKA)**.

## Fitur
- Upload foto anggota
- Isi nama, jabatan, generasi
- AI generate ucapan otomatis (Kak Taksaka & Dokter Taksaka)
- Download kartu sebagai PNG 1080×1920

## Struktur File
```
pagaska/
├── index.html       ← Aplikasi utama (semua-dalam-satu)
├── kak.png          ← Gambar Kak Taksaka (taruh sendiri)
├── dokter.png       ← Gambar Dokter Taksaka (taruh sendiri)
└── vercel.json      ← Config deploy Vercel
```

## Cara Deploy

### A. Vercel (Rekomendasi)
1. Install Vercel CLI: `npm i -g vercel`
2. Masuk folder ini: `cd pagaska`
3. Jalankan: `vercel`
4. Ikuti instruksi, deploy selesai!

**Atau pakai Vercel Dashboard:**
1. Push folder ini ke GitHub
2. Buka vercel.com → New Project → Import repo
3. Deploy otomatis!

### B. Hugging Face Spaces
1. Buat Space baru di huggingface.co/spaces
2. Pilih **Static HTML** sebagai SDK
3. Upload `index.html`, `kak.png`, `dokter.png`
4. Space langsung live!

## Gambar Karakter
Taruh file gambar karakter kamu:
- `kak.png`    → gambar Kak Taksaka (260×390px ideal)
- `dokter.png` → gambar Dokter Taksaka (260×390px ideal)

Gambar otomatis di-crop/resize di canvas, jadi ukuran bebas.

## API Key Anthropic
- Dapatkan gratis di: https://console.anthropic.com
- Input di form sebelum generate
- Key **tidak pernah dikirim ke server**, hanya dipakai di browser
- Tanpa key → ucapan pakai teks default

## Cara Ganti Teks Default
Di `index.html`, cari fungsi `generateUcapan` dan edit bagian `defaultUcapan`.
