# 📘 Pertemuan 2 - Bootstrap 5

Project ini merupakan implementasi Bootstrap 5 yang mencakup:

- ✅ Navbar
- ✅ Hero Section
- ✅ Informasi Toko
- ✅ Grid System (row & col)
- ✅ Card Produk
- ✅ Form
- ✅ Flexbox
- ✅ Footer
- ✅ Bootstrap Icons (via npm)

---

# 🚀 Setup Bootstrap 5

Project ini menggunakan Bootstrap 5 via CDN.

Tambahkan di dalam `<head>`:

```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
<link rel="stylesheet" href="assets/css/bootstrap-icons.css">
---
```
# 🎨 Setup Bootstrap Icons (Menggunakan NPM)

Project ini menggunakan Bootstrap Icons yang di-install melalui npm.

## 1️⃣ Install Node.js

Download dan install Node.js terlebih dahulu:

https://nodejs.org/

Cek apakah sudah terinstall:

```bash
node -v
npm -v
```

## 2️⃣ Install Bootstrap Icons

Masuk ke folder project lalu jalankan:

```npm install bootstrap-icons```

Setelah berhasil, akan muncul folder:
```
node_modules/bootstrap-icons/
```
## 3️⃣ Copy File ke Project (WAJIB untuk HTML Biasa)

Karena project ini hanya menggunakan HTML (tanpa bundler seperti Vite/Webpack),
file dari node_modules tidak bisa langsung digunakan.

Buka folder berikut:
```
node_modules/bootstrap-icons/font/
```

Di dalamnya terdapat:
- bootstrap-icons.css
- folder fonts

Copy:
- File bootstrap-icons.css
- Folder fonts

Pindahkan ke dalam project sehingga menjadi:
```pert2/
│
├── index.html
│
└── assets/
    ├── css/
    │   └── bootstrap-icons.css
    └── fonts/
        ├── bootstrap-icons.woff
        └── bootstrap-icons.woff2
```
## 4️⃣ Perbaiki Path Font (PENTING)

Buka file:
```
assets/css/bootstrap-icons.css
```
Cari bagian ini:
```
url("./fonts/bootstrap-icons.woff2")
```
Ubah menjadi:
```
url("../fonts/bootstrap-icons.woff2")
```
Karena:
- CSS ada di assets/css/
- Fonts ada di assets/fonts/
Maka harus naik satu folder (../)
- CSS ada di assets/css/
- Fonts ada di assets/fonts/

Maka harus naik satu folder (../)
