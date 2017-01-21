# grasp_pipeline
A pipeline for robot grasping



### Installation

Dependencies for moveit and gazebo

```bash
sudo apt-get install \
    ros-indigo-gazebo-ros \
    ros-indigo-eigen-conversions \
    ros-indigo-object-recognition-msgs \
    ros-indigo-roslint\
    ros-indigo-moveit-core \
    ros-indigo-shape-tools
```

Dependencies for graspit

```bash
sudo apt-get install \
    libsoqt4-dev \
    libcoin80-dev \
    libqt4-dev \
    libblas-dev \
    liblapack-dev \
    libqhull-dev

sudo apt-get install \
    ros-indigo-eigen-conversions \
    ros-indigo-household-objects-database \
    ros-indigo-household-objects-database-msgs \
    ros-indigo-manipulation-msgs \
    ros-indigo-object-recognition-msgs \
    ros-indigo-roslint
```

---

Install wstool

```bash
sudo apt-get install python-wstool
```

Create a workspace

```bash
mkdir -p ~/ws_graspit
cd ~/ws_graspit
```

Initialize workspace from rosinstall file

```bash
wstool init src https://raw.githubusercontent.com/hashb/grasp_pipeline/master/grasp_pipeline.rosinstall
```

Merge the rosinstall file

```bash
wstool merge -t src https://raw.githubusercontent.com/hashb/grasp_pipeline/master/grasp_pipeline.rosinstall
```

Update the workspace

```bash
wstool update -t src
```

---

Build the workspace

```bash
catkin build
```