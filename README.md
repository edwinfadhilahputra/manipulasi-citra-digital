# 📸 Tugas Mandiri: Manipulasi Citra Digital Menggunakan OpenCV

Repository ini berisi implementasi eksperimen **Manipulasi Citra Digital Pointwise (Linear & Non-Linear)** untuk memenuhi tugas mata kuliah **Pengolahan Sinyal Digital**. Eksperimen dilakukan menggunakan bahasa pemrograman Python dengan pustaka utama OpenCV, NumPy, dan Matplotlib.

---

## 👤 Identitas Mahasiswa
* **Nama:** Edwin Fadhilah Putra
* **NIM:** 452024611002
* **Program Studi:** Teknik Informatika
* **Instansi:** Universitas Darussalam Gontor

---

## 📂 Struktur Folder Repository
Proyek ini disusun dengan struktur folder formal sebagai berikut:
```text
manipulasi-citra-digital/
├── requirements.txt         # Daftar pustaka (library) Python yang dibutuhkan
├── notebook/
│   └── image_manipulation.ipynb  # File source code utama (Jupyter Notebook)
├── images/
│   ├── ea89bfee1efd875cca41982669b53591.jpg            # Citra Asli 1 (Spider-Man)
│   └── WhatsApp Image 2026-06-19 at 23.46.28 (1).jpeg  # Citra Asli 2 (Sendok)
└── report/
    └── laporan.pdf          # Laporan resmi format PDF (Standar Jurnal)

```

## 🚀 Alur Eksperimen & Fitur KodeKode program di dalam proyek ini mencakup 6 bagian manipulasi piksel utama:
Bagian A (Color Space Conversion): Mengubah pembacaan bawaan OpenCV dari ruang warna BGR ke RGB agar warna citra tampil natural pada Matplotlib.
Bagian B (Resizing): Menyelaraskan dimensi spasial kedua citra menjadi ukuran seragam $600 \times 400$ piksel agar kompatibel untuk operasi matriks.
Bagian C (Image Blending): Menggabungkan dua citra secara linear menggunakan fungsi cv.addWeighted dengan variasi bobot transparansi ($\alpha$ & $\beta$).
Bagian D (Image Negative): Membalikkan nilai intensitas piksel secara linear ($255 - r$) untuk analisis inversi warna dan efek pencerminan histogram.
Bagian E (Transformasi Logaritmik): Menerapkan fungsi non-linear $c \cdot \log(1 + r)$ untuk menonjolkan detail fitur visual pada area citra yang cenderung gelap (low-light).
Bagian F (Transformasi Gamma): Melakukan koreksi kecerahan non-linear (Power-Law) melalui variasi eksponen $\gamma = [0.5, 1.0, 2.0, 2.5]$.


## 📊 Ringkasan Hasil Analisis (HOTS)
Kondisi Minim Cahaya (Underexposed): Teknik terbaik adalah Transformasi Gamma ($\gamma = 0.5$) karena mencerahkan area gelap secara bertahap tanpa membuat warna latar belakang yang terang menjadi kabur putih (washed out).
Kondisi Terlalu Silau (Overexposed): Teknik terbaik adalah Transformasi Gamma ($\gamma > 1$) untuk meredam kilau cahaya (glare) dan mengembalikan tekstur objek yang hilang.
Analisis Histogram: Grafik histogram terbukti menjadi "sidik jari" pencahayaan citra. Operasi linear (seperti negatif) mencerminkan kurva secara simetris, sedangkan operasi non-linear (seperti log dan gamma) menggeser kurva secara melengkung demi mencapai kontras yang optimal.

## 🛠️ Cara Menjalankan Kode Program di Lokal
Jika Anda ingin menjalankan file notebook .ipynb di komputer lokal Anda, ikuti langkah-langkah berikut:
1. Clone Repository ini:
```bash
git clone [https://github.com/username-anda/manipulasi-citra-digital.git](https://github.com/username-anda/manipulasi-citra-digital.git)
cd manipulasi-citra-digital
```
3. Instalasi Library yang Dibutuhkan:
Pastikan Python sudah terinstal, lalu jalankan perintah:
```bash
pip install -r requirements.txt
```
5. Jalankan Jupyter Notebook:
```bash
jupyter notebook notebook/image_manipulation.ipynb
```

## 📚 Referensi
1. Gonzalez, R. C., & Woods, R. E. Digital Image Processing.

2. Dokumentasi Resmi OpenCV-Python.

3. Modul Praktikum Pengolahan Sinyal Digital, Universitas Darussalam Gontor.
