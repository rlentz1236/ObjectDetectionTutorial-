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
  - Give Virtual Environment a Name and select create
- Go to Home
  - Select Install on Jupyter Notebook
    - This will be used to run the Notebook files   
  - Select Install on CMD.exe Prompt or 
    - This will be used to pip install libraries and run model training/evaluation

## 1-Object_Detection_Workspace_Setup
This Notebook will walk you through downloading the libraries needed to run pre-trained and custom object detection models. 

### Pre-Trained Models
The link below is to the Tensorflow 2 Detection Model Zoo. 

Link: https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md 

To copy a new model link go to the page above and right click any of the model names in the table, then select copy link address.

### Project Directory
The variable PROJECT_NAME under section 2 sets the Project/Workspace path. Make sure to set it to the desired diretory before executing the code in the Notebook.

### Install Errors
- If given a Module not found error search python install Missing_Module_Name
  - After finding the apporaite install name use pip to install the library into the virtual environment 

### Dependencies
```
pip install --upgrade --user pip <br>
pip install --user wget opencv-python pyyaml protobuf matplotlib
```

## 2-Label_Pictures
This Notebook walks you through downloading a program call LableImg developed by tzutalin GitHub: https://github.com/tzutalin <br>
LabelImg can be used to create the annotation xml files needed to create a custom image dataset for training and testing custom object detection models.

When labeling images make sure you set the label name as the name you want your model to label them as. The label names created at this step will be the labels used for any model trained on the datset.

When drawing the annotation boxes keep them as tight as possible removing as much of the image that is not part of the object without removing any of the object

The annotation xml files must match the name of the image they are created for otherwise an error will occur during training. 

When creating a training dataset you want to have at least 20 different pictures of each object you are trying to detect.

### Dependencies
```
pip install --upgrade pyqt5 lxml 
```

## 3-Train_Custom_Object_Detection_Model
This Notebook walks you through creating a custom object detection model based on a custom image dateset using transfer learning. 

### Dependencies
```
pip install typeguard pytz gin-config tensorflow-addons
```

## 4-Detect_Objects_in_Images
This Notebook gives sample code for using a pre-trained or custom model to automatically label objects for a given directory of images

To run this code you will need to create your own object detection image dataset. The dataset will need to be split into training and testing sets with the training set containing 80% of the image dataset and the testing set containing the other 20%. Having more training data is more important than the testing data. 

### Pre-Trained Models
The link below is to the Tensorflow 2 Detection Model Zoo. If you train your model and do not get the results you want then you can try a different pre-trained model  however, I would recommend looking at the training dataset to make sure you have enough samples for each object. Sometimes you may need more than 20 and the samples need to be diverse for the model to detect objects in new unknown images. 

Link: https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md 

To copy a new model link go to the page above and right click any of the model names in the table, then select copy link address.


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
