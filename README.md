This is the implementation of our paper: "Building Maps for Autonomous Navigation Using Sparse Visual SLAM Features" in IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), 2017. Our implementation is built on the top of the open-source stereo SLAM [ORB-SLAM2](https://github.com/raulmur/ORB_SLAM2). It runs in ROS （developed in version of indigo）. Eigen, OpenCV, and CGAL are needed. 



## 环境配置 依赖库安装

- CGAL lib  (mapping中的 triangulation用到)
sudo apt-get install libcgal-dev
sudo apt-get install libcgal-qt5-dev

- 修改g2o eigen库的错误
typedef Eigen::PermutationMatrix<Eigen::Dynamic, Eigen::Dynamic, SparseMatrix::StorageIndex> PermutationMatrix;


## 代码测试

The high resolution video of our submitted paper is: 
https://1drv.ms/v/s!ApzRxvwAxXqQmRtBPbu_Q27V5o4f
(720p is recommmanded)

To run this code, complie it with ROS in linux system, and type:

`rosrun light_mapping ros_stereo_kitti `

It will read the configuration file in the config folder, such as KITTI05.yaml. Please adjust it accordingly to your environment.

The source code is released under [GPLv3](https://www.gnu.org/licenses/gpl-3.0.html) license.
If you use our code, please cite our paper:

[1] Yonggen Ling and Shaojie Shen, "Building Maps for Autonomous Navigation Using Sparse Visual SLAM Features" in IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), 2017.
For more questions, please contact ylingaa at connect dot ust dot hk .
