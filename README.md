# 🍎🍌 Image Classification: Fresh vs Rotten Fruits & Vegetables

A deep learning project comparing two image classification approaches — a **Custom CNN** and a **pretrained Vision Transformer (ViT)** — for detecting freshness in fruits and vegetables.

## 📌 Objective

To develop an accurate and efficient system for classifying fresh vs rotten produce, supporting quality control and automation in the agricultural supply chain.

## 👨‍💻 Team Members

- **Shayan Haider** - 21K-3211  
- **Ahmed Ali**     - 21K-3212  
- **Taha Hassan**   - 21K-4680  

---

## 🧠 Models Compared

### 🔷 1. Vision Transformer (ViT)
- **Base Model**: `google/vit-base-patch16-224`
- **Approach**: Transfer Learning + Fine-tuning
- **Framework**: PyTorch
- **Input**: 224x224 RGB
- **Epochs**: 5
- **Final Val Accuracy**: **99.74%**

### 🔶 2. Custom CNN
- **Architecture**: Manually designed convolutional layers
- **Framework**: TensorFlow / Keras
- **Input**: 224x224 RGB
- **Epochs**: 50
- **Final Val Accuracy**: ~**91%**

---

## 🧪 Dataset

- **Source**: [Kaggle dataset](https://www.kaggle.com/datasets/swoyam2609/fresh-and-stale-classification/data)
- **Size**: ~19,154 images
- **Classes**: 10 (fresh/rotten variants of apples, bananas, oranges, potatoes, and tomatoes)

---

## 🛠️ Methodology

### 🔄 Preprocessing
- Image resizing to 224×224
- Normalization
- Augmentation (flip, rotate, etc.)

### ⚙️ Training
- **CNN** trained from scratch
- **ViT** fine-tuned using pretrained weights
- Metrics: Accuracy, Precision, Recall, F1-score

### 🧪 Evaluation
| Class            | Precision | Recall | F1-Score |
|------------------|-----------|--------|----------|
| Fresh Apple      | 0.90      | 0.92   | 0.91     |
| Fresh Banana     | 0.91      | 0.96   | 0.93     |
| Rotten Tomato    | 0.90      | 0.92   | 0.91     |
| ...              | ...       | ...    | ...      |
| **Overall (CNN)**| **0.91**  | **0.91**| **0.91** |

---

## 📊 Results

| Model      | Accuracy | Inference Time | Resource Use |
|------------|----------|----------------|---------------|
| **ViT**    | 99.74%   | High           | High          |
| **CNN**    | 91%      | Low            | Low           |

---

## 💡 Use Case Recommendations

| Scenario                        | Recommended Model | Reason                                     |
|---------------------------------|-------------------|--------------------------------------------|
| High-accuracy production        | ViT               | Near-perfect accuracy, robust performance  |
| Resource-constrained devices    | CNN               | Lightweight, faster inference              |
| Fast prototyping                | CNN               | Easy to train and modify                   |

---

## 🚀 Deployment

- Best-performing model saved for inference
- Backend API available for real-time prediction (via Flask/FastAPI – optional)

---

## 📁 Repository Structure

├── ViT_model.ipynb # ViT implementation (PyTorch)<br>
├── DLP_proj.ipynb # Custom CNN (TensorFlow/Keras)<br>
├── Report.docx # Detailed project report<br>
├── README.md # Project overview (you are here)

