# CAPTCHA Reader

This project is designed to read and interpret CAPTCHA images using computer vision and machine learning techniques. The script takes CAPTCHA images as input, preprocesses them, and trains a Convolutional Neural Network (CNN) model to recognize individual characters. The trained model is then used to predict characters from new CAPTCHA images.

## How It Works

1. **Data Collection:** CAPTCHA images are collected from the 'dataset' folder, where each image contains multiple characters.

2. **Preprocessing:**
   - Images are converted to grayscale.
   - Adaptive thresholding is applied to enhance character visibility.
   - Morphological operations like closing and dilation are performed to improve character structure.
   - Gaussian blur is applied to reduce noise.

3. **Data Labeling:**
   - Images are divided into segments, each containing a single character.
   - Labels are extracted from the image names.

4. **Model Training:**
   - A CNN model is constructed using Keras with Conv2D, MaxPooling2D, Flatten, Dropout, and Dense layers.
   - The model is trained on the preprocessed images.

5. **Prediction:**
   - The trained model is utilized to predict characters from new CAPTCHA images.
   - Predicted characters are mapped back to their original labels using encoding information.

## Dependencies
- Python 3.7+
- OpenCV
- NumPy
- Pandas
- Matplotlib
- TensorFlow (Keras)

## Usage
1. Place your CAPTCHA images in the 'dataset' folder.
2. Run the script to train the model.
3. Provide new CAPTCHA images for prediction using the `pred` function.

Feel free to adapt and extend the script to handle different CAPTCHA styles or contribute to its improvement.

**Note:**
- Ensure proper installation of dependencies before running the script.
- The trained model is saved as 'captcha_reader.h5' for future predictions.

For predictions on new CAPTCHA images, use the `pred` function by providing the image path. Example usage is demonstrated in the script for images 'img-cap.jpg' and '244e2.png'.
