# webcam_point_features

Detection of ORB features from online webcam imges.

Class that implements a descriptor for key points. It uses an algorithm for Detecion key points and select the features.

The mask has been applied in a quarter of the total image, in the upper corner, it is a parameter that can be changed easily.

OpenCv lets create a ROI, Region of Interest inside the original image to make the differents experiments.

-----------------------------------------
Find ORB point fetaures and descriptors

// OpenCV Image Objects and ROI

cv::Mat camSubimage;
cv::Rect roi;

//clear previous points
point_set.clear(); 
        
//detect and compute(extract) features
orb_detector->detectAndCompute(camSubimage, cv::noArray(), point_set, descriptor_set);
        
//draw points on the image
cv::drawKeypoints(camSubimage, point_set, camSubimage, 255, cv::DrawMatchesFlags::DEFAULT ); 
-----------------------------------------


For more information:

http://docs.opencv.org/2.4/modules/features2d/doc/feature_detection_and_description.html
