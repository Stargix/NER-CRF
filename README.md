# NER with Conditional Random Fields (CRF)

This project demonstrates how to perform **Named Entity Recognition (NER)** using a **Conditional Random Field (CRF)** model. It includes steps for preprocessing data, feature extraction, model training, evaluation, and predictions.

## 📘 Contents

- **Dataset Preparation**: Loads and preprocesses data into BIO-tagged format suitable for NER tasks.
- **Feature Engineering**: Extracts token-level features such as:
  - Part-of-speech tags
  - Word casing and suffixes
  - Previous and next word context
- **Model Training**: Uses `sklearn_crfsuite` to train a CRF model.
- **Evaluation**: Computes precision, recall, F1-score, and supports detailed performance analysis.
- **Prediction**: Allows for inference on new sequences using the trained model.

## 🚀 Getting Started

1. Clone the repository or download the notebook.
2. Make sure the required libraries are installed.
3. Run `main-NER-CRF.ipynb` to execute the full pipeline.

## 📊 Example Output

After training, the notebook prints a detailed classification report, such as:

```
precision    recall  f1-score   support

     B-PER       0.95      0.93      0.94       200
     I-PER       0.90      0.92      0.91       150
     ...
```

## 🛠 Customization

- You can easily modify the feature function to include domain-specific features.
- The notebook is modular, allowing you to plug in other sequence labeling algorithms (e.g., BiLSTM-CRF).

## 📁 File Structure

- `main-NER-CRF.ipynb` - Main notebook with all steps from data preprocessing to evaluation.
- `person_names.txt` - List of common person names.
- `locations.txt` - List of cities and countries.
