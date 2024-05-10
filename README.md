# Identification of Species of Medicinal Leaves

This project implements a Streamlit application for identifying medicinal leaf species using a pre-trained Convolutional Neural Network (CNN) model.

## Overview

The application leverages the following libraries:

* Streamlit: User interface creation
* TensorFlow's Keras: Deep learning framework for CNN model
* PIL (Python Imaging Library): Image processing
* NumPy: Numerical computations
* Matplotlib: Visualization (optional)

Here's a breakdown of the key functionalities:

**1. Imports and Setup:**

The code imports the necessary libraries and sets up the Streamlit application structure with:

* A sidebar containing menu options (e.g., Home, About Us)
* Page configuration for title and layout

**2. Prediction Function `predict_leaf()`:**

This function takes an image file as input and performs these pre-processing steps:

* Resizing the image
* Converting it to a NumPy array
* Normalizing pixel values
* Expanding dimensions to match the model's input format

It then uses the pre-trained CNN model to predict the class probabilities, returning:

* Predicted class label
* Confidence score
* Predicted index
* Class labels
* Entire prediction array

**3. Uploading and Predicting Image:**

The application provides a file uploader using `st.file_uploader()`. When an image (supported formats: jpg, jpeg, png) is uploaded, the `predict_leaf()` function is called to process it. The predicted results are then displayed on the Streamlit interface using `st.write()`.

**4. Pre-Trained Model Loading:**

The code loads the pre-trained CNN model from the `model.h5` file using `keras.models.load_model()`.

**Image Processing:**

* **Image Acquisition:** The process of obtaining images.
* **Image Enhancement:** Modifying an image to make it more visually pleasing or improve its quality.
* **Image Restoration:** Techniques to restore degraded images.

**Image Enhancement:**

* Image Enhancement involves modifying an image to make it more visually pleasing or improve its quality.
* It's primarily for the benefit of human perception and interpretation, aiming to improve interpretation and perception for human observers.

**Filtering:**

* Filtering is the process of applying a filter to an image to modify or extract information from it. It's used to improve image quality, enhance features, remove noise, and prepare images for further processing.
* It's commonly applied as a pre-processing step before feature extraction, object detection, or image segmentation.

**RGB to Grayscale Image:**

* Grayscale images contain only one channel of intensity information per pixel, while RGB images have three channels (Red, Blue, Green).
* Converting to grayscale reduces data dimensionality, making it more efficient for processing and storage, especially in situations with limited computational resources.
* Simplifies analysis.

**Characteristics of Grayscale Images:**

* **Mean Intensity:** Represents the average pixel value in an image, indicating brightness or darkness. Adjusting overall brightness is important for tasks like image recognition.
* **Standard Deviation:** Measures variation in pixel values. Higher standard deviation can indicate regions with strong edges, useful for edge detection or image classification.
