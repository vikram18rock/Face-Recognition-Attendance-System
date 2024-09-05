# Face-Recognition-Attendance-System

## Overview
This project implements a face recognition attendance system using VGG19, a popular convolutional neural network architecture, to classify faces. The system is designed to recognize three different persons.

## Components
1. **Image Capturing**:
   - The `image_capturing.ipynb` notebook captures 100 images of each person using the Haar Cascade algorithm for face detection. These images serve as the training data for the face recognition model.

2. **Model Training**: 
   - The `recognition.ipynb` notebook trains the VGG19 model using the captured images. It preprocesses the data, fine-tunes the VGG19 architecture, and trains the model to classify the faces of the three specified persons.

3. **Python Script**:
   - A Python script `project.ipynb` is provided to perform face recognition in real-time. The script loads the pre-trained VGG19 model, initializes the camera, and captures the faces of individuals.
   - If the recognized name doesn't exist in the CSV file, it will add the name along with the current timestamp into the CSV file.

## Files
- **image_capturing.ipynb**: The notebook for capturing images of individuals using the Haar Cascade algorithm.
- **haarcascade_frontalface_default.xml**: This XML file contains the pre-trained Haar Cascade classifier for frontal face detection.
- **class_names.txt**: This file contains the names of the three persons the model is trained to recognize.
- **recognition.ipynb**: The notebook for training the VGG19 model with the captured images.
- **model.h5**: This file contains the pre-trained VGG19 model.
- **project.ipynb**: The Python script for real-time face recognition and attendance tracking.

## Usage
1. Ensure you have the necessary dependencies installed. You can install them using `pip install -r requirements.txt`.
2. Run the `image_capturing.ipynb` notebook to capture images of each person.
3. Run the `recognition.ipynb` notebook to train the VGG19 model with the captured images.
4. Finally, run the `project.ipynb` script: `python project.ipynb`.
5. The script will open your camera feed. It will recognize faces in real time and update the attendance CSV file accordingly.

## Dataset Structure
```
Datasets/
│
├── Train/
│   ├── venkat/
│   │   ├── image1.jpg
│   │   ├── image2.jpg
│   │   ├── ...
│   │   └── image80.jpg
│   ├── Aadarsh/
│   │   ├── image1.jpg
│   │   ├── image2.jpg
│   │   ├── ...
│   │   └── image80.jpg
│   └── santhosh/
│       ├── image1.jpg
│       ├── image2.jpg
│       ├── ...
│       └── image80.jpg
│
└── Test/
    ├── venkat/
    │   ├── image1.jpg
    │   ├── image2.jpg
    │   ├── ...
    │   └── image20.jpg
    ├── Aadarsh/
    │   ├── image1.jpg
    │   ├── image2.jpg
    │   ├── ...
    │   └── image20.jpg
    └── santhosh/
        ├── image1.jpg
        ├── image2.jpg
        ├── ...
        └── image20.jpg
```

## Results

<div style="display:flex; flex-direction:row;">
    <div>
        <h3>Accuracy</h3>
        <img src="https://github.com/venkatasai24/Face-Recognition-Attendance-System/blob/main/Accuracy%20Graph.jpeg" alt="Accuracy" width="400"/>
    </div>
    <div>
        <h3>Loss</h3>
        <img src="https://github.com/venkatasai24/Face-Recognition-Attendance-System/blob/main/Loss%20Graph.jpeg" alt="Loss" width="400"/>
    </div>
</div>

## Dependencies
- Python 3.x
- OpenCV
- Keras
- TensorFlow
- Numpy
- MatPlotLib
  
## Contributors
- Vedurupaka Venkata Sai
- Ponnuru Aadarsh
- Gayathri Vankadoth

## Contributing
We welcome contributions to improve this project! If you'd like to contribute:
- Fork the repository
- Create a new branch (`git checkout -b feature/improvement`)
- Make your changes and commit them (`git commit -am 'Add new feature'`)
- Push to the branch (`git push origin feature/improvement`)
- Create a new Pull Request

# Face-Recognition-Attendance-System
