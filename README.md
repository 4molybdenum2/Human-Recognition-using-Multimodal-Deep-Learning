# Human-Verification-using-Multimodal-Deep-Learning


![version](https://img.shields.io/badge/tensorflow-v2.4.1-gold.svg)
![version](https://img.shields.io/badge/numpy-v1.19.5-blue.svg)
![version](https://img.shields.io/badge/Keras-v2.4.3-green.svg)
![version](https://img.shields.io/badge/opencv-v4.1.2.30-red.svg)
![version](https://img.shields.io/badge/scikitlearn-v0.22.2-purple.svg)

This project explores the use of an aggregate network to verify the identity of a person using his facial and speech data.
The conventional method of deep learning is used to process huge amounts of a certain type of data to do a certain job. 
But us humans don't process data in a similar fashion. We use both audio and visual cues to understand data. 
The objective of this project is to explore how deep learning models can perceive data in a similar way. 

We thus applied this concept to make a Multimodal Network that helps us verify the identity of a person. The idea is to make a neural 
network that can incorporate multimodalities and train with less amounts of data.

***
## Siamese Network

Our deep learning model uses a siamese network to perform a one-shot learning task from the aggregated features of both the individual face and audio networks. Using a metric space method we have trained the model to identify if two given data points belong to the same class or not.

<p align='center'>
    <img src="./images/image1.png" alt="Sample" style="text-align:center; width: 600px;"/>
</p>

***
## Pipeline

1. Audio clips are converted into MEL spectrograms using matplotlib.
2. Preprocessing images and audio spectrograms into data pairs to feed into the fused neural network.
3. Forming train-test splits using sklearn
4. Model contains VGG16 as the base model for image recognition and multiple Conv2D layers in the audio and fused model with last dense layer as a sigmoid layer.
5. Training the model.

***
## Models

+ Base model: [VGG16](https://arxiv.org/abs/1409.1556)

***
## Datasets

+ [VoxCeleb1 Test](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/vox1.html)

***

## Results

| Model | Training Accuracy | Validation Accuracy |
| ------ | ---------------- | ------------------- |
| Image Classification | 80% | 77% |
| Audio Classification | 80% | 73% |
| Multimodal Classification | 89.13% | 88.81% |


<br><br>

Mutlimodal Verification Results:
<p align='center'>
<img src="./images/final_loss.png" alt="Sample" style="text-align:center; width: 400px;">
<img src="./images/final_accuracy.png" alt="Sample" style="text-align:center; width: 400px;">
</p>
<p align='center'>
<img src="./images/final_precision.png" alt="Sample" style="text-align:center; width: 400px;">
</p>

```Multimodal Precision: Training - 85.44%  Validation - 85.38% 
```

<p align='center'>
<img src="./images/final_recall.png" alt="Sample" style="text-align:center; width: 400px;">
</p>

```Multimodal Recall: Training - 94.56%  Validation - 93.11% 
```

***

## Setup

All of our training has been done on Colab Notebooks. So it is recommended to do so. 

For setup on PC conda environment is recommended:
```
git clone https://github.com/4molybdenum2/Human-Verification-using-Multimodal-Deep-Learning.git
cd Human-Verification-using-Multimodal-Deep-Learning
conda env create -f environment.yml
conda activate {environment name}
```
***
## Contributors


@4molybdenum2 [@harshoo3](https://github.com/harshoo3) [@ashutoshparmarap](https://github.com/ashutoshparmarap) <br>
Thanks to: [@Juhi-Purswani](https://github.com/Juhi-Purswani) for all the support!
