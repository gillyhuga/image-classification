# Deployment Model ANN (Kemangi VS Lidah Buaya)


## Deployment status

[![Heroku CI Status](https://heroku-badge.herokuapp.com/?app=image-prediction-ai)](https://image-prediction-ai.herokuapp.com/)

#


## Deskripsi singkat

Repository merupakan deployment model Machine Learning Image Classification menggunakan CNN (Artificial Neural Network). Adapun model yang digunakan merupakan model untuk memprediksi gambar daun kemangi atau lidah buaya.

#

## Sekilas mengenai input model

Agar dapat memprediksi daun kemangi atau lidah buaya, data input model harus mengikuti format sebagai berikut:

-   Gambar dengan format umum seperti .jpeg, .png, .webp, dsb.
-   Gambar dikonversi ke dalam bentuk array/tensor
-   Nilai pixel gambar memiliki rentang nilai 0-1 dengan cara membagi semua nilai pixelnya dengan 255.0

#

## Folder, file, dan kegunaannya

-   static/
    -   uploads/ --> Berisi gambar yang diunggah untuk diprediksi.
-   templates/
    -   index.html --> Berisi template website.
-   app.py --> Berisi konfigurasi route dan proses prediksi model untuk API.
-   elephant_lion_class_model.h5 --> Model Image Classification CNN yang sudah di-training.
-   requirements.txt --> Berisi daftar dependency/package Python yang diperlukan untuk menjalankan API dan model Image Classification CNN.

#

## Cara menjalankan API pada komputer Anda

1. Pastikan Anda sudah menginstall Anaconda.
1. Buka terminal/command prompt/power shell.
1. Buat virtual environment dengan\
   ```console
   conda create -n <nama-environment> python=3.9`
   ``` 
1. Aktifkan virtual environment dengan\
    ```console
   conda activate <nama-environment>
   ``` 
1. Install semua dependency/package Python dengan\
   ```console
   pip install -r requirements.txt
   ``` 
1. Jalankan API menggunakan perintah\
   ```console
   python app.py
   ``` 

## Akses melalui Website

1. Anda akan diberikan URL untuk membuka website berupa 
   ```console
   localhost:5000/
   ``` 
   atau 
   ```console
   `127.0.0.1:5000/`
   ```
1. Buka URL dengan browser, coba masukkan gambar daun lidah buaya atau daun kemangi yang ingin di prediksi.
1. Anda akan diberikan prediksi bahwa pada gambar tersebut adalah daun kemangi atau lidah buaya pada halaman website.
