
# Fake News Detection Model Report

**Date:** 2025-03-28

## 1. Model Overview
This report outlines the performance and structure of a deep learning model created for fake news detection.

## 2. Model Architecture
The model is built using a Bidirectional LSTM network with the following configuration:
- **Embedding Size:** 64
- **Vocabulary Size:** 5000
- **LSTM Units:** 64
- **Output Activation:** Sigmoid
- **Loss Function:** Binary Crossentropy
- **Optimizer:** Adam

## 3. Test Results
- **Test Loss:** 0.0032
- **Test Accuracy:** 100.00%

## 4. Classification Report
### Fake News:
- **Precision:** 1.00
- **Recall:** 1.00
- **F1-Score:** 1.00
- **Support:** 4650

### Real News:
- **Precision:** 1.00
- **Recall:** 1.00
- **F1-Score:** 1.00
- **Support:** 4330

### Overall:
- **Average Precision:** 1.00
- **Average Recall:** 1.00
- **Average F1-Score:** 1.00
- **Total Support:** 8980

## 5. Confusion Matrix
- **True Negative (TN):** 4639
- **False Positive (FP):** 11
- **False Negative (FN):** 17
- **True Positive (TP):** 4313

## 6. Model Performance Analysis
The model has shown exceptional performance with a perfect test accuracy of 100%. Precision, recall, and F1-scores are all at the maximum value of 1.00, indicating that the model is capable of correctly identifying both fake and real news with minimal false positives and false negatives.
