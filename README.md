# Drone Image Samples

A collection of imagery from some cheap drone models, for EXIF
extraction and configuring processing pipelines.

## Camera Models

| Drone | Camera Model | File |
|--|--|--|
| DJI Mini 2 | FC7303 | [link](./images/dji-mini-2.jpeg)
| DJI Mini 4 Pro | FC8482 | [link](./images/dji-mini-4-pro.jpeg)
| DJI Mini 5 Pro | FC9313 | [link](./images/dji-mini-5-pro.jpeg)
| Potensic Atom 3 | ATOM 3 | [link](./images/potensic-atom-3.jpeg)

## OpenSfM Brown Distortion Figures

In order to add a camera model to
[OpenSfM's code](https://github.com/OpenSfM/OpenSfM/blob/master/opensfm/data/camera_calibration.yaml):

1. Capture several independent flights/scenes with the drone, using
   the same camera mode and image dimensions.
2. Process each dataset through OpenDroneMap/OpenSfM, allowing camera
   parameters to be optimized during bundle adjustment.
3. Extract the resulting optimized Brown camera parameters
   (`focal_x`, `focal_y`, `c_x`, `c_y`, `k1`, `k2`, `p1`, `p2`, `k3`).
4. Compare the results across reconstructions and use stable/representative
   values as the camera's initial calibration.
5. Validate those parameters on a separate dataset before adding them to
   OpenSfM's calibration database.
