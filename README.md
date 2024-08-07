# jetracer-CollisionAvoidance
[JetRacer](https://www.waveshare.com/jetracer-pro-ai-kit.htm) is an autonomous AI Racing Robot kit based on the Jetson Nano Developer Kit. Supports deep learning, auto line following, autonomous driving, and so on. The JetRacer vehicle utilized in this study was acquired from Waveshare and configured in compliance with the instructions detailed in the official [Wiki](https://www.waveshare.com/wiki/JetRacer_Pro_AI_Kit).

<img src="https://www.waveshare.com/media/catalog/product/cache/1/image/800x800/9df78eab33525d08d6e5fb8d27136e95/j/e/jetracer-pro-ai-kit-1.jpg" width="400" height="400">

The objective of this repository is to implement a collision avoidance scenario using the JetRacer Pro AI Kit, drawing inspiration from the approach developed for the Jetbot robot, which enables it to stay within a rectangular area and navigate around obstacles.

![example1](https://github.com/chentyra/jetracer-CollisionAvoidance/assets/68944703/055e61a2-cb15-43c5-a609-035c3ba8e9b4)

Achieving collision avoidance with the JetRacer Pro AI Kit presents a significant challenge due to the fundamental differences between the JetRacer car and the [Jetbot robot](https://www.waveshare.com/jetbot-2gb-ai-kit.htm).

*Jetbot Robot Characteristics:*

- **Two-Wheeled Design**: The Jetbot robot utilizes a two-wheeled configuration, enabling it to achieve omnidirectional movement.
- **Direct Obstacle Avoidance**: This omnidirectional capability allows the Jetbot to directly circumvent obstacles by simply steering in the desired direction.

*JetRacer Car Characteristics:*

- **Four-Wheeled Design**: The JetRacer car employs a four-wheeled configuration, limiting its steering angle.
- **Indirect Obstacle Avoidance**: Due to its limited steering angle, the JetRacer cannot directly avoid obstacles; instead, it must rely on more complex strategies.

These differences necessitate a more cautious approach to training the JetRacer for collision avoidance. Alternative strategies may also be required to compensate for its limited maneuverability.

## Notebooks

To facilitate the achievement of this objective, this repository provides a collection of Jupyter notebooks which are interactive documents which combine text, code, and visualization.

### data_collection.ipnyb
This notebook facilitates the creation of a dataset using an interactive widget.

<img src="https://www.waveshare.com/w/A6Y79bcq/Kdy80nYY.php?f=JetBot_AI_Kit_Manual_13.jpg&width=600" width="400" height="300">

### train_model_res18.ipnyb
This notebook facilitates the training of the Resnet18 neural network utilizing the dataset generated by the preceding widget.

### build_trt.ipynb
This notebook enables the optimization of the previously developed neural network by enhancing its throughput and reducing its latency.

### live_demo.ipynb
This notebook facilitates the replication of the Jetbot robot's behavior for collision avoidance.

![ezgif-7-708044f095](https://github.com/chentyra/jetracer-CollisionAvoidance/assets/68944703/dc82ed98-f1c8-40f3-bdf2-80391472fae5)

### live_demo_backward.ipynb
This notebook employs additional strategies to circumvent obstacles that are in close proximity to the robot. Specifically, the task of collision avoidance is achieved by incorporating a reversing maneuver for the robot.

![example3](https://github.com/chentyra/jetracer-CollisionAvoidance/assets/68944703/7dfa7fa2-6bb9-4ddc-9904-9bd21f019835)

## See Also
- [JetBot](https://github.com/NVIDIA-AI-IOT/jetbot) - An educational AI robot based on NVIDIA Jetson Nano
- [JetCam](https://github.com/NVIDIA-AI-IOT/jetcam) - An easy to use Python camera interface for NVIDIA Jetson
- [JetCard](https://github.com/NVIDIA-AI-IOT/jetcard) - An SD card image for web programming AI projects with NVIDIA Jetson Nano
- [torch2trt](https://github.com/NVIDIA-AI-IOT/torch2trt) - An easy to use PyTorch to TensorRT converter

**If this repository was helpful to you, please give this repository a star!** :star:
