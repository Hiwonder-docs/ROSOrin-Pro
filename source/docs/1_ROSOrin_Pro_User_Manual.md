# 1. ROSOrin Pro User Manual

[TOC]



## 1.1 Introduction

ROSOrin Pro is an integrated AI robot for education and research. It integrates a high-performance controller, a high-precision LiDAR, a 6DOF robotic arm, a 3D depth camera, and an AI voice interaction box. These components make it easy to build creative applications, such as robot motion control, mapping and navigation, path planning, tracking and obstacle avoidance, motion interaction, and voice interaction. ROSOrin Pro is deployed with multimodal large AI models, so it can understand the environment, plan actions, and execute tasks flexibly to support advanced embodied AI applications.

<img src="../_static/media/chapter_1\section_1/media/image218.png" style="width:600px"  class="common_img" />

### 1.1.1 Packing List

The included components of the ROSOrin Pro robot are listed below.

<img src="../_static/media/chapter_1\section_1/media/image1.png"   class="common_img" />

<img src="../_static/media/chapter_1\section_1/media/image2.png"   class="common_img" />

<img src="../_static/media/chapter_1\section_1/media/image3.png"   class="common_img" />



## 1.2 Accessories Installation and Startup Preparation

### 1.2.1 Camera Installation

<img src="../_static/media/chapter_1\section_1/media/image219.png"   class="common_img" style="width:600px"/>

### 1.2.2 Voice Module Installation

<img src="../_static/media/chapter_1\section_1/media/image221.png" style="width:600px"  class="common_img" />

### 1.2.3 Robotic Arm Installation

<img src="../_static/media/chapter_1\section_1/media/image310.png" style="width:600px"  class="common_img" />

Connect the 3-pin servo cable to the robotic arm servo and the 3-pin servo port on the STM32 control board.

### 1.2.4 Display Installation

<img src="../_static/media/chapter_1\section_1/media/image311.png" style="width:600px"  class="common_img" />

### 1.2.5 Wiring Instruction

#### 1.2.5.1 Jetson Nano Wiring

<img src="../_static/media/chapter_1\section_1/media/image225.png" style="width:600px"  class="common_img" />

| Serial No. | Access Module |
| --- | --- |
| 1 | Jetson Nano controller power cable |
| 2 | DP port |
| 3 | Hub |
| 4 | Display |
| 5 | STM32 controller |
| 6 | AI voice interaction box |
| 7 | LiDAR |
| 8 | Reserved custom expansion port |
| 9 | Reserved custom expansion port |
| 10 | 3D depth camera |



#### 1.2.5.2 Jetson Orin Nano / Orin NX Wiring

<img src="../_static/media/chapter_1\section_1/media/image223.png" style="width:600px"  class="common_img" />

| Serial No. | Access Module |
| --- | --- |
| 1 | Jetson Orin Nano / Orin NX controller power cable |
| 2 | DP port |
| 3 | Hub |
| 4 | Display |
| 5 | STM32 controller |
| 6 | AI voice interaction box |
| 7 | LiDAR |
| 8 | Reserved custom expansion port |
| 9 | Reserved custom expansion port |
| 10 | 3D depth camera |



#### 1.2.5.3 Raspberry Pi 5 Wiring

<img src="../_static/media/chapter_1\section_1/media/image7.png" style="width:600px" />

In the figure above, labels **1** and **2** correspond to the **power cable** and the **display cable**.

<img src="../_static/media/chapter_1\section_1/media/image224.png" style="width:600px"  class="common_img" />



| Serial No. | Access Module |
| --- | --- |
| 1 | Hub |
| 2 | Display |
| 3 | STM32 controller |
| 4 | AI voice interaction box |
| 5 | Ethernet port |
| 6 | LiDAR |
| 7 | Reserved custom expansion port |
| 8 | Reserved custom expansion port |
| 9 | 3D depth camera |



## 1.3 Lithium Battery Usage Precautions

During transportation, the robot remains powered off and the battery is not fully charged. Connect the battery cable and charge the battery before first use. Charging the battery from 10 V to about 12.3 V takes approximately three hours.

> [!NOTE]
>
> **When the battery voltage falls below 10V, the buzzer will emit a "beep-beep-beep" low voltage warning. If the battery is low, turn off the robot immediately and charge the battery according to the recommended charging procedure.**



**1\. Always use the dedicated charger included with the kit to charge the robot. Turn off the robot while charging. Do not operate the robot and charge the battery at the same time.**

**2\. When the charger is connected to the battery but not plugged into a power outlet, the indicator light shows green. During charging, the indicator light turns red. When fully charged, it will return to green.**

**3\. Do not plug the charger directly into the DC power input on the Jetson controller, as shown in the diagram below, as it may damage the controller. The image is for reference only.**

<img src="../_static/media/chapter_1\section_1/media/image42.png" style="width:600px" />

**4\. Disconnect the charging cable promptly after charging to avoid overcharging and battery damage.**

**5\. To ensure stable robot performance, recharge the battery when its voltage drops below 10 V, indicated by a beeping buzzer on the expansion board.**

**6\. If the robot will not be used for an extended period, fully charge the battery and disconnect the battery cable.**

**7\. Store the battery in a cool, dry place to prevent reduced lifespan due to overheating or moisture. Do not hit, throw, or step on the battery.**

**8\. Do not use the battery in environments with strong static electricity or magnetic fields, as this may damage its safety protection circuitry.**

**9\. Do not plug the battery directly into a wall socket. Do not short-circuit the battery terminals with metal objects.**

**10\. Over-discharging may prevent the battery from recharging and could render it unusable. For long-term storage, fully charge the battery first.**

**11\. Do not attempt to modify, solder, or alter the battery or charger in any way.**

**12\. Keep batteries away from high temperatures and liquids to avoid overheating, fire hazards, or moisture-related damage.**

> [!NOTE]
>
> **Important Notice: Hiwonder is not responsible for any damage, economic loss, or safety incidents resulting from improper use of the product that does not follow the instructions outlined in this manual.**

### 1.3.1 Charging Instructions

1. The power input is located on the right side at the back of the robot. Plug in the charger to begin charging.

<img src="../_static/media/chapter_1\section_1/media/image47.png"  style="width:600px" />

<img src="../_static/media/chapter_1\section_1/media/image48.png" style="width:600px" />

2. Check the indicator light on the charger to monitor the charging status. The indicator shows red while charging and turns green when charging is complete.

<img src="../_static/media/chapter_1\section_1/media/image49.png" width="377" height="230" />

> [!NOTE]
>
> **After charging is complete, unplug the charger promptly to prevent overcharging.**



## 1.4 Initial Power-On Instructions

This section introduces the robot's startup sequence and verifies each module. After this step is completed, the following chapters can be used for app control and wireless controller control.

### 1.4.1 Power-On Preparations

1. **To ensure stable operation, recharge the battery promptly when its voltage drops below 10 V.**

2. **Do not place the robot near the edge of a table to avoid accidental falls and damage.**

3. **Always operate the robot on a flat, stable surface.**

4. **Maintain a safe distance from the robot before powering on to prevent accidental contact with moving parts.**

5. **Before powering on, ensure that the wiring is correct and the robot is fully charged. If the robot doesn't power on, check the wiring of each module.**

<p id ="anther1-4-2"></p>

### 1.4.2 Power-On Status

1. Make sure the robot's power button is not pressed.
   
   <img src="../_static/media/chapter_1\section_1/media/image43.png"  width="505" height="325" />
   
2. Remove the hex screws from the bottom of the robot and open the metal cover.
   
   <img src="../_static/media/chapter_1\section_1/media/image44.png" width="478" height="369" />
   
3. Connect the red wire to the red terminal and the black wire to the black terminal as shown in the figure below. The connectors include reverse-polarity protection. If the connector does not match, do not force it. Rotate the connector and try again, then reassemble the metal cover.
   
   <img src="../_static/media/chapter_1\section_1/media/image45.png"  width="491" height="354" />
   


<img src="../_static/media/chapter_1\section_1/media/image46.png"  width="491" height="354" />

4. Place the robot on a flat, smooth surface and press the switch located on the rear left side of the robot.

<img src="../_static/media/chapter_1\section_1/media/image43.png"  width="491" height="354" />

5. The blue LED1 at the lower right of the expansion board will light up and start blinking. At this stage, only the network configuration service is running, while the ROS system and other services have not yet fully started. Wait until a short beep sounds, indicating that the system has finished booting.

(1) The LED locations on the Jetson controllers are shown in the diagram below.

<img src="../_static/media/chapter_1\section_1/media/image50.png" class="common_img" />

(2) The LED locations on the Raspberry Pi 5 controller are shown in the diagram below.

<img src="../_static/media/chapter_1\section_1/media/image226.png" class="common_img" />

6. By default, the device is configured in AP direct-connect mode. After startup, a Wi-Fi hotspot beginning with **HW** will appear. To connect via the app or remote desktop, enter the default password: **hiwonder**.

<img src="../_static/media/chapter_1\section_1/media/image243.png" class="common_img" />

