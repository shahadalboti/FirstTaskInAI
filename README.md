# FirstTaskInAI
this repository is about how to install Ubuntu in VB and to setup ros2 in ubuntu.

#### Table of Contents  
* [About](https://github.com/shahadalboti/FirstTaskInAI#about-this-repository-)  
* Task1:
  
   -[Task1.1: Install ubuntu in VB ](https://github.com/shahadalboti/FirstTaskInAI#task1-) 
  
   -[Task1.2: Install Ros2 in ubuntu  ](https://github.com/shahadalboti/FirstTaskInAI#task1-) 
  
* [Resources](https://github.com/shahadalboti/FirstTaskInAI#resources-)  

## About this repository ❓:
this repository is about how to install Ubuntu in VB and to setup ros2 in ubuntu.

## Task1 :
## Task 1.1:
   how to install Ubuntu in VB

### steps to download Ubuntu in VB🖥️


Step 1: Open VirtualBox and click on the New button.
 

Step 2: Give a name to your Virtual Machine and select the location for it to install.

 
Step 3: Assign RAM size to your Virtual Machine.
 
 
Step 4: Create a Virtual Hard disk for the machine to store files.


Step 5: Select the type of Hard disk. Using VDI type is recommended.
 
 
Step 6: Either of the physical storage type can be selected. Using Dynamically allocated disk is by default recommended.
 
 
Step 7: Select disk size and provide the destination folder to install.

 
Step 8: After the Disk creation is done, boot the Virtual Machine and begin installing Ubuntu.

 
Step 9: If the installation disk is not automatically detected. Browse the file location and select the ISO file for Ubuntu.
 
 
Step 10: Proceed with the installation file and wait for further options.
 
 
Step 11: Click on the Install Ubuntu option, this might look different for other Ubuntu versions.
 
 
Step 12: Select Keyboard layout, if the defaults are compatible, just click on the continue button and proceed.
 
 
Step 13: Select installation type. By default, it is set to Normal installation, which is recommended, but it can also be changed to Minimal installation if there   is no need for all Ubuntu features.
 
 
Step 14: Click on the Install Now button and carry on with the installation. Do not get worried with the Erase disk option, it will only be effective inside the virtual machine, other system files outside the VirtualBox remain intact.
 
 
Step 15: Click on the continue button, and proceed with writing changes on the disk.
 
 
Step 16: Select your location to set the Time Zone.

 
Step 17: Choose a name for your computer and set a password to secure login info.

 
Step 18: Wait for the installation process to complete.

 
Step 19: Once the installation process is over, reboot your Virtual Machine.

 
Step 20: You’re finished with the installation process. Now you can use Ubuntu along with the Windows.





## Task 1.2: algorthim to download and install Ros2




1-Add the ROS 2 apt repository

  You will need to add the ROS 2 apt repositories to your system. To do so, first authorize our GPG key with apt 
    
      sudo apt update && sudo apt install curl gnupg2 lsb-release
    
      sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key  -o /usr/share/keyrings/ros-archive-keyring.gpg
 
 And then add the repository to your sources list:
  
            echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(lsb_release - cs) main"sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null


2-Downloading ROS 2
 
 
      mkdir -p ~/ros2_dashing

      cd ~/ros2_dashingtar xf ~/Downloads/ros2-dashing-linux-x86_64.tar.bz2


3-Installing and initializing rosdep
 
 
     sudo apt update
 
     sudo rosdep init
  
     rosdep update
 
 
4-Installing the missing dependencies
 
 
        rosdep install --from-paths ~/ros2_dashing/ros2-linux/share --ignore-src --rosdistro dashing -y --skip-keys "console_bridge fastcdr fastrtps libopensplice67         libopensplice69 osrf_testing_tools_cpp poco_vendor rmw_connext_cpp rosidl_typesupport_connext_c rosidl_typesupport_connext_cpp rti-connext-dds- 5.3.1tinyxml_vendortinyxml2_vendor urdfdom urdfdom_headers"


5-Environment setup
   
   
       ~/ros2_dashing/ros2-linux/setup.bash


6-create your own workspace and packages, and learn ROS 2 core concepts.





## Resources 📜:
- https://www.w3schools.com
-https://www.virtualbox.org/wiki/Downloads
-https://installati.one/ubuntu/22.04/ros-desktop/

