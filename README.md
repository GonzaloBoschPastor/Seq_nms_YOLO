# Seq_nms_YOLO

#### Membres: Yunyun SUN, Yutong YAN, Sixiang XU, Heng ZHANG, 

---

## Introduction

![](img/index.jpg) 

This project combines **YOLOv2**([reference](https://arxiv.org/abs/1506.02640)) and **seq-nms**([reference](https://arxiv.org/abs/1602.08465)) to realise **real time video detection**.
[Tutorial develop for Ubuntu].

## Steps

1. Open a terminal.
2. Create a virtual environment with python 2.7: 

  * `conda create --name EnvExample python=2.7`.
  * `conda activate EnvExample`.
  
3. Clone the repository:

  * `git clone https://github.com/carlosjimenezmwb/seq_nms_yolo.git`.
  
4. Make the project:
  * `cd seq_nms_yolo`.
  * `make`.

5. Download the yolo.weights and tiny-yolo.weights:
  * `wget https://pjreddie.com/media/files/yolo.weights`.
  * `wget https://pjreddie.com/media/files/yolov2-tiny.weights`.

7.
8.
9.
10.
11.
12.

And you will see detection results in `video/output`

## Reference

This project copies lots of code from [darknet](https://github.com/pjreddie/darknet) , [Seq-NMS](https://github.com/lrghust/Seq-NMS) and  [models](https://github.com/tensorflow/models).
