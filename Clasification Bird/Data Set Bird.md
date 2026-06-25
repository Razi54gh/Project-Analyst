# Himalayan Bird Species Classification

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Dataset](https://img.shields.io/badge/Dataset-Kaggle-20BEFF.svg)](https://www.kaggle.com/datasets/akash2907/bird-species-classification)

This project uses the Himalayan bird species classification dataset to build a deep learning–based computer vision model. The dataset originates from the **ICCVIP 2018 Bird Species Classification Challenge** hosted by IIT Mandi, and was re-uploaded to Kaggle by Akash Kumar.

## Overview

This dataset contains high-resolution photographs of 16 Himalayan bird species. The number of samples is very limited (150 training images, 158 test images), making it well suited for experiments in **transfer learning**, **data augmentation**, and **fine-grained image classification**.

## Dataset

| Attribute | Description |
|-----------|-------------|
| **Source** | [Bird Species Classification — Kaggle](https://www.kaggle.com/datasets/akash2907/bird-species-classification) |
| **Uploader** | [Akash Kumar (akash2907)](https://www.kaggle.com/akash2907) |
| **Origin** | [ICCVIP 2018 Challenge](http://www.iiitdmj.ac.in/CVIP-2018/challenges.html) |
| **Number of classes** | 16 Himalayan bird species |
| **Training data** | 150 images |
| **Test data** | 158 images (1 corrupted image) |
| **Resolution** | 800×600 to 6000×4000 pixels |
| **Class imbalance** | 5–20 images per species |
| **Task** | Multi-class classification (supervised) |

### 16 Bird Species

Class labels use short codes (as in the original dataset naming):

| Code | Code | Code | Code |
|------|------|------|------|
| `blasti` | `bonegl` | `brhkyt` | `cbrtsh` |
| `cmnmyn` | `gretit` | `hilpig` | `himbul` |
| `himgri` | `hsparo` | `indvul` | `jglowl` |
| `lbicrw` | `mgprob` | `rebimg` | `wcrsrt` |

### Characteristics & Challenges

- **Very high resolution** — image sizes vary widely, requiring careful resize/crop strategies.
- **Few samples** — only 150 training images for 16 classes; data augmentation is almost mandatory.
- **Class imbalance** — the number of images per species is uneven (5–20 per class).
- **Train vs. test distribution shift** — training images tend to show small birds (10–20% of the frame), while test images often show large birds (70–80% of the frame).
- **Condition variability** — lighting, pose, occlusion (leaves/branches), and complex backgrounds.

## Improving Suboptimal Accuracy

Poor accuracy can be improved by:

1. Increasing the number of training and test images to achieve better accuracy.
2. Adding CNN layers to improve feature extraction.
3. Hybridizing the CNN model with other model architectures.
4. Using alternative, more capable models.
The original implementation repository uses the [MIT license](https://github.com/AKASH2907/bird_species_classification/blob/master/LICENSE).




# Klasifikasi Spesies Burung Himalaya

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Dataset](https://img.shields.io/badge/Dataset-Kaggle-20BEFF.svg)](https://www.kaggle.com/datasets/akash2907/bird-species-classification)

Proyek ini menggunakan dataset klasifikasi spesies burung Himalaya untuk membangun model computer vision berbasis deep learning. Dataset berasal dari tantangan **ICCVIP 2018 Bird Species Classification Challenge** yang diselenggarakan oleh IIT Mandi, dan diunggah ulang di Kaggle oleh Akash Kumar.

## Ringkasan

Dataset ini berisi foto burung beresolusi tinggi dari 16 spesies burung Himalaya. Jumlah sampel sangat terbatas (150 gambar latih, 158 gambar uji), sehingga cocok untuk eksperimen **transfer learning**, **data augmentation**, dan **fine-grained image classification**.

## Dataset

| Atribut | Keterangan |
|---------|------------|
| **Sumber** | [Bird Species Classification — Kaggle](https://www.kaggle.com/datasets/akash2907/bird-species-classification) |
| **Uploader** | [Akash Kumar (akash2907)](https://www.kaggle.com/akash2907) |
| **Asal data** | [ICCVIP 2018 Challenge](http://www.iiitdmj.ac.in/CVIP-2018/challenges.html) |
| **Jumlah kelas** | 16 spesies burung Himalaya |
| **Data latih** | 150 gambar |
| **Data uji** | 158 gambar (1 gambar rusak/korup) |
| **Resolusi** | 800×600 hingga 6000×4000 piksel |
| **Ketidakseimbangan kelas** | 5–20 gambar per spesies |
| **Tugas** | Klasifikasi multi-kelas (supervised) |


Adapun hasil dari akurasi yang kurang baik bisa diperbaiki dengan:
1. Menambah jumlah gambar training dan test agar mendapatkan akurasi yang lebih baik
2. menambahkan lapisan CNN agar pembacaan pada fara menjadi lebih bagus
3. Menghybrid model CNN dengan Model lain
4. menggunakan model lain yang lebih baik.
