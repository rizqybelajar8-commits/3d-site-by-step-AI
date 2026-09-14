# NEXUS — The Future of Spatial Computing

<p align="center">
  <img src="https://img.shields.io/badge/Three.js-r128-black?style=for-the-badge&logo=three.js" alt="Three.js" />
  <img src="https://img.shields.io/badge/GSAP-3.12.2-88CE02?style=for-the-badge&logo=greensock&logoColor=white" alt="GSAP" />
  <img src="https://img.shields.io/badge/TailwindCSS-CDN-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind" />
  <img src="https://img.shields.io/badge/Lenis-Smooth_Scroll-22d3ee?style=for-the-badge" alt="Lenis" />
</p>

<p align="center">
  Landing page imersif bergaya <b>Awwwards-winning</b> untuk visi Spatial Computing — dibangun dalam <b>satu file HTML</b>, tanpa build step, tanpa framework.
</p>

<p align="center">
  <a href="#-demo">Demo</a> •
  <a href="#-fitur">Fitur</a> •
  <a href="#-tech-stack">Tech Stack</a> •
  <a href="#-cara-menjalankan">Cara Menjalankan</a> •
  <a href="#-struktur-proyek">Struktur</a> •
  <a href="#-deploy">Deploy</a>
</p>

---

## ✨ Tentang Proyek

**NEXUS** adalah konsep landing page futuristik untuk ekosistem Spatial Computing fiktif — dari *Nexus Core (2024)* sampai *Nexus Singularity (2028)*.

Halaman ini menggabungkan **3D real-time (Three.js)**, **animasi scroll sinematik (GSAP + ScrollTrigger)**, dan **smooth scrolling (Lenis)** untuk menciptakan pengalaman seperti produk Apple Vision Pro / sci-fi kelas atas.

> File utama: [`nexus-landing.html`](./nexus-landing.html) — buka langsung di browser, langsung jalan.

---

## 🚀 Demo

### Cara cepat coba (lokal)

```bash
git clone https://github.com/rizqybelajar8-commits/3d-site-by-step-AI.git
cd 3d-site-by-step-AI

# opsi 1: buka langsung
# double-klik nexus-landing.html

# opsi 2: pakai server lokal (recommended, biar ES module & CDN stabil)
npx serve .
# atau
python -m http.server 8000
```

Lalu buka: `http://localhost:8000/`

### Live Demo (GitHub Pages)

Aktifkan di: `Settings → Pages → Deploy from branch → main / (root)` → akses di:

```
https://rizqybelajar8-commits.github.io/3d-site-by-step-AI/
```

---

## 🌟 Fitur

| Area | Detail |
|------|--------|
| **🔮 Hero Sinematik** | Headline split-per-huruf dengan animasi `GSAP power4.out`, fade + blur saat scroll |
| **🌌 Background 3D Global** | Icosahedron shader + 2000 partikel interaktif yang mengikuti mouse (parallax kamera) |
| **💳 Product Timeline Horizontal** | Horizontal scroll yang di-pin (`ScrollTrigger pin + scrub`) — 5 generasi produk |
| **🔷 Mini 3D per Card** | Setiap kartu punya canvas Three.js sendiri: wireframe icosahedron + inner glow + orbit partikel |
| **⚡ Performance Section** | Animated counter (60 FPS, 120° FOV), metric bar animasi, TorusKnot wireframe |
| **🧲 Micro-interaction** | Custom cursor (dot + outline), magnetic CTA, tombol glow, 3D tilt di feature card |
| **📱 Fully Responsive** | Mobile menu fullscreen, kartu mengecil di `<768px`, cursor dimatikan di mobile |
| **⏳ Loading Screen** | Loader NEXUS + progress bar 1.8 detik sebelum animasi init |
| **📩 Waitlist Form** | Validasi email bawaan + feedback interaktif `✓ Reserved!` tanpa backend |
| **🔝 UX Polish** | Noise overlay, custom scrollbar, scroll-to-top button, divider gradient |

### Showcase Produk

1. **2024 — Nexus Core** — Room-scale tracking, 8K per eye
2. **2025 — Nexus Link** — Bridging VR / AR / hologram
3. **2026 — Nexus Orbit** — Cloud-native spatial computing
4. **2027 — Nexus Genesis** — Brain-to-reality interface
5. **2028 — Nexus Singularity** — Ambient spatial intelligence

---

## 🛠 Tech Stack

