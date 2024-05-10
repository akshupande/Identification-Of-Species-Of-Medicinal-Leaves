# Identification of Species of Medicinal Leaves

This project implements a Streamlit application for identifying medicinal leaf species using a pre-trained Convolutional Neural Network (CNN) model.

## Implementation

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

**Overall Functionality:**

Users can upload an image of a medicinal leaf, and the pre-trained model predicts the leaf species along with a confidence score. The results are displayed conveniently within the Streamlit app.
