# 📝 Sentiment Analysis of IMDB Movie Reviews

> A deep learning–based sentiment analysis system that classifies IMDB movie reviews as **positive** or **negative** using **transfer learning with pre-trained word embeddings** from TensorFlow Hub — achieving **84.9% test accuracy** on 50,000 movie reviews.

This project demonstrates practical Natural Language Processing (NLP) workflows using TensorFlow/Keras, pre-trained embeddings, and binary text classification.

---

# ⭐ Key Highlights

| Metric                     | Value                                    |
| -------------------------- | ---------------------------------------- |
| ✅ Test Accuracy            | **84.9%**                                |
| ✅ Peak Validation Accuracy | **87.9%**                                |
| ✅ Model Type               | Transfer Learning + Dense Neural Network |
| ✅ Embedding Dimension      | **50**                                   |
| ✅ Trainable Parameters     | **48.2 Million**                         |
| ✅ Framework                | **TensorFlow 2.x / Keras**               |
| ✅ Dataset Size             | **50,000 IMDB reviews**                  |

### 🔑 Core Concepts

`NLP` • `Sentiment Analysis` • `Transfer Learning` • `Word Embeddings` • `TensorFlow Hub` • `Binary Classification` • `Deep Learning` • `Text Processing`

---

# 🎯 Project Objective

The goal of this project was to build a neural network capable of automatically understanding sentiment from raw movie review text.

The model learns to classify reviews into:

* **Positive sentiment**
* **Negative sentiment**

using transfer learning with a pre-trained Neural Network Language Model (NNLM) embedding from TensorFlow Hub.

This project demonstrates:

* practical NLP pipeline design,
* transfer learning for text,
* deep learning–based sentiment classification,
* and model evaluation on real-world textual data.

---

# 🧠 Dataset

| Property         | Value               |
| ---------------- | ------------------- |
| Dataset          | IMDB Reviews        |
| Source           | TensorFlow Datasets |
| Total Reviews    | 50,000              |
| Classes          | Positive / Negative |
| Train Split      | 40,000              |
| Validation Split | 5,000               |
| Test Split       | 5,000               |

Each review is stored as:

* raw English text,
* paired with a binary sentiment label.

---

# 🧱 Model Architecture

```python
Input: Raw text string
    ↓
TensorFlow Hub NNLM Embedding
("https://tfhub.dev/google/nnlm-en-dim50/2")
    ↓
Dense(16, activation='relu')
    ↓
Dense(1)   # logits
```

---

# 🧠 Why Transfer Learning?

Instead of training word representations from scratch, this project uses a pre-trained NNLM embedding layer trained on large-scale language data.

Benefits:

* Faster convergence
* Better generalisation
* Reduced need for massive custom datasets
* Strong semantic understanding of words and phrases

The embedding layer is set to:

```python
trainable=True
```

allowing the model to fine-tune language representations specifically for sentiment classification.

---

# ⚙️ Training Configuration

| Component             | Setting                           |
| --------------------- | --------------------------------- |
| Optimizer             | Adam                              |
| Loss Function         | Binary Crossentropy (from logits) |
| Epochs                | 10                                |
| Batch Size            | 100                               |
| Embedding Fine-Tuning | Enabled                           |
| Framework             | TensorFlow / Keras                |

---

# 📊 Results & Performance

## Final Test Metrics

| Metric        | Value     |
| ------------- | --------- |
| Test Loss     | **0.626** |
| Test Accuracy | **84.9%** |

---

## Validation Accuracy Progression

| Epoch | Train Accuracy | Validation Accuracy |
| ----- | -------------- | ------------------- |
| 1     | 73.1%          | 85.0%               |
| 2     | 90.4%          | 87.9%               |
| 3     | 95.8%          | 87.7%               |
| 4     | 98.3%          | 87.5%               |
| 5     | 99.5%          | 87.3%               |
| 10    | 100%           | 86.7%               |

---

# 📈 Performance Analysis

The model learns sentiment patterns rapidly due to the strong pre-trained embedding representation.

### 🔹 Observations

* Validation accuracy peaks early (~87–88%)
* Training accuracy eventually reaches 100%
* Slight validation decline indicates overfitting caused by the high-capacity embedding layer

Despite this, the model maintains strong generalisation with:

* **84.9% test accuracy**
* stable validation performance
* strong binary sentiment separation

This demonstrates the effectiveness of transfer learning for NLP tasks even with relatively small classifier architectures.

---

# 🏆 Challenges & Solutions

| Challenge                                     | Solution                                                         |
| --------------------------------------------- | ---------------------------------------------------------------- |
| Variable-length raw text input                | Used TF Hub embeddings that directly accept strings              |
| Overfitting due to large trainable embeddings | Analysed training dynamics and proposed dropout/partial freezing |
| Long training time                            | Batched data and used TensorFlow pipelines                       |
| Efficient preprocessing                       | Used batching + prefetching                                      |

---

# 🛠️ Tech Stack

| Category      | Technology                           |
| ------------- | ------------------------------------ |
| Framework     | TensorFlow 2.x, Keras                |
| NLP Embedding | NNLM (TF Hub)                        |
| Dataset       | IMDB Reviews via tensorflow_datasets |
| Environment   | Jupyter Notebook / Google Colab      |

---

# ⚙️ Quick Start

## Prerequisites

* Python 3.8+
* TensorFlow 2.x
* TensorFlow Hub
* TensorFlow Datasets
* Jupyter Notebook

---

## Installation & Run

```bash
# Clone repository
git clone https://github.com/PriyanshiSingh19/Text-classification.git

cd Text-classification

# Install dependencies
pip install tensorflow tensorflow-hub tensorflow-datasets

# Launch notebook
jupyter notebook Text_classification.ipynb
```

Run all notebook cells to:

* download the IMDB dataset,
* load the pre-trained NNLM embedding,
* train the sentiment classifier,
* and evaluate performance on the test set.

---

# 📁 Project Structure

```text
Text-classification/
│
└── Text_classification.ipynb
```

> The repository consists of a single notebook containing the complete NLP pipeline, training workflow, and evaluation outputs.

---

# 🚀 Future Improvements

## 🔹 Model Improvements

* Add Dropout regularisation
* Freeze embedding partially during training
* Hyperparameter tuning

## 🔹 Better Embeddings

* Universal Sentence Encoder
* BERT embeddings
* Larger NNLM embeddings

## 🔹 Deployment

* FastAPI inference API
* Streamlit web demo
* TensorFlow Lite conversion

## 🔹 Explainability

* SHAP visualisations
* LIME explanations
* Attention-based analysis

---

# 📝 Resume-Ready Bullet Points

### Sentiment Analysis using Transfer Learning

Built a deep learning sentiment analysis model for IMDB movie reviews using transfer learning with TensorFlow Hub embeddings, achieving **84.9% test accuracy** on 50k reviews.

### NLP Pipeline Development

Implemented an end-to-end NLP workflow including raw text preprocessing, pre-trained embedding integration, neural network training, and evaluation using TensorFlow/Keras.

### Transfer Learning for NLP

Fine-tuned a pre-trained NNLM embedding model for binary sentiment classification, demonstrating practical application of transfer learning in Natural Language Processing.

### Model Evaluation & Analysis

Analysed training/validation behaviour to identify overfitting patterns and proposed regularisation strategies for improved generalisation.

---

# 📚 Key Concepts Demonstrated

* Transfer learning
* Word embeddings
* Binary sentiment classification
* TensorFlow Hub integration
* Deep learning for NLP
* Model evaluation
* Train/validation/test workflow
* Fine-tuning pre-trained models

---

# 👩‍💻 About This Project

This project demonstrates how modern NLP systems can leverage pre-trained language representations to solve sentiment classification tasks efficiently.

It highlights practical understanding of:

* transfer learning,
* neural text embeddings,
* deep learning workflows,
* and TensorFlow-based NLP pipelines.

The project intentionally focuses on clarity, reproducibility, and applied NLP engineering concepts rather than excessively complex architectures.

---

Built with 🧠 TensorFlow Hub and curiosity for understanding how machines interpret human language.
