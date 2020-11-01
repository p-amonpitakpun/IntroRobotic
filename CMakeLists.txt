cmake_minimum_required (VERSION 3.0.0)
project (IntroRobotic)

set (CMAKE_GENERATOR_PLATFORM x64)
include_directories (opencv/build/install/include)
link_directories (opencv/build/install/x64/vc16/lib)

add_executable (IntroRobotic ${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp)

set_property (DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} PROPERTY VS_STARTUP_PROJECT IntroRobotic)
file(GLOB LIB_FILES RELATIVE opencv/build/install/x64/vc16/lib/ *.lib)
target_link_libraries (IntroRobotic PRIVATE opencv_calib3d450.lib
								PRIVATE opencv_calib3d450d.lib
								PRIVATE opencv_core450.lib
								PRIVATE opencv_core450d.lib
								PRIVATE opencv_dnn450.lib
								PRIVATE opencv_dnn450d.lib
								PRIVATE opencv_features2d450.lib
								PRIVATE opencv_features2d450d.lib
								PRIVATE opencv_flann450.lib
								PRIVATE opencv_flann450d.lib
								PRIVATE opencv_gapi450.lib
								PRIVATE opencv_gapi450d.lib
								PRIVATE opencv_highgui450.lib
								PRIVATE opencv_highgui450d.lib
								PRIVATE opencv_imgcodecs450.lib
								PRIVATE opencv_imgcodecs450d.lib
								PRIVATE opencv_imgproc450.lib
								PRIVATE opencv_imgproc450d.lib
								PRIVATE opencv_ml450.lib
								PRIVATE opencv_ml450d.lib
								PRIVATE opencv_objdetect450.lib
								PRIVATE opencv_objdetect450d.lib
								PRIVATE opencv_photo450.lib
								PRIVATE opencv_photo450d.lib
								PRIVATE opencv_stitching450.lib
								PRIVATE opencv_stitching450d.lib
								PRIVATE opencv_video450.lib
								PRIVATE opencv_video450d.lib
								PRIVATE opencv_videoio450.lib
								PRIVATE opencv_videoio450d.lib)