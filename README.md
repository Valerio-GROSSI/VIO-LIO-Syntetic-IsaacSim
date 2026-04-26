# VIO-LIO-Syntetic-IsaacSim*

This mini-project is still a work in progress.

It aims to test Visual-Inertial Odometry (VIO) and LiDAR-Inertial Odometry (LIO) models on synthetic sensor data generated with Isaac Sim.

The tested models are Open-VINS and LIO-SAM.

<br>

## Testing OpenVINS on synthetic monocular camera and IMU data generated in Isaac Sim

<br>

<p align="center">
<b>OpenVINS on Isaac Sim Data – RViz Visualization
</b><br>
<img src="open_vins_isaacsim_syntetic_data.gif" width="80%">
</p>

<br>

<p align="center">
<b>Isaac Sim Configuration
</b><br>
<img src="isaacsim_vio_config.png" width="80%">
</p>

<br>

## Testing LIO-SAM on synthetic LiDAR-inertial data generated in Isaac Sim

<br>

LIO-SAM expects LiDAR point clouds in a specific format, including additional fields such as "intensity" and "ring" (laser channel index). 
However, the RTX LiDAR in Isaac Sim typically outputs a simpler PointCloud2 message that does not fully match these requirements. 

As a result, a preprocessing step is needed to adapt the simulated data to LIO-SAM’s expected input format. This involves augmenting the point cloud with the missing fields by computing or extracting them. 
This adaptation is currently a work in progress.

<br>

<p align="center">
<b>Isaac Sim Configuration
</b><br>
<img src="isaacsim_lio_config.png" width="80%">
</p>
