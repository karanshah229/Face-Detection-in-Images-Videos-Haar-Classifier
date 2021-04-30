# Face Detection in Images and Videos using OpenCV

Face Detection in Image and Videos using OpenCV - Haar Cascade Classifier

Draws a box around the face it recognizes. Using Haar Cascade and not deep learning  

Haar Cascade was the original algorithm to perform face detection long before Deep Learning came along  

Deep Learning using Features - small features, groups them together and combines them and builds on this to decide if something is a face  
Haar Cascade using Filters and Edge Detection to classify if something is a face

### How Haar Cascade works: 
0. Haar Cascade is a pre-trained model with its features selected
1. Read image as pixel values
2. Calculate Prefix Matrix / Integral Matrix
3. Down sample the image to 24 x 24 pixels and work on this
4. Calculate Haar Classifier features difference   
![alt text](https://github.com/karanshah229/Face-Detection-in-Images-Videos-Haar-Classifier/blob/main/images/haar_features.PNG "Haar Features")
5. For a simple 24 x 24 pixel image there could be 160000+ features.
6. But Haar Cascade has a way to removing the false images first and only after passing all the features test the final image is classified as a face
7. So, it is easier to discard an image as not a face than assert that it is a face  
![alt text](https://github.com/karanshah229/Face-Detection-in-Images-Videos-Haar-Classifier/blob/main/images/haar_feature_matching.png "Haar Feature Matching")
   
### Observations

* As you can see from the samples below, Haar Classifier can easily mis-classify something as well.  
* But when computation is costly, and we need a quick and fairly accurate method, Haar Cascade Classifier is the way to go

### Video:
* Performing this is a video is the same as videos, and a collection of frames  
* I have used the webcam in this project to supply the video with an option to locally supply the video as well  
* For a large duration Haar Cascade classifier were the way to go in Face Detection and Object Detection

Packages List:  
OpenCV
> python -m pip install opencv-python  

or  

> python3 -m pip install opencv-python 

Also, download the Haar Cascade Classifier .xml file (File in repo)

### Sample Images

![alt text](https://github.com/karanshah229/Face-Detection-in-Images-Videos-Haar-Classifier/blob/main/images/sample_image_webcam_1.PNG "WebCam")  

![alt text](https://github.com/karanshah229/Face-Detection-in-Images-Videos-Haar-Classifier/blob/main/images/sample_image_1.PNG "Image File")  

![alt text](https://github.com/karanshah229/Face-Detection-in-Images-Videos-Haar-Classifier/blob/main/images/sample_image_2.PNG "Image File")  
  
  
###### If you find a bug or want to suggest some improvements
Take a pull request or email:
> karanshah229@gmail.com