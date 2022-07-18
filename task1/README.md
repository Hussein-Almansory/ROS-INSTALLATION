# ROS-INSTALLATION

### First: Download and install VM VirtualBox in your PC.
### Second: Download and install ubuntu 20.04.4 64bit.
### Third: Open "Terminal" from ubuntu and follow these steps 

'' ROS Noetic installation instructions '' 

### 1- Setup your sources.list

```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

### 2- Set up your keys

``` 
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```

### 3- Installation

First, make sure your Debian package index is up-to-date:
```
sudo apt update
```
Now pick how much of ROS you would like to install.

**Desktop-Full Install:** (Recommended) : Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages

```
sudo apt install ros-noetic-desktop-full
```
**Desktop Install:** Everything in ROS-Base plus tools like rqt and rviz
```
sudo apt install ros-noetic-desktop
```
**ROS-Base:** (Bare Bones) ROS packaging, build, and communication libraries. No GUI tools.
```
sudo apt install ros-noetic-ros-base
```

There are even more packages available in ROS. You can always install a specific package directly.
```
sudo apt install ros-noetic-PACKAGE
```
e.g.
```
sudo apt install ros-noetic-slam-gmapping
```

### Environment setup
```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```
if you use zsh 

```
echo "source /opt/ros/noetic/setup.zsh" >> ~/.zshrc
source ~/.zshrc
```

### Dependencies for building packages

```
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```

### Initialize rosdep

```
sudo apt install python3-rosdep
```

With the following, you can initialize rosdep.

```
sudo rosdep init
rosdep update
```

### Finally: in the terminal we write this command to make sure **ROS** was downloaded successfully
```
roscore
```


![roscore](https://user-images.githubusercontent.com/65435678/178351120-4f438cc2-4dcc-4b7a-b462-64600a6b10a0.jpeg)









































