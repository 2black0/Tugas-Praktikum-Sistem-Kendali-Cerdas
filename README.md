# Konversi IPYNB ke PDF dengan Metadata dari Nama File

Proyek ini menyediakan solusi sederhana untuk mengotomatiskan konversi file notebook Jupyter (ipynb) ke format PDF, sekaligus menambahkan metadata judul ke PDF yang diambil dari nama file notebook.  Proyek ini diimplementasikan di Google Colab.

## Fitur

*   **Otomatisasi Metadata:** Judul PDF secara otomatis diambil dari nama file notebook (sebelum ekstensi .ipynb) dan ditambahkan sebagai metadata dokumen. Underscore (\_) dalam nama file akan diganti dengan spasi, dan setiap kata akan dikapitalisasi.
*   **Konversi ke PDF:** File notebook diubah menjadi format PDF menggunakan library `nbconvert`.
*   **Integrasi Google Colab:**  Kode ini dirancang untuk berjalan di lingkungan Google Colab, memanfaatkan fitur upload file dan download otomatis.
*   **User-Friendly:** Pengguna hanya perlu mengupload file IPYNB mereka, dan skrip akan menangani sisanya.
*   **Menangani Multiple File:** Dapat memproses banyak file IPYNB yang diunggah sekaligus.

## Cara Penggunaan

1.  Buka Google Colab dan buat notebook baru.
2.  Salin dan tempel kode Python yang disediakan ke dalam cell notebook.
3.  Jalankan cell tersebut.
4.  Ikuti instruksi yang ditampilkan: Klik "Choose Files" di panel sebelah kiri Google Colab untuk mengunggah file IPYNB Anda.
5.  Setelah file diupload, skrip akan otomatis memperbarui metadata dan mengkonversi file ke PDF.
6.  File PDF akan otomatis di-download ke komputer Anda.

## Contoh

Misalnya, Anda mengunggah file bernama `tugas_praktikum_sistem_kendali.ipynb`. Skrip akan:

1.  Membaca konten file.
2.  Menambahkan metadata `title` dengan nilai "Tugas Praktikum Sistem Kendali" ke dalam file IPYNB yang diupdate.
3.  Mengkonversi file IPYNB yang sudah diupdate ke PDF dengan judul yang sama.
4.  Mengunduh file PDF ke komputer Anda.

## Dependensi

Proyek ini menggunakan library berikut:

*   `json`: Untuk memanipulasi data JSON (metadata notebook).
*   `os`: Untuk manipulasi nama file dan path.
*   `google.colab`: Untuk integrasi dengan Google Colab (upload dan download file).
*   `nbconvert`: Untuk konversi notebook ke PDF.
*   `nbformat`: Untuk memanipulasi format notebook.

Semua library ini sudah tersedia di lingkungan Google Colab, sehingga Anda tidak perlu menginstalnya secara manual.

## Catatan

*   Pastikan file yang Anda unggah adalah file notebook Jupyter (ipynb).
*   Jika terjadi kesalahan saat update metadata, konversi ke PDF akan dibatalkan untuk file tersebut.  File lain yang diupload akan tetap diproses.

## Kontribusi

Kontribusi terhadap proyek ini dipersilakan.  Anda dapat membuka *issue* atau mengirimkan *pull request* jika ada perbaikan atau fitur baru yang ingin ditambahkan.