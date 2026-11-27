# ZAYMAR BUMBU — Starter Landing Page

Starter ini berisi landing page responsif dan kerangka dashboard admin berbasis Decap CMS.

## Isi
- `index.html`, `styles.css`, `app.js`: website publik.
- `content/products.json`: data katalog yang dibaca website.
- `admin/`: panel admin Decap CMS.
- `uploads/`: folder foto yang akan dibuat saat upload pertama melalui CMS.

## Sebelum deploy
1. Buat akun GitHub dan repository baru bernama misalnya `zaymar-bumbu`.
2. Upload seluruh isi folder ini ke branch `main`.
3. Edit `admin/config.yml`: repository sudah disiapkan sebagai `zaymarspices-cell/zaymar.bumbu`. Nama proyek Cloudflare Pages `zaymar-bumbu` dan URL OAuth Worker masih perlu disesuaikan setelah akun Cloudflare dibuat.
4. Edit `app.js`: nomor WhatsApp sudah diatur ke `6285218267489` (berasal dari 0852 1826 7489).
5. Sesuaikan Instagram di `app.js`.
6. Hubungkan repository ke Cloudflare Pages. Untuk starter HTML statis ini, gunakan build command kosong dan output directory `/` (root repository).
7. Siapkan GitHub OAuth App dan OAuth proxy Worker untuk Decap CMS. Jangan menaruh GitHub Client Secret di file frontend atau repository. Simpan sebagai Secret di Cloudflare Worker.

## Catatan autentikasi admin
Decap CMS GitHub backend memerlukan OAuth server/proxy. File `admin/config.yml` sudah menyediakan lokasi konfigurasi `base_url`, tetapi OAuth Worker belum disertakan atau dikonfigurasi karena harus dibuat khusus untuk GitHub OAuth App dan domain proyek Anda. Jangan membuka dashboard admin ke publik sebelum autentikasi selesai diuji.

## Cara kerja katalog
Admin mengubah `content/products.json` dan mengunggah foto ke `uploads/` di GitHub. Setiap perubahan masuk sebagai commit; Cloudflare Pages akan membangun ulang / menerbitkan versi terbaru setelah push.

## Penting
- Harga `0` ditampilkan sebagai "Tanya harga". Ganti dengan harga sebenarnya.
- Foto contoh belum disertakan; masukkan foto kemasan asli ZAYMAR melalui dashboard setelah CMS aktif.
- URL `*.pages.dev` gratis tersedia setelah proyek dibuat di Cloudflare Pages; nama proyek harus tersedia.


## Informasi brand awal
- Nama: ZAYMAR BUMBU
- Slogan: Racikan Rempah Pilihan, Cita Rasa Istimewa
- WhatsApp: 6285218267489
- Instagram: @zaymarbumbu
