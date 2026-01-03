# Thesis Data Analysis Project

This repository contains code and data for the analysis and modeling of public transport data as part of a thesis project. The workflow is organized into several stages, from raw data cleaning to model-specific experiments.

The data used is not provided by this project. It can be provided for free for academic research by [NDOV Loket](https://ndovloket.nl/).

## Project Structure

```
MainProject/
├── data-cleaning.ipynb
├── data/
│   ├── converted/
│   ├── input/
│   ├── models/
│   ├── NeTEx/
│   └── final/
├── data_preparationL002.ipynb
├── data_preparationL011.ipynb
├── data_preparationL321.ipynb
├── data_preparationL401.ipynb
├── dova/
│   ├── L002/
│   │   ├── data_l002.ipynb
│   │   └── dova_algorithm.ipynb
│   ├── L011/
│   │   ├── data_l011.ipynb
│   │   └── dova_algorithm.ipynb
│   ├── L321/
│   │   ├── data_l321.ipynb
│   │   └── dova_algorithm.ipynb
│   └── L401/
│       ├── data_l401.ipynb
│       └── dova_algorithm.ipynb
├── LR/
│   ├── linear_regression_L002.ipynb
│   ├── linear_regression_L011.ipynb
│   ├── linear_regression_L321.ipynb
│   └── linear_regression_L401.ipynb
├── lstm/
│   ├── lstm_gpu_L002.ipynb
│   ├── lstm_gpu_L011.ipynb
│   ├── lstm_gpu_L321.ipynb
│   └── lstm_gpu_L401.ipynb
└── xgboost/
	 ├── xgboost2_L002.ipynb
	 ├── xgboost2_L011.ipynb
	 ├── xgboost2_L321.ipynb
	 ├── xgboost2_L401.ipynb
	 └── models/
```

## Workflow Overview

### 1. Data Cleaning

- **`data-cleaning.ipynb`**: Performs initial cleaning and preprocessing of raw KV6 and NeTEx data files. This step ensures the data is in a consistent and usable format for further analysis.

### 2. Data Preparation

- **`data_preparationLXXX.ipynb`**: Each file (where `XXX` is a line code, e.g., L002, L011, etc.) prepares the cleaned data for input into the modeling stage. This includes feature engineering, filtering, and formatting specific to each line.

### 3. Model-Specific Folders

- **`LR/`**: Contains linear regression models for each line (e.g., `linear_regression_L002.ipynb`).
- **`lstm/`**: Contains LSTM (Long Short-Term Memory) neural network models for each line (e.g., `lstm_gpu_L002.ipynb`).
- **`xgboost/`**: Contains XGBoost models for each line (e.g., `xgboost2_L002.ipynb`).
- **`dova/`**: Contains DOVA algorithm notebooks for each line, with both data preparation and algorithm implementation files.

### 4. Data Folders

- **`data/`**: Contains subfolders for various stages of data (converted, input, models, NeTEx, final).
- **`input/`**: Stores input data for the models.
- **`models/`**: Stores trained model files and related outputs.

## Getting Started

1. **Environment Setup**
   - Use the provided `environment.yml` to set up the required Python environment:
     ```fish
     conda env create -f environment.yml
     conda activate <env_name>
     ```
2. **Data Cleaning**
   - Run `data-cleaning.ipynb` to process raw data.
3. **Data Preparation**
   - Run the relevant `data_preparationLXXX.ipynb` for your line of interest.
4. **Model Training & Evaluation**
   - Explore the `LR/`, `lstm/`, `xgboost/`, and `dova/` folders for model-specific notebooks.

## Notes

- Each model and data preparation notebook is line-specific (L002, L011, L321, L401).
- Ensure data is cleaned and prepared before running model notebooks.
- Outputs and trained models are saved in the corresponding folders.

## License

This project is for academic use. Please contact the author for other uses.
