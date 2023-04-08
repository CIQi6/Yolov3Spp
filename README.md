# YOLOv3SPP

## Projects

[ultralytics/yolov3](https://github.com/ultralytics/yolov3)

## Requirements

PyTorch 1.11.0

Python 3.8(ubuntu20.04)

Cuda 11.3

requirements.txt

## 数据集Pascal VOC2012 

Pascal VOC2012：http://host.robots.ox.ac.uk/pascal/VOC/voc2012/VOCtrainval_11-May-2012.tar

## Object class

aeroplane
bicycle
bird
boat
bottle
bus
car
cat
chair
cow
diningtable
dog
horse
motorbike
person
pottedplant
sheep
sofa
train
tvmonitor

## Pre-Processing

- Mosaic：随机拼接，随机旋转，缩放
- augment_hsv

## train()
第一次训练采用warmup热身训练加速.

进行30个epochs,batch_size=4。

使用multi-scale，每64张图片随机修改一次输入图片大小。

使用随机梯度下降。

## 关于使用

predict_test.py是一个简单的预测脚本,可以用来测试。

weights

`results20230406-214117.txt` :记录每个epoch的12个指标和总损失、lr

Average Precision (AP) @[IoU =0.50:0.95] | area = all | maxDets=100]  
Average Precision (AP) @[IoU =0.50] | area = all | maxDets=100]  
Average Precision (AP) @[IoU =0.75] | area = all | maxDets=100]  
Average Precision (AP) @[IoU =0.50:0.95] | area = smalll | maxDets=100]  
Average Precision (AP) @[IoU =0.50:0.95] | area = medium | maxDets=100]  
Average Precision (AP) @[IoU =0.50:0.95] | area = large | maxDets=100]  
Average Recall (AR) @[IoU =0.50:0.95] | area = all | maxDets=1]  
Average Recall (AR) @[IoU =0.50:0.95] | area = all | maxDets=10]  
Average Recall (AR) @[IoU =0.50:0.95] | area = all | maxDets=100]  
Average Recall (AR) @[IoU =0.50:0.95] | area = small | maxDets=100]  
Average Recall (AR) @[IoU =0.50:0.95] | area = medium | maxDets=100]  
Average Recall (AR) @[IoU =0.50:0.95] | area =large | maxDets=100]  





![](test_result.jpg)
![](learning_rate.png)
![](loss&obj_loss.png)
![](mAP1.png)
![](cls_loss&giou_loss.png)

