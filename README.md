## Ground-to-Top View Transformation using Computer Vision

This project introduces a novel approach to generate a top-view perspective from a ground-recorded video from Chauburgi, Lahore leveraging advanced computer vision techniques. The pipeline integrates several key algorithms including ground segmentation, object detection, homography computation, image stitching, and top-view generation. We also provide our own dataset for this purpose. Below, we outline the key algorithms employed in this project:

#### You can access our dataset at:
https://pern-my.sharepoint.com/:v:/g/personal/24100233_lums_edu_pk/ER8tUMO8NmhLtocTwMC5IO4BwNqkbOwWjPJ6SYZOZVcXjg?e=Vi6DWo


## Important Algorithms
**1) YOLOP (You Only Look Once for Roads and Objects with Homography)**

YOLOP is a custom adaptation of the YOLO (You Only Look Once) object detection model, tailored specifically for road segmentation and object detection. By employing a pre-trained YOLO model from the hustvl repository, we obtain masks for different objects within the video frames. Subsequently, these masks are converted into binary representations, where roads are designated as 1 and other elements as 0. This binary mask is then overlaid onto each frame of the video, resulting in an enhanced video with segmented roads highlighted.

**2) Homography Matrix Transformation**

The homography matrix transformation technique is utilized to compute the homography between a ground-level image and its corresponding top-view representation. Through this process, we establish a geometric mapping that allows for the transformation of perspectives from a ground-level view to a top-down view. This transformation is crucial for generating accurate top-view representations of the scenes captured in the input videos.

**3) SuperGlue Image Matching**

SuperGlue is employed for image matching and feature correspondence across different frames and viewpoints. This algorithm aids in identifying key points and establishing correspondences between images, facilitating the accurate alignment and stitching of multiple frames. By leveraging SuperGlue, we ensure seamless transitions and accurate composition in the final top-view video output.

## Important Files
**road_segmentation.ipynb** This file makes use of hustvl/yolop for segmenting roads from everything else.

**topViewGenerator.ipynb** This file helps in calculating homography of ground image to top image.

**Panorama_Stiching.ipynb** This file makes use of superglue to generate top view from ground view.