> [!NOTE]
>
> **If the hotspot does not appear after startup, troubleshoot as follows:**
>
> * **Verify that all steps in the [1.4.2 Power-On Status](#anther1-4-2) section have been followed.**
> * **If LED1 stays solid blue instead of blinking, the system may be in LAN mode. Long-press the KEY1 button on the expansion board for 5 to 10 seconds. If LED1 starts blinking, the HW Wi-Fi hotspot has been re-enabled.**
> * **If LED1 does not blink after pressing KEY1, the system may not detect the SD card or SSD. Remove and reinsert the SD card.**
> * **If the LED remains solid after reinserting it, the SD card may be corrupted, or the system image may not have been flashed for kits without a controller. Replace the SD card or reflash the image to the SD card.**
> * **If the issue persists, the Raspberry Pi 5 controller or Jetson controller may be faulty. Please contact customer support for assistance.**

The following table outlines how to test each hardware module.

| Module | Verification Steps | Result |
| --- | --- | --- |
| expansion board LED | Observe the LED's lighting and flashing behavior | By default, the LED is blue and flashing in AP direct connection mode, indicating that network service configuration is complete. |
| Buzzer | Check for a short beep | A short beep from the buzzer indicates that the onboard hardware of the expansion board is functioning normally. |
| LiDAR | Observe the rotation | The built-in blue LED of the LiDAR lights up and rotates continuously. |
| KEY1 on expansion board | Switch network status | After connecting to the STA local network mode via the app, press and hold the KEY1 button to check if the LED1 indicator flashes. |
| Microphone, sound card, speaker | Say **Hello Hiwonder** to the robot after powering on | There is feedback to the wake word, and the speaker plays the response **I'm here**. Only available for the kits that include a voice device. |
| Depth camera | 1. Open the app and connect to the robot.<br/>2. Open the **Robot Control** function and check the real-time feed from the depth camera. | Displays the real-time feed and rotates. |
| STM32 controller + encoder DC gear motor | After powering on, use the **Robot Control** function via the wireless controller or the app. | The robot moves normally. |
| Robotic arm | After powering on, use the **Robot Control** function in the app for operation. | The robotic arm operates normally, rotates, and grips objects. |




## 1.5 App Installation and Connection

> [!NOTE]
> 
> * **Please grant all permissions requested during installation to ensure the app functions properly.**
> 
> * **Turn on phone GPS and Wi-Fi before opening the app.**

This section explains how to install the **WonderAi** app to control the robot.

<p id ="anther5.1"></p>

### 1.5.1 App Installation

The app installation package is located in the directory:  
[2 Softwares\\1. App Installation Package](https://drive.google.com/drive/folders/1AigaXogFuhNV8uvy-vlNE0lmu1bftKg_?usp=sharing). Transfer the APK file to a phone and install it.

Or scan the QR code below to download the app.

<img src="../_static/media/chapter_1\section_1/media/image227.png" style="width:300px" class="common_img" />

### 1.5.2 Connection Modes

After the app is installed, the robot can be connected. The robot supports the two network modes below:

1. AP Direct Connection Mode: The controller creates a hotspot that a phone can connect to directly. External network access is unavailable in this mode.

2. STA LAN Mode: The controller actively connects to a specified hotspot or Wi-Fi network. External network access is available in this mode.

The robot uses AP direct connection mode by default. Regardless of whether AP direct connection mode or STA LAN mode is selected, the robot features remain the same.

AP direct connection mode is recommended first for feature experience. LAN mode can then be used as needed.

#### 1.5.2.1 AP Mode Connection (Must Read)

> [!NOTE]
>
> **This section uses the Android system and the mecanum-wheel version as the example. If switching to the Ackermann or differential version, refer to the robot-type change tutorial first, then follow the procedure below.**

1. Open the **WonderAi** app and select **Developer** > **ROSOrin Pro**.

<img src="../_static/media/chapter_1\section_1/media/image254.png" style="width:600px" class="common_img" />

2. Tap the **+** button in the bottom-right corner and choose **Direct Connection Mode**.

<img src="../_static/media/chapter_1\section_1/media/image255.png" style="width:600px" class="common_img" />

3. Search for the robot Wi-Fi network. The hotspot name starts with **HW**, and the hotspot password is **hiwonder**.

<img src="../_static/media/chapter_1\section_1/media/image243.png" style="width:400px" class="common_img" />

4. Return to the app, tap the corresponding robot icon, and enter the mode selection screen.

<img src="../_static/media/chapter_1\section_1/media/image256.png" style="width:600px" class="common_img" />

> [!NOTE]
>
> **If a message appears indicating that the network is unavailable, tap Keep Connection to continue.**

5. If the prompt **Whether to switch and enter the searched product interface?** appears, the product version selected in Step 1 is incorrect. Tap **CONFIRM** to switch directly to the correct mode-selection screen.

<img src="../_static/media/chapter_1\section_1/media/image56.png" style="width:500px" class="common_img" />

6. The mode selection interface is shown below.

<img src="../_static/media/chapter_1\section_1/media/image57.png" style="width:600px" class="common_img" />

<p id ="anther5.2.2"></p>

#### 1.5.2.2 LAN Mode Connection (Optional)

> [!NOTE]
>
> **After setting the robot to LAN mode, it will no longer broadcast a WiFi network starting with HW.**

1. First, connect the phone to a 5G Wi-Fi network. **Hiwonder_5G** is used here as the example. For dual-band routers with separate SSIDs, the default Wi-Fi names for the two bands are different.
2. Open the **WonderAi** app and select **Developer** > **ROSOrin Pro**.

<img src="../_static/media/chapter_1\section_1/media/image254.png" style="width:600px" class="common_img" />

3. Tap the **+** button in the bottom-right corner and choose **LAN Mode**.

<img src="../_static/media/chapter_1\section_1/media/image257.png" style="width:600px" class="common_img" />

4. The app prompts for the password of the connected Wi-Fi network. Make sure the password is correct. An incorrect password prevents the connection. After the password is entered, tap **OK**.

<img src="../_static/media/chapter_1\section_1/media/image258.png" style="width:400px" class="common_img" />

5. Tap **Go to connect device hotspots** to switch to the Wi-Fi settings.

<img src="../_static/media/chapter_1\section_1/media/image260.png" style="width:600px" class="common_img" />

6\. In the Wi-Fi list, find the hotspot starting with **HW**, and connect to it using the password **hiwonder**. After connecting, tap the **Back** icon to return to the app.

7\. The app has started connecting to the robot.

<img src="../_static/media/chapter_1\section_1/media/image261.png" style="width:300px" class="common_img" />

8\. After a few seconds, the robot's icon and name will appear on the main screen. The LED1 indicator on the expansion board will stay on.

<img src="../_static/media/chapter_1\section_1/media/image256.png" style="width:600px" class="common_img" />

<img src="../_static/media/chapter_1\section_1/media/image64.png" style="width:400px" class="common_img" />

9. Press and hold the robot icon to display its current IP address.

<img src="../_static/media/chapter_1\section_1/media/image263.png" style="width:400px" class="common_img" />

10. Enter the IP address in the remote desktop client to establish the connection. For detailed connection instructions, refer to [1.7 Development Environment Setup](#anther7.0).

### 1.5.3 App Control

The **WonderAi** app can be used to control the robot and experience part of its AI vision features. This section explains how each function in the app is used. The iOS system is used for demonstration, and the same method also applies to Android.

#### 1.5.3.1 Preparation

1. First, power on the robot. For details on startup status, refer to section [1.4.2 Power-On Status](#anther1-4-2).

2. Next, install the WonderAi app and connect the robot. For step-by-step instructions, see section [1.5.1 App Installation](#anther5.1).

#### 1.5.3.2 App Modes

The app provides five modes, including Robot Control, Lidar, Target Tracking, Line Following, and Driverless.

<img src="../_static/media/chapter_1\section_1/media/image57.png" style="width:600px" class="common_img" />

The table below offers a detailed overview of each mode.

| Icon | Mode | Description |
| --- | --- | --- |
| <img src="../_static/media/chapter_1\section_1/media/image66.png" /> | Robot control | Control the movement of the robot. |
| <img src="../_static/media/chapter_1\section_1/media/image67.png" /> | LiDAR | Provides three functions: LiDAR obstacle avoidance, LiDAR following, and LiDAR guarding. |
| <img src="../_static/media/chapter_1\section_1/media/image68.png" /> | Target tracking | Select the color of the target object, and the robot will track it. |
| <img src="../_static/media/chapter_1\section_1/media/image69.png" /> | Line following | Lay down a line and set its color as the target recognition color. The robot will follow the line. |
| <img src="../_static/media/chapter_1\section_1/media/image70.png" /> | Driverless | Experience the autonomous driving feature. |




#### 1.5.3.3 Robot Control

Tap Robot Control on the mode selection screen to enter the control interface.

<img src="../_static/media/chapter_1\section_1/media/image71.png" style="width:600px" class="common_img" />

The interface is shown below:

<img src="../_static/media/chapter_1\section_1/media/image72.png" style="width:600px" class="common_img" />

1\. The buttons on the left, from top to bottom, correspond to gravity control, forward/backward movement, and speed adjustment.

2\. The center displays the feedback video.

3\. The buttons on the right, from top to bottom, control steering.

4\. The top menu icons allow <img src="../_static/media/chapter_1\section_1/media/image73.png" width="37" height="33" style="display:inline;vertical-align:middle;"/> screenshot, <img src="../_static/media/chapter_1\section_1/media/image74.png" width="37" height="34" style="display:inline;vertical-align:middle;"/> hide navigation bar, and <img src="../_static/media/chapter_1\section_1/media/image75.png" width="37" height="32" style="display:inline;vertical-align:middle;"/> switch to full-screen mode. This function is typically used alongside the wireless controller.

5\. Clicking the full-screen button <img src="../_static/media/chapter_1\section_1/media/image75.png" width="37" height="32" style="display:inline;vertical-align:middle;"/> displays the feedback video in full screen, which is useful for monitoring real-time video while controlling the robot with the controller.

<img src="../_static/media/chapter_1\section_1/media/image76.png" style="width:600px" class="common_img" />

#### 1.5.3.4 Lidar

> [!NOTE]
> 
> * **Before starting this feature, place the robot on a spacious surface with enough room to move freely.**
> 
> * **In Lidar obstacle avoidance and Lidar following modes, the detection range is a 90-degree fan-shaped area in front of the robot.**

- #### Interface Overview

Tap **Lidar** on the mode selection screen to enter the control interface.

<img src="../_static/media/chapter_1\section_1/media/image82.png" style="width:600px" class="common_img" />

The **Lidar** mode includes three features: Lidar obstacle avoidance, Lidar following, and Lidar guard. This interface is divided into two sections:

1. In the left panel, enable or disable the feature.

2. In the right panel, display the live video feed from the camera.

<img src="../_static/media/chapter_1\section_1/media/image83.png" style="width:600px" class="common_img" />

- #### Function

| Icon | Function Description |
| --- | --- |
| <img src="../_static/media/chapter_1\section_1/media/image84.png" width="150" height="35" alt="LiDAR Obstacle Avoidance Switch Icon"> | Turn on/off the avoid obstacle mode. |
| <img src="../_static/media/chapter_1\section_1/media/image85.png" width="150" height="35" alt="LiDAR Follow Switch Icon"> | Turn on/off the Lidar following mode. |
| <img src="../_static/media/chapter_1\section_1/media/image86.png" width="150" height="35" alt="LiDAR Guard Switch Icon"> | Turn on/off the Lidar guarding mode. |
| <img src="../_static/media/chapter_1\section_1/media/image87.png" width="141" height="73" alt="Camera Feed Icon"> | Display the current camera feed. |




- #### Operating Steps and Effects

1. **Avoid obstacle**

   The robot continuously moves forward. When an obstacle is detected, it automatically changes direction to avoid it.

2. **Lidar following**

   When an obstacle is detected, the robot adjusts its position to maintain a safe distance from the object.

3. **Lidar guarding**

   When an obstacle is detected, the robot turns to face the object.

#### 1.5.3.5 Target Tracking

> [!NOTE]
> 
> * **Place the target object on the same surface as the robot and move it in a horizontal direction, which ensures a smoother tracking experience.**
> 
> * **Choose an appropriate color range for target extraction. If the range is too wide, unwanted colors may be included. If the range is too narrow, the target may be lost. Also, avoid having objects with similar colors to the target in the camera view.**

- #### Interface Overview

Tap **Target Tracking** on the mode selection screen to enter the control interface.

<img src="../_static/media/chapter_1\section_1/media/image88.png" style="width:600px" class="common_img" />

This interface is divided into two sections:

1. The left panel contains the mode switch and color extraction tools.

2. In the right panel, display the live video feed from the camera.

<img src="../_static/media/chapter_1\section_1/media/image89.png" style="width:600px" class="common_img" />

- #### Function

| Icon | Function Description |
| --- | --- |
| <img src="../_static/media/chapter_1\section_1/media/image90.png" width="200" height="50" alt="Mode Switch Icon"> | Turn on/off the mode. |
| <img src="../_static/media/chapter_1\section_1/media/image91.png" width="200" height="40" alt="Color Adjustment Icon"> | Adjust the color threshold range, with a value range of 0.05-1.00. |
| <img src="../_static/media/chapter_1\section_1/media/image92.png" width="200" height="66" alt="Color Extraction Icon"> | Extract the color from the specified area in the feed. |
| <img src="../_static/media/chapter_1\section_1/media/image93.png" width="200" height="60" alt="Color Confirmation Icon"> | After clicking the **Pick** button, it will switch to the **OK** button. Used to confirm the extracted color. |
| <img src="../_static/media/chapter_1\section_1/media/image94.png" width="150" height="120" alt="Color Display Icon"> | Display the extracted color. |
| <img src="../_static/media/chapter_1\section_1/media/image95.png" width="150" height="78" alt="Camera Feed Icon"> | Display the current camera feed. |

- #### Operating Steps and Effects

1\. Tap the **Pick** button, then drag the red circle in the video feed to the target object to select its color.

<img src="../_static/media/chapter_1\section_1/media/image96.png" style="width:600px" class="common_img" />

2\. Tap **OK**, and the selected color will be displayed in the **Selected color** area.

3\. Tap the **Start** button to activate the feature. Move the target object, and the robot will follow accordingly.

<img src="../_static/media/chapter_1\section_1/media/image97.png" style="width:600px" class="common_img" />

#### 1.5.3.6 Line Following

> [!NOTE]
> 
> * **Before starting this feature, lay out the tracking path with tape and place the robot on the track.**
> 
> * **Choose an appropriate color range for target extraction. If the range is too wide, unwanted colors may be included. If the range is too narrow, the target may be lost. Also, avoid having objects with similar colors to the target in the camera view.**
> 
> * **After the feature starts, please ensure there is no other object containing the recognition color except the target object within the camera view. Otherwise, the recognition result will be affected.**

- #### Interface Overview

Tap **Line Following** on the mode selection screen to enter the control interface.

<img src="../_static/media/chapter_1\section_1/media/image98.png" style="width:600px" class="common_img" />

This interface is divided into two sections:

1. The left panel contains the mode switch and color extraction tools.

2. In the right panel, display the live video feed from the camera.

<img src="../_static/media/chapter_1\section_1/media/image99.png" style="width:600px" class="common_img" />

- #### Function

| Icon | Function Description |
| --- | --- |
| <img src="../_static/media/chapter_1\section_1/media/image100.png" width="94" height="31" /> | Turn on/off the mode. |
| <img src="../_static/media/chapter_1\section_1/media/image91.png" width="200" height="36" /> | Adjust the color threshold range, with a value range of 0.05-1.00. |
| <img src="../_static/media/chapter_1\section_1/media/image92.png" width="200" height="50" /> | Extract the color from the specified area in the feed. |
| <img src="../_static/media/chapter_1\section_1/media/image93.png" width="150" height="50" /> | After clicking the **Pick** button, it will switch to the **OK** button. Used to confirm the extracted color. |
| <img src="../_static/media/chapter_1\section_1/media/image101.png" width="94" height="73" /> | Display the extracted color. |
| <img src="../_static/media/chapter_1\section_1/media/image102.png" width="151" height="101" /> | Display the current camera feed. |




- #### Operating Steps and Effects

1\. In this section, red tape is used as an example. After clicking the **Pick** button, drag the red circle in the live feed to the track to select its color.

<img src="../_static/media/chapter_1\section_1/media/image103.png" style="width:600px" class="common_img" />

2\. Tap **OK**, and the selected color will be displayed in the **Selected color** area.

3\. Tap **Start** to begin the feature, and the robot will follow the colored line automatically.

<img src="../_static/media/chapter_1\section_1/media/image104.png" style="width:600px" class="common_img" />

#### 1.5.3.7 Driverless

- #### Interface Overview

Tap **Driverless** on the mode selection screen to enter the control interface.

<img src="../_static/media/chapter_1\section_1/media/image105.png" style="width:600px" class="common_img" />

<img src="../_static/media/chapter_1\section_1/media/image106.png" style="width:600px" class="common_img" />

This interface is used for the autonomous driving feature. It is mainly divided into two sections:

1. The **Start** button on the left is used to activate the autonomous driving function.

2. The central area displays the live feed from the camera.

- #### Function

| **Icon**| **Function**|
|----------|----------|
| <img src="../_static/media/chapter_1\section_1/media/image100.png" width="94" height="31" />| Enable and disable the feature.|
| <img src="../_static/media/chapter_1\section_1/media/image107.png" width="151" height="99" />| Display real-time detection results for traffic signs, lane markings, and traffic lights.|

- #### Operating Steps and Effects

Click the **Start** button <img src="../_static/media/chapter_1\section_1/media/image108.png" width="113" height="30" /> to begin the autonomous driving feature. The robot will drive automatically along the center of the lane, slow down when approaching pedestrian crossings, respond to traffic signs accordingly, and follow traffic light signals, such as stopping at red lights and moving on green lights.

<img src="../_static/media/chapter_1\section_1/media/image109.png" style="width:600px" class="common_img" />



## 1.6 Wireless Controller Control

### 1.6.1 Notes

1. **Before powering on the device, make sure the wireless controller receiver is properly inserted. This can be ignored if the receiver was pre-inserted at the factory.**

2. **Pay attention to battery polarity when placing the batteries.**

<img src="../_static/media/chapter_1\section_1/media/image110.png"  width="529" height="202" />

(1) **Each time the robot is powered on, the app auto-start service launches automatically, including the wireless controller control service. If this service has not been disabled, no additional action is required. Simply connect and control.**

(2) **Since signals from wireless controllers can interfere with each other, it is recommended not to use this function when multiple robots are in the same area to avoid misconnection or unintended control.**

(3) **After the wireless controller is turned on, if it does not connect to the robot within 30 seconds or remains unused for 5 minutes after connection, it will enter sleep mode automatically. To wake the wireless controller and exit sleep mode, press START.**

(4) **If the robot does not respond while using the controller, try starting the relevant services. For detailed steps, refer to section [2.1 Motion Control Course](https://wiki.hiwonder.com/projects/rosorin-pro/en/latest/docs/2_Chassis_Motion_Control_Course.html#motion-control) in the 2. Chassis Motion Control Course.**

### 1.6.2 Device Connection

1. After the robot powers on, slide the wireless controller switch to the **ON** position. At this point, the red and green LED indicators on the wireless controller will start flashing simultaneously.

2. Wait a few seconds for the robot and wireless controller to pair automatically. Once pairing is successful, the green LED will remain solid while the red LED turns off.

<img src="../_static/media/chapter_1\section_1/media/image111.png" width="493" height="198" />

### 1.6.3 Button Functions

The following table describes the functions of the controller buttons and joysticks from the robot perspective:

> [!NOTE]
>
> **Lightly pushing the joysticks in any direction allows low-speed movement.**

| **Button**| **Function**| **Description**|
|----------|----------|----------|
| START| Stop and reset the robot.| Press|
| Left joystick up| Move forward| Push|
| Left joystick down| Move backward| Push|
| Left joystick left| Move left. | Push|
| Left joystick right| Move right. | Push|
| Right joystick left| Turn left. | Push|
| Right joystick right| Turn right. | Push|

<p id ="anther7.0"></p>

## 1.7 Development Environment Setup

### 1.7.1 Remote Control Tool Introduction and Installation

#### 1.7.1.1 Tool Introduction

There are two ways to remotely control the robot: graphical control and command-line control.

NoMachine and VNC are graphical remote-control software tools. After installation, the robot hotspot can be connected and the robot can be controlled directly from a computer. The Jetson Nano, Jetson Orin Nano, and Jetson Orin NX controllers use NoMachine, while the Raspberry Pi 5 controller uses VNC. When connected through either tool, the robot system desktop is displayed directly for intuitive operation.

In contrast to NoMachine and VNC, MobaXterm connects via SSH and focuses on command-line control. It does not display the full system desktop of the robot, only the command-line interface. For users who are familiar with terminal commands, this method allows faster robot control while reducing computational load and memory usage.

MobaXterm also includes a lightweight X11 server, which allows graphical applications to be displayed directly when needed. Regardless of the controller version, the MobaXterm SSH connection method is always supported.

In a word, NoMachine and VNC are best for scenarios requiring intuitive, visual operation, while MobaXterm is better suited for fast command execution. Select the remote-control software according to the application requirements.

#### 1.7.1.2 NoMachine Installation

> [!NOTE]
>
> **This tool is compatible with Jetson series controllers.**

1\. Navigate to the directory and double-click to open the folder [2. Softwares / 2. Remote Desktop Software / 1. Graphical Remote Desktop Access Tool](https://drive.google.com/drive/folders/1Cj9wV58u7ZNiLwH4SFcu4bR9aJ9jn6Xs?usp=sharing), and then double-click to open the installation package **nomachine_8.4.2_10_x64**.

2\. Click **Next**.

<img src="../_static/media/chapter_1\section_1/media/image112.png" width="453" height="351" />

3\. Select **English** as the installation language. Accept the license agreement by checking the box, then click **Next**.

<img src="../_static/media/chapter_1\section_1/media/image113.png" width="453" height="351" />

4\. Keep the default installation path and click **Next** again.

<img src="../_static/media/chapter_1\section_1/media/image114.png" width="453" height="351" />

5\. Wait for a moment, and the setup completion screen will appear. Click **Finish** to exit the installer.

<img src="../_static/media/chapter_1\section_1/media/image115.png" width="453" height="351" />

6\. Click **Yes** to restart the computer. This step must not be skipped!

<img src="../_static/media/chapter_1\section_1/media/image116.png" width="453" height="210" />

#### 1.7.1.3 VNC Installation

> [!NOTE]
>
> **This tool is compatible with Raspberry Pi controllers.**

1. Locate the folder at: [2. Software \\ 2. Remote Desktop Software \\ 1. Graphical Remote Desktop Access Tool](https://drive.google.com/drive/folders/1Cj9wV58u7ZNiLwH4SFcu4bR9aJ9jn6Xs?usp=sharing) to install it. Double-click the file **VNC-Viewer-6.17.731-Windows** in this folder. In the pop-up dialog, select **English** as the installation language and click **OK**.

<img src="../_static/media/chapter_1\section_1/media/image228.png" width="453" height="210" />

2. On the next screen, click **Next**.

<img src="../_static/media/chapter_1\section_1/media/image229.png" width="453" height="351" />

3. Agree to the license agreement, then click **Next**. Keep the default installation path, and click **Next**.

<img src="../_static/media/chapter_1\section_1/media/image230.png" width="453" height="351" />

4. Click **Install** to begin installation.

<img src="../_static/media/chapter_1\section_1/media/image231.png" width="453" height="351" />

5. Wait for the installation to complete, then click **Finish** to complete the setup.

<img src="../_static/media/chapter_1\section_1/media/image232.png" width="453" height="351" />

6. After installation, launch VNC Viewer by clicking its desktop icon <img src="../_static/media/chapter_1\section_1/media/image233.png"  />.

#### 1.7.1.4 MobaXterm Installation

> [!NOTE]
>
> **This tool is compatible with any controller.**

1. Locate the folder: [2. Software \\ 2. Remote Desktop Software \\ 2. SSH Remote Client](https://drive.google.com/drive/folders/1Cj9wV58u7ZNiLwH4SFcu4bR9aJ9jn6Xs?usp=sharing), and open the installer and follow the prompts to complete the installation.

<img src="../_static/media/chapter_1\section_1/media/image234.png" class="common_img"  />

2. Click **Next**.

<img src="../_static/media/chapter_1\section_1/media/image235.png" width="453" height="351"  />

3. Accept the license agreement by checking the box, then click **Next**.

<img src="../_static/media/chapter_1\section_1/media/image236.png" width="453" height="351"  />

4. Keep the default installation path and click **Next** again.

<img src="../_static/media/chapter_1\section_1/media/image237.png" width="453" height="351"  />

5. Click **Install**.

<img src="../_static/media/chapter_1\section_1/media/image238.png" width="453" height="351"  />

6. Wait for a moment, the setup completion screen will appear. Click **Finish** to exit the installer.

<img src="../_static/media/chapter_1\section_1/media/image239.png" width="453" height="351"  />

<p id ="anther7.2"></p>

### 1.7.2 AP Mode Connection Steps

**AP Mode: The controller creates a hotspot for direct connection by a phone and computer, but external network access is unavailable.**

> [!NOTE]
>
> **Before connecting the Jetson Orin Nano or Jetson Orin NX controller via NoMachine, ensure that a virtual display or an external monitor is connected. The connection location is shown in the diagram below at port 2. This section provides only a general overview.**

<img src="../_static/media/chapter_1\section_1/media/image223.png" style="width:600px"  class="common_img" />

<p id ="anther7.2.1"></p>

#### 1.7.2.1 Connecting via NoMachine

**AP Mode: The controller creates a hotspot for direct local connection, but external network access is unavailable.**

1\. The robot is set to AP mode by default. After powering it on, it will generate a Wi-Fi hotspot starting with **HW**. On the computer, search for and connect to the hotspot shown in the figure using the password **hiwonder**.

<img src="../_static/media/chapter_1\section_1/media/image240.png"  />

2\. Open NoMachine and enter the IP address **192.168.149.1** in the search bar. Click **Configure connection to new host 192.168.149.1**.

<img src="../_static/media/chapter_1\section_1/media/image117.png" width="566" height="103" />

3\. Once opened, change the **Name** field to **ROSOrin Pro**, leaving the other options unchanged, and click **Add**.

<img src="../_static/media/chapter_1\section_1/media/image241.png" style="width:600px"  />

4. Then, double-click the entry named **ROSOrin Pro**.

<img src="../_static/media/chapter_1\section_1/media/image242.png" style="width:600px"  />

5. In the **Username** and **Password** fields, enter the following according to the controller version: 

  For Jetson Nano, the default username is **hiwonder**, and the password is **hiwonder**. 
  For Jetson Orin Nano, the default username is **ubuntu**, and the password is **ubuntu**. 
  For Jetson Orin NX, the default username is **ubuntu**, and the password is **ubuntu**. 
  After entering the credentials, check the **Remember password** box and click the **Login** button. The following example uses the Jetson Orin Nano version:

<img src="../_static/media/chapter_1\section_1/media/image119.png" style="width:600px" class="common_img" />

> [!NOTE]
>
> **If the robot is configured in STA Mode, follow the same steps as above, but make sure to replace the IP address, Username, and Password in steps 2, 3, and 4 accordingly.**

6. For configuration settings, select the appropriate checkboxes and click **OK** to proceed.

<img src="../_static/media/chapter_1\section_1/media/image120.png" style="width:600px" class="common_img" />

<img src="../_static/media/chapter_1\section_1/media/image121.png" style="width:600px" class="common_img" />

<img src="../_static/media/chapter_1\section_1/media/image122.png" style="width:600px" class="common_img" />

<img src="../_static/media/chapter_1\section_1/media/image123.png" style="width:600px" class="common_img" />

#### 1.7.2.2 Connecting via VNC

1) Search for and connect to the hotspot starting with **HW** on the computer, as shown in the diagram below. The password for the connection is **hiwonder**.

<img src="../_static/media/chapter_1\section_1/media/image243.png" style="width:400px" class="common_img" />

2. Open the VNC client and enter the IP address in AP mode: **192.168.149.1** in the address bar, then press **Enter**. If a warning about an insecure connection appears, click **Continue**.

<img src="../_static/media/chapter_1\section_1/media/image244.png" style="width:600px" class="common_img" />

3. Wait for the login window to appear, then follow the steps in order: enter the username->enter the password->check **Remember password** ->click **OK**.

Enter **pi** in the Username field, and enter **raspberrypi** in the Password field.

<img src="../_static/media/chapter_1\section_1/media/image245.png" style="width:600px" class="common_img" />

4. Once connected, the Raspberry Pi remote desktop will be displayed as shown below.

<img src="../_static/media/chapter_1\section_1/media/image246.png" style="width:600px" class="common_img" />

#### 1.7.2.3 Connecting via MobaXterm

Using AP mode as the example, the same steps also apply to LAN mode, but the IP address must be replaced accordingly.

1. On the main interface, click **Session** in the upper-right corner to create a new session. In the session window, enter the recorded robot IP address **192.168.149.1**, and then click **OK**.

<img src="../_static/media/chapter_1\section_1/media/image247.png" style="width:600px" class="common_img" />

2. Select **SSH**.

<img src="../_static/media/chapter_1\section_1/media/image248.png" style="width:600px" class="common_img" />

3. Enter the fixed IP address for AP mode: **192.168.149.1**.

<img src="../_static/media/chapter_1\section_1/media/image249.png" style="width:600px" class="common_img" />

4. If a window like the one below appears, click the third option.

<img src="../_static/media/chapter_1\section_1/media/image250.png" style="width:600px" class="common_img" />

5. When prompted for the username and password, enter them according to the controller version shown below. The following example uses the Jetson Nano version:

For Jetson Nano, the default username is **hiwonder** and the password is **hiwonder**. 
For Jetson Orin Nano, the default username is **ubuntu** and the password is **ubuntu**. 
For Jetson Orin NX, the default username is **ubuntu** and the password is **ubuntu**. 
For Raspberry Pi 5, the default username is **pi** and the password is **raspberrypi**.

<img src="../_static/media/chapter_1\section_1/media/image251.png" style="width:600px" class="common_img" />

> [!NOTE]
> 
> * **The username must be entered in lowercase. Even if the account was originally created with uppercase letters, it must be typed in lowercase when logging in.**
> * **After entering the username, press Enter to proceed to the password field.**
> * **When typing the password, no characters will be displayed. After finishing, press Enter again to log in.**

6. If the password is correct, the system is accessed successfully, and the interface appears as shown below.

<img src="../_static/media/chapter_1\section_1/media/image252.png" style="width:600px" class="common_img" />

### 1.7.3 LAN Mode Connection

**STA Mode (LAN Connection): The controller connects to a specified Wi-Fi network, and Internet access is available in this mode.**

> [!NOTE]
>
> * **To configure the robot for LAN Mode through a smartphone, enable the location service on the phone beforehand.**
>
> * **LAN mode cannot be switched through the system default network settings shown in the figure below. Since the Wi-Fi has been specially configured, follow the network setup instructions provided later in this document.**
>
> * **After setting the robot to LAN mode, it will no longer broadcast a WiFi network starting with HW.**

Configuration steps:

1. Click the terminal icon <img src="../_static/media/chapter_1\section_1/media/image125.png" width="35" height="29" style="display:inline;vertical-align:middle;"/> in the system desktop to open a command-line window.

2. Enter the following command and press **Enter** to go to the configuration directory.

```bash
cd wifi_manager
```

3. Then enter the following command and press **Enter** to open the configuration file:

```bash
vim wifi_conf.py
```

4. First, set the value of `WIFI_MODE` to 2. 1 stands for Direct Connection Mode, while 2 stands for LAN Mode.

<img src="../_static/media/chapter_1\section_1/media/image128.png"  />

5. Next, modify `WIFI_STA_SSID` and `WIFI_STA_PASSWORD` to the Wi-Fi name and password of the target router. For example, **hiwonder_5G** is used here. Ensure that the WiFi name does not contain spaces and is in English only.

<img src="../_static/media/chapter_1\section_1/media/image129.png"  />

> [!NOTE]
>
> **A 5G Wi-Fi signal is recommended for faster transmission. If lag occurs with a standard Wi-Fi connection, switching to a 5G network is recommended.**

6. After confirming the input is correct, press **ESC**, then type `:wq` to save and exit the file.

<img src="../_static/media/chapter_1\section_1/media/image130.png"  />

7. Restart the robot's Wi-Fi service using the following command.

```bash
sudo systemctl restart wifi.service
```

> [!NOTE]
> 
> * **After restarting the robot's Wi-Fi service, NoMachine will disconnect automatically. This happens because the device is in LAN mode, and connecting to a different Wi-Fi network causes the IP address to change.**
> * **To switch to Direct Connection Mode, simply edit the configuration file, comment out all the lines, save the changes, and restart the robot.**

8. For instructions on finding the device IP address, refer to [1.5.2.2 LAN Mode Connection (Optional)](#anther5.2.2), then follow the steps in [1.7.2 AP Mode Connection Steps](#anther7.2) and replace the IP address accordingly.

### 1.7.4 Fixed-IP Connection Through a USB Data Cable

> [!NOTE]
>
> **This section applies only to Jetson series controllers. It is not supported for the Raspberry Pi 5 controller.**

The robot can achieve smoother remote operation by enabling the remote NDIS-compatible device and using a fixed IP address of **192.168.55.1**. This method does not require connecting to the robot's hotspot or Wi-Fi in LAN mode. The steps are as follows:

1. For the Jetson Nano controller, connect the robot to the computer using a Micro-USB data cable.

<img src="../_static/media/chapter_1\section_1/media/image132.png" style="width:600px" class="common_img" />

2. For the Jetson Orin Nano controller, connect the robot to the computer using a Type-C data cable.

<img src="../_static/media/chapter_1\section_1/media/image264.png" style="width:600px" class="common_img" />

3. On the computer, right-click **This PC** on the desktop and select **Manage**.

<img src="../_static/media/chapter_1\section_1/media/image133.png" width="302" height="240" />

4. Click **Device Manager** in the left panel, then find the NDIS driver under **Network Adapters**. Right-click the driver and select **Update Driver**.

<img src="../_static/media/chapter_1\section_1/media/image134.png" width="529" height="429" />

5. Next, follow the steps in [1.7.2 AP Mode Connection Steps](#anther7.2), and change the IP address field to **192.168.55.1**.

## 1.8 Manual Mapping

This section explains how to quickly experience manual mapping. No complex operations are required. The feature can be started by tapping the corresponding icon on the touchscreen.

Manual mapping requires robot motion to be controlled with a wireless controller or a keyboard. For single-robot scenarios, the wireless controller is recommended for convenience. In multi-robot environments, keyboard control is recommended instead. Wireless controller signals can interfere across robots, so this method is not recommended when multiple robots are operating in the same area, to avoid unintended connections or unintended control.

After mapping is completed, the generated map is saved. The autonomous navigation feature can then be started to review the mapping result. Note that autonomous navigation always loads the most recently created map. Regardless of the mapping method used, a newly created map overwrites the previous one.

### 1.8.1 Preparation

Before starting the robot, confirm that the remote desktop tool has been installed by following [1.7 Development Environment Setup](#anther7.0), and that the robot connection procedure is already familiar.

Also confirm that the wireless controller receiver is inserted into the robot USB port and is fully seated.

### 1.8.2 Operation Steps

> [!NOTE]
>
> * **This tutorial applies to Jetson Orin Nano, Jetson Orin NX, and Raspberry Pi 5.**
> * **In this mode, prepare an enclosed space in advance on a flat surface. If obstacles are placed, their height should be above the horizontal plane of the LiDAR.**

1. Place the robot in the area where mapping will be performed.
2. Tap the desktop on the touchscreen, then select and open the **SLAM** icon for manual mapping.

<img src="../_static/media/chapter_1\section_1/media/image265.png"  />

3. After it opens, several terminals start at the same time. Wait for a moment.

<img src="../_static/media/chapter_1\section_1/media/image266.png" style="width:600px" />

4. When the display interface appears, the feature has started successfully.

<img src="../_static/media/chapter_1\section_1/media/image171.png" style="width:600px" />

5. Mapping can now be controlled with the wireless controller. The controller button functions are listed below:

> [!NOTE]
>
> **Keep the controller within a reasonable distance from the robot to avoid disconnection.**

| Button / Joystick | Operation | Function |
| --- | --- | --- |
| START | Press | Exit sleep mode |
| Left joystick | Push forward / backward | Control forward and backward movement |
| Left joystick | Push left / right | Control left and right translation |
| Right joystick | Push left | Control left turning |

If keyboard control is used, connect to the remote desktop and select the terminal that supports keyboard control.

<img src="../_static/media/chapter_1\section_1/media/image267.png" style="width:600px"/>

The keyboard controls are listed below:

| **Key** | **Function** | **Description** |
| --- | --- | --- |
| W | Move forward | Short-press switches to the forward state and keeps the robot moving forward |
| S | Move backward | Short-press switches to the backward state and keeps the robot moving backward |
| A | Turn left | Long-press interrupts forward or backward movement and turns the robot left counterclockwise in place |
| D | Turn right | Long-press interrupts forward or backward movement and turns the robot right |

When **W** or **S** is pressed, the robot continues moving forward or backward. When **A** or **D** is pressed, the robot interrupts the forward or backward motion and rotates in place. Releasing **A** or **D** stops the rotation and leaves the robot in place.

6. After movement is completed, click **Save Map** to save the map that has been built.

<img src="../_static/media/chapter_1\section_1/media/image268.png" style="width:600px"/>

7. After mapping is completed, click the close button in the command-line terminal to turn off the quick mapping feature.

<img src="../_static/media/chapter_1\section_1/media/image269.png" style="width:600px"/>

## 1.9 Autonomous Navigation

> [!NOTE]
>
> **This tutorial applies to Jetson Orin Nano, Jetson Orin NX, and Raspberry Pi 5 controllers.**

1. Start the robot, tap the touchscreen, and select the **Navigation** icon to open the quick navigation feature.

<img src="../_static/media/chapter_1\section_1/media/image272.png" style="width:100px" />

2. After it opens, the program starts running in the terminal. Wait for the interface shown below to appear, which indicates the feature has started successfully.

<img src="../_static/media/chapter_1\section_1/media/image273.png" style="width:600px" />

3. In the software toolbar, **2D Pose Estimate** is used to set the robot initial position. **2D Goal Pose** is used to set a single target point for the robot and is suitable for basic navigation tasks that do not require complex obstacle avoidance or path planning. **Publish Point** is used to set multiple target points for the robot. **Nav2 Goal** is used to set more complex navigation goals, such as a target point, a target pose, or a target area.

<img src="../_static/media/chapter_1\section_1/media/image274.png" style="width:600px" />

4. The icon <img src="../_static/media/chapter_1\section_1/media/image275.png" style="width:200px;display:inline;vertical-align:middle;"/> changes the robot initial position on the map and is used to align it with the robot actual location.

5. Click the icon <img src="../_static/media/chapter_1\section_1/media/image276.png" style="width:150px;display:inline;vertical-align:middle;" />, then click a location on the map to set a target point. Clicking and dragging also sets the robot's orientation after it reaches the target point.

<img src="../_static/media/chapter_1\section_1/media/image277.png" style="width:600px" />

6. Click the lower-left icon <img src="../_static/media/chapter_1\section_1/media/image278.png" style="width:300px;display:inline;vertical-align:middle;"/> to enable multi-point navigation. Then click the icon <img src="../_static/media/chapter_1\section_1/media/image279.png" style="width:100px;display:inline;vertical-align:middle;"/> once to set one target point. Drag to choose the target-point orientation. Repeat this procedure to set multiple target points.

> [!NOTE]
>
> **Click "Nav2 Goal" before setting each target point.**

<img src="../_static/media/chapter_1\section_1/media/image280.png" style="width:600px" />

7. After all target points are set, click **Start Waypoint Following** at the lower-left corner to start navigation. The robot automatically avoids obstacles during navigation.

<img src="../_static/media/chapter_1\section_1/media/image281.png" style="width:600px" />



## 1.10 Hardware Introduction

This section introduces the robot hardware, including the electronic control system, ROS controller, LiDAR, depth camera, and other sensors.

### 1.10.1 Hardware System

Diagram of the STM32 controller ports:

<img src="../_static/media/chapter_1\section_1/media/image217.png"  style="width:600px" class="common_img" />

### 1.10.2 Electronic Control System

The robot electronic control system uses an STM32 controller as the low-level motion controller, connected to multiple DC geared motors with encoders. It also features a built-in IMU sensor with accelerometer and gyroscope, enabling chassis motion control and sensor data acquisition.

#### 1.10.2.1 STM32 Robot Controller

The STM32 robot motion controller is an open-source controller designed specifically for robotics development. It is compact and well-designed. A single board can control various chassis types, including Mecanum chassis, Ackermann chassis, differential drive chassis, and tank chassis.

The controller uses the STM32F407VET6 as its main processor, based on the ARM Cortex-M4 core, running at 168 MHz, with 512 KB of on-chip Flash and 192 KB of SRAM, and it includes an FPU and DSP instructions. The system block diagram of the STM32F40x/41x series is shown below.

<img src="../_static/media/chapter_1\section_1/media/image13.png" style="width:600px" class="common_img" />

The controller features an onboard IMU with accelerometer and gyroscope sensors, supports up to four DC encoder motors, and includes two 5V power outputs with a maximum current of 5A. With abundant onboard resources and expansion interfaces, it is ideal for ROS robot development and can be paired with Jetson series ROS controllers to form a complete ROS robot system.

The front panel layout of the controller is shown in the figure below:

<img src="../_static/media/chapter_1\section_1/media/image14.png" style="width:600px" class="common_img" />

The controller provides the circuit schematic and features an SWD debug port. It supports USB serial programming for STM32 firmware updates and enables secondary development. On-board resources and peripheral example code are provided to facilitate learning and usage.

The onboard resources and peripherals of the STM32F407VET6 processor are shown in the figure below. For detailed information, please refer to the appendix documents in the folder [STM32F407XX Data Sheet](https://drive.google.com/drive/folders/1GH1QO6Cm1baFc5bdf17NPWIly7CVZbx_?usp=sharing).

<img src="../_static/media/chapter_1\section_1/media/image15.png" style="width:600px" class="common_img" />

- **IMU Sensor**

A 6-axis IMU sensor, the MPU6050, features a 3-axis accelerometer and a 3-axis gyroscope. It connects to the controller via the I2C port. The six axes of the IMU accelerometer and gyroscope are defined as shown in the figure below.

<img src="../_static/media/chapter_1\section_1/media/image16.png"  />

<img src="../_static/media/chapter_1\section_1/media/image17.png"  />

- **Reserved Ports**

The reserved expansion ports provide connections for custom development.

<img src="../_static/media/chapter_1\section_1/media/image18.png" style="width:600px" class="common_img" />

- **SWD Debug Port**

The pins highlighted in red, 3V3, PA14, GND, PA13, serve as the SWD debug port, supporting SWD debugging.

PA14 serves as SWD_CLK and PA13 as SWD_DIO. Connect these pins to the corresponding port for debugging.

<img src="../_static/media/chapter_1\section_1/media/image19.png" style="width:600px" class="common_img" />

- **Power Supply Ports**

The STM32 controller provides multiple external power ports, distributed as shown in the figure below.

<img src="../_static/media/chapter_1\section_1/media/image20.png" style="width:600px" class="common_img" />

For more detailed information, please refer to [4. Hardware Resources\\1. STM32 Controller Files](https://drive.google.com/drive/folders/1ITrr0a_EAi3al5hOrIHmCNFlZunjZ0LM?usp=sharing).

#### 1.10.2.2 Power Supply

The robot uses a dedicated 11.1 V 6000 mAh lithium battery.

| Capacity          | 11.1V 6000mAh                                                | Charging voltage    | 12.6V                                         |
| ----------------- | ------------------------------------------------------------ | ------------------- | --------------------------------------------- |
| Discharge current | ≤ 10 A                                                       | Discharge connector | SM connector with reverse-polarity protection |
| Safety            | Supports overcharge protection, overcurrent protection, overdischarge protection, and short circuit protection |                     |                                               |


The robot should be charged with the dedicated charger included in the kit. The red charger indicator means charging is in progress, while the green indicator means the battery is fully charged or not connected. The indicator is green with no load, red during charging, and green again when charging is complete.

<img src="../_static/media/chapter_1\section_1/media/image24.jpeg"  style="width:600px"  class="common_img" />

> [!NOTE]
>
> **Do not charge the robot while it is powered on. Charging is only allowed when the robot is turned off.** 

#### 1.10.2.3 Hall Encoder DC Geared Motor

The Hall encoder is a speed-sensing module that uses a Hall-effect sensor, paired with a strong magnetic disk, and outputs pulse signals through AB-phase channels. The motor operates at 12V. The figure below shows the motor used in the robot and its pin configuration:

<img src="../_static/media/chapter_1\section_1/media/image25.png" style="width:200px" />

<img src="../_static/media/chapter_1\section_1/media/image26.png" style="width:400px"  />

For more details:

1\. The voltage between VCC and GND depends on the microcontroller supply, typically 3.3V or 5V.

2\. The frequency of the square wave output on C1 and C2 depends on the motor speed and the number of pole pairs in the magnetic disk.

3\. The voltage between M1 and M2 corresponds to the motor operating voltage.

The table below lists the specifications of the motors used in the robot:

|    Parameter    |          Value           |      Parameter      |                 Value                 |
| :-: | :-: | :-: | :-: |
| Rated voltage | 12V | Gear ratio | 1:90 |
| No-load speed | 110rpm | Rated speed | 85rpm |
| Stall torque | 15kg.cm | Rated torque | 2.6kg.cm |
| Stall current | 3.2A | Rated current | 0.36A |
| Rated power | Approx. 8.3W | Encoder type | AB two-phase encoder |
| Motor type | Brushed permanent magnet | Output shaft | 6mm D-shaped eccentric shaft |
| Encoder voltage | 3.3~5V | Magnetic ring lines | 11 lines |
| Interface type | PH2.0-6PIN | Function | Built-in pull-up shaping, single-chip |



#### 1.10.2.4 Bus Servo

The ROSOrin Pro robotic arm uses a bus servo to control gripping and rotation. The servo model is the HX-12H digital servo.

<img src="../_static/media/chapter_1\section_1/media/image27.png" class="common_img" />

|      Parameter      |              Value              |
| :-: | :-: |
| Operating voltage | DC 9-12.6V |
| No-load current | 300mA |
| Stall current | 1.3A |
| Control method | UART serial commands |
| Connector model | 5264-3P |
| Control angle range | 0-1000, corresponding to 0-240° |
| Rotation speed | 0.2 sec/60° at DC 11.1V |
| Stall torque | 12kg·cm at DC 11.0V |
| Rotation range | 0-240° |
| Servo accuracy | 0.3° |
| Cable length | 20cm |
| Gear type | Metal gears |
| Dimensions | 35.19 x 26.19 x 27.20 mm |
| Weight | 36.3 g |
| Applicable for | Various biomimetic robot joints |



#### 1.10.2.5 OLED Display Module

The OLED display module uses a 0.91-inch blue OLED display. It features a wide viewing angle, fast response, stable graphics, high brightness, and high resolution. The driver chip is SSD1306, which controls the display content. The module also includes LEGO-compatible mounting holes for more creative DIY applications.

<img src="../_static/media/chapter_1\section_1/media/image28.png" class="common_img" />

Specifications:

|      Parameter       |                Value                 |
| :-: | :-: |
| Operating voltage | DC 5V |
| Communication method | I2C |
| PWR indicator | Turns on after the sensor is powered |
| Dimensions | 50 x 20 mm |

0.91-inch blue OLED display specifications:

|                        Parameter                         |         Value          |
| :------------------------------------------------------: | :--------------------: |
|                        Resolution                        |        128 x 32        |
|                    Outline dimensions                    | 30.0 x 11.50 x 1.45 mm |
|                       Display area                       |   22.384 x 5.584 mm    |
|                       Pixel pitch                        |    0.175 x 0.175 mm    |
|                        Pixel size                        |    0.159 x 0.159 mm    |
|                       Driver chip                        |        SSD1306         |
|                     Module structure                     |          COG           |
| Compatible with modular installation and the LEGO series |                        |

Port Description:

| Pin | Description |
| :-: | :-: |
| GND | Ground |
| 5V | Power input |
| SDA | SDA data line |
| SCL | SCL clock line |


#### 1.10.2.6 PS2 Wireless Controller

A USB receiver is connected to the chassis, enabling chassis movement control via a PS2 wireless controller.

<img src="../_static/media/chapter_1\section_1/media/image29.png" width="552" height="343" />

<img src="../_static/media/chapter_1\section_1/media/image30.png" width="553" height="288" />

PS2 controller pinout and connection diagram to the controller:

<img src="../_static/media/chapter_1\section_1/media/image31.png" width="330" height="282" />

<img src="../_static/media/chapter_1\section_1/media/image32.png"  width="553" height="441" />

Concept:

The USB receiver transmits differential signals through a pair of data lines, D+ and D-. When receiving the signals sent from the controller, it forwards them to the STM32, which then performs decoding.

STM32 Decoding: The STM32 reads the electrical signals on the data lines and converts them into binary data. Following the PS2 protocol, it decodes this data into specific commands.

The button mappings correspond to the table below.

| Button | Function | Description |
| --- | --- | --- |
| START | Stop and reset the chassis, wake up the controller connection | Press START |
| Left joystick left | Move forward | Hold |
| Left joystick right | Move backward | Hold |
| Right joystick left | Move left | Hold |
| Right joystick right | Move right | Hold |



### 1.10.3 ROS Main Controller

ROSOrin Pro provides full support for ROS controllers. The operation is similar across different controllers. Raspberry Pi 5 runs Debian 12, while the Jetson series runs Ubuntu. The table below compares the specifications of Raspberry Pi 5, Jetson Nano, Jetson Orin Nano, and Jetson Orin NX controllers.

<img src="../_static/media/chapter_1\section_1/media/image282.png" style="width:600px" />

#### 1.10.3.1 Jetson Nano Version

<img src="../_static/media/chapter_1\section_1/media/image33.png" style="width:600px" />

The robot uses a Jetson Nano as its ROS controller, consisting of a Jetson Nano core board and an expansion board. The core board is a compact yet powerful computer capable of running mainstream deep learning frameworks, providing sufficient computing power for most AI projects.

The expansion board exposes the LED indicators and control buttons, enabling network status to be monitored through LED signals and network modes to be switched from a mobile device. It also provides GPIO and I2C ports for hardware expansion.

**The core board runs Ubuntu 18.04 with the ROS Melodic environment pre-installed, and a ROS2 Humble environment configured within a Docker container.**

#### 1.10.3.2 Jetson Orin Nano/Orin NX Version

<img src="../_static/media/chapter_1\section_1/media/image283.png" style="width:600px" />

The robot uses a Jetson Orin Nano as its ROS controller, consisting of a Jetson Orin Nano core board and an expansion board. The core board is a compact yet powerful computer capable of running mainstream deep learning frameworks, providing sufficient computing power for most AI projects.

The expansion board exposes the LED indicators and control buttons, enabling network status to be monitored through LED signals and network modes to be switched from a mobile device. It also provides GPIO and I2C ports for hardware expansion.

**The core board runs Ubuntu 22.04 and comes preinstalled with the ROS 2 Humble environment.**

#### 1.10.3.3 Raspberry Pi 5 Version

<img src="../_static/media/chapter_1\section_1/media/image284.png" style="width:600px" />

### 1.10.4 Aurora Depth Camera

<img src="../_static/media/chapter_1\section_1/media/image285.png" style="width:600px" />

The robot is equipped with a Deptrum depth camera.

The Aurora930, part of the Deptrum Aurora 930 series, uses 3D structured light technology to capture the three-dimensional structure of objects and spaces. By fusing RGB images from the color camera with depth data, it provides efficient and convenient 3D perception capabilities.

Its specifications are shown in the diagram and table below.

**Module Specifications**

|         Item          |           Specification           |
| :-------------------: | :-------------------------------: |
|     Overall size      |       76.5 x 20.7 x 21.8 mm       |
|       Baseline        |               40 mm               |
|       Interface       |       USB 2.0 wafer socket        |
|    Depth accuracy     |            8 mm @ 1 m             |
|    Depth precision    |     3 mm @ 0.5 m, 7 mm @ 1 m      |
|   Working distance    |           15 to 300 cm            |
| Operating temperature |           -10°C to 55°C           |
|  Operating humidity   |     0% to 95%, non-condensing     |
|     Ambient light     |          3 to 80,000 lux          |
|     Power supply      |           5V ±10%, 1.5A           |
|   Power consumption   | Average power consumption < 1.6 W |
|        Safety         |       Class 1 laser safety        |

**Image Performance**

|               Item               |         Specification          |
| :------------------------------: | :----------------------------: |
|        Depth data format         |             Raw 16             |
|  Depth resolution / frame rate   | 640 x 400 at 12 fps, 74° x 51° |
|        Color data format         |              NV12              |
|  Color resolution / frame rate   | 640 x 400 at 12 fps, 74° x 51° |
|       Infrared data format       |             Raw 8              |
| Infrared resolution / frame rate | 640 x 400 at 12 fps, 74° x 51° |

**Firmware and System Compatibility**

|         Item         |         Specification         |
| :------------------: | :---------------------------: |
|   Firmware upgrade   |  Supports USB online upgrade  |
|   Warm start delay   |            <300 ms            |
| System compatibility | Linux / ARMv8 / ROS / Windows |



### 1.10.5 LiDAR

LiDAR is a sensor that uses laser beams to obtain precise positional information. It has a wide range of applications in robotics, including obstacle avoidance, object following, SLAM mapping, and navigation.

The robot is equipped with a COIN-D6 LiDAR.

<img src="../_static/media/chapter_1\section_1/media/image37.png" style="width:400px" />

|         Item          |          Specification          |         Item          |            Specification            |
| :-: | :-: | :-: | :-: |
| LiDAR model | COIN-D6 LiDAR | Measurement principle | TOF distance measurement |
| Recommended scenarios | Indoor and outdoor applications | Supply voltage | 5V |
| Scanning range | 360 degrees | Measurement radius | Black object: 12m |
| Communication rate | 230400bps | Sampling frequency | 4000 times/s |
| Scanning frequency | 9.5~10.5Hz, default 10Hz | Angular resolution | 0.9 degrees |
| Supply current | Typical 240mA | Output interface | Standard asynchronous serial (UART) |
| Operating temperature | -10 to 50 degrees | Distance accuracy | <= 4mm [0.1m~2m), <= 15mm [2m~12m] |
| Product size | 52.7mm x 45.2mm x 34.4mm |  |  |




Wiring Instructions:

<img src="../_static/media/chapter_1\section_1/media/image38.png" style="width:400px" />

| Pin | Signal | Attribute | Description |
| :-: | :-: | :-: | :-: |
| 1 | Tx | Serial data transmit | Tx, device transmit, 0V~3.3V |
| 2 | Rx | Serial data receive | Rx, device receive, 0V~3.3V |
| 3 | GND | Power input negative | GND, 0V |
| 4 | VCC | Power input positive | DC 5V, 4.5V~5.5V |



## 1.11 ROS Introduction

The core system of the ROS robot consists of two main parts. The first is chassis control, driven by the STM32 controller, responsible for robot motion control and sensor data acquisition. The second is ROS control, centered on the ROS main controller, which runs the ROS system and associated functional algorithms.

### 1.11.1 ROS Controller Hardware Connection

The standard connection setup requires a power cable and a USB serial cable. Communication between the STM32 controller and the ROS controller is established via the onboard USB serial interface. The ROS controller can be powered directly through the STM32 power output port. The connection diagram is shown below:

<img src="../_static/media/chapter_1\section_1/media/image10.png" style="width:600px" />

### 1.11.2 ROS Serial Communication Overview

Serial communication is one of the most common input and output methods in microcontroller development and robotic systems. In this robot, data exchange between the Jetson Nano and the STM32 controller is carried out via a serial interface.

To ensure smooth communication between software tools and hardware devices, a standardized RRC protocol based on hexadecimal data transmission is adopted. This protocol serves as the foundation for communication and programming between the upper and lower controllers in this and subsequent products.

For detailed information on the communication protocol and its parsing, refer to the document RRC Communication Protocol with the Host Computer located under [4. Hardware Materials \\ 1 STM32 Controller Resources](https://drive.google.com/drive/folders/1ITrr0a_EAi3al5hOrIHmCNFlZunjZ0LM?usp=sharing).



## 1.12 System Software Architecture

### 1.12.1 Introduction to File Directory Structure

Open the ROS2 terminal, enter the command line, type `ls`, and press **Enter** to view the files in the **home** directory.

```
ls
```

The table below describes the folders.

| Directory name | Function |
|----------|----------|
| wifi_manager | Wi-Fi management tool |
| software | Software directory |
| ros2_ws | Workspace containing all feature functions |
| third_party | Directory for function packages such as YOLOv5 training models |
| Music | Music files |
| Pictures | Image storage directory |
| Public | Custom directory |
| Templates | Template directory for custom use |
| Videos | Video storage directory |

Enter the command `cd ros2_ws/` and press **Enter** to access the robot workspace directory, then type `ls` to list the files and folders inside.

```
cd ros2_ws/
ls
```

The table below describes the folders.

| **Directory/File name** | **Description** |
|----------|----------|
| build | Build space that stores cache information generated during compilation |
| command | Stores command files for implementing different functions |
| install | Stores compiled target files and executable files |
| log | Directory for log files |
| src | Source code directory for function packages |

Enter the command `cd ros2_ws/src` and press **Enter** to access the robot workspace directory, then type `ls` to list the files and folders inside.

```
cd ros2_ws/src
ls
```

The table below describes the folders.

| **Directory name** | **Type description** | **Function** |
|----------|----------|----------|
| app | App feature directory | Gesture control, LiDAR, line following, and more |
| interfaces | Communication interface directory | ROS message communication and service communication files |
| slam | Mapping feature directory | Map generation and map saving |
| bringup | System service directory | Starts the app, wireless controller control, and other functions |
| multi | Multi-robot feature directory | Multi-robot mapping, multi-robot navigation, and more |
| large_models_examples | Large model feature directory | Large model features |
| large_models | Large model communication interface directory | ROS message communication and service communication files |
| calibration | Calibration parameter directory | IMU, linear velocity, angular velocity calibration, and more |
| navigation | Navigation feature directory | Waypoint publishing, RViz navigation, and more |
| xf_mic_asr_offline | Voice control feature directory | Voice control features |
| xf_mic_asr_offline_msgs | Voice control communication interface directory | ROS service communication files |
| driver | Driver directory | Kinematics and communication between the main board and the STM32 |
| peripherals | External device configuration directory | Includes different LiDAR models, wireless controller control, keyboard control, and more |
| example | Example feature directory | Creative features such as gesture control, posture control, and color tracking |
| simulations | Simulation file directory | Gazebo, URDF, and more |

* **Introduction to Function File Directory**

The following uses **ros2_ws/src/app** as an example to explain the feature files.

1. Enter the directory where the feature files are stored. Two folders can be found: **launch** and **app**.

```
cd ros2_ws/src/app
```

<img src="../_static/media/chapter_1\section_1/media/image303.png"  />

2. The **launch** folder contains the launch files, and the **app** contains the feature source code.

```bash
cd launch
```

```bash
ls
```

<img src="../_static/media/chapter_1\section_1/media/image304.png"  />

```bash
cd app
```

```bash
ls
```

<img src="../_static/media/chapter_1\section_1/media/image305.png"  />


## 1.13 Image Flashing

### 1.13.1 Preparation

* **Hardware:**

For Jetson Nano and Raspberry Pi 5 versions, prepare an SD card with a capacity suitable for the image. In the example shown on the left, a 64GB SD card is used. Also, prepare a card reader and a computer, with Windows 10 recommended as the operating system.

<img src="../_static/media/chapter_1\section_1/media/image286.png" style="width:300px" class="common_img"/>

<img src="../_static/media/chapter_1\section_1/media/image287.png" style="width:300px" class="common_img"/>

For Jetson Orin Nano and Jetson Orin NX versions, prepare an SSD with a capacity suitable for the image, an SSD writer that needs to be prepared separately, and a computer. Windows 10 is recommended as the operating system.

<img src="../_static/media/chapter_1\section_1/media/image288.png" class="common_img"  />

* **Software:**

A disk initialization tool called **DiskGenius.exe** and an image flashing tool called **Win32DiskImager**. This section uses these two tools as examples.

> [!NOTE]
> 
> * **Before flashing the image, the disk initialization tool provided in [2. Software\\3. Image Flashing Tools\\1. Disk Formatting Tool](https://drive.google.com/drive/folders/1uvSJQj1So71ljqpwb4xJuxOnK7N1OYPZ?usp=sharing) can be used to delete all extra partitions on the SD card.**
> 
> * **After the image is written, the system may display multiple partitions as separate drives. Do not format them. Simply cancel the prompts.**

<img src="../_static/media/chapter_1\section_1/media/image289.png" class="common_img"  />

### 1.13.2 SD Card / SSD Formatting

> [!NOTE]
>
> **If the SD card or SSD is blank, formatting is not required.**

1) Remove the SD card from Jetson Nano, Jetson Orin Nano, or Raspberry Pi 5. For SSDs, remove them from the Jetson Orin Nano or the Jetson Orin NX.

**Jetson Nano / Jetson Orin Nano**

<img src="../_static/media/chapter_1\section_1/media/image290.png" style="width:600px" class="common_img"  />

**Raspberry Pi 5**

<img src="../_static/media/chapter_1\section_1/media/image291.png" style="width:600px" class="common_img"  />

Jetson Orin NX

<img src="../_static/media/chapter_1\section_1/media/image292.png" style="width:600px" class="common_img"  />

2) In the provided materials, locate the compressed package under **[2. Softwares \\ 3. Image Flashing Tools \\ 1. Disk Formatting Tool](https://drive.google.com/drive/folders/1uvSJQj1So71ljqpwb4xJuxOnK7N1OYPZ?usp=sharing)**, extract it, and open **DiskGenius.exe** to format the SD card or SSD. Make sure the correct drive is selected. Choosing the wrong drive may result in formatting the computer's hard disk.
3) After the SD card or SSD is inserted into the computer, an additional drive letter appears besides the existing computer drives.

<img src="../_static/media/chapter_1\section_1/media/image293.png" style="width:600px" class="common_img"  />

4) Right-click the SD card drive and select **Delete All Partitions**.

<img src="../_static/media/chapter_1\section_1/media/image294.png" style="width:600px" class="common_img"  />

5) As shown in the figure below:

<img src="../_static/media/chapter_1\section_1/media/image295.png" style="width:600px" class="common_img"  />

6) Once deleted, create a new partition so the computer can recognize the SD card. Confirm any pop-up prompts.

<img src="../_static/media/chapter_1\section_1/media/image296.png" style="width:600px" class="common_img"  />

7) Then click **Save All**.

<img src="../_static/media/chapter_1\section_1/media/image297.png" style="width:600px" class="common_img"  />

8) When complete, the SD card or SSD is formatted successfully.

<img src="../_static/media/chapter_1\section_1/media/image298.png" style="width:600px" class="common_img"  />

### 1.13.3 Image Flashing

1) Open Win32DiskImager and click the icon <img src="../_static/media/chapter_1\section_1/media/image299.png" class="common_img"  style="width:70px;display:inline;vertical-align:middle;"/> to select the image file. Download and extract it beforehand, and the image shown in the examples is for reference only. In the **Device** field, select the SD card or SSD drive letter, then click **Write** to start flashing the image.

<img src="../_static/media/chapter_1\section_1/media/image300.png" style="width:600px" class="common_img"  />

> [!NOTE]
>
> **The image file path must contain only English characters.**

2) If prompted with the figure below, click **Yes** to continue.

<img src="../_static/media/chapter_1\section_1/media/image301.png" style="width:600px" class="common_img"  />

3) Once **Write Successful** appears, the image has been written successfully. If an error occurs, disable the firewall software, reinsert the SD card or SSD, and repeat the steps in this section.

<img src="../_static/media/chapter_1\section_1/media/image302.png" style="width:200px" class="common_img"  />

> [!NOTE]
>
> **Once the image has been successfully written, any prompt asking to format the partition can be ignored.**

4) After the flashing is complete, reinsert the SD card or SSD into the controller. Power it on, wait a few moments, and the system will boot successfully.



