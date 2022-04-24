# yolov5v6_pnnx
使用ncnn调用pnnx转化的yolov5s6.pt，适用于任何6.0版本权值。
需要在本系统中构建构建好ncnn后将ncnn/build/install中的include、lib复制到项目目录中新建的ncnn文件夹中，或在>>https://github.com/Tencent/ncnn/releases 中下载好对应系统的预编译库放在项目目录中并且改写cmake中的ncnn目录。
需要opencv环境，作者构建于arch linux，贴出对应的linux命令： 
        sudo pacman -Syu hdf5 vtk opencv

