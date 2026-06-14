<div align="center">

# PCA vs Autoencoder pada FashionMNIST

### Perbandingan Reduksi Dimensi dan Visualisasi t-SNE

<p align="center">
Eksperimen Data Mining menggunakan PCA, Autoencoder, dan t-SNE pada dataset FashionMNIST
</p>

![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python)
![PyTorch](https://img.shields.io/badge/PyTorch-CUDA-red?style=for-the-badge&logo=pytorch)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-PCA%20%7C%20t--SNE-orange?style=for-the-badge&logo=scikitlearn)
![Status](https://img.shields.io/badge/Status-Siap%20Dijalankan-success?style=for-the-badge)

</div>

---

# Gambaran Umum

Project ini membandingkan dua metode reduksi dimensi, yaitu **Principal Component Analysis (PCA)** dan **Autoencoder**, pada dataset **FashionMNIST**. Hasil representasi fitur dari kedua metode kemudian divisualisasikan menggunakan **t-SNE** untuk melihat pola cluster setiap kelas.

Eksperimen juga menyertakan baseline **Raw Pixel + t-SNE** agar hasil PCA dan Autoencoder dapat dibandingkan dengan representasi pixel mentah.

---

# Alur Eksperimen

1. Memuat dataset FashionMNIST.
2. Mengubah citra 28 x 28 menjadi vektor 784 fitur.
3. Mereduksi dimensi menggunakan PCA menjadi 32 fitur.
4. Melatih Autoencoder dengan latent dimension 32.
5. Mengambil latent representation dari Autoencoder.
6. Memvisualisasikan Raw Pixel, PCA, dan Autoencoder menggunakan t-SNE.
7. Membandingkan reconstruction error, explained variance, silhouette score, dan visualisasi cluster.

---

# Struktur Project

```bash
PCA_vs_Autoencoder_FashionMNIST/
│
├── notebooks/
│   ├── 01_setup_and_dataset.ipynb
│   ├── 02_pca_reduction.ipynb
│   ├── 03_autoencoder_training.ipynb
│   └── 04_tsne_visualization_and_analysis.ipynb
│
├── results/
│   ├── figures/
│   ├── features/
│   ├── pca_results.csv
│   ├── autoencoder_results.csv
│   ├── tsne_metrics.csv
│   └── reduction_comparison.csv
│
├── models/
│   ├── pca_model.pkl
│   └── autoencoder_fashionmnist.pth
│
├── data/
├── README.md
├── requirements.txt
└── .gitignore
```

---

# Cara Menjalankan

## Install dependencies

```bash
pip install -r requirements.txt
```

## Urutan menjalankan notebook

1. `01_setup_and_dataset.ipynb`
2. `02_pca_reduction.ipynb`
3. `03_autoencoder_training.ipynb`
4. `04_tsne_visualization_and_analysis.ipynb`

---

# Catatan

- Autoencoder akan menggunakan CUDA jika PyTorch berhasil mendeteksi GPU NVIDIA.
- Dataset akan diunduh otomatis pada eksekusi pertama.
- Folder `data/` dan `venv/` tidak perlu diunggah ke GitHub.
- t-SNE berjalan menggunakan CPU sehingga mungkin memerlukan waktu beberapa menit.
