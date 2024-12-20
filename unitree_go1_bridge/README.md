# unitree_go1_bridge

Currently, we are targeting **Unitree Go1 EDU** model.
Possibly, in the future, it may correspond to work on models other than Unitree Go1 EDU.

# Setup Unitree Go1

ROS node is running on Raspberry Pi when Unitree Go1 EDU is purchased.
Therefore, if you send a command to the internal controller, it will compete with other nodes sending command values.

To avoid this problem, I have the following settings.

```bash
$ ssh pi@192.168.123.161
$ mv .config/autostart/unitree.desktop .config/autostart/unitree.desktop.backup
$ sudo reboot
```

In order to disable all autostarts, WIFI hotspots are also disabled.

# Build dependencies

See [package.xml](package.xml) for basic dependencies.

Please install and use the following repositories for [unitree_legged_sdk](https://github.com/unitreerobotics/unitree_legged_sdk) library.

[NaokiTakahashi12/unitree_legged_sdk](https://github.com/NaokiTakahashi12/unitree_legged_sdk)

This is created because there is no library installation and no configuration for CMake.
