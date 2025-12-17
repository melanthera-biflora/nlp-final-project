# Climate Sentiment Analysis of Corporate Disclosures

This repository contains the code and analysis for a final project on climate-related sentiment classification in corporate disclosures. The project evaluates multiple natural language processing (NLP) models and examines model interpretability using Integrated Gradients.

---

## Project Description

The objective of this project is to analyze how different NLP approaches perform on climate sentiment classification and to understand the relationship between dataset characteristics, modeling choices, and interpretability outcomes.

The task is formulated as a three-class classification problem, where each text segment is labeled according to whether climate change is framed as a **risk**, **neutral**, or an **opportunity**.

---

## Repository Structure

tree /F

## Dataset

The dataset used in this project is the **ClimateBERT** expert-annotated corpus, obtained from HuggingFace. It consists of climate-related paragraphs extracted from corporate annual reports and sustainability reports.

- **Labels**
  - `0`: Risk  
  - `1`: Neutral  
  - `2`: Opportunity  

- **Splits**
  - Training set: 1,000 samples  
  - Test set: 320 samples  

The cleaned datasets used for modeling are stored as `train_clean.csv` and `test_clean.csv` in the `data/` directory.

---

## Models and Experiments

The following models are implemented and evaluated:

### Baseline Models
- Logistic Regression  
- Naïve Bayes  

### Transformer-based Models
- BERT  
- RoBERTa  
- ClimateBERT  

All models are evaluated using accuracy and macro-averaged precision, recall, and F1 score.

---

## Interpretability Analysis

Integrated Gradients is applied to analyze token-level attributions for model predictions. Both correctly classified and misclassified examples are examined to understand model behavior and failure cases. The analysis also highlights interpretability challenges introduced by subword tokenization and special characters.

---

## Requirements

This project is implemented in Python using Jupyter Notebooks. Key libraries include:

- `transformers`
- `torch`
- `scikit-learn`
- `pandas`
- `numpy`
- `matplotlib`

All experiments were conducted in a notebook-based environment.

---

## Notes

- The repository is organized to support reproducibility of experiments.
- Each notebook is self-contained and corresponds to a specific stage of the project.
- Figures and evaluation outputs are generated directly within the notebooks.

---

## Author

Final project for an NLP course.
