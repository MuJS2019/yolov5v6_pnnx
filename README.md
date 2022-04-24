# yolov5v6_pnnx
使用ncnn调用pnnx转化的yolov5s6.pt，修改于ncnn源项目example中的yolov5_pnnx.cpp，在代码中修改引用的权值文件即可调用任何6.0版本权值。  
需要在本系统中构建构建好ncnn后将ncnn/build/install中的include、lib复制到项目目录中新建的ncnn文件夹中，或在<https://github.com/Tencent/ncnn/releases>中下载好对应系统的预编译库放在项目目录中并且改写cmake中的ncnn目录。  
需要opencv环境，作者构建于arch linux，贴出对应的linux命令： 
```bash
sudo pacman -Syu hdf5 vtk opencv
```
构建完环境后，只需要在项目文件夹里：
```bash
mkdir build & cd build
cmake ..
make
```
就可以在build文件夹里生成可运行的文件了，将对应的权值文件放到同目录下即可调用，调用样例为：
```bash
./yolov5v6_ncnn 0.jpg
```
