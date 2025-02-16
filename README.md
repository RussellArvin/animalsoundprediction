# Animal Sound Prediction Project

## Team Members
- Russell Arvin [GitHub](https://github.com/RussellArvin)
- Leanne Yeong [GitHub](https://github.com/leanneyeong)
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

5. **Model Training and Evaluation:** We trained and evaluated the selected models using appropriate evaluation metrics, such as accuracy, to assess their performance in classifying animal sounds.

## Conclusion and Insights

### Best Performing Model
After extensive testing and evaluation of various machine learning models, the **Random Forest Classifier** emerged as the best performing model for our animal sound prediction project. This model provided the most robust results due to its ability to handle the complex structures within the audio feature set effectively. The Random Forest Classifier, known for its high accuracy and ability to run efficiently on large databases, proved ideal for dealing with the multi-dimensional and diverse nature of our environmental sound dataset.

### Insights on Outlier Removal
An unexpected yet valuable insight from our project was the effect of outlier removal on the model's performance. Contrary to our initial assumption that removing outliers would enhance model accuracy by reducing noise, we observed a decrease in accuracy. This phenomenon can be attributed to the nature of audio data, particularly in biodiversity and environmental monitoring contexts. In such settings, what might be classified as outliers could actually represent rare but crucial animal sounds that are critical for accurate classification. Removing these 'outliers' might lead to a model that is less capable of recognizing less frequent, yet significant, animal sounds in the dataset.

This underscores the importance of a nuanced approach to data preprocessing in audio analysis, where outlier management must be balanced with the preservation of rare and informative audio samples that could be vital for the success of environmental sound classification.

### Future Directions
Going forward, we plan to refine our preprocessing techniques to better distinguish between noise and rare sound events. Further exploration into more sophisticated outlier detection methods tailored specifically for audio data will also be a priority. Enhancing our model's ability to generalize to new, unseen data will be crucial as we continue to support biodiversity studies and environmental monitoring efforts.

This project has not only advanced our understanding of machine learning applications in audio analysis but also highlighted critical considerations that could guide future research in this field.
