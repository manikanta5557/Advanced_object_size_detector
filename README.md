# Handbag_size_detection
For detecting object using computer vision we need to have a reference object,we choose credit card for that.  
Inorder to detect size of an object provided, it should contain credit/debit card place anywhere in image.  
According to PIXEL METRIX RATIO the size of object will be detected.In our case objects are handbags  
# How to use
Add target images in the INPUT_IMAGES folder  
Run the handbag_size_detection and enter the name of image in INPUT_IMAGES that you want to work on  
Enter the name of image with extension  
The output will be displayed in separate window and that output will be saved in Results folder with the name "marked"+image name  

# How it works
We are using YOLO Algorithm to detect object(handbag) and reference (credit card)  
after detecting the credit card the co-ordinates of the reference object and image will go through GRABCUT algorithm  
This will segment the object and remove the background so that we can easily find the contours of the object  
after getting the contours of reference object we can find the height and width of its contours  
Since we already know the size of reference object we can calculate pixel metric ratio from it  
The same process will be done to the target object too  
By the height and width of object's contours and pixel metric ratio height and width of the object will be calculated in centimeters

# Here is a sample output
![alt text](https://github.com/Kashyap2502/Handbag_size_detection/blob/main/Results/output.png?raw=true)
