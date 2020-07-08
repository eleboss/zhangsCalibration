cmake_minimum_required (VERSION 2.6)
project (zhangCla)


SET( CMAKE_CXX_FLAGS "-std=c++11 ")

find_package( OpenCV )
include_directories( ${OpenCV_INCLUDE_DIRS} )


find_package( PkgConfig )
pkg_check_modules( EIGEN3 REQUIRED eigen3 )
include_directories( ${EIGEN3_INCLUDE_DIRS} )

add_executable(zcal zhangsCalbration.cpp)


target_link_libraries(zcal ${OpenCV_LIBS} )
target_link_libraries (zcal ${EIGEN3_INCLUDE_DIRS})

