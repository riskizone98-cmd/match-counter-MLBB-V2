# Match Counter MLBB — KYY VJESTT

Proyek Android WebView yang membungkus HTML Match Counter MLBB V4 menjadi aplikasi Android. HTML asli disimpan di `app/src/main/assets/index.html`.

## Cara mendapatkan APK lewat GitHub
1. Buat repository baru di GitHub.
2. Upload seluruh isi folder proyek ini ke repository (bukan folder ZIP di dalam repository).
3. Buka tab **Actions** dan pilih workflow **Build Android APK**.
4. Jika workflow belum berjalan otomatis, tekan **Run workflow**.
5. Tunggu sampai status selesai dengan tanda centang hijau.
6. Buka hasil run workflow, unduh artifact **MatchCounterMLBB-APK**, lalu ekstrak ZIP.
7. Instal `app-debug.apk` di HP Android. Jika diminta, izinkan instalasi dari sumber tersebut.

Workflow juga otomatis membuat APK setiap kali ada push ke branch `main` atau `master`.

## Build lokal
Gunakan Android Studio dengan JDK 17 dan Android SDK Platform 35, lalu buka folder proyek ini dan jalankan task `app > Tasks > build > assembleDebug`.

Package: `id.kyyvjestt.matchcounter`  
Versi: `1.0` (debug APK)


## Fitur pembekuan pelanggan

Setiap pelanggan memiliki tombol **Bekukan/Aktifkan**. Pelanggan yang dibekukan tidak akan terkena pengurangan match per pelanggan maupun pengurangan massal, dan penghitung match tetap tersimpan. Status beku juga tersimpan di perangkat.


## Fitur versi 5 (2 room)
- Dua room ditampilkan berdampingan dalam satu layar.
- Setiap room memiliki pelanggan, statistik, pengurangan massal, dan undo yang terpisah.
- Status pelanggan dibekukan tersimpan dan tidak ikut pengurangan massal.
- Data versi sebelumnya dimigrasikan otomatis ke Tim 1 / Room 1.
