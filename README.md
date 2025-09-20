````markdown
# Chest X-Ray Pneumonia Classifier

This project uses TensorFlow/Keras to classify chest X-ray images as **Normal** or **Pneumonia**.  
It demonstrates a full workflow: data loading, preprocessing, a small CNN baseline, and a **MobileNetV2** transfer-learning pipeline with evaluation.

---

## Features
- Data loading via `image_dataset_from_directory`
- Normalization and on-the-fly data augmentation
- Baseline CNN model
- Transfer learning with **MobileNetV2**
- Metrics: accuracy, precision, recall, F1
- Confusion matrix and classification report

---

## Repository Contents
- `main.ipynb` — end-to-end notebook (data → training → evaluation)
- `requirements.txt` — Python dependencies


---

## Quick Start

### 1) Clone or download
```bash
git clone https://github.com/<YOUR_USERNAME>/<REPO_NAME>.git
cd <REPO_NAME>
````

### 2) Create a virtual environment (recommended)

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

The dataset is **not included** in this repository. Use the Kaggle API to download **Chest X-Ray Images (Pneumonia)**:

```bash
kaggle datasets download -d paultimothymooney/chest-xray-pneumonia
unzip chest-xray-pneumonia.zip -d data/
```

The typical directory layout after extraction is:

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

1. Set the dataset path in the notebook to the extracted folder (e.g., `data/chest_xray`).
2. Execute the cells in order:

   * Data loading and preprocessing
   * Baseline CNN training
   * MobileNetV2 transfer learning
   * Evaluation (classification report + confusion matrix)

---

## Results and Evaluation

The notebook prints key metrics and plots:

* Training/validation accuracy and loss curves
* Confusion matrix
* Precision, recall, and F1-score

Use these to compare the baseline vs. transfer-learning performance.

---




```
```