| Teknologi | Fungsi | CDN |
|-----------|--------|-----|
| **Three.js r128** | Rendering 3D background, mini orb, TorusKnot | `cdnjs.cloudflare.com/.../three.min.js` |
| **GSAP 3.12.2 + ScrollTrigger** | Split-text, reveal, pin horizontal scroll, counter | `cdnjs.cloudflare.com/.../gsap.min.js` |
| **Tailwind CSS (Play CDN)** | Layout utility-first + custom config font | `cdn.tailwindcss.com` |
| **Lenis 1.0.42** | Smooth scrolling buttery | `unpkg.com/@studio-freight/lenis` |
| **Google Fonts** | Inter + Space Grotesk + JetBrains Mono | `fonts.googleapis.com` |
| **Vanilla JS + CSS** | Tanpa build tools, tanpa npm | — |

Tidak ada `package.json`, tidak ada bundler. **Clone → buka → jadi.**

---

## 📂 Struktur Proyek

```
3d-site-by-step-AI/
├── index.html           # ← entry point utama (untuk GitHub Pages)
├── nexus-landing.html   # ← file sumber asli (isi sama dengan index.html)
└── README.md            # dokumentasi ini
```

Arsitektur di dalam `nexus-landing.html`:

```
<head>  → Tailwind, Fonts, Three.js, GSAP, <style> custom
<body>
  ├── #loader            → loading screen
  ├── .noise             → film grain overlay
  ├── #canvas-container  → background 3D global (fixed)
  ├── nav                → glassmorphism navbar + mobile menu
  ├── .content
  │    ├── #hero         → headline + CTA
  │    ├── #features     → 3 pilar (Neural Rendering, Quantum Sync, Holographic UI)
  │    ├── #showcase     → horizontal product timeline (pinned)
  │    ├── #about        → performance + TorusKnot canvas
  │    ├── #waitlist     → email form
  │    └── footer        → links + copyright
  └── <script>           → Lenis, cursor, Three.js scenes, GSAP triggers
```

---

## 💻 Cara Menjalankan

Butuh koneksi internet (karena semua library via CDN).

```bash
# 1. Clone
git clone https://github.com/rizqybelajar8-commits/3d-site-by-step-AI.git

# 2. Masuk folder
cd 3d-site-by-step-AI

# 3. Jalankan (pilih salah satu)
npx serve .
# atau
python -m http.server 8000
# atau
php -S localhost:8000
```

Lalu buka browser ke `http://localhost:8000/` (otomatis membuka `index.html`).

### Kustomisasi Cepat

| Mau ubah apa? | Di mana? |
|---------------|----------|
| Warna tema cyan/violet | `:root` → `--cyan`, `--violet` di `<style>` (~baris 38) |
| Teks hero | `<h1 id="hero-headline">` |
| Produk timeline | Duplikat / edit blok `<div class="product-card">` |
| Kecepatan smooth scroll | `new Lenis({ duration: 1.2 })` |
| Jumlah partikel | `const particleCount = 2000` |
| Durasi loader | `setTimeout(..., 1800)` |

---

## 🌍 Deploy

### GitHub Pages (gratis, 1 menit)

`index.html` sudah ada di repo, jadi tinggal aktifkan:

1. Buka repo di GitHub → **Settings → Pages**
2. **Build and deployment → Deploy from a branch**
3. Branch: **`main` / `(root)` → Save**
4. Tunggu ±1 menit → live di `https://rizqybelajar8-commits.github.io/3d-site-by-step-AI/`

> Catatan: `index.html` dan `nexus-landing.html` isinya sama. Kalau edit satu, copy ke yang lain supaya sinkron.

### Vercel / Netlify

Drag & drop folder ini ke [vercel.com](https://vercel.com) atau [netlify.com](https://netlify.com) — tidak perlu setting build, output = file statis.

---

## 🗺 Roadmap

- [ ] Pisah CSS/JS ke file eksternal (`style.css`, `main.js`)
- [x] Tambah `index.html` sebagai entry point utama
- [ ] Mode terang / gelap (theme toggle)
- [ ] Integrasi backend waitlist (Formspree / Supabase)
- [ ] Optimasi performa mobile (kurangi particle count otomatis)
- [ ] SEO meta + Open Graph image

Kontribusi welcome! Fork → buat branch → PR.

---

## 📄 Lisensi

MIT License — bebas dipakai untuk belajar, portofolio, maupun proyek komersial.

---

<p align="center">
  Dibuat dengan 💜 + Three.js<br/>
  <b>NEXUS Technologies — The future is spatial.</b><br/>
  © 2026
</p>
