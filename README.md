# Human Detection and Counting System

The Human Detection and Counting System is done through Webcam otherwise we can give our own videos or images as input.

# Why Human Detection and Counting System?

Counting people in visual surveillance is hard and challenging problem. 
Automatic counting surveillance of individuals publicly areas is vital for safety control.
The tough task is that it is not feasible for human operator to sit all the time in front of the CCTV  and monitor/count the crowd. 
There is a need of an automated system which can provide us some meaningful information from  live or recorded videos.
And in such cases Human detection and counting system can be used.


# Installation

TODO: These are the packages needed to be installed before,   
These packages can work on 3.9 version of python   

pip install opencv-python   
pip install imutils.   


# What these Libraries are for:

OpenCV is a field of AI that enables computers  to derive meaningful information from digital images, videos and other visual inputs .
Imutils are a series of convenience functions to make basic image processing functions such as translation, rotation, resizing and displaying images.
Argparse , let the user to provide values for variables at runtime.


# How the process actually is:

In this project HOG Algorithm is used,    
HOG (Histogram of Oriented Gradient Descriptor) is a computer vision and image processing for the purpose of object detection.  
Detect method is used to detect object by using hog descriptor and svm
hog descriptors() : used to detect object .
svm() : used to detect the objects detected by the hog descriptor is actually a human or not.
   
A video combines a sequence of images to form a moving picture. We call these images as Frame. 
Detect() method take a frame to detect a person in it. 
Make a box around a person and show the frame and return the frame with person bounded by a green box.
   
In the DetectByPathVideo() Module,                                                                                               
If path of a Video is given as Input. Firstly,checks if the video on the provided path is found or not.
If input is found,then each frame of the input is successfully read and after the last frame the loop gets terminated.
And the ouput gets displayed on a window with green boxes where human is found.
   
In the DetectbyCamera() Module,   
It enables the webcam to detect Humans in live.To bring this module to action the '-c' is given in Input,then it reads the video frames in live 
and shows it on window,to terminate the webcam 'q' key is pressed.
   
In the DetectbyImage() Module,   
If the input given to the .py file is an 'image path' then the 'detectbyimagepath' module takes given imagepath as its input,
reads the path and after detecting  humans in input , image is returned from 'detectframe' module.Later using cv2.imwrite 
displays/writes the output image to the windowscreen.
   
Argparse method is used to give input in command line,   
Initially there will be no arguments in this method. When we give input in command line, then by using argparse.add_argument 
function it will take arguments as video or image or by camera and then it will parse the argument to human detector method.
   
# Usage   
Input Format is given below:   
Input to the file is given from the terminal of the environment you are using.   
1.If the input wanted to give is an image then:   
   
   python filename.py -i path_to_the_image   
   

2.If the input wanted to give is an video then:   
   
   python filename.py -v path_to_the_video   
   
3.If the input wanted to give through webcam:   
   
   python filename.py -c  true   
