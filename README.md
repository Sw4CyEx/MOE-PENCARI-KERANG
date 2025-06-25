# MOE PENCARI KERANG

Sebuah skrip PHP sederhana namun dengan tampilan menarik untuk membantu memindai file PHP yang mencurigakan (potensi shell backdoor) di direktori website Anda. Skrip ini dirancang dengan antarmuka pengguna yang lembut dan "moe", serta memiliki beberapa fitur untuk mempermudah identifikasi ancaman:

*   **Pemindaian Terfokus**: Hanya memindai file dengan ekstensi `.php`.
*   **Deteksi Berbasis Pola**: Menggunakan daftar pola string dan nama file yang umum ditemukan pada shell/backdoor.
*   **Kesadaran Joomla**: Mencoba untuk mengabaikan file inti Joomla Administrator untuk mengurangi false positive.
*   **Urutkan berdasarkan Tanggal Modifikasi**: Hasil pemindaian diurutkan berdasarkan tanggal modifikasi file terakhir (terbaru di atas), membantu menemukan file yang baru saja diunggah/diubah.
*   **Lihat Konten File**: Kemampuan untuk melihat konten file yang mencurigakan langsung dari antarmuka.
*   **Hapus File**: Tombol untuk menghapus file yang teridentifikasi (gunakan dengan sangat hati-hati!).
*   **Antarmuka Moe**: Tampilan yang lembut dan menarik secara visual.

## Disclaimer & Peringatan Sangat Penting!

⚠️ **RISIKO TINGGI! GUNAKAN DENGAN KEHATI-HATIAN EKSTREM!** ⚠️

Skrip ini memiliki kemampuan untuk **MENGHAPUS FILE** dari server Anda. Penggunaan yang salah, atau jika skrip ini diakses oleh pihak yang tidak berwenang, dapat menyebabkan **KERUSAKAN PARAH** pada website Anda, termasuk **KEHILANGAN DATA PERMANEN**.

*   🛑 **SELALU BACKUP WEBSITE ANDA SECARA KESELURUHAN** sebelum mengunggah atau menjalankan skrip ini.
*   🤔 **PAHAMI KODE**: Luangkan waktu untuk memahami cara kerja skrip ini sebelum menggunakannya.
*   🔬 **DETEKSI TIDAK SEMPURNA**: Metode deteksi berbasis pola bersifat dasar. Skrip ini **MUNGKIN TIDAK MENEMUKAN SEMUA ANCAMAN** dan **MUNGKIN MEMBERIKAN FALSE POSITIVE** (mendeteksi file aman sebagai berbahaya). Selalu verifikasi sebelum menghapus file.
*   🗑️ **HAPUS SETELAH DIGUNAKAN**: **SEGERA HAPUS SKRIP INI DARI SERVER ANDA** setelah selesai digunakan untuk menghindari penyalahgunaan.
*   🔑 **AMANKAN AKSES**: Jika Anda harus menyimpannya sementara di server, letakkan di direktori yang dilindungi kata sandi atau ubah namanya menjadi sesuatu yang tidak mudah ditebak.
*   👨‍💻 **BUKAN PENGGANTI PROFESIONAL**: Skrip ini adalah alat bantu dan bukan pengganti solusi keamanan siber profesional atau audit keamanan menyeluruh.

**Pengembang tidak bertanggung jawab atas kerusakan atau kehilangan data yang disebabkan oleh penggunaan atau penyalahgunaan skrip ini.**

## Cara Penggunaan

1.  **Unduh Skrip**: Unduh file `moe-pencari-kerang.php` (atau nama file terbaru dari repositori ini).
2.  **(SANGAT DISARANKAN)** **Backup Website Anda**: Buat backup lengkap dari semua file dan database website Anda.
3.  **Unggah Skrip**: Unggah file PHP tersebut ke direktori root website Anda, atau direktori lain yang dapat diakses melalui web.
    *   *Keamanan Tambahan*: Pertimbangkan untuk mengganti nama file menjadi sesuatu yang acak dan sulit ditebak (misalnya, `scan_utility_ab3x9z.php`).
4.  **Akses Melalui Browser**: Buka browser Anda dan navigasikan ke URL skrip tersebut (misalnya, `http://www.websiteanda.com/moe-pencari-kerang.php`).
5.  **Masukkan Path (Opsional)**: Secara default, skrip akan memindai direktori root dokumen web Anda. Anda dapat memasukkan path direktori spesifik yang ingin dipindai.
6.  **Pindai**: Klik tombol "Pindai Direktori".
7.  **Tinjau Hasil**:
    *   File yang terdeteksi sebagai mencurigakan akan ditampilkan dalam tabel.
    *   Hasil diurutkan berdasarkan tanggal modifikasi terakhir (terbaru di atas).
    *   Periksa kolom "Alasan" untuk mengetahui mengapa file tersebut ditandai.
8.  **Lihat Konten (Opsional & Hati-hati)**: Klik tombol "Lihat" untuk memeriksa konten file. Ini dapat membantu Anda memverifikasi apakah file tersebut benar-benar berbahaya.
9.  **Hapus File (SANGAT HATI-HATI!)**:
    *   Jika Anda **100% yakin** sebuah file berbahaya dan merupakan bagian dari serangan, Anda dapat menggunakan tombol "Hapus".
    *   Akan ada konfirmasi sebelum file dihapus secara permanen.
    *   **Jika ragu, JANGAN HAPUS.** Konsultasikan dengan ahli keamanan atau pulihkan dari backup.
10. **PENTING: HAPUS SKRIP INI**: Setelah selesai menggunakan alat ini, **SEGERA HAPUS FILE SKRIP INI DARI SERVER ANDA**. Meninggalkannya di server merupakan risiko keamanan.

## Persyaratan

*   Server web dengan PHP (direkomendasikan PHP 7.x atau lebih baru).
*   Izin baca pada direktori dan file yang akan dipindai.
*   Izin tulis pada file yang akan dihapus (jika menggunakan fitur hapus).

## Batasan

*   Deteksi hanya berdasarkan pola string dan nama file yang telah ditentukan. Mungkin tidak dapat mendeteksi shell yang sangat canggih atau diobfuscate dengan metode baru.
*   Tidak ada jaminan akan menemukan semua jenis malware atau backdoor.
*   Performa dapat menurun pada direktori dengan jumlah file yang sangat besar.
*   Pemeriksaan string Joomla bersifat dasar dan mungkin tidak mencakup semua variasi atau file dari ekstensi pihak ketiga.

## Kontribusi

Kontribusi untuk meningkatkan skrip ini sangat diharapkan! Jika Anda memiliki ide untuk:

*   Pola deteksi baru
*   Peningkatan performa
*   Fitur tambahan yang berguna
*   Perbaikan bug

Silakan buat *Issue* atau kirim *Pull Request*.

## Lisensi

Proyek ini dilisensikan di bawah [Lisensi MIT](LICENSE.md) (Anda perlu membuat file `LICENSE.md` jika belum ada, atau pilih lisensi lain).

---

**Ingatlah untuk selalu memprioritaskan keamanan dan bertindak dengan hati-hati.** Alat ini disediakan "sebagaimana adanya" tanpa jaminan apa pun.
