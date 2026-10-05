# 🐍 Retro Cyber Snake Game

Sebuah game ular klasik arcade dengan estetika **Cyber Neon Dark** modern, dibangun sepenuhnya mandiri dalam satu file HTML (`index.html`) tanpa dependensi pustaka luar. 

Dirancang dengan pendekatan **Mobile-First**, responsif di semua ukuran layar (Smartphone & Desktop), mendukung kontrol sentuh (Touch D-pad & Swipe) serta Keyboard (Arrow Keys & WASD).

---

## 🎮 Fitur Utama

- **Mobile-First & Responsif Penuh:** Canvas permainan otomatis terpusat (*centered*) dan menyesuaikan rasio layar HP maupun monitor desktop tanpa distorsi atau zooming.
- **Kontrol Fleksibel (Multi-Input):**
  - **Layar Sentuh (Smartphone):** D-pad virtual ergonomis di bawah arena + dukungan gestur *Swipe* langsung di area canvas.
  - **Desktop:** Tombol Panah (`↑`, `↓`, `←`, `→`) dan `W`, `A`, `S`, `D`.
  - **Jeda & Lanjut:** Tombol `Spasi` atau `P`.
- **Sistem Skor & High Score Permanen:** Skor tertinggi tersimpan secara lokal di browser (`localStorage`) sehingga tidak hilang saat halaman di-refresh.
- **Akselerasi Kecepatan Progresif:** Kecepatan dan level permainan meningkat setiap kali memakan apel neon.
- **Efek Visual & Audio 8-Bit:**
  - Partikel percikan neon dan apel berdenyut (*pulse glow*).
  - Efek suara sintetis retro menggunakan Web Audio API tanpa file audio eksternal.
  - Tombol toggle Suara (Mute / Unmute).
- **Siklus Permainan Tanpa Bug:** Alur *Ready*, *Playing*, *Paused*, hingga *Game Over* dengan pembersihan state yang sempurna saat *Restart*.

---

## 🚀 Cara Menjalankan Secara Lokal

1. **Unduh atau Clone repositori ini:**
   ```bash
   git clone https://github.com/<username>/myfirstgame.git
   cd myfirstgame
   ```
2. **Buka file `index.html`:**
   - Cukup klik ganda (*double-click*) file `index.html` di File Explorer, atau
   - Buka menggunakan ekstensi *Live Server* di VS Code / IDE pilihan Anda.

---

## 🌐 Panduan Deployment

### 1. Upload ke GitHub (Public Repository)
```bash
git init
git add .
git commit -m "feat: initial commit classic snake game"
git branch -M main
git remote add origin https://github.com/<username>/myfirstgame.git
git push -u origin main
```

### 2. Deploy ke Vercel (Gratis & Otomatis)
1. Buka [vercel.com](https://vercel.com) dan login dengan akun GitHub Anda.
2. Klik tombol **"Add New..."** -> **"Project"**.
3. Pilih repositori `myfirstgame` dari daftar repositori GitHub Anda.
4. Karena proyek ini adalah *pure static HTML*, biarkan seluruh pengaturan default (Framework Preset: *Other*).
5. Klik **"Deploy"**. Dalam beberapa detik situs game Anda akan online dengan domain gratis seperti `https://myfirstgame.vercel.app`.

### 3. Deploy ke Firebase Hosting
1. Install Firebase CLI jika belum:
   ```bash
   npm install -g firebase-tools
   ```
2. Login dan inisialisasi:
   ```bash
   firebase login
   firebase init hosting
   ```
   - Pilih *Use an existing project* atau *Create a new project*.
   - Saat ditanya *What do you want to use as your public directory?*, ketik `.` (folder saat ini tempat `index.html` berada).
   - *Configure as a single-page app?* -> Pilih `No` (atau `Yes`).
3. Deploy ke cloud:
   ```bash
   firebase deploy --only hosting
   ```

---

## 📄 Lisensi
Proyek ini bersifat open-source di bawah lisensi MIT.
