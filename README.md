# Tugas_APBO A_Class Diagram_Use Case_Entity Relation Diagram Daycare

## Latar Belakang
Daycare adalah layanan yang menyediakan perawatan dan pengawasan bagi anak-anak usia bayi 
hingga pra sekolah saat orang tua atau wali mereka bekerja ataupun memiliki keperluan lain.
Layanan utama daycare secara garis besar meliputi penyediaan kebutuhan anak makan, minum, 
tidur siang, dan mengganti popok. Menawarkan aktivitas bermain dan belajar yang sesuai dengan 
usia anak untuk mendukung perkembangan kognitif, fisik, sosial, dan emosional. Memastikan 
lingkungan yang aman dan terlindungi bagi anak-anak. Menyediakan makanan dan minuman yang 
sehat dan bergizi. Menjaga kebersihan lingkungan dan menerapkan praktik kesehatan yang baik 
untuk mencegah penyebaran penyakit.

## Class Diagram 
www.plantuml.com/plantuml/png/TPJ13jCm38RlVOgeN82f4rntsiHE20c9xJvPZKdDt6nAt4qJujt96Z1PQK-JlxhDrzzUjr4WoD1prJB4QBu6yEuuWFbP6RCYU_eBDeQyF9c7FXK72UHTgXlW1AGaWepNYoyHza1SW5L0Hr4mVEg8xTjtJpHSBGZkKL9hpEX6U1yx3cs7Tc2Su6_fd209_gh--EyydDKTKh7eBOvFt8MDsOFW_8lClRv3KSKvQpKv27nNavYAHPFh9LAaoS4_mDw1zPw0xINOdGXw2xuTWr3Q2jr87fcr0K7m_sG-ZmzKeydpEmWl1dSuot3g1uQ4ZzJZFnYHCPRuZ8v0m9Vp1LlEJ7CgMCwo06hw1P8x-57rJLBbNAkhW7SEM2UtcWfare6by0ARoKuqvMJCJF0Qvnw87vgfud89TJFBwFNlL7-iJTEO-iDw_RxEMxen7SGgZqMlfvznSVB5iU_bLWqdDuozImtPKOzOQYFVyc1JtnQzVNu9VWC0

### Penjelasan Class Diagram
OrangTua:
Atribut: id_OrangTua, nama, alamat, telepon, email
Metode:
registerChild(): Mendaftarkan anak.
updateDetails(): Memperbarui detail orang tua.
viewChildSchedule(): Melihat jadwal kegiatan anak.
viewChildReport(): Melihat laporan harian anak.

Anak:
Atribut: id_anak, nama, tgl_lhr, alamat, id_OrangTua
Metode:
getDetails(): Mendapatkan detail anak.
updateDetails(): Memperbarui detail anak.

Staf:
Atribut: id_staf, nama, posisi, id_jadwal
Metode:
recordAttendance(): Mencatat kehadiran anak.
recordActivity(): Mencatat kegiatan harian anak.
createReport(): Membuat laporan harian.

Jadwal:
Atribut: id_jadwal, hari, waktu_mulai, waktu_selesai, kegiatan
Metode:
addSchedule(): Menambah jadwal.
updateSchedule(): Memperbarui jadwal.
getSchedule(): Mendapatkan jadwal.

Laporan:
Atribut: id_laporan, tanggal, kegiatan, kehadiran, id_anak, id_staf, id_jadwal
Metode:
createDailyReport(): Membuat laporan harian.
createChildReport(): Membuat laporan harian anak.
viewReport(): Melihat laporan.

## Use Case
www.plantuml.com/plantuml/png/TPFDQiCm48JlUeebTqFi_FTG4XBeiILfUb-aRIBgoa5QD-JjQs4Lox9xCJEU3u-qhBUEqNBzNGgKN5bujMWkxpK6kpFu5UI9yLE8sf54Hp0vqaKx9WlxgoxL1D31UPzt-Vcca0dUq99XE12ZBbt0YWxxq7HlFm4dUILLbnIWsIXqf5jbEI3p3daX3aI_Qf6UQ9HQnlUIbLMmOoQZq4WAo6g8IDO_cXy1M7V0tf9lEZGDZ_w9DoaqTgrysb4xDHXCFfnoIXJzmQHnCjgaVIx4tnP0blatYIyIFqlyNFYrQVKYqalXTwZLgqYl8xs9T3wDJHwR8ZQpoFZJDq_8L7KtsRDlXIVGHfQr8jT4goZQzAFrVv7Oab7-7_a5

### Penjelasan Use Case
- Aktor "OrangTua" memiliki use cases untuk mendaftarkan anak, memperbarui detail orang tua, melihat jadwal anak, dan melihat laporan anak.
- Aktor "Anak" memiliki use cases untuk mendapatkan detail anak dan memperbarui detail anak.
- Aktor "Staf" memiliki use cases untuk mencatat kehadiran, mencatat aktivitas, membuat laporan harian, membuat laporan anak, menambahkan jadwal, memperbarui jadwal, mendapatkan jadwal, dan melihat laporan.
- Beberapa use cases memiliki hubungan "includes" karena mereka terkait erat dalam fungsionalitasnya.

## Entity-Relation Diagram
![erd daycare](https://github.com/FarhanRamadhan23/Tugas-APBO-erd-usecase-class-diagram/assets/167953699/6901484c-b099-484c-8fdd-0a1481af2327)

### Penjelasan ERD
Relasi:
Orang Tua memiliki banyak Anak: Setiap orang tua dapat memiliki banyak anak.
Anak dimiliki oleh satu Orang Tua: Setiap anak hanya memiliki satu orang tua.
Anak memiliki banyak Laporan: Setiap anak dapat memiliki banyak catatan laporan.
Staf membuat banyak Laporan: Setiap staf dapat membuat banyak laporan.
Laporan dibuat oleh satu Staf: Setiap laporan hanya dibuat oleh satu staf.
Jadwal memiliki banyak Kegiatan: Setiap jadwal dapat memiliki banyak kegiatan.
Kegiatan dimiliki oleh satu Jadwal: Setiap kegiatan hanya dimiliki oleh satu jadwal.
