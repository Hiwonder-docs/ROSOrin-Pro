# 3. LiDAR Course

## 3.1 LiDAR Introduction

### 3.1.1 Overview

LiDAR is a high-precision, high-speed remote sensing technology that plays an important role in map construction, autonomous driving, environmental perception, and robot navigation. This document introduces the principles, components, working methods, application fields, advantages, and development trends of LiDAR.

LiDAR plays a key role in autonomous driving and intelligent transportation by detecting obstacles, pedestrians, and vehicles on the road in real time while providing accurate distance and position information. In robot navigation and environmental perception, LiDAR provides robots with accurate map information and surrounding-environment data. In addition, LiDAR is widely used in fields such as 3D modeling and mapping, security monitoring, and remote sensing surveying.

<img src="../_static/media/chapter_4\section_1/media/image2.png" style="width:600px"  class="common_img" />

### 3.1.2 LiDAR Components and Classification

LiDAR consists of a laser emitter, receiver and photodetector, scanning mechanism, and angle-resolution module. The laser emitter generates the laser beam, the receiver and photodetector receive the reflected light signal, the scanning mechanism scans the surrounding environment, and the angle-resolution module determines the position of the target object.

According to the scanning method, LiDAR can be divided into the following categories:

Rotating LiDAR: It performs full horizontal scanning by rotating the emitter or scanning mechanism. It usually offers high scanning speed and high measurement accuracy, and is widely used in autonomous driving, 3D environment modeling, and map construction.

Solid-State LiDAR: It uses a solid-state laser emitter and does not require rotating parts. It is generally more compact, lighter, and lower in power consumption. It is suitable for mobile devices, drones, robots, and similar applications.

Mechanical LiDAR: It uses mechanical components such as rotating mirrors or rotating prisms to scan the laser beam. It usually provides a longer measurement distance and higher measurement accuracy, but the scanning speed is relatively lower. It is widely used in terrain surveying, building scanning, and navigation.

Phase-Modulated LiDAR: It measures the distance between the target object and the LiDAR by changing the phase of the laser beam. It usually provides high measurement accuracy and a large measurement range, and is widely used in map construction, surveying, and industrial applications.

Flash LiDAR: It uses a short, high-power laser pulse to illuminate the entire scene at one time, and then captures the reflected light signal through a receiver array. It offers the advantages of high speed and high resolution, and is suitable for rapid scene capture and motion tracking.

## 3.2 LiDAR Working Principle and Distance Measurement Methods

### 3.2.1 LiDAR Distance Measurement

There are two common methods for LiDAR to obtain the distance to a target. One is triangulation, and the other is time of flight, or TOF.

ToF ranging can be understood by referring to the diagram below. The LiDAR first shines light onto the object, which then reflects the light directly back to the LiDAR. The LiDAR calculates the time it takes for the light to return, multiplies this time by the speed of light, and divides the result by two to determine the distance between the object and the LiDAR.

<img src="../_static/media/chapter_4\section_1/media/image12.png" style="width:600px"  class="common_img" />

Triangulation can be understood with the figure below. During manufacturing, the LiDAR is adjusted so that the light does not strike the object directly, but instead reaches it at a fixed angle. This angle is preset and does not change during operation. The distance from the object to the LiDAR can then be calculated by applying trigonometric relationships to that angle.

<img src="../_static/media/chapter_4\section_1/media/image13.png" style="width:600px"  class="common_img" />

### 3.2.2 LiDAR Performance

The figure below illustrates the LiDAR effect. The LiDAR emits light that falls on the surface of an object. When the reflected light returns to the LiDAR, the contour of the object is marked at the positions reached by the light.

<img src="../_static/media/chapter_4\section_1/media/image14.png" style="width:600px"  class="common_img" />

## 3.3 LiDAR Obstacle Avoidance

The robot detects the distance between the object directly in front of it and the robot body, then turns left or right to avoid obstacles according to the preset distance. If no obstacle is encountered, the robot continues moving forward.

This feature can be enabled in two ways. The first is through the app. The second is through commands after a remote connection to the system.

