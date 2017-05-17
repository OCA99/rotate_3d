# Rotation along specific axes

## Animation

![](example/rotate_x_dx5.gif)
Rotate along X axis and translate 5 pixel along X axis

![](example/rotate_xz.gif)
Rotate along XZ axis

## Prerequisites

- Linux
- Python 2.7 with numpy
- OpenCV 2.4.9

## Usage

Change main function with ideal [arguments](#parameters)

```bash
python rotate_3d.py [name of the image] [degree to rotate]
```
e.g.,
Example of rotating an image along yz-axis from 0 to 360 degree
```python
- rotated_img = rotate_along_axis(img, phi = ang, dx = 5)
+ #rotated_img = rotate_along_axis(img, phi = ang, dx = 5)

- #rotated_img = rotate_along_axis(img, phi = ang, gamma = ang)
+ rotated_img = rotate_along_axis(img, phi = ang, gamma = ang)
```
Then
```bash
python rotate_3d.py 000001.jpg 360
```

## Parameters:

```python
rotate_along_axis(image, theta=0, phi=0, gamma=0, dx=0, dy=0, dz=0):
```
image     : the image that you want rotated
theta     : the rotation around the x axis
phi       : the rotation around the y axis
gamma     : the rotation around the z axis (basically a 2D rotation)
dx        : translation along the x axis
dy        : translation along the y axis
dz        : translation along the z axis (distance to the image)


## Acknowledgments

Code ported and modified from [jepson](http://jepsonsblog.blogspot.tw/2012/11/rotation-in-3d-using-opencvs.html) and [stackoverflow](http://stackoverflow.com/questions/17087446/how-to-calculate-perspective-transform-for-opencv-from-rotation-angles). Thanks for their excellent work!

## Author

Hou-Ning Hu / [@eborboihuc](https://eborboihuc.github.io/)
