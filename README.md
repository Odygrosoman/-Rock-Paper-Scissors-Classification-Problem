# Rock-Paper-Scissor game -  Classification-Problem
This Python project implements a Rock-Paper-Scissors game using machine learning for image classification. The game takes input images of rock, paper, or scissors, and uses a trained model to classify the input, enabling the computer to make strategic choices against the opponent. For machine learning model training used Rock-Paper-Scissors Images (https://www.kaggle.com/datasets/drgfreeman/rockpaperscissors).

<p align="center">
  <img src="https://miro.medium.com/v2/resize:fit:931/1*HA5CCzjaGqLpScvNznqDww.png" alt="Your Image Alt Text" />
</p>


To solve the classification problem, I first trained Random Forest, K-Nearest Neighbors (KNN), Support Vector Classifier (SVC), and XGBoost separately to assess their individual accuracies. Subsequently, I employed the voting method from the scikit-learn library to combine their predictions and determine if an ensemble approach could yield improved accuracy. Finally, recognizing the suitability of Convolutional Neural Networks (CNN) for image classification tasks, I trained a CNN.

The accuracies of each model are shown in the table below.
| Model | Accuracy |
|----------|----------|
| Random Forest | 96,34% |
| SVC | 96,8% |
| KNN | 94,29% |
| Hard Vote (RF,SVC,KNN) | 97,48% |
| CNN | 99,31% |

For solving classification problem i choose the CNN model.

# **Description of a Game**

My agent will bet €1 against a 'Random Agent' for a total of N rounds. If your my wins, it receives €2, in case of a tie it gets €1 back, otherwise, it loses €1. The Random Agent always plays as the first player, selecting a random image from a pool of 2100 images, which could be either rock, paper, or scissors. The Random Agent have,  may apply a vertical flip with a probability of p1 = 0.5. Additionally, it may apply a horizontal flip with a probability of p. Finally, the Random Agent applies random noise (white noise) to each pixel of the image with a mean value of 0 and a standard deviation of 5% of the maximum pixel value.

My agent and the opponent's agent played 500 games. Their beginning budget was 1000€ each. After the completion of the game, the remaining money of the two players were shaped as follows:

![αρχείο λήψης](https://github.com/Odygrosoman/-Rock-Paper-Scissors-Classification-Problem/assets/118894987/6832b150-a10a-4b2c-8e1a-1a418d07ddb9)

As you can see, my agent has achieved to win  the opponent agent. The accuracy of images prediction was 85,8%.

Subsequently i tryed to test my agent in a harder dataset. I use the images of the dataset: https://www.kaggle.com/datasets/glushko/rock-paper-scissors-dataset

<p align="center">
  <img src="https://www.romaglushko.com/blog/rock-paper-scissors/rock-paper-scissors-cover.jpeg" alt="Your Image Alt Text" />
</p>

With this dataset the prediction accuracy was 29,8% and the opponent agent has achieved to win my agent. 

![αρχείο λήψης (2)](https://github.com/Odygrosoman/-Rock-Paper-Scissors-Classification-Problem/assets/118894987/4b1aba1f-3ebd-411c-b759-dc423610f38a)


