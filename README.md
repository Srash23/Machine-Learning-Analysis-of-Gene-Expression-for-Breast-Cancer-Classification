# Gene Expression-Based Classification of Breast Adenocarcinoma

This repository presents a logistic regression model to classify breast tissue samples as either **normal** or **adenocarcinoma**, using transcriptomic gene expression data. The workflow involves standardizing features, training a logistic regression model, interpreting coefficients to identify key predictive genes, and visualizing the results.

## Project Overview

This project applies logistic regression on high-dimensional transcriptomic data to distinguish normal breast tissue from breast adenocarcinoma. It demonstrates the utility of simple linear models in bioinformatics and provides biological insights through gene feature interpretation.

## Objectives

- Preprocess transcriptomic data and remove non-informative identifiers  
- Standardize gene expression values for model training  
- Train a logistic regression classifier to predict tumor status  
- Extract and interpret model coefficients to identify top predictive genes  
- Visualize gene influence using bar plots, heatmaps, and dimensionality reduction

## Dataset Description

| Component        | Description                                           |
|------------------|--------------------------------------------------------|
| `type`           | Class label: `normal` or `breast_adenocarcinoma`       |
| `samples`        | Sample identifiers (removed during preprocessing)      |
| Gene columns     | ~36,000 gene/transcript expression values              |
| Total samples    | 289 breast tissue samples                              |

## Pipeline Summary

### 1. Data Preprocessing
- Load the gene expression CSV dataset using pandas  
- Drop the `samples` identifier column  
- Standardize gene expression features using `StandardScaler`

### 2. Model Training
- Split dataset into 80:20 train/test split  
- Train `LogisticRegression` with `max_iter=10000`  
- Evaluate performance using accuracy and classification report

### 3. Coefficient Extraction
- Extract feature coefficients from the trained model  
- Sort coefficients to identify the top 20 upregulated (adenocarcinoma) and 20 downregulated (normal) genes

### 4. Visualization (Basic)
- Create a horizontal bar chart using Plotly Express  
- Color-code bars by class label to highlight influential genes

## Visual Analysis

To enhance interpretability and present deeper model diagnostics, additional plots were created using the top 40 genes:

### 1. Coefficient Bar Chart  
Shows the 20 most upregulated and 20 most downregulated genes influencing the classifier.
<img width="1349" alt="Screenshot 2025-04-21 at 9 00 38 PM" src="https://github.com/user-attachments/assets/a37671ca-44a2-4411-905a-a8559d64ee48" />

### 2. Coefficient Histogram  
Visualizes the distribution of all model coefficients, highlighting sparsity and directional skewness.
<img width="589" alt="Screenshot 2025-04-21 at 9 01 03 PM" src="https://github.com/user-attachments/assets/0942f865-9365-473e-8db0-9d8b5241c234" />

### 3. Lollipop Chart  
Provides a clear and minimalistic alternative to bar charts, emphasizing magnitude via dots and stems.
<img width="1353" alt="Screenshot 2025-04-21 at 9 04 03 PM" src="https://github.com/user-attachments/assets/2a444f62-6642-41b0-af9d-c30d61711ac8" />

### 4. Heatmap (Top Genes)  
Visualizes simulated expression profiles of the top 20 genes across synthetic samples, showing clustering patterns.
<img width="1025" alt="Screenshot 2025-04-21 at 9 02 00 PM" src="https://github.com/user-attachments/assets/3c7da82f-19eb-41b5-a8b3-96a7205f21a4" />

### 5. 3D PCA Plot  
Performs dimensionality reduction using Principal Component Analysis (PCA) on simulated data. Shows sample variance and potential separability in 3D space.
<img width="393" alt="Screenshot 2025-04-21 at 9 02 53 PM" src="https://github.com/user-attachments/assets/9977c5ff-a0c6-46a3-9975-e08a95d398d6" />

## Tools Used
- **Language**: Python
- **Libraries**: pandas, scikit-learn, plotly
- **Model**: Logistic Regression

## Insights & Applications
- Logistic regression can uncover biologically meaningful gene expression patterns
- Coefficients offer interpretability for biomarker discovery
- Visualization aids in the communication of key gene-level drivers in cancer

## License
MIT License
