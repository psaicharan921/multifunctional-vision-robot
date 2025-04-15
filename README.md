# multifunctional-vision-robot
Simulated a multifunctional robot integrating object tracking, road sign recognition, leader-follower, and CNN-based self-driving. Developed and trained a CNN for steering control using Udacity simulator and deployed in Webots for real-time navigation.

# 🤖 Mini-Simulation of Autonomous Multifunctional Mobile Robot Using Machine Vision

This project demonstrates the simulation of a multifunctional autonomous robot that integrates four key computer vision capabilities — road sign recognition, object tracking, leader-follower functionality, and CNN-based self-driving — within Webots and Udacity simulator environments.

📄 [View Full Paper](docs/REPORT.pdf)

---

## 📷 Overview

The robot uses an RGB camera and deep learning for vision-based control. It responds to road signs for navigation, detects and follows moving objects, and uses CNN to steer autonomously in simulation.

### 👇 Core Functionalities:
✅ Road Sign Recognition using visual tags  
✅ Object Tracking using bounding box logic  
✅ Leader-Follower formation using front-facing camera  
✅ End-to-end Self-Driving with CNN model trained in Udacity simulator  

---

## ⚙️ Tools & Technologies

- **Simulators**: Webots, Udacity Self-Driving Car Simulator  
- **Languages**: Python, C++  
- **Libraries**: Opencv, Keras, TensorFlow  
- **Hardware Modelled**: Vision Sensor, Differential Drive, Rotational Motors  
- **AI Models**: 2D Convolutional Neural Networks (CNN)  
- **Vision Features**: Bounding box tracking, lane-edge detection, road symbol tagging

---

## 📈 CNN Training Workflow

1. Captured 13,074 images using triple-camera simulator setup  
2. Cleaned and reduced dataset to 3,505 meaningful training samples  
3. Preprocessed images: cropped, flipped, brightness adjusted, zoomed  
4. Developed CNN with batch normalisation + ELU activation  
5. Achieved <10% loss after 10 epochs without overfitting

---

## 🧠 Pseudocode: Object Tracking Decision Logic

```python
if x <= 440:
    # Turn left
elif x >= 640:
    # Turn right
elif area >= 116000:
    # Move backward (object close)
elif area <= 87320:
    # Move forward (object far)
else:
    # Stop
