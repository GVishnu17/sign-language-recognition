# 🤟 Sign Language Recognition: CNN vs Vision Transformer (ViT)

A deep learning project that classifies American Sign Language (ASL) hand gestures from images, comparing a baseline CNN against a fine-tuned Vision Transformer (ViT).

## 📊 Overview

This project explores two approaches to image-based gesture classification:
1. | CNN (baseline, trained from scratch, 8 epochs) | 95.19% |
2. | ViT (pretrained, classifier head trained, 5 epochs) | 96.54% |
3. ### Error analysis (ViT)
Overall test accuracy is 96.54% on 7,172 images. The weakest classes are N
(recall 0.79) and R (precision 0.80). The most frequent confusions are
N→M (32), N→S (26), K→D (20), K→R (18) and E→M (18). Many of these are
signs with similar hand shapes (for example N, M, S and E are all closed
fists that differ mainly in thumb position), which likely explains the errors.

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

The pretrained ViT slightly outperformed the CNN baseline (96.54% vs 95.19%)
even though only its classifier head (~20K parameters) was trained. The CNN
learned faster in early epochs but plateaued around 95%, while the ViT was
still improving when training stopped, so more epochs or unfreezing more layers
would likely help. Test accuracy was monitored during training with no separate
validation set, and Sign Language MNIST images are clean and centred, so
accuracy on real webcam photos is expected to be lower.

## 👤 Author

**Gongadi Vishnu Vardhan**
- GitHub: [@GVishnu17](https://github.com/GVishnu17)
- LinkedIn: [gongadi-vishnuvardhan](https://www.linkedin.com/in/gongadi-vishnuvardhan-3aa8a7208)
