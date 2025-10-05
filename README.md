# Incorporating 3D Gaussian Splatting for Monocular Vision Spacecraft Pose Estimation and Tracking




## Abstract 
Precise spacecraft pose estimation and tracking is a key technology for space exploration and on-orbit servicing. However, 1) existing methods typically rel y on refined depth information or prior 3D reference models, this dependency renders these methods inapplicable to non-cooperative targets; 2) the complex and dynamic space environment  could dramatically degrade the accuracy of pose estimation. To tackle these challenges, we propose a spacecraft pose estimation and tracking network incorporating 3D Gaussian splatting, termed 3DGS-SPN, that aims to implement instance detection, 3D model reconstruction, and 6DoF pose estimation and tracking for non-cooperative or unknown targets using only RGB images from a monocular vision sensor. 


## Environment Setup 

conda env create -f environment.yaml

conda activate 3DGS-SPN   

## Download the datasets

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
