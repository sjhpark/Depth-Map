# Depth-Map
Depth map (disparity map) of stereo vision images

![left_images_compressed](https://user-images.githubusercontent.com/83327791/216810695-f6107eef-dbdd-4948-bf83-0a7224d810fe.gif)
![depth_maps](https://user-images.githubusercontent.com/83327791/216809049-2ad7d0da-6a2a-4e4c-8ccc-f56f23034872.gif)
---

### Dataset
Dataset from Kitti Stereo 2015: https://www.cvlibs.net/datasets/kitti/eval_scene_flow.php?benchmark=stereo

The datasets used here are already rectified.

#### Reference:
- https://www.baeldung.com/cs/disparity-map-stereo-vision
- https://johnwlambert.github.io/stereo/#first-algorithm

#### Disparity Map
- Stereo vision has 2 visions (e.g. one from left and another from right).
- Image captured from the left camera and the image captured from the right camera have disparity (difference in the position).
- Further the object is from the camera, smaller the disparity. Closer the object is from the camera, greater the disparity.
- Disparity map makes the pixels brighter if there is more disparity. --> In other words, brighter pixels for closer objects. --> Disparity map captures the objects' relative positions.

#### Algorithm Steps
- Image Rectification: Usually, you first simplify the problem by rectifying the stereo images. After rectification, the corresponding points will lie on the same horizontal line. --> Reduces the 2D stere0 correspondence problem to a 1D problem --> There will be disparity along only one axis (x-axis in this case).
- Block (Window; Kernel) Matching
- SAD (Sum of Absolute Differences): The SAD is the sum of the absolute differences between the corresponding pixels in the two images.

#### Result Example
![image](https://user-images.githubusercontent.com/83327791/216760919-b167ffbc-5942-4c83-afa5-8f6cb9ab8599.png)
