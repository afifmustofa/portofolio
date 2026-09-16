# Portofolio — Ahmad Al Afif

Website portofolio statis (HTML/CSS/JS murni, tanpa build tools) siap di-deploy ke GitHub Pages.

## Isi folder

- `index.html` — struktur halaman
- `style.css` — semua styling
- `script.js` — menu mobile & filter portofolio
- `photo.png` — foto profil (dipakai di hero & about)
- `konsulin-cover.jpg` — screenshot cover untuk kartu portofolio Konsulin

## Cara publish ke GitHub Pages

1. Buat repository baru di GitHub, misalnya `afif-porto`.
2. Upload semua file di atas ke root repository:
   ```
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/USERNAME/afif-porto.git
   git push -u origin main
   ```
3. Buka **Settings > Pages** di repository.
4. Pada **Source**, pilih branch `main` dan folder `/ (root)`, lalu **Save**.
5. Tunggu 1-2 menit, website akan aktif di:
   `https://USERNAME.github.io/afif-porto/`

## Catatan penting: preview website di kartu Portofolio

6 kartu portofolio (Fugui Construction, BMArtha Global, Bouqetwe Florist, Archapadma, Unibyte Solutions, Gudang Mebel) menampilkan **live preview** situs asli lewat `<iframe>` yang di-scale kecil — bukan gambar statis. Ini akan tampil normal begitu file di-hosting di GitHub Pages (tidak ada batasan seperti di sandbox preview Claude).

**Namun** ini hanya berhasil jika situs tujuan **tidak memblokir embedding** (lewat header `X-Frame-Options` atau plugin keamanan WordPress seperti Wordfence). Kalau setelah publish ada kartu yang tampil kosong/putih, kemungkinan situs tersebut memblokirnya. Solusinya:
1. Cek dan nonaktifkan opsi "prevent framing"/X-Frame-Options di plugin keamanan situs tersebut, **atau**
2. Ganti `<iframe>` pada kartu itu dengan `<img>` memakai screenshot statis (seperti yang dipakai pada kartu Konsulin).

## Yang perlu disesuaikan

- Ganti alamat email di bagian Kontak (`index.html`, cari `mailto:`) kalau mau pakai email pribadi (`afif.ahmad02@gmail.com`) alih-alih email agensi.
- Tambah/kurangi kartu portofolio di section `#portofolio` sesuai kebutuhan.
- Kategori filter portofolio bisa ditambah dengan mengganti nilai `data-filter` dan `data-cat`.
