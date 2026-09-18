# Kas RT-01, Kiyaran, Gombang

Aplikasi laporan kas RT berbasis GitHub Pages + Firebase.

## Yang perlu dilakukan
1. Buat project Firebase.
2. Aktifkan Authentication > Email/Password.
3. Buat 1 akun bendahara.
4. Buat Firestore Database.
5. Pasang isi `firestore.rules` pada Rules Firestore.
6. Daftarkan Web App Firebase.
7. Salin konfigurasi Firebase ke `app.js`.
8. Upload semua file ke repository GitHub.
9. Aktifkan GitHub Pages.

## Catatan keamanan
Jangan menyimpan password di source code. File `app.js` hanya berisi konfigurasi web Firebase. Hak perubahan data ditentukan oleh Firestore Security Rules.

Untuk produksi, lebih ketat lagi: gunakan Custom Claims/role `bendahara` pada akun bendahara, lalu ubah rules agar hanya role tersebut yang boleh write.
