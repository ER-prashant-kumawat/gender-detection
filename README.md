# gender-detection

This project uses a deep learning model to detect faces in a webcam feed and classify the detected faces as either "Male" or "Female". The code is implemented in Python using OpenCV, a popular library for computer vision.

Table of Contents
Overview
Requirements
Installation
Usage
How It Works
Notes
Overview
This project utilizes a Caffe-based deep learning model for gender classification in real time. The code performs the following steps:

Captures frames from a webcam.
Detects faces in each frame.
Classifies the gender of each detected face.
Displays the processed frames with gender labels directly in a Jupyter Notebook.
Requirements
Python 3.x
OpenCV
NumPy
IPython (for displaying frames in Jupyter Notebooks)
ipywidgets (for creating control buttons)
Installation
Install the necessary libraries by running:

bash
Copy code
pip install opencv-python-headless numpy ipywidgets
Usage
Download the Model Files:

Download gender_deploy.prototxt and gender_net.caffemodel and place them in the same directory as the script. These files contain the structure and weights for the gender detection model.
Run the Code in a Jupyter Notebook:

Copy and paste the code into a Jupyter Notebook cell and execute it.
Enable the Webcam:

Click the "Start Webcam" button to begin the live stream with gender detection.
Stop the Webcam:

Press 'q' to stop the webcam feed.
How It Works
Model Setup: A pre-trained Caffe model is used to classify gender. The model expects input images in the form of a 227x227 pixel blob with specific mean values subtracted for normalization.

Face Detection: OpenCV’s Haar Cascade classifier detects faces in each frame.

Gender Classification:

Each detected face is extracted, resized, and processed into a blob.
The blob is then passed to the pre-trained gender classification model to get predictions.
Display Results:

Each face is labeled with the predicted gender and drawn on the frame, which is then displayed directly in the Jupyter Notebook.
