cmake_minimum_required(VERSION 3.16.4)
project(openCV_QRCode)

set(CMAKE_CXX_STANDARD 14)

#find_library(OpenCV)
find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

#set(CMAKE_CXX_STANDARD 11)

add_executable(openCV_QRCode_t  QRCode_Locate.cpp)
target_link_libraries(openCV_QRCode_t ${OpenCV_LIBS} ${raspicam_CV_LIBS} ${ZBAR_LIBRARIES} zbar)

add_executable(qr_test_q  QR_test_q.cpp)
target_link_libraries(qr_test_q ${OpenCV_LIBS} ${raspicam_CV_LIBS} ${ZBAR_LIBRARIES} zbar)

add_executable(road_line  road_line.cpp)
target_link_libraries(road_line ${OpenCV_LIBS} )