# Keypoints, Descriptors and Matches in order to reconstruct corrupted images. 
Computer Vision course final project

The aim of this project was applying different combinations of features description algorithms and matching strategies in order to reconstruct a series of corrupted images, by trying to compute the correct relationship with their missing patches.

This was achieved, firstly, by testing several methods, such as SIFT, SURF and ORB, to separately calculate the keypoints and descriptors on both the corrupted images and their patches, and then use the obtained results to find eventual matches between them.

Once the various matches were computed, they were used to estimate the mapping parameters defining the relationship between images and their patches, assuming that images and patches were linked together by an affine transform, through the RANSAC algorithm.

Finally, I handled the found homography parameters to overlay the patches over the image, in order to fix the corrupted regions and reconstruct it.
All the steps and operations above-mentioned were carried out by exploiting the build-in methods of the C++ extension of OpenCV software library.
