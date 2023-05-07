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

Check the result in [logo folder](https://github.com/Mark618/HT_Consulting_Interview/tree/main/logo).

![sample 1](https://github.com/Mark618/HT_Consulting_Interview/blob/b84bb4b7031b7773d9c3c26a52ac88b41188207a/logo/sample_1.jpg)

logo.ipynb are also solution refer to the first question. Trying to use Yolov5 transfer learning to detect logo.

Steps:
1. Data preparation by collecting logo image from internet and label image using label studio. Data augmentation using Roboflow to generate new training data.
2. Download Yolov5s and set up the training image and validation image folder path in .yaml file.
3. Freeze 10 layer and train the model
4. Validate model

Model can be improve by increasing training data and increase trainable parameter.

![Yolo_result 1](https://github.com/Mark618/HT_Consulting_Interview/blob/77d9eb4879f5fd9c572890cb21de08cfd2737aba/logo/output.jpeg)

sentiment.ipynb and text.ipynb for the second question.

In sentiment.ipynb contain steps on loading data sets,data exploration and also sentiment analysis using pre-trained model Vadersentiment-multi.

Vadersentiment-multi using google translate api to translate tweets to english and provides sentiment scores. Results are saved in sentiment_sample.csv.

text.ipynb is working with tweets that have been clean out using tweet-preprocessor. It does not contain urls,mention and emoji. The purpose of this is to show the difference result of word cloud between tweets that contain urls,mention and emoji and tweets without these.

| With Preprocess  | Without Preprocess |
| ------------- | ------------- |
| ![With Preprocess 1](https://github.com/Mark618/HT_Consulting_Interview/blob/af9252a98bf0e416759dcb61a0a76165d807e5d9/image/pre.png)  | ![With Preprocess 1](https://github.com/Mark618/HT_Consulting_Interview/blob/af9252a98bf0e416759dcb61a0a76165d807e5d9/image/without.png)  |
