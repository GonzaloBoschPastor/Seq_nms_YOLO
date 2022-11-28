# Seq_nms_YOLO

#### Membres: Yunyun SUN, Yutong YAN, Sixiang XU, Heng ZHANG, 

---

## Introduction

![](img/index.jpg) 

This project combines **YOLOv2**([reference](https://arxiv.org/abs/1506.02640)) and **seq-nms**([reference](https://arxiv.org/abs/1602.08465)) to realise **real time video detection**.
[Tutorial develop for Ubuntu]. 

`The lines attached under this colour in this repository are for running under the Ubuntu terminal.`

## Steps

1. Open a terminal.
2. Create a virtual environment with python 2.7: 

   * `conda create --name EnvExample python=2.7`.
   * `conda activate EnvExample`.
  
3. Clone the github repository in the folder you would like to have the project:

    * `git clone https://github.com/carlosjimenezmwb/seq_nms_yolo.git`.
  
4. Go inside the project:
    * `cd seq_nms_yolo`.
  
5. Make the proyect using the command:
    * `make`.

6. Download the yolo.weights and tiny-yolo.weights:
    * `wget https://pjreddie.com/media/files/yolo.weights`.
    * `wget https://pjreddie.com/media/files/yolov2-tiny.weights`.
  
7. You must have the following libraries installed (with indicated versions)
  * cv2 `pip install opencv-python==4.2.0.32`.
  * matplotlib `pip install matplotlib`.
  * scipy `pip install scipy`.
  * pillow `conda install -c anaconda pillow`.
  * tensorflow `conda install tensorflow=1.15`.
  * tf_object_detection `conda install -c conda-forge tf_object_detection`.
  
8. Copy a video file that you want to use to the video (/seq_nms_yolo/video) folder, for example, 'input.mp4';

9. Go to the directory /seq_nms_yolo/video and run video2img.py and get_pkllist.py:
  * `python video2img.py -i input.mp4`.
  * `python get_pkllist.py`.
  
10. Export the paths:
  * `export PATH=/usr/local/cuda-10.1/bin${PATH:+:${PATH}}`.
  * `export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda-10.1/lib64s`.
  * `export LIBRARY_PATH=$LIBRARY_PATH:/usr/local/cuda-10.1/lib64`.

11.Return to root folder and run yolo_seqnms.py to generate output images in video/output:
  * `python yolo_seqnms.py`.
  
12. If you want to reconstruct a video from these output images, you can go to the video folder and run img2video.py:
  * `python img2video.py -i output`.

And you will see detection results in `video/output`

## Reference

This project copies lots of code from [darknet](https://github.com/pjreddie/darknet) , [Seq-NMS](https://github.com/lrghust/Seq-NMS) and  [models](https://github.com/tensorflow/models).
