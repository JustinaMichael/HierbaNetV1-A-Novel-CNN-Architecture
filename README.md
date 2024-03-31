[![Reproducible Capsule](https://img.shields.io/static/v1?label=&message=code+ocean&color=blue)](https://codeocean.com/capsule/5579071/tree/v1)

# HierbaNetV1
HierbaNetV1 is a novel convolutional neural network (CNN) architecture with a cutting-edge feature extraction technique. This architecture extracts and integrates both low-level and high-level features. The high-level features that are generated exhibit features with different levels of complexity. The resulting low-level features show the essential traits of the region of interest, which. Feature integration facilitates a deeper comprehension of the object's patterns.

## Ideation of HierbaNetV1
The idea of HierbaNetV1 is to perform intensive feature extraction from each data sample focusing on multiple levels of complexity, irrespective of the ROI size, and emphasize low-level features consistently.

## Architecture of HierbaNetV1
The architecture is made up of 72 layers with 14.3 million parameters. The internal working of the architecture is detailed in the video article entitled "HierbaNetV1: A novel convolutional neural network architecture" published in 'Science Talks' - Elsevier journal, that can be accessed via the URL https://www.sciencedirect.com/science/article/pii/S2772569324000240

## Dataset utilized
'SorghumWeedDataset_Classification', a crop-weed research dataset used for testing the performance of HierbaNetV1. The following references relate to the dataset: </br>
a. First appeared at https://data.mendeley.com/datasets/4gkcyxjyss/1 </br>
b. GitHub repository: https://github.com/JustinaMichael/SorghumWeedDataset_Classification.git </br>
c. Detailed description of the data acquisition process: https://www.sciencedirect.com/science/article/pii/S2352340923009678

## Code capsule from code ocean
The implementation of HierbaNetV1 is Python and is available as a 'Reproducible code' in code ocean, that can be accessed via the URL https://codeocean.com/capsule/5579071/tree/v1

### Getting started
The source code 'HierbaNetV1.py' can be executed by clicking the 'Reproducible Run' button in the right pane of the capsule. The dataset is available in the 'data' folder in the left pane, which is imported implicitly for training the model. The 'data' folder also contains 'HierbaNetV1_SorghumWeedDataset_Classification_SKfold.h5', the trained HierbaNetV1 weights file that can be used for model testing.

### Testing HierbaNetV1
By default, the model is SET in ONLY TESTING MODE by initializing "Train_Val == 0" (line 214 in code). In this case, the trained HierbaNetV1 pre-trained weights are loaded to perform testing (line 351 in code).

### Training and Validating HierbaNetV1
To enable TRAIN and VALIDATE MODE, initialize "Train_Val == 1" (line 214 in code). HierbaNetV1 trains and validates with stratified 10-fold cross-validation.

## Results
HierbaNetV1 produces the highest accuracy of 0.9806 and the lowest loss of 0.07.

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
The figure below shows the base architecture of HierbaNetV1 followed by its Block I and Block II in detail.

![Fig 4  HierbaNetV1 – Base Architecture A Novel Convolutional Neural Network (CNN) Architect](https://github.com/JustinaMichael/HierbaNetV1_Sorghum_Weed_Classifier/assets/67352212/ab0f36cd-53fa-4539-898a-a76090bcc97e)
Fig 1: HierbaNetV1 - Base architecture

![Fig 5  HierbaNetV1_BlockI](https://github.com/JustinaMichael/HierbaNetV1_Sorghum_Weed_Classifier/assets/67352212/24a6979c-58fa-457a-87f7-2058262384b4)
Fig 2: HierbaNetV1 - Block I

![Fig  6  HierbaNetV1_BlockII](https://github.com/JustinaMichael/HierbaNetV1_Sorghum_Weed_Classifier/assets/67352212/4f3f3f20-c8f5-4962-8af7-af613bff8e42)
Gig 3: HierbaNetV1 - Block II

## Contributors profile <br/>
1. Justina Michael. J <br/>
        Google Scholar: https://scholar.google.com/citations?user=pEEzO14AAAAJ&hl=en&oi=ao <br/>
        ORCID: https://orcid.org/0000-0001-8072-3230 </br>
2. Dr. M. Thenmozhi <br/>
        Google Scholar: https://scholar.google.com/citations?user=Es49w08AAAAJ&hl=en&oi=ao <br/>
        ORCID: https://orcid.org/0000-0002-8064-5938 <br/>
