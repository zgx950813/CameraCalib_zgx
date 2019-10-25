# 指定允许执行的最低 CMake 版本要求；不写会出警告
CMAKE_MINIMUM_REQUIRED( VERSION 2.8 )

# 指定解决方案的名称，通常对应于解决方案文件夹名
PROJECT( CameraCalib )

# 寻找OPENCV库
FIND_PACKAGE( OpenCV REQUIRED )

#添加源文件
AUX_SOURCE_DIRECTORY( src DIR_SRCS )

# 指定头文件的搜索路径，相当于指定gcc的-I参数
INCLUDE_DIRECTORIES( ${OpenCV_INCLUDE_DIRS} )

# 指定编译目标文件
ADD_EXECUTABLE( CameraCalib ${DIR_SRCS} )

# 添加链接库，相同于指定-l参数
TARGET_LINK_LIBRARIES( CameraCalib ${OpenCV_LIBS} )