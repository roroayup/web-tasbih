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

## Pratinjau (GitHub Pages)
https://roroayup.github.io/web-tasbih/ — aktifkan sekali di Settings → Pages → Source: **GitHub Actions**.

## Hosting (Firebase)
Live: **https://portfolio-tasbih.web.app** (project Firebase: `portfolio-tasbih`)

Deploy manual: `npx firebase-tools deploy --only hosting`

### Deploy otomatis (GitHub Actions)
Workflow `firebase-hosting.yml` deploy setiap push ke `main`, tapi dilewati selama
secret `FIREBASE_SERVICE_ACCOUNT` belum diset. Untuk mengaktifkan:

1. Buat service account: `firebase init hosting:github` atau
   Google Cloud Console (project `portfolio-tasbih`) → IAM → Service Accounts → key JSON
   (role *Firebase Hosting Admin*).
2. Simpan isi JSON sebagai secret repo `FIREBASE_SERVICE_ACCOUNT`.

Untuk deploy ke project lain, ubah `.firebaserc` atau set repository variable `FIREBASE_PROJECT_ID`.
