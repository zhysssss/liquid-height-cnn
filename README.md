# liquid-height-cnn

This is a CNN-based method for liquid height estimation using audio signals when pouring liquid into a container. I found that https://github.com/lianghongzhuo/AudioPouring has used RNN(LSTM) method to measure height, but I think CNN is more suitable since spectrogram is used as features. Also, CNN is not only faster than LSTM but also has less parameters, which is helpful to real-life usage.

## Dataset Download
Please visit the link above for dataset downloading. This dataset contains over 3000 audio records of water pouring. After downloading, create a new document called "pickle" to save the dataset. Run *model/preprocess_cnn.py* to preprocess the original data into *.npy* file which contains information like spectrogram and groundtruth of air column length for training models.

## Important File Information
### 1.assets/
This document contains pre-trained 2-layer LSTM model and CNN model. You can load them to test results.

### 2.config/
This document contains parameters of target containers, which represent the relationship between each container's air column length and weight of water.

### 3.model/
This document contains files like *model.py* and *preprocess_cnn.py*.

### 4.main_cnn.py
This python file is model training code.

## Run Training Code
1. Run *preprocess_cnn.py* to generate a document named "dataset", which includes preprocessed train data and test data.
2. Run *generate_npy_list.py* to convert data into *.npy* file.
3. Run *main_cnn.py* to train model.

