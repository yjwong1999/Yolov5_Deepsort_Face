# Yolov5_DeepSort_Face


### Features
Yolov5 Object Detection with DeepSORT Tracking, using OpenSphere Face Recognition Module


### Steps to run Code

- Create a conda environment, and activate it
```
conda create --name pipeline python=3.8.10
conda activate pipeline
```


- Clone the repository
```
git clone https://github.com/yjwong1999/Yolov5_DeepSort_Face.git
```

- Goto cloned folder
```
cd Yolov5_DeepSort_Face/Yolov5_DeepSort_Face
cd yolov5
```

- Install the yolov5 package
```
pip install -r requirements.txt
```

- Back to pipeline directory.
```
cd ../
```

- Do Tracking with mentioned command below
```
# video file
python3 track.py --source dataset_cam1.mp4 --yolo_model best.pt --img 640 --save-vid --show-vid
```

## Acknowledgement
Many thanks to our funder Greatech Integration (M) Sdn Bhd for sponsoring this project

### Reference Code
1. [Yolov5 + DeepSort for Object Detection and Tracking](https://github.com/nicedaddy/Yolov5_DeepSort_Pytorch) </br>
2. [Yolov8 + DeepSort for Object Detection and Tracking](https://github.com/mikel-brostrom/yolov8_tracking) </br>
3. [OpenSphere Face Recognition](https://github.com/ydwen/opensphere) </br>

- Technically, I used Reference [1] for detection & tracking, where Reference [2] is forked from a past version of Reference [2] </br>
- Reference [1] and [2] assign ID based on tracks (which means each tracking has an ID, disregarding the object identity itself) </br>
- Thus, [3] is used to learn the face identity, which is assigned as the ID for the tracking ID
