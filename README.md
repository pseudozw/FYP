# FYP
MobileNetV2 SSD on Fabric Defect Detection

Scripts used for FYP. Ran in Kaggle.
*Note that the recent update to Tensorflow 2.16.1 may lead to issues when cloning the tensorflow models repository. Should this error occur, remove the code that clones the tensorflow models repository and replace the `tfr_labels` function with the `tfr_labels` function in focal-mobilenetv2-ssd.ipynb.*

How to run:
1. Clone the repository or download the script
2. Create Roboflow account and get your Roboflow API key
3. Add your API key to the scripts
4. Change the path to the pretrained model

Base: MobileNetV2 SSD trained on Capstone (comparing image resolution)
Backbone: MobileNetV2, DenseNet121, SEResNeXt50, EfficientNetB0
Feature Fusion: Concatenate or Elemental Sum (80+40 or 80+40, 40+20 or 80+40+20 or 80+40+20, 40+20)
Detection: Feature Pyramid, FPN, PAFPN, BiFPN
Transfer Learning: Tilda, Daffodil, Thesis using MobileNetV2 SSD pretrained on Capstone
Best: SE ResNeXt50 BiFPN and MobileNetV2 BiFPN

Datasets: From Roboflow

Credit to the following GitHub repositories:
- https://github.com/FurkanOM/tf-ssd/tree/master
- https://github.com/flash10042/EfficientDet/tree/master
- https://github.com/SunYanCN/TensorFlow/blob/master/TensorFlow-Code-PPT/lesson26-fasterRCNN/detection/models/necks/fpn.py
- https://github.com/TanyaChutani/SSD-Tensorflow2.0/tree/master 