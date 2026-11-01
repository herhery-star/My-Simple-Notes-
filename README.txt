LITTLE THINGS — PWA REBUILT
===========================

ISI PAKET
- index.html: aplikasi Little Things versi redesign fokus fungsi.
- manifest.json: identitas dan konfigurasi instalasi PWA.
- service-worker.js: cache offline dan pembaruan versi (v4).
- icons/: ikon PNG 192, PNG 512, maskable PNG 512, dan SVG.

INSTALASI / PEMBARUAN DI GITHUB PAGES
1. Ekstrak ZIP.
2. Upload SELURUH ISI folder ini ke root repository/folder publik yang digunakan.
   Pastikan index.html, manifest.json, service-worker.js, dan folder icons sejajar.
3. Pastikan GitHub Pages aktif dan situs dibuka melalui HTTPS.
4. Buka URL aplikasi di Chrome Android, muat ulang, lalu pilih menu Chrome > Install app
   atau Add to Home screen (label menu dapat berbeda).
5. Jika aplikasi lama sudah pernah dipasang:
   - Hapus shortcut/aplikasi Little Things lama dari layar utama.
   - Chrome > Setelan > Setelan situs > Semua situs > pilih domain GitHub Pages
     > Hapus & reset (ini juga dapat menghapus data situs lokal).
   - Buka ulang URL versi terbaru, tunggu halaman termuat, lalu instal kembali.

PENTING TENTANG DATA
- Daftar dan catatan tetap disimpan lokal pada browser/perangkat.
- Menghapus data situs dapat menghapus data aplikasi. Export JSON terlebih dahulu.
- Tidak ada integrasi Google Drive/database cloud pada paket ini.

PEMERIKSAAN
- Manifest menggunakan start_url dan scope relatif agar cocok untuk GitHub Pages
  baik di root domain maupun repository path.
- Ikon 192x192, 512x512, dan maskable 512x512 disertakan.
- Service worker memakai cache v4 agar cache lama diganti saat update.
- Offline fallback tersedia setelah kunjungan online pertama berhasil.
