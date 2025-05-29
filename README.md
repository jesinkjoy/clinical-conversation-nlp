# 🧠 Clinical Conversation Classification using NLP

This project focuses on classifying physician-patient conversations into 15 categories based on **Social Support Theory**, using both traditional machine learning and deep learning models. Completed as part of the INFO 617 – Text Analytics course at VCU.

---

## 📁 Project Structure

- **Baseline Models:** TF-IDF with Logistic Regression, SVM, Ridge Classifier, etc.
- **Deep Models:** CNN, ClinicalBERT, and DistilBERT for context-rich classification
- **Class Imbalance Handling:** SMOTE and oversampling techniques to improve minority class representation
- **Model Comparison:** Evaluated accuracy, F1 score, and generalization across all approaches

---

## 🧠 Objectives

- Classify individual sentences from physician-patient dialogues into support types like TREAT, EXPLAIN, THANK, etc.
- Compare traditional ML with transformer-based models for medical text understanding
- Identify model trade-offs in accuracy, generalization, and computational efficiency

---

## 🔧 Tools & Technologies

- Python (pandas, NumPy, scikit-learn)
- TF-IDF, SMOTE, RandomOverSampler
- Deep Learning: TensorFlow, Keras
- NLP Models: DistilBERT, ClinicalBERT
- Google Colab

---

## 📈 Key Results

| Model            | Validation F1 | Test Accuracy | Notes |
|------------------|----------------|----------------|-------|
| Logistic Regression | 0.65          | ~65%           | Strong baseline |
| CNN               | 0.70          | ~70%           | Lightweight DL model |
| ClinicalBERT      | ~0.80         | ~81%           | Domain-specific fine-tuning |
| **DistilBERT**    | **0.81**      | **81.7%**      | Best performing & efficient |

- **Top Confusions**: DIAGNOSE ↔ EXPLAIN, REQUEST ↔ QUES — due to semantic overlaps
- **DistilBERT** showed the best generalization and minimal preprocessing requirement

---

## 💡 Insights & Challenges

- **Class Imbalance**: Mitigated using SMOTE and oversampling, but rare classes like FUTURE_SUPPORT remained difficult
- **Traditional Models**: Fast and interpretable but lacked contextual understanding
- **Transformer Models**: Superior accuracy with minimal feature engineering
- **ClinicalBERT** showed domain adaptation value, but **DistilBERT** had better overall performance due to its general pretraining and lightweight architecture

---

## 📂 Files

- `TraditionalModels.ipynb` – All baseline ML models with TF-IDF
- `ClinicalBert.ipynb` – Fine-tuning and evaluation of ClinicalBERT
- `Distil_BERT.ipynb` – Best performing model implementation
- `INFO 617_Group Project Train Val.xlsx` – Training and validation data
- `INFO 617_Group Project Test Set.xlsx` – Final test dataset
- `nlp_project_presentation.pptx` – Executive summary and model comparison

---

## 📌 Note

This project is academic and not affiliated with any real-world medical organization. All data used was labeled for research purposes, and results should not be interpreted as clinical advice.
