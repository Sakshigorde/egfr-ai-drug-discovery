# AI-Based Drug Discovery: EGFR Activity Prediction

## Project Overview
This project uses machine learning to predict the activity of chemical compounds against EGFR (Epidermal Growth Factor Receptor), a protein associated with several cancers.

## Technologies Used
- Python
- ChEMBL database
- RDKit
- Pandas and NumPy
- Scikit-learn
- Matplotlib

## Methodology
1. Retrieved EGFR IC50 activity data from ChEMBL.
2. Processed chemical structures using SMILES.
3. Generated 2048-bit Morgan fingerprints using RDKit.
4. Labelled compounds using an IC50 threshold of 1000 nM.
5. Trained a Random Forest classifier.
6. Evaluated performance using random and scaffold splits.
7. Developed a function to predict activity from a compound's SMILES.

## Results

| Metric | Result |
|---|---:|
| Random split accuracy | 90.67% |
| Scaffold split accuracy | 83.58% |
| Scaffold split ROC-AUC | 0.932 |

## Example Prediction
- Compound: Gefitinib
- Predicted class: Active
- Model-estimated active probability: 72%

This prediction is not proof of drug efficacy.

## Limitations
- Results depend on the chosen activity threshold.
- Repeated measurements and assay differences may affect predictions.
- Independent validation and further testing are needed.

## Future Improvements
- Test on an independent dataset.
- Improve data cleaning and assay consistency.
- Compare additional machine-learning algorithms.
- Develop an interactive prediction interface.

## Data Source
[ChEMBL Database](https://www.ebi.ac.uk/chembl/)

## Disclaimer
This project is for educational and research purposes only. Model predictions do not establish clinical effectiveness or suitability as a medicine.
