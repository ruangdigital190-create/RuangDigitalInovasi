# RUANGDIGITAL190 — GitHub Pages (Versi 3)

Website katalog statis RUANGDIGITAL190 dengan desain neon-modern, daftar aplikasi berjalan yang bisa diklik, filter produk terpisah, daftar harga Diamond MLBB dan Free Fire, serta pemesanan WhatsApp.

## Fitur

- Katalog aplikasi premium: Netflix, CapCut, Canva, ChatGPT, Alight Motion, Gemini, Grammarly, dan QuillBot.
- Logo aplikasi/game tampil di setiap kartu dan di carousel berjalan.
- Carousel aplikasi bergerak otomatis, bisa diklik untuk membuka detail paket, dan berhenti saat diarahkan mouse.
- Filter katalog terpisah: Semua, Aplikasi Premium, Mobile Legends, dan Free Fire.
- Klik kartu Mobile Legends menampilkan hanya daftar harga Mobile Legends; klik Free Fire menampilkan hanya daftar harga Free Fire.
- Daftar harga MLBB: 25 nominal Diamond.
- Daftar harga Free Fire: 20 nominal Diamond + Membership Mingguan, BP Card, dan Membership Bulanan.
- Klik setiap nominal untuk membuat pesan WhatsApp yang menanyakan apakah stok paket masih tersedia.
- Popup detail paket aplikasi dengan tombol WhatsApp per paket.
- Tombol WhatsApp mengambang dapat diklik dan digeser.
- Metode pembayaran: GoPay, QRIS, DANA, SeaBank.
- Tidak ada keranjang belanja.
- Siap untuk GitHub Pages; tidak memerlukan framework atau build step.

## Nomor WhatsApp

Nomor toko disetel ke `6285725423328` (085725423328). Untuk menggantinya, edit `STORE.whatsapp` di bagian awal script `index.html`. Gunakan format kode negara tanpa `+`, spasi, atau tanda hubung.

## Mengubah data produk aplikasi

Di dalam `index.html`, cari `const APPS = [...]`. Setiap produk memiliki properti:

- `title`, `short`, `description`, `info`: teks yang tampil di katalog dan popup.
- `variants`: daftar paket yang muncul di popup.
- `logo`: sumber logo utama.
- `fallback`: logo lokal di folder `assets/logos/` jika gambar utama gagal dimuat.

Harga aplikasi premium belum ditampilkan sebagai angka karena daftar harga aplikasi belum diberikan. Pembeli diarahkan untuk menanyakan harga dan ketersediaan kepada admin.

## Mengubah harga Mobile Legends dan Free Fire

Cari bagian:

- `const MLBB_PRICES = [...]`
- `const FREEFIRE_PRICES = [...]`
- `const FREEFIRE_MEMBERSHIPS = [...]`

Contoh format:

```js
{ "amount": 30, "price": 11000 }
```

`price` ditulis sebagai angka rupiah tanpa titik. Contoh `11000` akan tampil sebagai `Rp11.000`.

## Logo dan sumber

Logo dipakai untuk mengidentifikasi produk pada katalog, bukan untuk menyatakan afiliasi atau kemitraan.

- Alight Motion: ikon aplikasi dari listing Google Play resmi Alight Motion.
- Free Fire: ikon pendek (short logo) dari halaman aset merek resmi Garena Free Fire.
- Mobile Legends: menggunakan logo oranye-emas versi terbaru yang diperkenalkan MOONTON pada Desember 2024. Referensi visual logo: aset gambar pada halaman Alejandrawr; pengumuman pembaruan logo oleh MOONTON diberitakan pada Desember 2024. Logo tetap merupakan merek dagang MOONTON.
- Logo aplikasi lain memakai ikon merek dari Simple Icons atau favicon domain resmi jika tidak tersedia di Simple Icons.

Merek dan logo merupakan milik masing-masing pemegang hak. RUANGDIGITAL190 adalah katalog independen dan tidak menyatakan adanya afiliasi resmi dengan pemilik merek tersebut.

## Struktur repository

```text
ruangdigital190/
├── index.html
├── README.md
├── .nojekyll
├── robots.txt
└── assets/
    ├── ruangdigital-logo.png
    └── logos/
        ├── netflix.svg
        ├── capcut.svg
        ├── canva.svg
        ├── chatgpt.svg
        ├── alightmotion.svg
        ├── gemini.svg
        ├── grammarly.svg
        ├── quillbot.svg
        ├── mlbb.svg
        ├── freefire.svg
        └── ruangdigital-favicon.svg
```

## Upload ke GitHub

1. Buat repository bernama `ruangdigital190` di https://github.com.
2. Ekstrak ZIP dan unggah **seluruh isi folder**, termasuk folder `assets`.
3. Klik **Commit changes**.
4. Buka **Settings → Pages**.
5. Pilih **Deploy from a branch**, branch `main`, folder `/(root)`, lalu klik **Save**.
6. Tunggu sampai GitHub Pages menampilkan URL website.

## Memperbarui harga dan stok

Edit file `index.html`, ubah array harga atau data aplikasi, lalu commit perubahan ke GitHub. Website ini statis; perubahan pada file lokal tidak akan tampil di website publik sampai diunggah/commit ke repository.

Sebelum pembayaran, pembeli tetap perlu mengonfirmasi ketersediaan paket dan memastikan User ID/Zone ID atau Player ID benar. Jangan meminta password akun game.
