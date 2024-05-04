# Face Recognition with VGG16

![image](https://github.com/TITHI-KHAN/Face-Recognition-with-VGG16/assets/65033964/eb93c26f-cb66-4b37-93ef-2e910c183214)

## Dataset

Labelled Faces in the Wild (LFW) Dataset - https://www.kaggle.com/datasets/jessicali9530/lfw-dataset

opencv-face-recognizer Dataset - https://www.kaggle.com/datasets/libor8/opencvfacerecognizer

## Code Explanation

1. **Data Preparation**:
   - You create directories to organize the dataset for training and testing.
   - Metadata for training and testing splits is loaded from CSV files.
   - Functions are defined to normalize person names and prepare the dataset by copying images into the appropriate folders.

2. **Model Building**:
   - You utilize the VGG16 architecture pre-trained on ImageNet for feature extraction.
   - New dense layers are added on top of the pre-trained VGG16 model for classification.
   - Data generators are set up for data augmentation during training.

3. **Training**:
   - The model is compiled with the Adam optimizer and categorical cross-entropy loss.
   - Training and validation data are fed into the model using data generators.
   - Model training progresses for a specified number of epochs.

4. **Model Evaluation**:
   - Model performance metrics such as accuracy and loss are visualized using Matplotlib.
   - The trained model is saved for future use.

5. **Face Detection and Recognition**:
   - Face detection is performed on input images using a pre-trained face detection model.
   - Detected faces are cropped and passed through a pre-trained deep learning model to extract facial embeddings.
   - These embeddings are compared with stored embeddings to recognize faces.
   - Recognized faces are annotated with bounding boxes and labels on the input images.

6. **Visualization**:
   - Detected faces with recognition labels and confidence scores are displayed using Matplotlib.

7. **Utility Functions**:
   - Utility functions are provided for face detection, feature extraction, and face recognition.

By combining these steps, you're able to build a face recognition system that can detect and recognize faces in images with reasonable accuracy.
