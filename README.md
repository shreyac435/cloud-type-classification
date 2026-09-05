# Cloud Type Classification 

An educational Deep Learning project that classifies ground-based sky images into 11 different cloud genus categories (including contrails) using Convolutional Neural Networks (CNNs).

## Project Overview
Atmospheric scientists rely on cloud classification to understand weather patterns and climate change. This project automates the process using the **Cirrus Cumulus Stratus Nimbus (CCSN) Database**. 

The repository features two distinct models:
1. **Custom CNN Baseline**: A lightweight 3-block CNN trained from scratch.
2. **Transfer Learning Model**: A robust `EfficientNetB3` model pre-trained on ImageNet.

> **Note**: This codebase is designed as an educational debugging exercise. The Jupyter Notebook currently contains placeholders where 8 common machine learning bugs (dimension mismatches, data leakage, catastrophic forgetting, etc.) will be injected for debugging practice.

## Dataset
The CCSN dataset contains 2,543 images categorized into the 11 WMO-defined cloud genera:
`Ac` (Altocumulus), `As` (Altostratus), `Cb` (Cumulonimbus), `Cc` (Cirrocumulus), `Ci` (Cirrus), `Cs` (Cirrostratus), `Ct` (Contrail), `Cu` (Cumulus), `Ns` (Nimbostratus), `Sc` (Stratocumulus), and `St` (Stratus).

Download the dataset zip from [here](https://drive.google.com/file/d/1OY6ljltOdKAeTIQowI8fARxOB7pzHt_I/view?usp=drive_link).

## Getting Started

### Prerequisites
Make sure you have Python 3.8+ installed. 

### Installation
Clone the repository
```bash
git clone https://github.com/your-username/cloud-type-classification.git
```
Navigate to the project directory
```bash
cd cloud-type-classification
```
Create a virtual environment (recommended)
```bash
python -m venv venv
```
Activate the virtual environment

On Windows:
```bash
#First run: cd venv/Scripts 
#Then: ./Activate.ps1
```

On macOS and Linux:
```bash
#First run: cd venv/bin 
#Then: source ./activate
```
Install project dependencies from requirements.txt
```bash
pip install -r requirements.txt
```

### Setup
1. Download the dataset from Kaggle and extract it into a folder named `dataset/` in the root directory.
2. Launch Jupyter Notebook or upload the `.ipynb` file to Google Colab.
```bash
jupyter notebook
```
3. Open and run `cloud_type_classification (1).ipynb`.

## Tech Stack
- **TensorFlow / Keras**: Model building, augmentation, and training
- **OpenCV**: Image ingestion and preprocessing
- **Scikit-Learn**: Stratified data splitting, class weights, and evaluation metrics
- **Matplotlib / Seaborn**: Visualizations and confusion matrices
