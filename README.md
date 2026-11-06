# SiHadir - Sistem Absensi Siswa Online Berbasis Lokasi GPS
SMP Negeri 2 Wanadadi, Banjarnegara, Jawa Tengah

Aplikasi Android untuk manajemen presensi siswa berbasis lokasi GPS dan validasi selfie.

## Fitur Utama

1. **Role Administrator (Aksen Biru)**
   - Kelola Data Siswa, Data Kelas (9A - 9G), dan Data Guru Piket.
   - Pengaturan Profil Sekolah dan Titik Koordinat GPS Sekolah beserta Radius Presensi.
   - Pengaturan Jam Absen (Mulai Masuk, Batas Tepat Waktu, Tutup Masuk, Mulai Pulang, Tutup Pulang) menggunakan MaterialTimePicker.
   - Laporan Presensi per Kelas (Harian, Mingguan, Bulanan, Tahunan).
   - Ekspor Laporan ke PDF dengan kop surat resmi dan tanda tangan Kepala Sekolah.
   - Pengelolaan permintaan reset password siswa dan guru.

2. **Role Guru Piket (Aksen Hijau)**
   - Pemantauan kehadiran siswa hari ini secara real-time per kelas.
   - Identifikasi daftar siswa yang belum melakukan presensi.
   - Pencatatan Izin atau Sakit secara langsung untuk siswa dengan keterangan wajib.
   - Laporan dan ekspor dokumen PDF.

3. **Role Siswa (Aksen Oranye / Teal)**
   - Pemantauan jam digital dan status lokasi GPS terhadap radius sekolah secara langsung.
   - Presensi Masuk dengan pengambilan foto selfie dan validasi radius otomatis.
   - Penentuan status Hadir atau Terlambat secara otomatis oleh sistem berdasarkan waktu presensi.
   - Presensi Pulang dengan pengambilan foto selfie dalam rentang waktu yang telah ditentukan.
   - Pengajuan Izin atau Sakit mandiri dengan keterangan wajib.
   - Riwayat dan rekap presensi pribadi (Harian, Mingguan, Bulanan, Tahunan).
   - Ekspor rekap kehadiran pribadi ke dokumen PDF.

## Spesifikasi Teknis

- Bahasa: Kotlin
- Antarmuka: XML dengan View Binding
- Arsitektur: MVVM (ViewModel, LiveData, Coroutine)
- Autentikasi & Database: Firebase Authentication, Cloud Firestore, Firebase Storage
- Layanan Lokasi: Google Play Services Location (FusedLocationProviderClient)
- Ekspor Dokumen: android.graphics.pdf.PdfDocument bawaan Android
- Minimum SDK: 24 (Android 7.0)
- Target SDK: 36 (Android 16)
- Package Name: com.smpn2wanadadi.sihadir
- Versi: 1.0.0 (versionCode 1)

## Konfigurasi Firebase

1. Masukkan berkas `google-services.json` ke dalam direktori `app/`.
2. Aktifkan Authentication dengan penyedia Email/Password di Firebase Console.
3. Buat database Cloud Firestore dan terapkan aturan pada berkas `firestore.rules`.
4. Buat bucket Firebase Storage dan terapkan aturan pada berkas `storage.rules`.
