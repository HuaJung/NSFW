# AI in Not Safe For Work Detection

### Introduction
- To prohibit NSFW (Not Safe for Work) photos, in Facebook, there are 15,000 ”content moderators” around the world who needs to examine 25,000 post daily. 

- CEO of Facebook, Mark Zuckerberg, admitted that moderators “make the wrong call in more than one out of every 10 cases.

- The goal of the project is to build an AI detection model for filtering the photos with sex and nudity. We use CNN as our fundamental algorithm and optimize model performance by using different parameters and datasets. 

### Dataset
- The dataset used in projects (NSFW vs SFW) is open dataset on Kaggle, and is available via <https://www.kaggle.com/datasets/omeret/not-safe-for-work>
- There were many incorrect labelling on raw dataset, after relabeling by hand, the datasets were rearranged as below:

| Data Mode \ Classes |NSFW |SFW| 
|:--------:|:------:|:------:|
|Training Data |2,155pcs | 2,155pcs|
|Validation Data| 909pcs |  909pcs|


### Methodology and Results
- In order to get best classifier which can detect most of NSFW photos, we plan to use different models, image augmentation techniques and hyperparameters.

  * Model: EfficientNet-B7, ResNet18, ResNet34, ResNet50, DenseNet161
  * Augmentation: RandomHorizontalFlip, RandomVerticalFlip, Grayscale, ColorJitter
  * Hyperparameter: Epoch, Batch size, Learning rate

- Since the goal of project is to detect as much as NSFW photos under at least 95% classified accuracy ( the accuracy of moderator is 90%), Type II error and accuracy are used as the criteria of model selection. 

- EfficientNet has a much higher  accuracy among all models (96.2%), with the lowest type II error 1.71%.

![alt 文字](https://github.com/HuaJung/NSFW/blob/main/img%20for%20README/model%20comparison.png)
![alt 文字](https://github.com/HuaJung/NSFW/blob/main/img%20for%20README/confusion%20matrix.png)

### Discussion and Conclusion
- EfficientNet-B7 is our best model with higher accuracy and the lowest type II error.
- We can't upload NSFW data on google drive for model training
- Image misjudgement

### Future Work
- Add more images of misjudgment types into datasets to improve the accuracy 
- Add other NSFW categories such as violence, terrorism, drug abuse

### Reference
- Karen Simonyan & Andrew Zisserman, Very Deep Convolutional Networks for Large-scale Image Recognition (2015).
- Kaiming He, Xiangyu Zhang, Shaoqing Ren & Jian Sun, Deep Residual Learning for Image Recognition (2015).
- Gao Huang, Zhuang Liu & Laurens van der Maaten, Densely Connected Convolutional Networks (2018).
- Koetsier, J. Report: Facebook Makes 300,000 Content Moderation Mistakes Every Day. Forbes(2020).
- OmerEven Tzur. (2020, April). NSFW Not Save For Work, Version 1. Retrieved March 24, 2022, from <https://www.kaggle.com/datasets/omeret/not-safe-for-work>

