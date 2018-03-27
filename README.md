# jetson-tx2-tips
A collection of solutions I found while trying to make stuff run on the TX2

#TensorFlow
## Pre-built wheels for Python 2.7
- [1.3 and 1.5](https://github.com/JesperChristensen89/TensorFlow-Jetson-TX2)

#OpenCV
## Installation
Follow tips from JetsonHacks [here](https://github.com/jetsonhacks/buildOpenCVTX2)

# Movidius SDK
## Installation
If you are building the ncsdk with opencv, make sure to install opencv AFTER the ncsdk. Otherwise you will be prompted to uninstall it everytime.

# PyTorch
## Building PyTorch
In pytorch/aten/src/ATen/CMakeLists.txt, change the line "LIST(APPEND CPU_CAPABILITY_FLAGS "-O3" "-O3 -mavx" "-O3 -mavx2")" to "LIST(APPEND CPU_CAPABILITY_FLAGS "-O3" "-O3" "-O3")" as neither of the flags will work.
