# Landmark-Image-Matching

The notebook in this repository visualizes keypoints between images from two different viewpoints of the same location and calculates the fundamental matrix between the two images.

# Keypoint Matching

Keypoints are generated for image pairs using LoFTr and SIFT. A brute-force matcher is used on the SIFT-generated keypoints to find matches between image pairs. Then, LoFTr matches are filtered using the SIFT matches so that only the closest matches remain.

# Fundamental Matrix

To change the perspctive from one image to another, each point of the first image is multiplied by a fundamental matrix that transforms the point to it's corresponding match in the second image. Using the Kornia library, the generated matches are used to approximate the fundamental matrix for the image pair.
