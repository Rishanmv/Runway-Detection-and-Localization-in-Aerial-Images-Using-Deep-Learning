# Runway-Detection-and-Localization-in-Aerial-Images-Using-Deep-Learning

# Objective

To build a vision based system using deep learning and image processing techniques to detect runway and localize the runway. Vision based systems provides low cost solution to detect landing sites by providing rich textual information. So we are trying implement a low cost runway localization system which use only use camera as extra hardware to detect runway.

# GUI

*GUI will be created using tkinter
*GUI will contain a window with a button to choose image file
*If runway detected then localized image will be displayed.


# System Model

1)Creating runway detection model

*All the aerial images (45 classes) from dataset are loaded and given corresponding labels
*All images are resized to specific size
*Image augmentation techniques are applied by choosing random images from dataset to increase efficiency of runway detection in bad weather. Rotation, translation,random noise insertion, brightness adjustment are applied.
*Prepare resnet50 architecture by changing last dense layer to 45 outputs
*Load pretrained weights for resnet50
*Fine tune resnet50 with aerial images (training)
*Save model

2)Creating Runway localization model

*Load all images of runway from dataset
*Annotate runway in all images using labelme package of python
*Output will be json documents with runway annotation for each image
*Load MRCNN model
*Train MRCNN model using image and corresponding json files
*Save MRCNN model

3)Runway detection

*Load image
*Resize image
*Load trained runway detection model
*Use runway detection model to detect runway in the image

4)Runway localization

*Load image
*Resize image
*Load runway localization model
*Use runway localization model to localize runway in image
*Use Hough transform technique to detect lines in runway image
*Merge images to get more accurate runway image
  

# Note : Accuracy of deep learning algorithm depends on quality of data used. Training will be performed using google colab.


# Hardware Specification
*	Processor: i5 or i7
*	RAM: 8GB (Minimum)
*	Hard Disk: 500GB or above
*	Mouse
*	Keyboard

# Software Specification
*	Tool: Python IDLE
*	Python: version3
*	Operating System: Windows 10
*	Front End: Python Tkinter




## Link for the code ; ##

## ml_env.rar ##
https://drive.google.com/file/d/1_Flba2YB7I55BvkweZG9c3_rhG4pTjJN/view?usp=drive_link

## NWPU-RESISC45 (DATA SET) ##
https://drive.google.com/file/d/1TyB63irWgqPXSu8QBubA-koJwCTutGAe/view?usp=sharing

## Runway_detection ##
https://drive.google.com/file/d/1QjFx2N8dz8-nbM3RqP5zbOPuHYklZ0P4/view?usp=sharing
