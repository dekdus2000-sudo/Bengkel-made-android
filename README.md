# Bengkel Made Android

Aplikasi Android pembungkus Bengkel Made dan penerima menu Bagikan untuk PDF, foto, video, dokumen, dan teks.

- Tampil sebagai **Bengkel Made** pada menu Bagikan Android.
- Menerima maksimal 5 berkas sekaligus, masing-masing maksimal 25 MB.
- Menyalin berkas ke penyimpanan sementara aplikasi agar izin file dari My Bisnis/Galeri tidak hilang.
- Memasukkan berkas ke antrean IndexedDB `bm-share-v1`; halaman Bagikan Cepat memprosesnya saat internet tersedia.
- Memuat ulang otomatis ketika jaringan kembali aktif.

Build otomatis tersedia melalui GitHub Actions. Hasilnya bernama `Bengkel-Made-APK`.


## Perbaikan v1.1.4
- Mencegah file Bagikan ganda dari EXTRA_STREAM/ClipData.
- Antrean share tidak dianggap selesai sebelum IndexedDB benar-benar tersimpan.
- Menambahkan penanda kompatibilitas localStorage + event untuk halaman web.
- Retry lebih aman ketika jaringan/WebView belum siap.


## Perbaikan v1.1.5
- Pemilih file WebView sekarang berfungsi untuk tombol unggah PDF/foto/dokumen pada halaman Bengkel Made.
- Share baru tidak lagi menghapus antrean lama yang belum tersimpan.
- Retry jaringan memprioritaskan antrean Bagikan Cepat tanpa reload yang tidak perlu.
- Network callback dilepas saat Activity ditutup untuk mencegah kebocoran lifecycle.
- Artifact GitHub Actions diperbarui ke v1.1.5.
