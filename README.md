# ObjectDetectionTutorial

Introduction to Object Detection Tutorial using Transfer Learning for UNF Guest Lecture

## Program Dependencies
Microsoft C++ Build Tools - Install Link: https://visualstudio.microsoft.com/visual-cpp-build-tools/ <br>
Git - Install Link: https://git-scm.com/downloads <br>
Anaconda - Install Link: https://www.anaconda.com/ <br>

**Restart OS after Installing Programs Above**

## Anaconda Setup
Open Anaconda Navigator
- Go to Environments -> Create
  - Given Virtual Environment a Name and select create
- Go to Home
  - Select Install on Jupyter Notebook
    - This will be used to run the Notebook files   
  - Select Install on CMD.exe Prompt or 

## 1-Object_Detection_Workspace_Setup
This Notebook will walk you through downloading the libraries needed to run pre-trained and custom object detection models.

### Dependencies
```
pip install --upgrade --user pip <br>
pip install --user wget opencv-python pyyaml protobuf matplotlib
```

## 2-Label_Pictures
This Notebook walks you through downloading a program call LableImg developed by tzutalin GitHub: https://github.com/tzutalin <br>
LabelImg can be used to create the annotation xml files needed to create a custom image dataset for training and testing custom object detection models.

### Dependencies
```
pip install --upgrade pyqt5 lxml 
```

## 3-Train_Custom_Object_Detection_Model
This Notebook walks you through creating a custom object detection model based on a custom image dateset. 

### Dependencies
```
pip install typeguard pytz gin-config tensorflow-addons
```

## 4-Detect_Objects_in_Images
This Notebook gives sample code for using a pre-trained or custom model to automatically label objects for a given directory of images

## 5-Video_to_Pictures
This Notebook walks you through extracted pictures froma specified video

The images from the video can be labeled using LabelImg to create a custom image dataset for training and testing

### Dependencies
```
pip install opencv-python
```

## Resources
This resource was used to create the majority of the code in the Notebooks above. Highly Recommend Watching the Tensorflow Object Detection Walkthrough Video. <br>
Link: https://github.com/nicknochnack/TFODCourse

This resource was used to create the code in the Video_to_Pictures Notebook <br>
Link: https://www.geeksforgeeks.org/extract-images-from-video-in-python/
