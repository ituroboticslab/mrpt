#Build Instructions
- Check out the latest source from itulabs git repo

```
$ cd /where/you/want/to/install/mrtpt
$ git clone https://github.com/ituroboticslab/mrpt.git
```

- Install main dependencies. See [here](http://www.mrpt.org/Building_and_Installing_Instructions#23_Interesting_build_options) for further instructions.

```
$ sudo apt-get install build-essential pkg-config cmake \
   libwxgtk2.8-dev libftdi-dev freeglut3-dev \
   zlib1g-dev libusb-1.0-0-dev libudev-dev libfreenect-dev \
   libdc1394-22-dev libavformat-dev libswscale-dev \
   libassimp-dev libjpeg-dev libopencv-dev libgtest-dev \
   libeigen3-dev libsuitesparse-dev libpcap-dev
```

- Go to mrpt folder where you checkout the mrpt library

```
$ cmake-gui
```
where is the source code => /where/did/you/checkout/mrpt

where to build the binaries => mkdir /bin folder under /mrpt and point out here

if you want to see examples, select "BUILD_EXAMPLES"
if you want to integrate with matlab, select "BUILD_MATLAB" feel free to make your own changes. Example: 

![Example Configuration](http://s32.postimg.org/lweuv0zyd/cmake_gui1.png)


## Setup with QT

- Open QT. Select one of the examples or your own build CMakeLists.txt from "Open File or Project" option.

- Compile with the cmake argument that points out to your /bin folder under /mrpt:

```
 -DMRPT_DIR:PATH="/home/onur/SW/mrpt/bin" 
```
Example:

![cmake option in QT](http://s32.postimg.org/ky5dvcop1/qt_cmake.png)

Build & Run (Ctrl+B && Ctrl+R) the project.


If you have problems see the [FAQ](http://www.mrpt.org/tutorials/programming/first-steps/mrpt_faq/)  first.

