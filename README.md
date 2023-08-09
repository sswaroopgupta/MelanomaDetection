# MelanomaDetection

This is a project of multiclass classification model using a custom convolutional neural network in TensorFlow. 

## Problem statement 

To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

## Dataset details
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.


The data set contains the following diseases:

Actinic keratosis
Basal cell carcinoma
Dermatofibroma
Melanoma
Nevus
Pigmented benign keratosis
Seborrheic keratosis
Squamous cell carcinoma
Vascular lesion

Comaparing the models

|Model Name|Optimization|Final Epoch Details|Comments|
|----------|-----------|------|----------|
|cnnForMelnama_no_opt|No dropout, no batch normalization|loss: 0.8686 - sparse_categorical_accuracy: 0.6694 - val_loss: 0.8501 - val_sparse_categorical_accuracy: 0.6747|The loss and accuracy curves are varying significantly|
|cnnForMelnama_64_7_5_3_1_exp|Dropout and batch normalization|loss: 0.5139 - sparse_categorical_accuracy: 0.8046 - val_loss: 0.5487 - val_sparse_categorical_accuracy: 0.8086|The loss value has significantly lowered and the performance has improved however the curves are still varying significantly|
|cnnForMelnama_32_7_5_3_1_exp|Dropout and batch normalization|loss: 0.8878 - sparse_categorical_accuracy: 0.6666 - val_loss: 0.6390 - val_sparse_categorical_accuracy: 0.7815|The loss and accuracy curves are varying but better than before|
|cnnForMelnama_dropout|Dropout and batch normalization|loss: 0.9659 - sparse_categorical_accuracy: 0.6315 - val_loss: 0.7142 - val_sparse_categorical_accuracy: 0.7365|The curves are more stable than before but the gap between training results and validation results is more|
|cnnForMelnama_8_7_5_3_1_exp|dropout and batch normalization|loss: 0.7749 - sparse_categorical_accuracy: 0.7048 - lr_metric: 0.0022 - val_loss: 0.6044|average curve variations are present|
|cnnForMelnama_batch|Batch normalization|loss: 0.5684 - sparse_categorical_accuracy: 0.7915 - val_loss: 0.5058 - val_sparse_categorical_accuracy: 0.8189|The loss value has significantly lowered and the performance has improved and the curves are stable|
