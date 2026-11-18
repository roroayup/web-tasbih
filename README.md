# web-tasbih

Penghitung tasbih digital dengan bacaan dzikir yang bisa ditulis sendiri.

## Fitur
- Ketuk lingkaran untuk menambah hitungan; tombol − untuk mengurangi
- Target hitungan (33, 99, 100, 1000, atau angka bebas) dan langkah +1/+3/+5/+10
- Ikon pensil: pilih bacaan atau tulis bacaan sendiri (teks Arab, latin, arti, target)
- Penghitung putaran (ikon ↺), getar saat target tercapai
- Ikon mata: sembunyikan angka agar fokus berdzikir
- Tersimpan otomatis di perangkat (localStorage), bisa dipasang sebagai aplikasi (PWA)
- Keyboard: Spasi/Enter untuk tambah, Backspace untuk kurang

## Hosting (Firebase)
Deploy otomatis lewat GitHub Actions setiap push ke `main`.

1. Buat project Firebase (ID default: `web-tasbih`; kalau berbeda, ubah `.firebaserc`
   atau set repository variable `FIREBASE_PROJECT_ID`).
2. Buat service account: `firebase init hosting:github` atau
   Google Cloud Console → IAM → Service Accounts → key JSON (role *Firebase Hosting Admin*).
3. Simpan isi JSON sebagai secret repo `FIREBASE_SERVICE_ACCOUNT`.

Deploy manual: `npx firebase-tools deploy --only hosting`
