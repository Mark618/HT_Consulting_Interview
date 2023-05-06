# HT_Consulting_Interview
## Solution for  take-home AI task
only_opencv.ipynb contain steps for the first question. This solution will be only using openCV to detect Rototype Logo.
Steps:
1. Import library
2. Read image
3. Resize Image
4. Convert Image from RGB to GrayScale image
5. Blur Image with (7*7) window
6. Binarize Image and using OTSU to determined the threshold value
7. Invert Image
8. Replace Image border with black pixel
9. Find Contour
10. Filter bounding rectangle
11. Retrieve result

![sample 1](https://github.com/Mark618/HT_Consulting_Interview/blob/b84bb4b7031b7773d9c3c26a52ac88b41188207a/logo/sample_1.jpg)

logo.ipynb are also solution refer to the first question. Trying to use Yolov5 transfer learning to detect logo.

Steps:
1. Data preparation by collecting logo image from internet and label image using label studio. Data augmentation using Roboflow to generate new training data.
2. Download Yolov5s and set up the training image and validation image folder path in .yaml file.
3. Freeze 10 layer and train the model
4. Validate model

![Yolo_result 1](https://github.com/Mark618/HT_Consulting_Interview/blob/77d9eb4879f5fd9c572890cb21de08cfd2737aba/logo/output.jpeg)
