# Kaggle-Dogs-vs.-Cats
To get further information of this Kaggle competition, please check: https://www.kaggle.com/competitions/dogs-vs-cats-redux-kernels-edition/leaderboard

### Goal:
The goal of this project is to train the algorithm on 25,000 image files and predict the labels for dogs and cats.

### Modeling:
The project aimed to achieve high accuracy in classifying images of dogs and cats using transfer learning. The approach involved training the entire model with a new binary-classifier head that predicts the probabilities of "dog" and "cat." The base model used was EfficientNetV2B3, pre-trained on the ImageNet dataset, which comprises 1.4 million images and 1000 classes. To prevent the loss of useful information during training, I froze the base model throughout training by setting its trainable property to False.

Further, I added a GlobalAveragePooling2D layer before the DenseBN layer (a fully connected layer followed by Batch Normalization) and applied a relu activation function to the model. This approach resulted in a 99% accuracy rate with a single training epoch. Overall, the transfer learning model's architecture successfully incorporated the pre-trained base model, resulting in an improved performance in classifying images of dogs and cats.

### Result:
The success of the project will be measured by achieving a private score of 0.04946.
