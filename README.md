# Catatan Rilis — CKG Sekolah Auto Input

Catatan perubahan ekstensi Chrome **CKG Sekolah Auto Input** untuk operator.

Baca versi rapinya di: https://ryanadip2601.github.io/ckg-catatan-rilis/

## v0.30.0 — Input Pemeriksaan CKG Sekolah
- Menu baru **Input Pemeriksaan**: rekam formulir jadi template Excel, isi hasilnya, lalu ekstensi mencari peserta, mengisi tiap layanan, menekan Kirim, dan Selesaikan Layanan.
- Pertama kali dibuka, Chrome meminta izin `form.kemkes.go.id` (halaman formulir pemeriksaan). Tekan Izinkan.
- Sekolah, Kelas, dan Tanggal Pemeriksaan dipilih di panel. Peserta yang tidak ditemukan dilewati; bisa **Lanjutkan** setelah jeda.
- Halaman CKG dimuat ulang otomatis bila macet atau panel tidak terhubung.

## v0.29.0 — Login dengan email pembelian
- Kode 6 angka dikirim ke email pembelian; satu langganan aktif di satu Chrome (login di Chrome lain mengambil alih).
- Tombol Keluar. Kode lisensi lama tetap berlaku.

## v0.28.1 — Panel tidak lagi macet di "Halaman belum siap"
- Bila sambungan ke halaman terputus, panel meminta refresh tab CKG (F5) dengan pesan yang jelas.
- Tombol **Muat ulang ekstensi** (di bawah status) dan **Muat ulang** (di bawah panel): ekstensi dimuat ulang lalu tab CKG di-refresh otomatis. Ditolak saat proses sedang berjalan.
- Mode Konfirmasi Hadir tidak lagi meminta file Excel.
- Pertama kali memasang: buka `chrome://extensions`, tekan Reload, lalu F5 di tab CKG.

## v0.28.0 — Copas langsung ke template
- Template boleh diisi dengan copas dari file Excel lain; ekstensi menyesuaikan format saat diunggah.
- Tanggal lahir: `26-01-1992`, `26 Januari 1992`, tanggal Excel, bahkan `Balikpapan, 26-01-1992` (hanya tanggalnya yang diambil).
- NIK dibersihkan dari tanda petik, spasi, titik, dan strip.
- Ditolak dengan alasan jelas: dua tanggal dalam satu sel, sel tanpa tanggal, serta NIK/WhatsApp yang sudah berubah menjadi angka (digitnya hilang di file sumber).
