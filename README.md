# xmobots
this project is part of the xmobots AI and Computer Vision case

![alt text](assets\example.jpg)

The task involves training a machine learning or deep learning model using a labeled dataset, where each image is associated with a class label (tree or no tree). The model learns to extract features from the images and uses them to make predictions on unseen images.

----
## training
For the base model, I used MobileNetV3Small from tensorflow applications, which is a standard model trained on imagenet, and added a standard fully-connected layer at the end. And fine-tuned the model with weighted categorical cross entropy loss and Adam optimizer.

The complete code for training can be found here:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AllanKamimura/xmobots/blob/main/train.ipynb)

----
## inference
Inference for an image binary classification model refers to the process of using the trained model to make predictions on new, unseen images.

The code expects as an input, a path to a folder containing ```.jpg``` or ```.png``` image files and the output is a file in the ```cwd``` with a csv, where the first column is the image name and the second column is the class (tree or no tree) that the image belongs to.

The complete code for inference can be found here:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AllanKamimura/xmobots/blob/main/predict.ipynb)

---
## Report
A detailed report can be found here:
[report.pdf](xmobots%20report.pdf)

----
## Bonus
As a bonus, I also included the saved weights for 2 more models, that use a different approach to the problem, the inference code for those are included in the inference code

Image Segmentation    |  Object Detection
:-------------------------:|:-------------------------:
![alt text](assets\image_segmentation.png) | ![alt text](assets\object%20detection.png)


