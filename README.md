# KasirPro Appflow-ready v2

Versi ini memperbaiki masalah build awal Appflow:
- menambahkan `package-lock.json` agar `npm ci` tidak gagal,
- mengganti konfigurasi Capacitor ke `capacitor.config.json` agar tidak butuh TypeScript.

## Upload ke GitHub
Upload seluruh isi folder ini ke root repository.

## Build di Appflow
- Platform: Android
- Build type: Debug
- Build command: `npm install && npm run build`
- Web directory: `www`

## Catatan
Jika setelah ini Appflow masih meminta platform Android native, langkah berikutnya adalah menambahkan folder `android/` ke repo.
