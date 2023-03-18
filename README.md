# Localization, Pose Estimation and Visual Odometry Using Visual Tags
An USC Race On Project using AprilTags and OpenCV

**Fall 2020:**
- Developed ATDetector class that contains AprilTag visualization and pose estimation functions
- Wrote Markdown lessons on Fisheye Camera Calibration and Pose Esimation using AprilTags for future Race On Workshops
- Created Jupyter Notebook demo of ATDetector functionality and visualization of pose estimation accuracy (or lack there-of)

**Spring 2020: In Progress** 
- Using Kalman Filtering to improve localization accuracy by utilizing prior knowledge of vehicle model.
- Creating visual odometry scripts that use either AprilTags or ML-based feature point extraction (or maybe both!)


**When in competition you need to disable wifi on raspberry pi**
Modifying the Boot Config to Disable Wi-Fi
In this section, we will be modifying the Raspberry Pi’s boot configuration file.

By modifying this file, we will be able to disable the Wi-Fi connection during the start-up sequence.
  1. If you are editing this file on your Raspberry Pi, you can do so by running the following command.
     To edit this file, we will use nano as it is one of the easiest terminal-based text-editors to use.
     You can also edit this file when the SD card is plugged into another device. The file will be available on the partition that is named “boot“.

      sudo nano /boot/config.txt

   2. Within this section, find the following block of text.

      You can use the CTRL + W shortcut to search the text file when using nano.

       [all]

   3. Below this text, you need to add the following lines.

      This line tells the system that it needs to disable the Raspberry Pi’s Wi-Fi module.

        dtoverlay=disable-wifi

      You can also use this file to disable the Bluetooth module by adding the following line.

        dtoverlay=disable-bt

   4. You can now save the changes to the configuration file.


      If you are doing this on your Raspberry Pi, save the file by pressing CTRL + X, then Y, followed by the ENTER key.

   5. For this change to take effect, you will need to restart your Raspberry Pi.

      To safely reboot the device, you can use the following command.

        sudo reboot

