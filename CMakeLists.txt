# 指定CMake的最低版本要求
cmake_minimum_required(VERSION 3.5.0)

# 设置项目名称
project(CppVSCodeProj)

# 设置 C++ 标准
set(CMAKE_CXX_STANDARD 17)

# 查找源文件（cpp）和头文件（h）
file(GLOB SOURCES "src/*.cpp")
# file(GLOB HEADERS "include/*.h")

# # 如果你希望包含头文件目录，可以使用 include_directories 或 target_include_directories
include_directories(${CMAKE_SOURCE_DIR}/include)

# 配置生成可执行文件
add_executable(main ${SOURCES})

# # 链接库
# target_link_libraries(MyExecutable PRIVATE SomeLibrary)