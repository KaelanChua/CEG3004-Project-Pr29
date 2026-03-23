# CEG3004 Environmental Sound Classification

## Group
Pr_29

## Overview
This repository contains the final implementation for the CEG3004 environmental sound classification project.

The system classifies 50 environmental sound classes using a DSP-based feature extraction pipeline and an SVM classifier.

## Files
- `CEG3004_Project_Colab_pr_29.ipynb` — final Colab notebook
- `CEG3004_Project_Colab_pr_29.py` — Python export of the final implementation
- `README.md` — project documentation

## Pipeline

### Preprocessing
The preprocessing stage performs:
- silence trimming
- pre-emphasis filtering
- peak normalization
- fixed-length padding/truncation to 5 seconds

### Feature Extraction
The final feature set includes:
- MFCC
- delta MFCC
- delta-delta MFCC
- log-mel spectrogram statistics
- spectral centroid
- spectral bandwidth
- spectral rolloff
- zero-crossing rate
- spectral contrast

Feature pooling is done using:
- mean
- standard deviation
- median
- 25th percentile
- 75th percentile

### Model
The final model is:
- `StandardScaler`
- `SVC(kernel='rbf', C=10, gamma='scale', class_weight='balanced')`

## Experiments
The baseline notebook was improved through:
- preprocessing changes
- expanded feature extraction beyond baseline MFCC statistics
- comparison of different SVM hyperparameters
- comparison of alternative feature configurations

The final configuration was selected based on validation Macro-F1.

## Best Validation Result
- Macro-F1: `0.6299`

## Reproducibility
To run the project:
1. Open the notebook in Google Colab
2. Run the cells from top to bottom
3. Download and extract the dataset through the notebook
4. set the correct `GROUP_ID`
5. train the model
6. generate the submission CSV

## Outputs
The notebook generates:
- prediction CSV
- trained `.joblib` model file
