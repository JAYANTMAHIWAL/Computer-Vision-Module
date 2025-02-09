# Computer Vision Assignment: Camera Calibration Module

## Introduction
This assignment focuses on camera calibration, where we estimate intrinsic and extrinsic parameters of a camera using a checkerboard pattern. Calibration helps correct distortions and map 3D world points to 2D image points, which is crucial for applications like 3D reconstruction and robotics.

## Requirements
### Software
- Python 3.x
- OpenCV (`cv2`)
- NumPy
- Matplotlib (optional for visualization)

### Hardware
- A camera (webcam or external)
- Checkerboard pattern (e.g., 6x9 grid)

## Files
- `calibration.py`: Script to perform camera calibration
- `checkerboard_images/`: Folder containing checkerboard images
- `calibration_results.npz`: Saved calibration parameters
- `undistort.py`: Script to correct distorted images using calibration data

## Steps for Calibration
1. **Capture Checkerboard Images**: Take multiple images from different angles.
2. **Detect and Refine Corners**: Use OpenCV functions to find and refine checkerboard corners.
3. **Estimate Camera Parameters**: Compute intrinsic and extrinsic matrices, and distortion coefficients.
4. **Save Calibration Data**: Store results for future undistortion.

## Usage
### Running Calibration
```sh
python calibration.py --images checkerboard_images/
```

### Undistorting an Image
```sh
python undistort.py --image test_image.jpg --calibration calibration_results.npz
```

## Output
- **Camera Matrix (Intrinsic Parameters)**: Focal lengths and optical center.
- **Distortion Coefficients**: Corrects radial and tangential distortions.
- **Rotation & Translation Vectors**: Defines camera pose relative to the checkerboard.

## References
- OpenCV Documentation: https://docs.opencv.org/
- Camera Calibration Tutorial: https://docs.opencv.org/4.x/dc/dbb/tutorial_py_calibration.html
