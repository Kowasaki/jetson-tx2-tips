# jetson-tx2-tips
A collection of solutions I found while trying to make stuff run on the TX2

# Movidius SDK
## Installation
If you are building the ncsdk with opencv, make sure to install opencv AFTER the ncsdk. Otherwise you will be prompted to uninstall it everytime.

# PyTorch
## Building PyTorch
In pytorch/aten/src/ATen/CMakeLists.txt, change the line "LIST(APPEND CPU_CAPABILITY_FLAGS "-O3" "-O3 -mavx" "-O3 -mavx2")" to "LIST(APPEND CPU_CAPABILITY_FLAGS "-O3" "-O3" "-O3")" as neither of the flags will work.
