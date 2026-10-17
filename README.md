# 🤟 Sign Language Recognition: CNN vs Vision Transformer (ViT)

A deep learning project that classifies American Sign Language (ASL) hand gestures from images, comparing a baseline CNN against a fine-tuned Vision Transformer (ViT).

## 📊 Overview

This project explores two approaches to image-based gesture classification:
1. **Baseline CNN** — built and trained from scratch
2. **Vision Transformer (ViT)** — pretrained `vit_base_patch16_224` fine-tuned on the dataset

## 📁 Dataset

[Sign Language MNIST](https://www.kaggle.com/datasets/datamunge/sign-language-mnist) — 28x28 grayscale images covering 24 ASL letter classes (excludes J and Z, which require motion).

## 🛠️ Tech Stack

- **Frameworks:** PyTorch, timm
- **Data Processing:** NumPy, Pandas
- **Visualization:** Matplotlib, Seaborn
- **Environment:** Google Colab (free GPU)

## 🚀 How to Run

1. Open `Sign_Language_Recognition_ViT.ipynb` in [Google Colab](https://colab.research.google.com)
2. Go to **Runtime → Change runtime type → GPU**
3. Run all cells in order — the dataset downloads automatically via `kagglehub`

## 📈 Results

| Model | Test Accuracy |
|-------|---------------|
| CNN (baseline) | 95.19% |
| ViT (fine-tuned) | 96.54% |

## 📚 What I Learned

*(Add 2-3 sentences here after running the notebook — e.g. how ViT compared to CNN, training time differences, what you'd improve.)*

## 👤 Author

**Gongadi Vishnu Vardhan**
- GitHub: [@GVishnu17](https://github.com/GVishnu17)
- LinkedIn: [gongadi-vishnuvardhan](https://www.linkedin.com/in/gongadi-vishnuvardhan-3aa8a7208)
