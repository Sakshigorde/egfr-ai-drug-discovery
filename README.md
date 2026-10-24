# AI-Based Drug Discovery: EGFR Activity Prediction

## Project Overview
This project uses machine learning to predict whether chemical
compounds may be active against EGFR (Epidermal Growth Factor Receptor),
a target associated with several cancers.

## Technologies Used
- Python
- ChEMBL bioactivity database
- RDKit for molecular processing
- Pandas and NumPy
- Scikit-learn
- Matplotlib

## Methodology
1. Retrieved EGFR IC50 activity records from ChEMBL.
2. Processed molecular structures represented as SMILES.
3. Generated 2048-bit Morgan fingerprints using RDKit.
4. Labelled compounds using an IC50 threshold of 1000 nM.
5. Trained a Random Forest classifier.
6. Evaluated performance using random and scaffold splits.
7. Built a function to predict activity for new SMILES inputs.

## Results
- Random split accuracy: 90.67%
- Scaffold split accuracy: 83.58%
- Scaffold split ROC-AUC: 0.932

## Example Prediction
A Gefitinib SMILES input was classified as Active,
with a model-estimated active probability of 72%.

This is a model prediction and not proof of drug efficacy.

## Limitations
- Activity labels depend on the selected IC50 threshold.
- Assay differences and repeated measurements may affect results.
- Further validation using independent compounds is needed.
- Predictions do not establish clinical effectiveness.

## Future Improvements
- Validate on an independent dataset.
- Improve data curation and assay consistency.
- Compare Random Forest with other machine-learning models.
- Build an interactive compound-prediction interface.

## Data Source
ChEMBL: https://www.ebi.ac.uk/chembl/

## Disclaimer
This project is for educational and research purposes only.
It does not provide medical advice or identify clinically effective drugs.
