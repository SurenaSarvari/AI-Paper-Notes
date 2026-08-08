# ImageNet Classification with Deep Convolutional  Neural Networks

Paper : https://papers.nips.cc/paper_files/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf

year : 2012

Authors : Alex Krizhevsky, Ilya Sutskever, Geoffrey E. Hinton

-----------------------------------------------

## TL;DR
Using a large and deep CNN for object recognition task instead of using traditional computer vision techniques or shallow machine learning models (like SVMs). training on two GPUs and using augmentation, dropout to prevent overfitting
and ReLU to prevent gradient vanishing.

## Why this paper?
1. Hand crafted features vs. Learned features : Other algorithms like HOG or SIFT relied on handcrafted features that researchers define them mathematically like specific edges
   or corners. But the real world images were too messy and highly variable So the model would underfit somehow.But in the AlexNet it gets the raw image and extract features
   using convolutional layers.

2. Vanishing gradient : AlexNet use ReLU as a non-saturating activation function instead of using tan-h; so the it allows gradient to flow for through deep, 8 layers network without vanishing. And it leads to way faster training than using tan-h. When we train the model on a big dataset , training speed is crucial. 

3. The computation and data bottleneck : Using small datasets cause overfitting in model. Beside that using CPU for training is so slow for a large dataset and big model.So
   AlexNet use ImageNet as the training dataset with 1.2 million images to train the the model with 60 million parameters. And because of these, we need to train model on two
   gpus with well optimized code

## Note 
- CNNs already existed.
- ReLU had been proposed before.
- Dropout had been introduced before.
- GPU computing for neural networks was already being explored.

### What did AlexNet change?
- Demonstrated that this ideas could combine into large and powerful CNN that could be trained on ImageNet.
- Using deep CNN as the dominant approach of computer vision.
- Demonstrated the importance of GPU in DL.
- Invented a specific mathematical formula for normalization across channels. This was created specifically to control the unbounded, high-value outputs of the newly adopted ReLU activations.
  
