# LIDAR-Camera-Object-Detection.
LIDAR and Camera Object Detection is a project on which i integrated electronics and machine learning algorithms..This project uses LIDAR to measure accurate distance using TOF or time of flight algorithm of an object in front of it. We also use a camera to detect the object using TensorFlow machine learning algorithm. The LIDAR and camera is therefore integrated on a single package using raspberry PI. The LIDAR and camera is attached to a servo that continuously sweeps 180 degrees several times per second. This project is intended to be applied on applications such as autonomous driving ,military applications, robots etc. for the ahead lying  robotics era.

LIDAR is a surveying method that measures distance to a target by illuminating the target with laser light and measuring the reflected light with a sensor. Differences in laser return times and wavelengths can then be used measure distance of the target. The name LIDAR stands for light detection and ranging. Camera can be used to identify the target using TensorFlow Ai Algorithm. We can train the algorithm to identify our required objects for applications like military surveillance and autonomous driving etc. 

Our project is based on a LIDAR module and Webcam on a servo motor. We are using Raspberry PI 3B+ as its brains to control the required detection and ranging. LIDAR is given as input to the Raspberry PI using serial min UART pins and a python script spins the servo 180 degrees several times reading the distance to the target and outputs it to a terminal. The servo turns the LIDAR module and the webcam. TensorFlow Ai API is used for object detection and training. We trained the algorithm to detect specific objects. The LIDAR’s precise range of the target along with the identification of the object using Tensoflow is outputted into a windows on Raspberry PI OS. Currently autonomous cars and military drones, unmanned vehicles use IR cameras and thermal imagery technology along with ranging technologies like SONAR etc. Such solutions are expensive, less accurate, less precise and short ranged. With our LIDAR¬-Camera implementation we intend to solve these problems and open new doors for such applications

![Screenshot 2022-08-26 190443](https://user-images.githubusercontent.com/111580618/186915743-6f736c49-68a1-4251-8861-c540bad0c5c2.png)

TensorFlow API.

TensorFlow is an end-to-end open source platform for machine learning. It has a comprehensive, flexible ecosystem of tools, libraries and community resources that lets researchers push the state-of-the-art in ML and developers easily build and deploy ML powered applications. TensorFlow is a library developed by the Google Brain Team to accelerate machine learning and deep neural network research. It was built to run on multiple CPUs or GPUs and even mobile operating systems, and it has several wrappers in several languages like Python, C++ or Java.

Installation on Raspberry PI terminal.
1.	git clone https://github.com/TensorFlow/TensorFlow.git
2.	cd TensorFlow

WORKING

![Screenshot 2022-08-26 190529](https://user-images.githubusercontent.com/111580618/186915923-54085153-bd3c-4b91-acb3-9a7dad8e72a5.png)

•	The python script makes the servos sweep 180 degrees 4 times per second via the Raspberry PI GPIO pin PWM control signal.
•	The LIDAR and webcam is mounted on top of the servo which detects the object, its distance and identifies what the object is using tensor flow algorithm processing.
•	The LIDAR is collecting data and giving its output to the raspberry pi via its transmit pin and the python script. The LIDAR finally outputs its readings to a separate terminal after executing the python script.
•	The camera outputs its data to raspberry pi via the USB serial port which then is processed by TensorFlow algorithms after executing TensorFlow on a terminal window. Finally, a separate window with real time view and object detection appears.
•	Both the LIDAR distance readings and object detection window appear on raspberry pi(OS) with real time reading of the object and its detection.
•	Raspberry PI is accessed via VNC protocol which allows us to remotely and wirelessly access, control it. 

