# KasirPro Appflow-ready

Project ini sudah disiapkan agar bisa diupload ke GitHub lalu dihubungkan ke **Ionic Appflow** untuk build APK Android di cloud.

## Struktur
- `www/index.html` → file web app KasirPro terbaru
- `package.json` → dependency Capacitor
- `capacitor.config.ts` → konfigurasi app Android
- `ionic.config.json` → supaya dikenali oleh Ionic/Appflow

## Cara pakai di Appflow

### 1. Upload ke GitHub
- Buat repository baru di GitHub, misalnya: `kasirpro-app`
- Upload semua isi folder ini ke repository tersebut

### 2. Hubungkan ke Ionic Appflow
- Buka [https://ionic.io/appflow](https://ionic.io/appflow)
- Buat app baru
- Connect ke repository GitHub Anda
- Framework type: **Capacitor / Custom**

### 3. Konfigurasi build
Build command:
```bash
npm install
npm run build
```

Web directory:
```bash
www
```

### 4. Tambahkan Android platform
Appflow akan membaca konfigurasi Capacitor. Bila perlu, jalankan langkah init platform lokal sekali sebelum push final:
```bash
npm install
npx cap add android
```
Lalu commit folder Android bila Appflow workflow Anda membutuhkannya.

### 5. Build APK di Appflow
- Pilih Android build
- Pilih debug build untuk uji coba awal
- Jalankan build
- Download APK hasilnya

## Catatan
- Ini **Appflow-ready**, tapi beberapa workflow Appflow lebih stabil jika folder `android/` sudah pernah di-generate sekali.
- Untuk tahap awal, Anda bisa generate `android/` lokal sekali, commit, lalu Appflow build sisanya.
- Tahap berikutnya untuk printer Bluetooth adalah menambahkan plugin ESC/POS Android.
