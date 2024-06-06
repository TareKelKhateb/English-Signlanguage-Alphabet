# Real-time American Sign Language (ASL) Alphabet Classifier

## Overview
Welcome to the Real-time ASL Alphabet Classifier project! This innovative application utilizes cutting-edge technology to recognize and classify the 26 letters of the English alphabet in real-time using American Sign Language (ASL) gestures. Let's delve into its components and functionalities.

## Project Components

### 1. Model Training
- **Data Preparation**: An extensive ASL alphabet dataset comprising approximately 86,000 images was meticulously curated and split into training (85%) and validation (15%) sets for robust model training.
- **Image Augmentation**: To enhance the model's robustness, ImageDataGenerator was employed to rescale pixel values and introduce horizontal flipping, augmenting the dataset's diversity.
- **Model Architecture**: Leveraging a pre-trained MobileNet model as the foundation, additional layers were seamlessly integrated, including batch normalization, global average pooling, dense layers with ReLU activation, dropout for regularization, and a final dense layer with softmax activation for precise classification.
- **Training**: The meticulously crafted model underwent rigorous training for 10 epochs, harnessing the power of Adam optimizer and categorical_crossentropy loss function to optimize performance.

### 2. Real-time Hand Detection and Classification
- **Hand Detection**: Leveraging the robust MediaPipe Hands solution, the application adeptly detects and tracks hands in real-time from webcam input, laying the groundwork for accurate classification.
- **Bounding Box Extraction**: Each detected hand is meticulously enclosed within a bounding box, facilitating precise classification.
- **Image Preprocessing**: The extracted hand region undergoes meticulous resizing to 200x200 pixels and normalization, preparing it optimally for classification.
- **Prediction**: Harnessing the prowess of the pre-trained MobileNet model, the application seamlessly classifies the hand sign with remarkable accuracy.
  
### 3. Real-time Application
- **Initialization**: The application promptly initializes the webcam to capture frames, laying the foundation for real-time interaction.
- **Hand Detection**: Employing MediaPipe, hands are swiftly detected within each frame, setting the stage for classification.
- **Extraction and Preprocessing**: The application diligently extracts a larger region surrounding the detected hand, preprocesses it meticulously, and prepares it for classification.
- **Prediction and Display**: Leveraging the trained MobileNet model, the application accurately predicts the hand sign and showcases the bounding box and predicted class seamlessly on the video feed, ensuring an immersive user experience.

## Get Started
1. **Clone the Repository**: Begin by cloning the repository containing the project files.
2. **Install Dependencies**: Ensure all necessary dependencies, including OpenCV and MediaPipe, are installed to facilitate seamless execution.
3. **Run the Application**: Execute the application script to launch the real-time ASL alphabet classifier and witness its remarkable functionality firsthand!

####  data set https://www.kaggle.com/datasets/grassknoted/asl-alphabet

---

 ![Recording 2023-09-04 135857 - Trim](https://github.com/TareKelKhateb/English-Signlanguage-Alphabet/assets/110000941/41791bef-5e07-4aed-bb5e-7a972b65340c)

### Note: I have included a presentation explaining the project


 ![image](https://github.com/TareKelKhateb/English-Signlanguage-Alphabet/assets/110000941/109a8bfa-3072-4d10-bbd0-ca8973ec5b21)


![image](https://github.com/TareKelKhateb/English-Signlanguage-Alphabet/assets/110000941/73560429-3452-4f05-9ab7-a9c9bf66bb98)

