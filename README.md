# Tugas Manipulasi Citra Digital Menggunakan OpenCV

* **Nama:** Edwin Fadhilah Putra
* **NIM:** 452024611002
* **Mata Kuliah:** Pengolahan Sinyal Digital

## Deskripsi Proyek
Repository ini berisi eksperimen manipulasi citra digital menggunakan Python dan OpenCV, yang mencakup konversi ruang warna BGR ke RGB, resizing, image blending, image negative, transformasi logaritmik, dan koreksi gamma.

## Citra yang Digunakan
1. Citra 1: Foto Spider-Man (Format JPG)
2. Citra 2: Foto Sendok Ikonik (Format JPEG)

## Library yang Dibutuhkan
* OpenCV (`opencv-python`)
* NumPy
* Matplotlib

## Struktur Folder
* `/notebook`: Berisi file jupyter notebook pengerjaan kode.
* `/images`: Berisi file citra asli yang digunakan dalam eksperimen.
* `/report`: Berisi laporan resmi format PDF dan dokumentasi proyek.

## Ringkasan Kesimpulan
Dari hasil eksperimen, dapat disimpulkan bahwa operasi linear seperti *blending* dan *negative* bekerja pada seluruh piksel secara merata. Sedangkan operasi non-linear seperti *logarithm* dan *gamma* sangat efektif untuk memanipulasi rentang dinamis citra (kontras dan kecerahan) pada area tertentu tanpa merusak kualitas visual citra secara keseluruhan.
