# Incorporating 3D Gaussian Splatting for Monocular Vision Spacecraft Pose Estimation and Tracking


https://private-user-images.githubusercontent.com/116131194/499754319-fddee666-84b7-44c3-a63c-28da6671736a.mp4?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NjAwODQ1NDUsIm5iZiI6MTc2MDA4NDI0NSwicGF0aCI6Ii8xMTYxMzExOTQvNDk5NzU0MzE5LWZkZGVlNjY2LTg0YjctNDRjMy1hNjNjLTI4ZGE2NjcxNzM2YS5tcDQ_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUxMDEwJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MTAxMFQwODE3MjVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05MzFiNGEyYWRkMjQyZDg3ODA5ZDkyYjY0YzAwY2I2OThkYzg2Y2U4NTRiNDcyM2QxY2NiODc4OTQ4NWNhMDUzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.G4R958oUnLs36Oxb85EZIQdi0ZFfdm73Ba3wMh43Fwk



## Abstract 
Precise spacecraft pose estimation and tracking is a key technology for space exploration and on-orbit servicing. However, 1) existing methods typically rel y on refined depth information or prior 3D reference models, this dependency renders these methods inapplicable to non-cooperative targets; 2) the complex and dynamic space environment  could dramatically degrade the accuracy of pose estimation. To tackle these challenges, we propose a spacecraft pose estimation and tracking network incorporating 3D Gaussian splatting, termed 3DGS-SPN, that aims to implement instance detection, 3D model reconstruction, and 6DoF pose estimation and tracking for non-cooperative or unknown targets using only RGB images from a monocular vision sensor. 


## Environment Setup 

conda env create -f environment.yaml

conda activate 3DGS-SPN   

## Download the Datasets

### 1) Training Dataset:
#### MegaDepth and the dataset indices   

- [``MegaPose/gso_1M``](https://www.paris.inria.fr/archive_ylabbeprojectsdata/megapose/webdatasets/) 
- [``MegaPose/google_scanned_objects.zip``](https://www.paris.inria.fr/archive_ylabbeprojectsdata/megapose/tars/) 



### 2) Testing Dataset:
- [SPARK 2024: Datasets for Spacecraft Semantic Segmentation and Spacecraft Trajectory Estimation Dataset] https://https://cvi2.uni.lu/spark-2024-dataset/


## Data Preparation

Training dataset are organised under the ``dataspace`` directory, as below,

```
dataspace/
├── MegaPose/
│   ├── webdatasets/gso_1M
│   └── google_scanned_objects
...
```

Testing dataset are organised under the ``SPARK2024`` directory, as below,

```
SPARK2024/
├── RT509/
├── RT519/
├── RT529/
├── RT539/
├── RT549/
├── RT559/
├── RT569/
├── RT579/
├── RT589/
├── RT599/

```

## Evaluation

Evaluation on the subset of SPARK2024 (comparison with Mobile-URSONet, Gen6D, OnePose, OnePose++).

## Pose Tracking Visualization



## Training


      
## Acknowledgement
Our work are based on [3D Gaussian Splatting](https://github.com/graphdeco-inria/gaussian-splatting?tab=readme-ov-file) and [MegaPose](https://github.com/megapose6d/megapose6d), and we use their code. If you use the part of code related to data generation, testing and evaluation, you should cite these paper and follow their license.


## Citation
If you find this project useful, please cite:
```
@article{,
  title={Incorporating 3D Gaussian Splatting for Monocular Vision Spacecraft Pose Estimation and Tracking},
  author={Yuan Li, Dapeng Wu, Yaping Cui, Peng He, Yuan Zhang and Ruyan Wang},
  journal={Arxiv},
  year={2025}
}
```
