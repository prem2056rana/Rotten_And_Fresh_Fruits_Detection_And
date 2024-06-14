# Rotten_And_Fresh_Fruits_Detection_And_Separation
## Overview

This project is designed to detect and separate fresh and rotten fruits, specifically focusing on apples and tomatoes. Using the YOLOv7-tiny model for real-time object detection, the system identifies whether the fruit is fresh or rotten and classifies it accordingly. Once classified, the system uses a servo motor to separate the fruits into two different boxes.

## Features

- **Fruit Detection**: Identify and classify fruits as either fresh or rotten.
- **Fruit Classes**:
  - Fresh Apple
  - Rotten Apple
  - Fresh Tomato
  - Rotten Tomato
- **Separation Mechanism**: Uses a servo motor to separate the fruits into two boxes based on their classification.

## Getting Started

### Prerequisites

- **Hardware**:
  - Raspberry Pi 4
  - Camera module (for capturing images of fruits)
  - Servo motor
  - Connecting wires or PCB for connections
  - Boxes or containers for separated fruits
  - Stepper Motor (For Conveyor belt)
- **Software**:
  - Raspbian OS (or any Raspberry Pi-compatible OS)
  - Python 3
  - OpenCV
  - PyTorch
  - YOLOv7-tiny model(you can use other version YOLO)
  - TensorFlow Lite (optional, if you plan to run a TFLite model)
  - GPIO library for Raspberry Pi
  - Roboflow (For labeling datasheet)
  - Putty
  - VNC viewer
  - 

### Installation

1. **Set up Raspberry Pi**:
    - Install the latest Raspbian OS on your Raspberry Pi 4.
    - Ensure your Raspberry Pi is connected to the internet.

2. **Clone the Repository**:
    ```sh
    git clone https://github.com/your_username/Rotten_And_Fresh_Fruits_Detection_And_Separation.git
    cd Rotten_And_Fresh_Fruits_Detection_And_Separation
    ```

3. **Install Required Packages**:
    ```sh
    sudo apt-get update
    sudo apt-get install python3-pip
    pip3 install opencv-python torch
    ```

4. **Download YOLOv7-tiny Model**:
    - Download the YOLOv7-tiny model weights and configuration files and place them in the `models` directory of the project.

5. **Set up the Camera and Servo Motor**:
    - Connect the camera module to the Raspberry Pi.
    - Connect the servo motor to the GPIO pins of the Raspberry Pi.

### Usage

1. **Run the Detection and Separation Script**:
    ```sh
    python3 detect_and_separate.py
    ```

2. **Place a Fruit in Front of the Camera/Conveyor belt**:
    - The system will classify the fruit as Fresh Apple, Rotten Apple, Fresh Tomato, or Rotten Tomato.
    - Conveyor Belt move continuously.
    - The servo motor will move the fruit into the appropriate box based on its classification.

### Script Details

- **detect_and_separate.py**: Main script to capture images from the camera, run the YOLOv7-tiny model for detection, classify the fruit, and control the servo motor to separate the fruits accordingly.

### Documentation

- [Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/)
- [OpenCV Documentation](https://docs.opencv.org/)
- [PyTorch Documentation](https://pytorch.org/docs/)
- [YOLOv7 Documentation](https://github.com/WongKinYiu/yolov7)

### Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

### Paper
 For detailed information about the project, you can read this paper:
[https://www.researchgate.net/publication/379986263_Recognition_and_separation_of_fresh_and_rotten_fruits_using_YOLO_algorithm]

### Authors

- **Prem Bahadur Rana** -[https://github.com/prem2056rana/Rotten_And_Fresh_Fruits_Detection_And_Separation]

### Acknowledgments

- Special thanks to the developers of YOLOv7, OpenCV, and PyTorch.
- Thanks to the community for support and contributions.
