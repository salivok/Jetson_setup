# Jetson_setup

Librealsense building From Source
Ubuntu 14.04/16.04/18.04
Ensure apt-get is up to date
  sudo apt-get update && sudo apt-get upgrade
Install python3.6
  sudo apt-get install python python-dev or sudo apt-get install python3 python3-dev
Run the top level CMake command with the following additional flag -DBUILD_PYTHON_BINDINGS:bool=true:
  git clone
  mkdir build
  cd build
  cmake ../ -DBUILD_PYTHON_BINDINGS:bool=true -DPYTHON_EXECUTABLE=[full path to the exact python executable} (python3)
  make -j4
  sudo make install
update your PYTHONPATH environment variable to add the path to the pyrealsense library
export PYTHONPATH=$PYTHONPATH:/usr/local/lib
Alternatively, copy the build output (librealsense2.so and pyrealsense2.so) next to your script.
Note: Python 3 module filenames may contain additional information, e.g. pyrealsense2.cpython-35m-arm-linux-gnueabihf.so)
