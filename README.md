# Scene Classification using Transfer Learning
* Used **CNNs** and **Transfer Learning** to classify different scenes
* Three different models (MobileNetV2, Xception, and Inc-ResNetV2) adopted as the base model
* Fine-tuned the models to our small dataset of scene pictures
* Results demonstrated 94% accuracy in scene classification
<br>_Keywords(Classification, CNN, Transfer Learning, Fine-Tunning)_

## Dataset
We have chosen the “Scene Classification” dataset for training our model that includes a wide range of natural scenes. It contains about 25000 RGB images with 150x150 pixels. The images come in 6 classes which are tagged with Buildings, Forests, Mountains, Glacier, Street, and Sea.

## Methodology
Since the dataset is small, we did some augmentations on images including flipping, zooming, shifting, and rotating images after reding the data. we used ImageDataGenerator to make a generator out of all authentic images.

In transfer learning, there are two phases that we need to satisfy:
First, we need to extract features from the input data. At this level, we utilize the pre-defined model to get the pre-trained weights on ImageNet. The key here is that there is a softmax layer at the top of the pre-trained model to classify the dataset that the model has been trained on. However, we need to remove this layer to make our classifier. 
Second, we need to fine-tune the model based on setting some layers (or blocks) of the pre-trained model to trainable neurons, which means the weights can be updated according to the backpropagation process.

All three base models include multiple blocks; we have decided to unfreeze the same number of blocks of the base models, which means the neurons in those layers can be updated in backpropagation. In our experiments, we unfreeze the last one, three, and five blocks of each pre-trained model in three phases. Besides unfreezing those blocks, we also tested three different models by stacking from one up to three fully connected layers on top of the base model.

## Results
### 1. Experiment results with MobileNetV2 Model with fine-tuning:
<img src="https://github.com/saeidesm/scene-classification-transfer-learning/blob/main/results-img/MobileNetV2.jpg" width="600" height="400" />

### 2. Experiment results with Xception Model with fine-tuning:
<img src="https://github.com/saeidesm/scene-classification-transfer-learning/blob/main/results-img/Xception.jpg" width="600" height="400" />

### 3. Experiment results with Xception Model with fine-tuning:
<img src="https://github.com/saeidesm/scene-classification-transfer-learning/blob/main/results-img/Inc-ResNetV2.jpg" width="600" height="400" />

In the following figure, the training and validation accuracy and loss of the Xception model with three fully connected layers and fine-tuning the top 5 blocks of the pre-trained model, depicted in the plot which has the best accuracy over all other models on the scene classification dataset.
<img src="https://github.com/saeidesm/scene-classification-transfer-learning/blob/main/results-img/best-result.jpg" width="1000" height="400" />

