The functions xyz_data_read.m and xyz_write.m can be used to write point cloud information to an XYZ file through simply sending in the pointcloud matrix as well as the number of points. 


When writing or reading an .xyz file with normals, the point cloud variable must first run through the findPointNormals.m function and then the mergeVerticesAndNormals.m function before being inputted into the xyz_data_read.m function. Inside the function itself, the xyz() iterator must also be changed to 1:6 and three extra '%14f'must be added into the fprintf statement; look at the function for further explanation. 

The xyz files generated are primarily used in pointcloud denoising in the CGAL WLOP and Outlier Removal functions. 


