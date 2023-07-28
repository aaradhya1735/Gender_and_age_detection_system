Images for testing are given above
Google Collab Link: https://colab.research.google.com/drive/1gYG5oL1Uwhvs6zktmZvA46IB1SLUi0EK?usp=sharing

# Gender_and_age_detection_system

This code appears to be an implementation of an age and gender detection model using pre-trained deep learning models. The code performs the following tasks:

1. Cloning the GitHub repository:
   - It clones the GitHub repository named "age_and_gender_detection" using the Git command `!git clone`.

2. Navigating to the cloned repository:
   - The code changes the current directory to the "age_and_gender_detection" folder using `%cd age_and_gender_detection`.

3. Downloading and unzipping pretrained data:
   - It downloads a pre-trained model and weight files from Google Drive using the command `!gdown`.
   - Then it unzips the downloaded "modelNweight.zip" file using `!unzip`.

4. Importing required modules:
   - The code imports various modules needed for image processing and deep learning, such as `cv2` (OpenCV), `math`, `time`, and `cv2_imshow` (for displaying images in Google Colab).

5. Defining the function `getFaceBox`:
   - This function takes a deep learning network, an input frame (image), and a confidence threshold as input.
   - It processes the input frame and detects faces using the provided deep learning network.
   - It returns the modified frame with bounding boxes drawn around the detected faces and a list of bounding box coordinates.

6. Defining the model paths and other constants:
   - The code sets the paths for the pre-trained models for face detection, age estimation, and gender prediction.
   - It also defines model-specific constants such as `MODEL_MEAN_VALUES`, `ageList`, and `genderList`.

7. Loading the pre-trained models:
   - The code loads the pre-trained age estimation, gender prediction, and face detection models using `cv2.dnn.readNet`.

8. Defining the `age_gender_detector` function:
   - This function takes an input frame (image) and performs the following steps:
      - Uses the `getFaceBox` function to get bounding boxes around the detected faces in the input frame.
      - For each detected face:
         - Extracts the face region from the frame.
         - Processes the face image and predicts the gender and age using the pre-trained models.
         - Draws the predicted gender and age as labels on the frame.
   - The function returns the modified frame with labels.

9. Reading an input image and applying age and gender detection:
   - The code reads an image named "image.jpg" using `cv2.imread`.
   - It calls the `age_gender_detector` function to process the input image and obtain the output frame.
   - Finally, it displays the output frame using `cv2_imshow` for visualization.

Note: The provided code is specifically designed to work within a Google Colab environment. To run this code outside Colab, you may need to make some modifications, especially related to paths and image reading/displaying functions.
