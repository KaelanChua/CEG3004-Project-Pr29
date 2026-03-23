# CEG3004-Project-Pr29
Sound classification project for CEG3004 
## Project Overview
This project implements an environmental sound classification pipeline for 50 environmental sound classes using digital signal processing feature extraction and a machine learning classifier in Google Colab.

## Baseline Modifications
Only the sections marked as `TODO` in the provided notebook were modified.

The following components were improved:
- audio preprocessing
- feature extraction
- model selection and hyperparameters

## Preprocessing
The preprocessing pipeline includes:
- trimming leading and trailing silence
- pre-emphasis filtering
- peak normalization
- fixed-length padding/truncation to 5 seconds

## Feature Extraction
The extracted features include:
- MFCC
- delta MFCC
- delta-delta MFCC
- log-mel spectrogram statistics
- spectral centroid
- spectral bandwidth
- spectral rolloff
- zero-crossing rate

The feature statistics used are:
- mean
- standard deviation
- median

## Model
The final classifier used is:
- `StandardScaler`
- `SVC` with RBF kernel
- `class_weight='balanced'`

## Validation Result
Validation Macro-F1 achieved:
- `0.5876`

## Repository Contents
- `CEG3004_Project_Pr29.ipynb` — final Google Colab notebook
- `README.md` — project documentation

## How to Run
1. Open the notebook in Google Colab
2. Run the cells from top to bottom
3. Download and extract the dataset in the notebook
4. Ensure the correct `GROUP_ID` is entered
5. The notebook will generate:
   - prediction CSV
   - trained model file



