[![Reproducible Capsule](https://img.shields.io/static/v1?label=&message=code+ocean&color=blue)](https://codeocean.com/capsule/5579071/tree/v1)

# HierbaNetV1
HierbaNetV1 is a novel convolutional neural network (CNN) architecture with a cutting-edge feature extraction technique. This architecture extracts and integrates both low-level and high-level features. The high-level features that are generated exhibit features with different levels of complexity. The resulting low-level features show the essential traits of the region of interest. Feature integration facilitates a deeper comprehension of the object's patterns.

## Ideation of HierbaNetV1
The idea of HierbaNetV1 is to perform intensive feature extraction from each data sample focusing on multiple levels of complexity, irrespective of the ROI size, and emphasize low-level features consistently.

## Architecture of HierbaNetV1
The architecture is made up of 72 layers with 14.3 million parameters. The internal working of the architecture is detailed in the video article entitled "HierbaNetV1: A novel convolutional neural network architecture" published in 'Science Talks' - Elsevier journal, which can be accessed via the URL https://www.sciencedirect.com/science/article/pii/S2772569324000240

## Dataset utilized
'SorghumWeedDataset_Classification', a crop-weed research dataset used for testing the performance of HierbaNetV1. The following references relate to the dataset: </br>
a. First appeared at https://data.mendeley.com/datasets/4gkcyxjyss/1 </br>
b. GitHub repository: https://github.com/JustinaMichael/SorghumWeedDataset_Classification.git </br>
c. Detailed description of the data acquisition process: https://www.sciencedirect.com/science/article/pii/S2352340923009678

## Implementation of HierbaNetV1
Python implementation of HierbaNetV1 is released in two formats.
</br> 1. Reproducible Python code at Code Ocean
</br> 2. Interactive Python Notebook at GitHub repository

## 1. HOW TO USE - 'HierbaNetV1.py'
'HierbaNetV1.py' is a Code Ocean Compute Capsule that contains the implementation of HierbaNetV1 in Python. It is available as a 'Reproducible code' in code ocean at https://codeocean.com/capsule/5579071/tree/v1

### Getting started
The source code 'HierbaNetV1.py' can be executed by clicking the 'Reproducible Run' button in the right pane of the capsule. The dataset is available in the 'data' folder in the left pane, which is imported implicitly for training the model. The 'data' folder also contains the 'HierbaNetV1_SorghumWeedDataset_Classification_SKfold.h5', the trained HierbaNetV1 weights file that can be used for model testing.

### Training and Validating HierbaNetV1
To enable TRAIN and VALIDATE MODE, initialize "Train_Val == 1" (line 214 in code). HierbaNetV1 trains and validates with stratified 10-fold cross-validation.
```python
Train_Val = 0
if Train_Val == 1:
  # ===============Stratified K-Fold======================
  skf = StratifiedKFold(n_splits=num_folds, shuffle=True)
  ...
  ...
```

### Testing HierbaNetV1
By default, the model is SET in ONLY TESTING MODE by initializing "Train_Val == 0" (line 214 in code). In this case, the trained HierbaNetV1 pre-trained weights are loaded to perform testing (line 351 in code).
```python
elif Train_Val == 0:
  test_datagen = ImageDataGenerator(rescale=1./255)
  test_set = test_datagen.flow_from_directory(
 ...
  ...
```

## 2. HOW TO USE - 'HierbaNetV1 - Implementation in Python.ipynb' 
'HierbaNetV1 - Implementation in Python.ipynb' is an Interactive Python Notebook found along with this GitHub repository. This contains the interactive version of the implementation of HierbaNetV1 in Python and can be opened in the Google Collaboratory (or any other Jupyter Notebook environment). 

### Cloning the dataset
The dataset is cloned from the respective GitHub repository using the following command: 
```python
!git clone https://github.com/JustinaMichael/SorghumWeedDataset_Classification.git
```

### Cloning model weights
HierbaNetV1 weights trained on the 'SorghumWeedDataset_Classification' dataset are cloned from the respective GitHub repository using the following command: 
```python
!git clone https://github.com/JustinaMichael/HierbaNetV1-A-Novel-CNN-Architecture.git
```

### Model training, validating, testing
To enable TRAIN and VALIDATE MODE, initialize "Train_Val == 1". HierbaNetV1 trains and validates with stratified 10-fold cross-validation. By default, the model is SET in ONLY TESTING MODE by initializing "Train_Val == 0". In this case, the trained HierbaNetV1 pre-trained weights are loaded to perform testing.

## Results
HierbaNetV1 produces the highest accuracy of 0.9806 and the lowest loss of 0.07 when trained on 'SorghumWeedDataset_Classification' with stratified 10-fold cross-validation.

## Patent 
'HierbaNetV1' architecture is patented under the Indian Patent Act and is part of our research work.

## Licence
'HierbaNetV1_Sorghum_Weed_Classifier' software is licensed under the APACHE LICENSE, VERSION 2.0.

## Citation 
Please give credit to the "HierbaNetV1" architecture if you find it useful and utilize it in your work by citing 
```
J. Justina Michael and M. Thenmozhi, HierbaNetV1: A novel convolutional neural network architecture, (2024), https://doi.org/10.1016/j.sctalk.2024.100316
```

## HierbaNetV1_Base, HierbaNetV1_Block1, and HierbaNetV1_BlockII
The HierbaNetV1 base architecture's schematic is displayed below, followed by blocks I and II.

![Fig 4  HierbaNetV1 – Base Architecture A Novel Convolutional Neural Network (CNN) Architect](https://github.com/JustinaMichael/HierbaNetV1_Sorghum_Weed_Classifier/assets/67352212/ab0f36cd-53fa-4539-898a-a76090bcc97e)
Fig 1: HierbaNetV1 - Base architecture

![Fig 5  HierbaNetV1_BlockI](https://github.com/JustinaMichael/HierbaNetV1_Sorghum_Weed_Classifier/assets/67352212/24a6979c-58fa-457a-87f7-2058262384b4)
Fig 2: HierbaNetV1 - Block I

![Fig  6  HierbaNetV1_BlockII](https://github.com/JustinaMichael/HierbaNetV1_Sorghum_Weed_Classifier/assets/67352212/4f3f3f20-c8f5-4962-8af7-af613bff8e42)
Fig 3: HierbaNetV1 - Block II

## Contributors profile <br/>
1. Justina Michael. J <br/>
        Google Scholar: https://scholar.google.com/citations?user=pEEzO14AAAAJ&hl=en&oi=ao <br/>
        ORCID: https://orcid.org/0000-0001-8072-3230 </br>
2. Dr. M. Thenmozhi <br/>
        Google Scholar: https://scholar.google.com/citations?user=Es49w08AAAAJ&hl=en&oi=ao <br/>
        ORCID: https://orcid.org/0000-0002-8064-5938 <br/>
