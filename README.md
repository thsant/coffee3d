# Coffee3D - 3-D reconstructions of coffee trees using multiple-view stereo

**english**

This is a set of images, odometry data, and 3-D point clouds for 8
coffee tree specimens. Images were captured by a Logitech C920
camera. Odometry data was produced using monocular visual SLAM by
Mur-Artal & Tardos' [ORB-SLAM2](https://github.com/raulmur/ORB_SLAM2)
SLAM system under [3dmcap](https://github.com/thsant/3dmcap).

Two multiple-view stereo systems were employed in 3-D reconstruction:
Furukawa & Ponce [PMVS](https://www.di.ens.fr/pmvs/) and Schöenberger's
[COLMAP](https://colmap.github.io).

## Files

For each plant and date you will find:

* `3dmc_calibration_matrix.txt`: internal camera parameters for
  Logitech C920.

* `3dmc_odometry.txt`: odometry data, ie, external camera parameter
  for each image

* `pmvs/models/3dmc-3dmodel.cfg.ply`: point cloud produced by PMVS

* `colmap/dense/fused.ply`: point cloud produced by COLMAP
