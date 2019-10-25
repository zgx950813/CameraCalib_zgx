# CameraCalib_zgx
使用CMake生成sln执行档
Where is the source code: ./
Where to build the binaries: ./build

"Configure" twice
"Generate"
"Open Project"

打开解决方案资源管理器
卸载并移除ALL_BUILD和ZERO_CHECK
然后在上方的"项目"->"属性"->"调试"->"命令参数"输入../input/in_VID5.xml

在input中确认各个文件的属性
在main.cpp中确认对于高分辨率照片的缩放比例scale_x和scale_y
无误后，点击运行
