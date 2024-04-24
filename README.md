# Animal Sound Prediction Project

## Team Members
- Russell Arvin [GitHub](https://github.com/RussellArvin)
- Leanne Yeong [GitHub](https://github.com/sockgothole)
- Koh Jia Jun [GitHub](https://github.com/kohjiajun)

## Overview
This project focuses on the prediction of animal sounds from environmental recordings using machine learning. We utilize the Librosa library for audio feature extraction and an environmental sound dataset to train our model. The goal is to accurately identify and classify animal sounds, aiding in biodiversity studies and environmental monitoring.

## Features
- **Audio Feature Extraction:** Utilize Librosa for advanced audio feature extraction, including MFCCs, chroma-stft, spectral contrast, and tonnetz features.
- **Dataset:** Training performed on a curated dataset of environmental sounds, specifically focused on various animal calls.
- **Model Training:** Implementation of a machine learning model capable of classifying animal sounds with high accuracy.

## Methodology
1. **Exploratory Data Analysis (EDA):** We conducted an extensive EDA on the different audio features extracted using Librosa. This analysis helped us understand the characteristics and distributions of each feature.

2. **Feature Selection:**
  - **Correlation Analysis (Overall):** We performed correlation analysis between the audio features and the presence of any animal sound to identify the most relevant features for overall animal sound detection.
  - **Correlation Analysis (Specific Animals):** Additionally, we conducted correlation analysis between the audio features and the presence of specific animal sounds to identify the most relevant features for classifying individual animal species.

3. **Data Preprocessing:**
  - **Outlier Removal:** We identified and removed outliers from the dataset to ensure better model performance and reduce noise.

4. **Model Selection and Hyperparameter Tuning:**
  - **Model Selection:** Based on the nature of the problem and the analysis performed, we selected appropriate machine learning models for animal sound classification. The selected models include XGBoost, RandomForestClassifier, SVC, KNeighbors Classifier, LogisticRegression, MLP, DecisionTreeClassifier, BaggingClassifier, and GaussianNB.
  - **Hyperparameter Tuning:** We employed a search algorithm (e.g., Grid Search or Random Search) to find the optimal hyperparameters for each model, enhancing their performance and generalization capabilities.

5. **Model Training and Evaluation:** We trained and evaluated the selected models using appropriate evaluation metrics, such as accuracy, precision, recall, and F1-score, to assess their performance in classifying animal sounds.