For the app method, refer to [1.5 App Installation and Connection](https://wiki.hiwonder.com/projects/rosorin-pro/en/latest/docs/1_ROSOrin_Pro_User_Manual.html#app-installation-and-connection).

1. Start the robot and connect it through NoMachine. For remote connection instructions, refer to [1.7.2 AP Mode Connection Steps](https://wiki.hiwonder.com/projects/rosorin-pro/en/latest/docs/1_ROSOrin_Pro_User_Manual.html#ap-mode-connection-steps).

2. Click the terminal icon <img src="../_static/media/chapter_4\section_1/media/image15.png"  class="common_img" /> on the system desktop to open the command-line terminal.

3. Enter the following command and press **Enter** to stop the app auto-start service.

```bash
sudo systemctl stop start_app_node.service
```

4. Enter the following command and press **Enter** to start the robot startup program.

```bash
ros2 launch app lidar_node.launch.py debug:=true
```

5. Open another terminal, enter the following command, and press **Enter** to enable the LiDAR feature.

```bash
ros2 service call /lidar_app/enter std_srvs/srv/Trigger {}
```

<img src="../_static/media/chapter_4\section_1/media/image18.png"  class="common_img" />

6. In the current terminal, enter the following command and press **Enter** to start the LiDAR obstacle avoidance feature.

```bash
ros2 service call /lidar_app/set_running interfaces/srv/SetInt64 "{data: 1}"
```

7. To stop the current function, enter the following command in the current terminal and press **Enter**.

```bash
ros2 service call /lidar_app/set_running interfaces/srv/SetInt64 "{data: 0}"
```

8. To stop this feature, press **Ctrl + C** directly in the terminal window used in Step 4 or Step 5.

## 3.4 LiDAR Following

The robot detects the distance between the object directly in front of it and the robot's body. When the object gets too close to the front of the robot, the robot moves forward, backward, and turns to track the obstacle.

This feature can be enabled in two ways. The first is through the app. The second is through commands after a remote connection to the system.

For the app method, refer to [1.5 App Installation and Connection](https://wiki.hiwonder.com/projects/rosorin-pro/en/latest/docs/1_ROSOrin_Pro_User_Manual.html#app-installation-and-connection).

1. Start the robot and connect it through NoMachine. For remote connection instructions, refer to [1.7.2 AP Mode Connection Steps](https://wiki.hiwonder.com/projects/rosorin-pro/en/latest/docs/1_ROSOrin_Pro_User_Manual.html#ap-mode-connection-steps).

2. Click the terminal icon <img src="../_static/media/chapter_4\section_1/media/image15.png" /> on the system desktop to open the command-line terminal.

3. Enter the following command and press **Enter** to stop the app auto-start service.

```bash
sudo systemctl stop start_app_node.service
```

4. Enter the following command and press **Enter** to start the local app services and chassis control service.

```bash
ros2 launch app lidar_node.launch.py debug:=true
```

5. Open another terminal, enter the following command, and press **Enter** to enable the LiDAR feature.

```bash
ros2 service call /lidar_app/enter std_srvs/srv/Trigger {}
```

<img src="../_static/media/chapter_4\section_1/media/image18.png"  class="common_img" />

6. In the current terminal, enter the following command and press **Enter** to start the LiDAR following feature.

```bash
ros2 service call /lidar_app/set_running interfaces/srv/SetInt64 "{data: 2}"
```

7. To stop the current function, enter the following command in the current terminal and press **Enter**.

```bash
ros2 service call /lidar_app/set_running interfaces/srv/SetInt64 "{data: 0}"
```

8. To stop this feature, press **Ctrl + C** directly in the terminal window used in Step 4 or Step 5.

## 3.5 LiDAR Guarding

The robot detects the distance between the object directly in front of it and the robot's body. When the object gets too close to the front of the robot, the robot turns in place to follow the obstacle.

This feature can be enabled in two ways. The first is through the app. The second is through commands after a remote connection to the system.

For the app method, refer to [1.5 App Installation and Connection](https://wiki.hiwonder.com/projects/rosorin-pro/en/latest/docs/1_ROSOrin_Pro_User_Manual.html#app-installation-and-connection).

1. Start the robot and connect it through NoMachine. For remote connection instructions, refer to [1.7.2 AP Mode Connection Steps](https://wiki.hiwonder.com/projects/rosorin-pro/en/latest/docs/1_ROSOrin_Pro_User_Manual.html#ap-mode-connection-steps).

2. Click the terminal icon <img src="../_static/media/chapter_4\section_1/media/image15.png"  class="common_img" /> on the system desktop to open the command-line terminal.

3. Enter the following command and press **Enter** to stop the app auto-start service.

```bash
sudo systemctl stop start_app_node.service
```

4. Enter the following command and press **Enter** to start the local app services and chassis control service.

```bash
ros2 launch app lidar_node.launch.py debug:=true
```

5. Open another terminal, enter the following command, and press **Enter** to enable the LiDAR feature.

```bash
ros2 service call /lidar_app/enter std_srvs/srv/Trigger {}
```

<img src="../_static/media/chapter_4\section_1/media/image18.png"  class="common_img" />

6. In the current terminal, enter the following command and press **Enter** to start the LiDAR guarding feature.

```bash
ros2 service call /lidar_app/set_running interfaces/srv/SetInt64 "{data: 3}"
```

7. To stop the current function, enter the following command in the current terminal and press **Enter**.

```bash
ros2 service call /lidar_app/set_running interfaces/srv/SetInt64 "{data: 0}"
```

8. To stop this feature, press **Ctrl + C** directly in the terminal window used in Step 4 or Step 5.
