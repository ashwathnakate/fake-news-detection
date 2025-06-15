# 📰 Fake News Detection using Deep Learning

This repository contains a deep learning model for detecting fake news using a Bidirectional LSTM (Long Short-Term Memory) network. The model is trained on a dataset of real and fake news articles and achieves **high accuracy** in distinguishing between real and fake news.

---

## 🚀 **Project Overview**

The goal of this project is to build a binary classification model that can accurately classify news articles as `FAKE` or `REAL`. The model leverages a combination of:

- **Embedding Layer** – For converting text into numerical format
- **Bidirectional LSTM Layer** – For capturing long-term dependencies in both directions
- **Global Average Pooling Layer** – For dimensionality reduction
- **Dense Layers** – For final classification

---

## 📂 **Dataset**
The dataset consists of two CSV files:
- `True.csv` – Contains real news articles
- `Fake.csv` – Contains fake news articles
- Dataset can be found at [https://www.kaggle.com/datasets/abaghyangor/fake-news-dataset/data]

| **Class** | **Number of Samples** |
|-----------|-----------------------|
| Fake News | 4650                  |
| Real News | 4330                  |

---

## 🧠 **Model Architecture**
```python
model = tf.keras.Sequential([
    Embedding(input_dim=5000, output_dim=64, input_length=500),
    Bidirectional(LSTM(64, return_sequences=True)),
    GlobalAveragePooling1D(),
    Dense(64, activation='relu'),
    Dense(1, activation='sigmoid')
])

model.compile(loss='binary_crossentropy', optimizer='adam', metrics=['accuracy'])
model.summary()
```

---

## 📊 **Performance Metrics**
### ✅ **Test Accuracy:** 99.67%

### ✅ **Loss:** 0.0032

### ✅ **Confusion Matrix:**
| Actual \ Predicted | Fake | Real |
|-------------------|------|------|
| **Fake**           | 4639 | 11   |
| **Real**           | 17   | 4313 |

### ✅ **Classification Report:**
| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| Fake  | 1.00      | 1.00   | 1.00     | 4650    |
| Real  | 1.00      | 1.00   | 1.00     | 4330    |
| **Accuracy** |       |        | 1.00     | 8980    |

---

## 💻 **How to Run**
### 1. Clone the repository:
```bash
git clone https://github.com/your-username/fake-news-detection.git
```

### 2. Install dependencies:
```bash
pip install -r requirements.txt
```

### 3. Run the training script:
```bash
python train.py
```

### 4. Predict on new data:
```python
from predict import predict_news
text = "Your news article text here"
result = predict_news(text)
print(f"Prediction: {result}")
```

---

## 🌟 **Future Work**
- Improve model performance using transformer-based architectures (e.g., BERT).
- Integrate more complex text preprocessing techniques.
- Deploy as a web-based API or mobile app.

---

## 🤝 **Contributing**
Feel free to contribute by submitting a pull request or opening an issue.

---

## 📜 **License**
This project is licensed under the [MIT License](LICENSE).

