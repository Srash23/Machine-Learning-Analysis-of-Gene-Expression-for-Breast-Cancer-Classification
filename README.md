# Breast Cancer Gene Expression Analysis

## Introduction

Breast cancer, a significant global health issue, necessitates advanced diagnostic approaches. This study integrates oncology with machine learning, utilizing logistic regression to analyze large-scale gene expression data. The objective is to identify key genes that distinguish between 'normal' and 'adenocarcinoma' breast cancer classes. By examining the expression levels of approximately 35,982 genes, the analysis reveals critical patterns aiding early detection and personalized treatment strategies.
![_- visual selection](https://github.com/user-attachments/assets/a1cb49fc-2ede-4f7a-8c19-536f5dc4b56e)

## Installation and Usage (For End-Users)

**1. Install Python (>=3.7) and necessary libraries:**

pip install pandas scikit-learn plotly

**2. Clone the repository:**

git clone https://github.com/Srash23/Breast-Cancer-Gene-Expression.git

**3. Navigate to the project directory:**

cd Breast-Cancer-Gene-Expression

**4. Run the analysis:**

python breast_cancer_analysis.py

## Methodology

### Step 1: Data Preprocessing

1. The dataset contains gene expression values for normal and adenocarcinoma samples.

2. Features (gene expression levels) are scaled to standardize values.

### Step 2: Logistic Regression Model

1. The dataset is split into training and test sets.

2. A logistic regression model is trained to distinguish between the two classes.

3. Coefficient values are extracted to identify genes with the highest influence on classification.

### Step 3: Identifying Key Genes

1. The top 20 most positive and 20 most negative coefficients are selected.

2. These genes represent potential oncogenes (upregulated in cancer) and tumor suppressors (downregulated in cancer).

### Step 4: Visualization

1. A bar chart visualizes the most influential genes for classification.

## Key Insights

**1. Significant Biomarkers Identified:** Genes like ENST00000426370 and ENST00000358739 show strong predictive influence.

**2. Machine Learning for Cancer Detection:** Logistic regression effectively classifies normal vs. cancerous tissues.

**3. Expression Level Trends:** Some genes are highly upregulated in adenocarcinoma, while others are repressed.

**4. Potential for Clinical Applications:** These findings can assist in biomarker discovery and targeted therapies.

## Conclusion

This study demonstrates how logistic regression applied to gene expression data can uncover key molecular patterns distinguishing breast cancer from normal tissues. The identification of influential genes contributes to cancer diagnostics and personalized medicine, paving the way for targeted therapeutic strategies.
