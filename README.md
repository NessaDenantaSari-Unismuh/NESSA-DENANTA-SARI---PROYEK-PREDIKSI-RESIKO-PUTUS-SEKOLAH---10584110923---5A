# 🎓 Analisis dan Prediksi Risiko Putus Sekolah Siswa SMA/MA Kota Makassar
Proyek Klasifikasi Biner untuk membangun Sistem Peringatan Dini risiko putus sekolah di SMA/MA Kota Makassar menggunakan data statistik pendidikan tahun 2021-2024.

## 1. 🌟 Sekilas Proyek & Tujuan
   Proyek ini bertujuan untuk menciptakan Model Prediktif yang membantu Dinas Pendidikan mengidentifikasi Kecamatan mana yang memiliki risiko paling tinggi terhadap angka
   putus sekolah.
   a. Tujuan Utama: Klasifikasi Risiko Putus Sekolah (Tinggi / Rendah).
   b. Algoritma Kunci: Random Forest Classifier (berdasarkan analisis di latihan.ipynb).
   c. Manfaat: Memungkinkan intervensi kebijakan yang lebih cepat dan tertarget, terutama berdasarkan faktor Gender dan Wilayah.

## 2. 📁 Struktur Repositori & File

| File/Direktori | Deskripsi |
| :--- | :--- |
| `Proyek_Putus_Sekolah.ipynb` | Kode Utama (Preprocessing, Pelatihan Model, Evaluasi, dan Deployment). |
| `Laporan_Tugas_Besar.pdf` | Dokumen Laporan Akhir Proyek (termasuk LK Perancangan Proyek). |
| `data/data_putus_sekolah.csv` | Dataset utama mengenai jumlah siswa putus sekolah per Kecamatan. |
| `model/model_rf_final.pkl` | File model Random Forest yang telah dilatih dan disimpan. |
| `app.py` | Skrip Python mandiri untuk menjalankan aplikasi antarmuka Gradio. |
| `requirements.txt` | Daftar semua pustaka Python yang diperlukan. |

## 3. 📊 Dataset & Tahapan Data PreparationSumber
   a. Data: Data sekunder resmi Statistik Siswa Putus Sekolah (SMA/MA) Kota Makassar.
   b. Periode: 2021-2024.
   c. Target (Y): Risiko Putus Sekolah (Biner: 1=Risiko Tinggi, 0=Risiko Rendah).

   Proses Kunci (Tahapan Data Preparation)
   a. Pembersihan Data: Missing Values diisi dengan nol (0) (imputasi) dan pemeriksaan data duplikat.
   b. Feature Engineering: Menciptakan variabel Target Biner (Risiko Putus Sekolah) berdasarkan ambang batas (threshold) dari total angka putus sekolah per Kecamatan.
   c. Transformasi Data:One-Hot Encoding pada fitur Kecamatan.Standard Scaling pada fitur numerik untuk menyeimbangkan skala.

## 4. 🎯 Hasil Kunci & Metrik Evaluasi

Berikut adalah metrik kinerja dari Model **Random Forest Classifier** yang telah dioptimasi, dengan akurasi di atas 90%:

| Metrik Evaluasi | Hasil | Keterangan & Prioritas |
| :--- | :--- | :--- |
| **Akurasi (*Accuracy*)** | **91.20%** | Kinerja prediksi keseluruhan. |
| **Presisi (*Precision*)** | 90.40% | Penting untuk meminimalisir intervensi yang salah (*False Positives*). |
| **Recall (Kelas Risiko Tinggi)** | **89.70%** | **KRITIS:** Mengukur kemampuan model mendeteksi semua kasus risiko (meminimalisir *False Negatives*). |
| **F1-Score** | 90.05% | Ukuran keseimbangan model. |

## 5. 🚀 Deployment Aplikasi (Gradio)
Model yang sudah dilatih di-deploy menggunakan Gradio untuk menyediakan antarmuka web interaktif yang sederhana.

## 6. 👤 Kontributor & Pengumpulan
   Nama: NESSA DENANTA SARI
   NIM: 105841110923
   Kelas: 5AI - A
   Institusi: Universitas Muhammadiyah Makassar
