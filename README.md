## Point Cloud Registration
'''Based on Huang et al, 2017 (1)'''

 * Input: two point clouds
 * For each point cloud:
    * Supervoxel Clustering following Papon et al, 2013 (2)
    * For each cluster:
      * Compute the ESF descriptors of the cluster following Wohlkinger & Vincze, 2011 (3)
    * For each edge between adjacent clusters:
      * Compute angle_x, angle_y, angle_z, distance following Huang et al, 2017 (1)
 * Match the two resulting graphs
 * Apply RANSAC algorithm to the point clouds
 * Apply ICP algorithm to the point clouds


 References:
 (1) "A Systematic Approach for Cross-Source Point Cloud Registration by Preserving Macro and Micro Structures", Huang, Zhang, Fan, Wu, Yuan, IEEE Transactions on Image Processing, 2017
 (2) "Voxel Cloud Connectivity Segmentation - Supervoxels for Point Clouds", Papon, Abramov, Schoeler, Wörgötter, IEEE Conference on Computer Vision and Pattern Recognition, 2013
 (3) "Ensemble of Shape Functions for 3D Object Classification", Wohlkinger, Vincze, IEEE International Conference on Robotics and Biomimetics, 2011
