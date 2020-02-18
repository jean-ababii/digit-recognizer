# digit-recognizer
This project consists in creating a digit classifier using the well-known MNIST dataset. The goal of this project is to improve my knowledge in the machine learning field, but also discover new tools such as Kaggle, Google Colab and Github. 

## Tools

### Google Colab
The project was realized using a Jupyter notebook directly on the Google colab platform. The advantage is that Google Colab allows us to use GPU or TPU to compute our code, which can significantly increase the training speed of neural networks. Indeed, in my CNN, it takes 9 seconds per epoch while using the GPU, and around 5 minutes per epoch while using the CPU, which is 30x faster.

### Kaggle
We can find a lot of very different datasets on Kaggle, but it also hosts competitions in the data field. For some of them, there are big cash rewards (1 000 000 $ for the Deepfake Detection Challenge), but the Digit Recognizer one is there for educational purposes.

In order to access directly the needed dataset from the notebook, it is necessary to first link it to your Kaggle account with a API token system. A complete description of the necessary steps can be found here:
https://www.kaggle.com/zaynena/using-colab-for-kaggle-competitions

## Code
The code is composed of the following parts:
- Download the dataset
- Visualization
- Simple Neural Network
- Convolutional Neural Network
- Test

In order to create and train neural networks, the Keras framework was used in all this project.

The first network was trained using a model composed of 2 layers of neurons with a ReLU activation function, and then a softmax layer to classify the pictures.

The CNN was trained using some additional functions such as the convolutions and the max-pooling. These techniques help us to generalize our problem easier, especially in image processing problems. 

In order to obtain better results, I tried different combinations of some parameters such as the number of neurons per layer, the kernel size in the CNN or the number of convolutions. I also tried to introduce some dropout layers after the max-pooling ones, which are useful to help the network to generalize better.

## Results

Even if the simple neural network gave good results, the CNN was better. With the CNN, the obtained validation accuracy was around 0.991 for the best combinations.

My best result in the test was 0.99057, which gave me the 953rd place in the leaderboard (top 40%). The network generalized very well since the test accuracy is nearly the same that the validation accuracy.

## Sources

For this project, my code was inspired of other projects or articles, which are listed below:

- Thibault Neveu's Github repository, for the general structure: https://github.com/thibo73800/tensorflow2.0-examples
- Yassine Ghouzham's article, for the CNN: https://www.kaggle.com/yassineghouzam/introduction-to-cnn-keras-0-997-top-6
- Siraj Raval's "Kaggle Earthquake Prediction Challenge" Youtube video
