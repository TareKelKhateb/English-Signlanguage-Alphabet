# Real-time American Sign Language (ASL) Alphabet Classifier
### Overview
#### This project is a real-time ASL alphabet classifier that uses a webcam to recognize and classify the 26 letters of the English alphabet. The classifier is built using a pre-trained MobileNet model fine-tuned on a dataset of approximately 86,000 images of hands showing different ASL signs. MediaPipe is used for real-time hand detection and tracking, allowing the model to focus on classifying the hand signs.

## Project Components
### 1. Model Training
#### The MobileNet model was trained using the following steps:

##### 1- Data Preparation: The ASL alphabet dataset, containing 86,000 images, was split into training (85%) and validation (15%) sets using the splitfolders library.
##### 2- Image Augmentation: ImageDataGenerator was used to rescale pixel values and apply horizontal flipping for data augmentation.
##### 3 - Model Architecture: A pre-trained MobileNet model (excluding the top layers) was used as the base model. Additional layers were added for batch normalization, global average pooling, dense layers with ReLU activation, dropout for regularization, and a final dense layer with softmax activation for classification.
##### 4 - Training: The model was trained for 10 epochs with Adam optimizer and categorical_crossentropy loss function.

## 2. Real-time Hand Detection and Classification

#### The real-time application was built using OpenCV and MediaPipe:

##### 1-  Hand Detection: MediaPipe Hands solution was used to detect and track hands in real-time from webcam input.
##### 2-  Bounding Box Extraction: For each detected hand, the bounding box was calculated, and a larger region around the hand was extracted for better classification accuracy.
##### 3 - Image Preprocessing: The extracted hand region was resized to 200x200 pixels and normalized before being fed into the model.
##### 4 -  Prediction: The pre-trained MobileNet model was used to classify the hand sign. The predicted class was displayed on the video feed.

## 3. Real-time Application
#### The real-time ASL alphabet classifier application runs as follows:

##### 1- Initialize Webcam: Capture frames from the webcam.
##### 2- Hand Detection: Use MediaPipe to detect hands in the frame.
##### 3- Extract and Preprocess Hand Region: Extract a larger region around the detected hand and preprocess it.
##### 4- Make Prediction: Use the trained MobileNet model to classify the hand sign.
##### 5- Display Results: Display the bounding box and predicted class on the video feed.

####  data set https://www.kaggle.com/datasets/grassknoted/asl-alphabet

---

 ![Recording 2023-09-04 135857 - Trim](https://github.com/TareKelKhateb/English-Signlanguage-Alphabet/assets/110000941/41791bef-5e07-4aed-bb5e-7a972b65340c)

### Note: I have included a presentation explaining the project


 ![image](https://github.com/TareKelKhateb/English-Signlanguage-Alphabet/assets/110000941/109a8bfa-3072-4d10-bbd0-ca8973ec5b21)


![image](https://github.com/TareKelKhateb/English-Signlanguage-Alphabet/assets/110000941/73560429-3452-4f05-9ab7-a9c9bf66bb98)

