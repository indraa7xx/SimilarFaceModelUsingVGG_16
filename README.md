A Python based code that uses transfer learning with the VGG16 model to determine the visual similarity between a new input image and a pre-defined set of base images.

^ So How It Works?
This project avoids training a model from scratch. Instead, it uses a pre-trained CNN (VGG16) as a fixed feature extractor.

1.  Feature Extraction: The script processes a directory of "training" images, feeding each one through the VGG16 model (without its top classification layer) to generate a feature vector (a numerical representation of the image).
   2. Prototype Vector: It calculates the mean of all the training vectors to create a single "prototype" vector that represents the average features of the training set.
3. Comparison: For any new "test" image, it generates its own feature vector and uses Cosine Similarity to measure how closely it aligns with the prototype vector. A score above a certain threshold (e.g., 0.69) is considered a match.

## Core Technologies
- Python
- TensorFlow / Keras
- NumPy
- Scikit-learn
- Pillow

^How to Run

1.  Clone this repository.
2.  Install the required libraries: `pip install tensorflow numpy scikit-learn Pillow`
3.  Create a folder named `images_for_model` and place your base/training images inside it.
4.  Create a folder named `test_image` and place any images you want to test inside it.
5.  Run the Python script: `python your_script_name.py`
