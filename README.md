# MSA-ML-RECRUITMENT-PROJECT
# Simple ML Model: Predicting Solubility (logS)

A basic machine learning project that predicts a molecule's solubility using a Linear Regression model.

## What does it do?

This project uses a few properties (like molecular weight and lipophilicity) of a compound to predict its solubility in water (logS). This is a common task in chemistry and drug discovery.

## How does it work?

1.  **Data:** It uses a public dataset with 1144 molecules and their properties.
 The dataset used is the Delaney solubility dataset, which is a standard benchmark in this field.

    Source: https://raw.githubusercontent.com/dataprofessor/data/master/delaney_solubility_with_descriptors.csv

    Size: 1144 molecules, 5 columns

    Features (X):

        MolLogP: Molecular lipophilicity (Octanol-water partition coefficient)

        MolWt: Molecular weight

        NumRotatableBonds: Number of rotatable bonds

        AromaticProportion: Proportion of aromatic atoms in the molecule

    Target (y):

        logS: Logarithm of the aqueous solubility (mol/L), the value we want to predict.
2.  **Model:** A simple Linear Regression model is trained to find the relationship between the molecular properties and their solubility.
3.  **Result:** The model learns this relationship and can then predict the solubility of new molecules.

## Performance

The model's performance is measured on a held-out test set:
*   **Test R² Score:** `0.79`
*   **Test MSE:** `1.02`

An R² score of 0.79 means the model explains 79% of the variance in the solubility data, which is a good result for a simple model.
    ```
3.  Open and run the `MSA_ML_project.ipynb` google colab Notebook. The code will automatically download the data, train the model, and show the results.
