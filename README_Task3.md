# Handwritten Digit Recognition (MNIST + CNN)

CodeAlpha Machine Learning Internship, Task 3.

## Objective
Identify handwritten digits (0 to 9) from images using a Convolutional Neural Network (CNN).

## Dataset
MNIST, loaded through Keras.
* 70,000 grayscale images, each 28 x 28 pixels
* 60,000 for training and 10,000 for testing
* 10 classes (digits 0 to 9)

## Method
1. Loaded the data and viewed sample images.
2. Scaled pixel values from the 0 to 255 range to 0 to 1.
3. Built a CNN with two convolution layers (32 and 64 filters), two max pooling layers, a dropout layer (0.3) and a dense layer with 128 units.
4. Trained for 8 epochs with the Adam optimizer. 10% of the training data was used for validation.
5. Evaluated on the 10,000 test images with Accuracy, Precision, Recall, F1 Score and a Confusion Matrix.
6. Tested the model on my own handwritten digit photo.

## Results

**Test accuracy: 99.1%** (about 90 wrong predictions out of 10,000)

| Digit | Precision | Recall | F1 Score |
|---|---|---|---|
| 0 | 0.9899 | 0.9969 | 0.9934 |
| 1 | 0.9904 | 0.9982 | 0.9943 |
| 2 | 0.9894 | 0.9952 | 0.9923 |
| 3 | 0.9921 | 0.9950 | 0.9936 |
| 4 | 0.9869 | 0.9990 | 0.9929 |
| 5 | 0.9899 | 0.9854 | 0.9876 |
| 6 | 0.9937 | 0.9896 | 0.9916 |
| 7 | 0.9893 | 0.9854 | 0.9873 |
| 8 | 0.9938 | 0.9897 | 0.9918 |
| 9 | 0.9949 | 0.9742 | 0.9845 |

## Observations
* Digits 4 and 1 were recognized best (recall above 99.8%).
* Digit 9 was the weakest (recall 97.42%). Some 9s were mistaken for other digits with similar shapes.
* Digits 5 and 7 also had slightly lower recall (98.54%).

## Limitations
* MNIST digits are clean, centered and size normalized. Photos of real handwriting with bad lighting or messy backgrounds can give lower accuracy.
* The model recognizes one digit per image. It does not read full words or sentences.

## How to run
1. Open the notebook file in Google Colab.
2. Click Runtime, then Run all.
3. In the last section, upload a photo of a single digit written with a dark pen on white paper.

## Tools
Python, TensorFlow/Keras, NumPy, Matplotlib, Scikit-learn
