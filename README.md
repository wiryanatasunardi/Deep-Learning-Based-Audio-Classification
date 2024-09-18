# Deep-Learning-Based-Audio-Classification

This project aims to classify audio files and identify the musical instruments used in them by developing deep learning models using CNN and RNN architectures. The dataset consists of audio files categorized into 10 different instrument classes.

## Dataset
The dataset contains audio files from the following 10 classes:
- Acoustic Guitar
- Bass Drum
- Cello
- Clarinet
- Double Bass
- Flute
- Hi Hat
- Saxophone
- Snaredrum
- Violin

Project Overview

This project is implemented in a Jupyter Notebook and follows the following steps:

### 1. Dataset Preprocessing
The initial step involves converting the audio files into a CSV format. The CSV files contains the length and the label of each file in the dataset. The class distribution is then visualized using a pie chart to understand the balance of the dataset.

![Class Distribution](https://github.com/wiryanatasunardi/Deep-Learning-Based-Audio-Classification/blob/main/Documentation/Class_Distribution.png)

### 2. Feature Extraction
For each class, the following features were extracted from the audio samples:
- Time Domain Signals: Raw audio signal plotted over time.
- Frequency Domain Signals: The audio that has been transformed using Fourier Transform.
- Filter Banks: Representation of the power spectrum density in different frequency bands.
- MFCCs (Mel-Frequency Cepstrl Coefficients): Captures important audio characteristics useful for classification.

The following chart represents the features extraction result of the samples used in the features extraction process.
![Time Domain Signals Feature Extraction](https://github.com/wiryanatasunardi/Deep-Learning-Based-Audio-Classification/blob/main/Documentation/Audio_Feature_Plot.png)
![Frequency Domain Signals Feature Extraction](https://github.com/wiryanatasunardi/Deep-Learning-Based-Audio-Classification/blob/main/Documentation/Audio_Frequency_Domain.png)
![Filter Banks Signals Feature Extraction](https://github.com/wiryanatasunardi/Deep-Learning-Based-Audio-Classification/blob/main/Documentation/Audio_Filter_Banks.png)
![MFCC Signals Feature Extraction](https://github.com/wiryanatasunardi/Deep-Learning-Based-Audio-Classification/blob/main/Documentation/Audio_MFCC.png)

### 3. Data Cleaning
Using librosa library, the audio data was cleaned by:
- Resampling: Changing the sampling rate of the audio files for consistency
- Envelope Function: Creating an envelope function to describe the changes in signal amplitude over time.

### 4. Model Development
There are two models developed for this classification:

#### 1. RNN Model
In this model, there are LSTRM layers used to capture temporal dependencies in the audio signals.

#### 2. CNN Model
In this model, there are Convolutional layers that are paired with MaxPooling layers to extract spatial features from the audio representations.

### 5. Model Evaluation 
Both models were trained and evaluated using accuracy as the evaluation metric. The following chart shows the training and validation accuracy and loss over epoch for RNN model.

![RNN Model Evaluation](https://github.com/wiryanatasunardi/Deep-Learning-Based-Audio-Classification/blob/main/Documentation/RNN_Evaluation.png)

The following chart shows the training and validation accuracy and loss over epoch for CNN model.

![CNN Model Evaluation](https://github.com/wiryanatasunardi/Deep-Learning-Based-Audio-Classification/blob/main/Documentation/CNN_Evaluation.png)

The CNN model achieved the highest accuracy of 92.137%
