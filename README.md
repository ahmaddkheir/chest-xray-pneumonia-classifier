# Chest X-Ray Pneumonia Classifier

This project uses **TensorFlow/Keras** to classify chest X-ray images as **Normal** or **Pneumonia**.  
It demonstrates the full workflow: dataset handling, preprocessing, a baseline CNN model, and a **MobileNetV2** transfer learning pipeline with evaluation.

---

## Features
- Data loading with `image_dataset_from_directory`
- Image normalization and on-the-fly data augmentation
- Baseline CNN model
- Transfer learning with **MobileNetV2**
- Evaluation metrics: accuracy, precision, recall, F1-score
- Confusion matrix and classification report

---

## Repository Contents
- `main.ipynb` — end-to-end notebook (data → training → evaluation)
- `requirements.txt` — Python dependencies

---

## Setup Instructions

### 1) Clone the repository
```bash
git clone https://github.com/<YOUR_USERNAME>/<REPO_NAME>.git
cd <REPO_NAME>
```

### 2) Create and activate a virtual environment (recommended)
```bash
python -m venv .venv
# macOS/Linux
source .venv/bin/activate
# Windows (PowerShell)
.venv\Scripts\Activate.ps1
```

### 3) Install dependencies
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4) Launch the notebook
```bash
jupyter notebook main.ipynb
```

---

## Dataset

The dataset is **not included** in this repository.  
Download **Chest X-Ray Images (Pneumonia)** using the Kaggle API:

```bash
kaggle datasets download -d paultimothymooney/chest-xray-pneumonia
unzip chest-xray-pneumonia.zip -d data/
```

Expected directory structure after extraction:

```
data/
  chest_xray/
    train/
      NORMAL/
      PNEUMONIA/
    val/
      NORMAL/
      PNEUMONIA/
    test/
      NORMAL/
      PNEUMONIA/
```

---

## How to Run (in the notebook)

1. Update the dataset path in the notebook (e.g., `data/chest_xray`).
2. Run the notebook cells in order:
   - Data loading and preprocessing
   - Baseline CNN training
   - MobileNetV2 transfer learning
   - Model evaluation (classification report + confusion matrix)

---

## Results and Evaluation

The notebook provides:
- Training vs. validation accuracy/loss curves
- Confusion matrix visualization
- Classification metrics (precision, recall, F1-score)

These outputs allow direct comparison between the **baseline CNN** and **MobileNetV2 transfer learning**.

---

