# smartMethods2ndWeek2ndTask
Object detection for face and eyes using OpenCV library. 
A python code that uses Haar Feature-based Cascade Classifiers, in OpenCV library.
Line no. 4 and 5: The code uses a cascade classifier that return an xml file containing the trained dataset for the objects it's detecting (in our case a face and eyes). 
Line no. 11: First it converts each image in the stream from BGR color formal to gray format using cvtColor().
Line no. 14: The face cascade detects objects of different sizes in the input image using detectMultiScale(), the detected objects are returned as a list of rectangles, using the gray format of the image as input. (other parameters include: scaleFactor: Parameter specifying how much the image size is reduced at each image scale. minNeighbors: Parameter specifying how many neighbors each candidate rectangle should have to retain it.)
Line no. 16: A rectangle is drawn around the face that's detected. 
Line no. 17 and 19: The region of interest (that's the face) is saved in a 2D array.
Line no. 23: Within the face region, the eyes cascade detects objects of different sizes in the input image using detectMultiScale(), the detected objects are returned as a list of rectangles using the 2D array of region of interest (the face) as input. (other parameters include: scaleFactor: Parameter specifying how much the image size is reduced at each image scale.
minNeighbors: Parameter specifying how many neighbors each candidate rectangle should have to retain it)
Line no. 25: A rectangle is drawn around the eyes that are detected.
After running the code. You can quit the video by pressing q.
