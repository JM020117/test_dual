笔记本的虚拟机的gazebo_ros2_control版本为0.4.4,所以在解析URDF文件为字符串时没有报错
但是换台电脑，gazebo_ros2_control版本为0.4.8，注释中包含特殊字符就会解析失败，TF错误
https://github.com/ros-controls/gazebo_ros2_control/issues/295

解决方法：
直接解析生成的URDF文件（而不是XACRO文件），删除URDF和SDRF文件中的全部注释
