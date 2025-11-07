# AI Image Classifier

This project is a web-based image classification application that uses a pre-trained deep learning model to identify objects in images. It's built with Python, Streamlit, and TensorFlow.

## Prerequisites

- Python 3.12 or higher
- pip

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/your-repository.git
   cd your-repository
   ```

2. **Install the dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Run the application:**

   ```bash
   streamlit run main.py
   ```

2. **Open your web browser and navigate to the provided URL (usually `http://localhost:8501`).**

3. **Upload an image to classify it.**

## How It Works

The application uses a pre-trained MobileNetV2 model, a lightweight and efficient convolutional neural network, for image classification. Here's a breakdown of the key functions in `main.py`:

- **`load_model()`**: This function loads the MobileNetV2 model with pre-trained weights from ImageNet, a large visual database.

- **`preprocess_image(image)`**: Before the image is fed into the model, it's preprocessed. This function resizes the image to 224x224 pixels (the input size expected by MobileNetV2), preprocesses it using a specific MobileNetV2 function, and converts it into a batch of images.

- **`classify_image(model, image)`**: This is the core classification function. It takes the model and the uploaded image as input, preprocesses the image, and then uses the model to make predictions. The function returns the top 3 predictions with their corresponding labels and scores.

- **`main()`**: This function sets up the Streamlit web application. It creates the user interface, handles file uploads, and displays the classification results. It also uses Streamlit's caching to load the model only once, which improves performance.
