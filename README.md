# Scene Classification using Transfer Learning
* Used **CNNs** and **Transfer Learning** to classify different scenes
* Three different models (MobileNetV2, Xception, and Inc-ResNetV2) adopted as the base model
* Fine-tuned the models to our small dataset of scene pictures
* Results demonstrated 94% accuracy in scene classification
<br>_Keywords(Classification, CNN, Transfer Learning, Fine-Tunning)_

## Dataset
We have chosen the “Scene Classification” dataset for training our model that includes a wide range of natural scenes. It contains about 25000 RGB images with 150x150 pixels. The images come in 6 classes which are tagged with Buildings, Forests, Mountains, Glacier, Street, and Sea.

Since the dataset is small, I did some augmentations on images including flipping, zooming, shifting, and rotating images. I used ImageDataGenerator to make a generator out of all authentic images.

## Results
### 1. Experiment results with MobileNetV2 Model with fine-tuning:
<img src="https://github.com/saeidesm/scene-classification-transfer-learning/blob/main/results-img/MobileNetV2.jpg" width="600" height="400" />

### 2. Experiment results with Xception Model with fine-tuning:
<img src="https://github.com/saeidesm/scene-classification-transfer-learning/blob/main/results-img/Xception.jpg" width="600" height="400" />

### 3. Experiment results with Xception Model with fine-tuning:
<img src="https://github.com/saeidesm/scene-classification-transfer-learning/blob/main/results-img/Inc-ResNetV2.jpg" width="600" height="400" />
