# liquid-height-cnn

This is a CNN-based method for liquid height estimation using audio signals when pouring liquid into a container. I found that https://github.com/lianghongzhuo/AudioPouring has used RNN(LSTM) method to measure height, but I think CNN is more suitable since spectrogram is used as features. Also, CNN is not only faster than LSTM but also has less parameters, which is helpful to real-life usage.

## Dataset Download
Please visit the link above for dataset downloading. This dataset contains over 3000 audio records of water pouring. After downloading, create a new document called "pickle" to save the dataset. Run *model/preprocess_cnn.py* to preprocess the original data into *.npy* file which contains information like spectrogram and groundtruth of air column length for training models.

## File Information
### assets/
This document contains pre-trained 2-layer LSTM model and CNN model. You can load them to test results.

### config/


