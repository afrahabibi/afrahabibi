# 🚀 Panduan Setup & Deploy GitHub Profile README

Berikut panduan langkah demi langkah untuk mengunggah dan mengaktifkan GitHub Profile README ke akun GitHub Anda (**@afrahabibi**).

---

## 📌 Prasyarat: Buat Repository Khusus GitHub Profile

1. Buka browser dan login ke GitHub Anda: [https://github.com](https://github.com)
2. Klik tombol **New Repository** (atau buka [https://github.com/new](https://github.com/new)).
3. Pada kolom **Repository name**, ketikkan nama username GitHub Anda persis sama:
   ```text
   afrahabibi
   ```
4. Pastikan repository diatur ke **Public** (Penting: GitHub Profile README hanya muncul jika repository bersifat Public).
5. Jangan centang "Add a README file" (karena kita sudah membuat README.md lengkap di lokal).
6. Klik **Create repository**.

---

## 💻 Langkah 1: Inisialisasi Git & Push dari Lokal

Buka terminal (PowerShell atau Git Bash) di folder `D:\about me\afrahabibi`, lalu jalankan perintah berikut:

```powershell
cd "D:\about me\afrahabibi"

# Inisialisasi git repository lokal
git init

# Pastikan branch utama bernama main
git branch -M main

# Tambahkan seluruh file (README.md, .github/workflows, assets)
git add .

# Buat initial commit
git commit -m "feat: setup premium animated cyberpunk github profile readme"

# Hubungkan dengan remote repository GitHub Anda
# (Ganti URL jika menggunakan SSH)
git remote add origin https://github.com/afrahabibi/afrahabibi.git

# Push ke GitHub
git push -u origin main
```

---

## ⚙️ Langkah 2: Konfigurasi Permissions GitHub Actions (Wajib untuk Animasi Snake & Pacman)

Agar GitHub Actions memiliki izin untuk menulis (*write permissions*) file animasi SVG ke branch `output`, aktifkan pengaturan berikut di repository GitHub Anda:

1. Di repository `github.com/afrahabibi/afrahabibi`, klik tab **Settings** (di menu atas).
2. Di sidebar sebelah kiri, klik **Actions** -> **General**.
3. Gulir ke bawah ke bagian **Workflow permissions**.
4. Pilih opsi:
   - ✅ **Read and write permissions**
   - ✅ Centang **Allow GitHub Actions to create and approve pull requests**
5. Klik **Save**.

---

## 🕹️ Langkah 3: Jalankan GitHub Actions Pertama Kali

Workflow otomatis akan berjalan setiap hari Sabtu pukul 21:00 UTC, namun untuk menampilkan animasi Snake & Pacman langsung pertama kali:

1. Di repository `github.com/afrahabibi/afrahabibi`, klik tab **Actions**.
2. Di sebelah kiri, klik workflow **Generate Contribution Animations**.
3. Klik tombol dropdown **Run workflow** di sebelah kanan.
4. Pilih branch `main`, lalu klik tombol hijau **Run workflow**.
5. Tunggu sekitar 1–2 menit hingga workflow berstatus hijau centang (Success).
6. GitHub Actions akan secara otomatis membuat branch baru bernama `output` yang berisi `github-snake-dark.svg` dan `pacman-contribution-graph-dark.svg`.
7. Refresh halaman profil utama GitHub Anda (`https://github.com/afrahabibi`), dan seluruh animasi akan menyala sempurna!

---

## 🎨 Kustomisasi Cepat

- **Ganti Bio & Fokus:** Edit bagian `[SYSTEM.BIO]` di `README.md`.
- **Ganti Tech Stack:** Tambahkan atau kurangi query icon di parameter `i=...` pada link `skillicons.dev`.
- **Update Link Proyek:** Ganti URL pada bagian `[PROJECTS.DASHBOARD]` dengan repository asli proyek Anda.
