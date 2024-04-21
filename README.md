# Colab-ML
ini merupakan hasil submission dari dicoding dan merupakan proyek mandiri yang di berikan dari dicoding untuk syarat kelulusan sertifikasi kelas machine learning pemula

Kode tersebut menjalankan program untuk membangun dan melatih model jaringan saraf konvolusi (Convolutional Neural Network/CNN) menggunakan TensorFlow. Berikut adalah perintah yang dijalankan dan library yang digunakan:

Mengunduh dataset rockpaperscissors.zip dari GitHub menggunakan urllib.request.urlretrieve dari library urllib.request.
Mengekstrak dataset menggunakan zipfile.ZipFile dari library zipfile.
Membuat direktori untuk data latih (train) dan data validasi (val) menggunakan os.makedirs dari library os.
Membagi dataset menjadi data latih dan data validasi untuk setiap kelas (rock, paper, scissors) dengan pembagian 40% menggunakan os.listdir, os.path.join, dan os.rename dari library os.
Melakukan augmentasi gambar menggunakan ImageDataGenerator dari library tensorflow.keras.preprocessing.image.
Membangun model Sequential dengan arsitektur CNN yang terdiri dari lapisan-lapisan Conv2D, MaxPooling2D, Flatten, dan Dense menggunakan Sequential dari library tensorflow.keras.models dan lapisan-lapisan tersebut dari library tensorflow.keras.layers.
Mengkompilasi model dengan pengoptimum Adam dan fungsi kerugian categorical crossentropy menggunakan compile dari library tensorflow.keras.models.
Membuat objek EarlyStopping sebagai callback untuk menghentikan pelatihan jika metrik val_accuracy tidak mengalami peningkatan setelah beberapa epoch menggunakan EarlyStopping dari library tensorflow.keras.callbacks.
Melatih model menggunakan metode fit dari model Sequential, dengan menggunakan data generator untuk data latih dan data validasi, serta menyertakan callback EarlyStopping, dan menyimpan riwayat pelatihan dalam variabel history.
Library yang digunakan adalah:

TensorFlow (tensorflow)
TensorFlow Keras (tensorflow.keras)
TensorFlow Keras Preprocessing (tensorflow.keras.preprocessing.image)
Python Standard Library: os, zipfile, urllib.request
