# Three-Class Document Classification

## Project Description
This project implements a machine learning model to classify news articles into three specific categories: **Technology**, **Sports**, and **Politics**.

The goal was to build a lightweight, efficient classifier using the **AG News** dataset, filtering out irrelevant classes and training a model using standard NLP techniques.

### Dataset
* **Source:** [AG News (Hugging Face)](https://huggingface.co/datasets/fancyzhx/ag_news)
* **Class Mapping & Filtering:**
    * `Sci/Tech` $\rightarrow$ **Technology**
    * `Sports` $\rightarrow$ **Sports**
    * `World` $\rightarrow$ **Politics**
    * (The `Business` class was dropped as per requirements)

### Chosen Model
* **Model:** Logistic Regression
* **Vectorization:** TF-IDF (Term Frequency-Inverse Document Frequency)
* **Reasoning:** Logistic Regression was chosen because it provides a strong baseline for text classification, is computationally efficient, and offers high interpretability compared to complex deep learning models.

---

## Setup Instructions

Follow these steps to run the project locally.

### 1. Clone the Repository
```bash
git clone https://github.com/chithraka-kal/document-classification-model
cd document-classification-model
```

### 2. Install Dependencies
Ensure you have Python installed, then install the required libraries:

```bash
pip install -r requirements.txt
```
### 3. Run the Notebook
Launch Jupyter Notebook to view the code and execution:

```bash
jupyter notebook notebook.ipynb
```

## Results Summary

**Performance**
The model achieved excellent performance on the test set:
* **Final Accuracy:** 95%
* **Precision/Recall:** consistently high (>0.94) across all three classes.


**Key Observations**
    
1. **Sports** is the easiest category to classify (F1-score: 0.97), likely due to distinct vocabulary (e.g., "score", "team", "Olympic").

2. **Politics** and Technology occasionally overlap. Misclassifications often occur when articles discuss government regulations on tech companies or policy decisions involving science.

3. The **Logistic Regression** model proved to be highly effective without the need for complex deep learning architectures, satisfying the requirement for a simple, lightweight solution.

## Project Structure

```bash
project-folder/
├── notebook.ipynb      # Main analysis and modeling code
├── README.md           # Project documentation
└── requirements.txt    # Python dependencies

```

