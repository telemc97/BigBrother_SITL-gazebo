# BigBrother_SITL-gazebo

#### This is a 3D model of the BigBrother Quadcopter which can be found [here](https://github.com/telemc97/BigBrother).
It's goal is to be used with the PX4 Toolchain and Gazebo SITL Simulation.

![bigbrother-gazebo](https://user-images.githubusercontent.com/57395320/135770673-e39983aa-c4c0-48ac-a090-d5d7a7273c61.png)

## Installation instructions
The following instructions for installing a SITL gazebo model in PX4 Toolchain apply both on this model and every other custom one.
- Move the model folder (*bigbrother*) under **Tools/sitl_gazebo/models**.
- Move the airframe file (*9000_bigbrother*) under **PX4-Autopilot/ROMFS/px4fmu_common/init.d-posix/airframes** and **PX4-Autopilot/build/px4_sitl_default/etc/init.d-posix/airframes**.
- Add the airframe name (``` bigbrother ```) to **PX4-Autopilot/src/modules/simulation/simulator_mavlink/sitl_targets_gazebo-classic.cmake** under ``` models ```.
- (Optional) move launch file (*bigbrother.launch*) under **launch** folder.
- Start gazebo with ``` DONT_RUN=1 make px4_sitl gazebo_bigbrother ```
