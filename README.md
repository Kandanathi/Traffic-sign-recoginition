# Traffic-sign-recoginition

A new version using SSD will be released this summer for anyone need higher accuracy detection method. Stay tuned for new update!
1. Description
This project is a traffic signs detection and classification system on videos using OpenCV. The detection phase uses Image Processing techniques that create contours on each video frame and find all ellipses or circles among those contours. They are marked as candidates for traffic signs.

Detection strategy:

Increase the contrast and dynamic range of the video frame
Remove unnecessary colors like green with HSV Color range
Use Laplacian of Gaussian to display border of objects
Make contours by Binarization.
Detect ellipse-like and circle-like contours
In the next phase - classification phase, a list of images are created by cropping from the original frame based on candidates' coordinate. A pre-trained SVM model will classify these images to find out which type of traffic sign they are.

Currently supported traffic signs (The name of each sign's file is corresponding to their class in SVM):  Note:

All signs which belong to class 8 and above are marked as OTHERS because a competition requires this. There is also a class 0 which are marked as non-traffic-sign
Only the biggest sign in the current frame is cropped and classified
![image](https://github.com/user-attachments/assets/80b3e4db-c79e-4ddf-897a-e1301801b245)
