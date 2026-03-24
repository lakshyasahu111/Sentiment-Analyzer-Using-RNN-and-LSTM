# 🧠 Sentiment Analysis using RNN & LSTM

## 📌 Overview

This project implements a **Sentiment Analysis model** to classify movie reviews into **Positive** or **Negative** sentiments.

Two deep learning architectures were explored and compared:

* **Vanilla RNN (Recurrent Neural Network)**
* **LSTM (Long Short-Term Memory)**

The goal is to analyze performance differences between basic and advanced sequence models.

---

## 🎯 Objective

* Perform sentiment classification on text data
* Compare RNN vs LSTM performance
* Analyze loss and accuracy trends

---

## 🧠 Model Architectures

### 🔹 Vanilla RNN

1. Embedding Layer
2. Simple RNN Layer
3. Fully Connected Layer
4. Output Layer (Sigmoid)

⚠️ Limitation:

* Struggles with long-term dependencies
* Suffers from vanishing gradient problem

---

### 🔹 LSTM Model

1. Embedding Layer
2. LSTM Layer (with memory cells)
3. Fully Connected Layer
4. Output Layer (Sigmoid)

✅ Advantages:

* Captures long-term dependencies
* Better gradient flow
* Improved performance on text data

---

## 📊 Model Performance Comparison

### 🔴 Vanilla RNN Results

| Epoch | Train Loss | Val Loss | Val Accuracy |
| ----- | ---------- | -------- | ------------ |
| 1     | 0.7031     | 0.6944   | 49.63%       |
| 5     | 0.6866     | 0.6981   | 50.54%       |
| 10    | 0.6596     | 0.7122   | 52.32%       |

➡️ **Observation:**

* Accuracy stagnates around ~50–52%
* Model fails to learn meaningful patterns
* Validation loss increases → overfitting / poor learning

---

### 🟢 LSTM Results

| Epoch | Train Loss | Val Loss | Val Accuracy |
| ----- | ---------- | -------- | ------------ |
| 1     | 0.6920     | 0.6933   | 50.49%       |
| 3     | 0.6440     | 0.6309   | 66.98%       |
| 6     | 0.5642     | 0.5693   | 73.18%       |
| 9     | 0.4224     | 0.5418   | 76.02%       |
| 10    | 0.4266     | 0.5830   | 71.25%       |

➡️ **Observation:**

* Significant improvement over RNN
* Accuracy reaches **~76%**
* Loss decreases consistently
* Better generalization

---

## ⚖️ Key Comparison

| Aspect           | RNN      | LSTM       |
| ---------------- | -------- | ---------- |
| Accuracy         | ~52%     | ~76%       |
| Learning Ability | Poor     | Strong     |
| Loss Trend       | Unstable | Decreasing |
| Overfitting      | High     | Controlled |
| Memory Handling  | Weak     | Strong     |

---

## 📈 Conclusion

* Vanilla RNN is **not effective** for this task due to inability to capture long-term dependencies.
* LSTM significantly improves performance by maintaining context over sequences.
* For NLP tasks like sentiment analysis, **LSTM is clearly superior to basic RNN**.

---

## 🛠️ Tech Stack

* Python
* PyTorch
* Google Colab
* NumPy, Pandas
* Matplotlib


---


MIT License
