# Cross-Dataset Evaluation of Machine Learning Models for Stress Prediction and Exploring the Use of Domain Adaption Techniques to Improve a Model’s Generalisability

## Description

This project evaluates the **cross-dataset generalisability** of machine learning algorithms trained on smartwatch data for **stress prediction**. Models are trained on the **WESAD dataset** and tested on the **AffectiveROAD dataset**, with a focus on investigating the role of **domain adaptation techniques** in improving generalisation.

---

## Features

- Implement data-cleaning techniques to standardise WESAD and AffectiveROAD datasets for cross-dataset generalisation.
- Research and implement multiple ML models for stress prediction:
  - Feed-Forward Neural Network (FFNN)
  - Logistic Regression
  - Random Forest
  - AdaBoost
  - Support Vector Machine (SVM)
- Evaluate models using **Leave-One-Subject-Out (LOSO)** cross-validation on WESAD.
- Assess **cross-dataset generalisability** by testing models trained on WESAD with AffectiveROAD data.
  - Explore the distribution of the datasets.
- Research and implement domain adaptation techniques:
  - **CORAL (Correlation Alignment)**
  - **Importance Weighting**
  - **TCA (Transfer Component Analysis)**

---

## Installation

### Recommended Python version

- Python 3.12.2 or above

1. **Download the project folder**
2. **Install required libraries**
   pip install -r requirements.txt

---

## Project Structure

stress-prediction/
├── AffectiveROAD_Preprocessing/   # contains all AffectiveRoad's raw data and processing notebooks
│   ├── Left_Wrist/
│   │   ├── Drv1/
│   │   │   ├── preprocessing.ipynb
│   │   │   ├── BVP.csv
│   │   │   ├── EDA.csv
│   │   │   ├── SM_Drv.csv   # stress labels
│   │   │   └── TEMP.csv
│   │   ├── Drv3/
│   │   └── … (Drv4-Drv13, excluding Drv2)
│   └── Right_Wrist/
│       ├── Drv1/
│       └── … (Drv3-13, excluding Drv2)
│
├── WESAD_Preprocessing/
│   ├── S2/
│   ├── S3/
│   └── … (S2-17, excluding S12)
│   └── Experimental_Info/
│
├── Generalised Stress Models/
│   ├── Processed_WESAD_Data/
│   ├── AB Model.ipynb
│   ├── FFNN Model.ipynb
│   ├── LR Model.ipynb
│   ├── RF Model.ipynb
│   └── SVM Model.ipynb
│
└── Models and_Domain Adaption/
├── FFNN (Test and DA).ipynb
├── AB (Test and DA).ipynb
├── LR (Test and DA).ipynb
├── RF (Test and DA).ipynb
├── SVM (Test and DA).ipynb
├── Data Exploration.ipynb    # exploration of WESAD and AffectiveROAD's distribution
├── Processed_WESAD_Data/
└── Processed_AffectiveROAD_Data/

## Usage

1. Run each WESAD preprocessing notebook
2. Run each AffectiveRoad preprocessing notebook
3. Run each notebook within the generalised stress models folder
4. Run each notebook within the models and domain adaption folder

## Author

Ronan Sarkar – MSc Data Science, University of Bath

## References

1. P. Schmidt, A. Reiss, R. Duerichen, C. Marberger, K.V. Laerhoven. 2018. Introducing WESAD, a multimodal dataset for wearable stress and affect detection. ICMI ’18: Proceedings of the 20th ACM International Conference on Multimodal Interaction, pp. 400-408. DOI: 10.1145/3242969.3242985
2. El Haouij, N., Poggi, J.-M., Sevestre-Ghalila, S., Ghozi, R., and Jaïdane, M., 2018. AffectiveROAD system and database to assess driver’s attention. SAC ’18: Proceedings of the 33rd Annual ACM Symposium on Applied Computing, pp. 800-803. DOI: 10.1145/3167132.3167395
