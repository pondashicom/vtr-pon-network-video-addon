cmake_minimum_required(VERSION 3.25)
project(vtr_pon_network_video_addon VERSION 0.3.0 LANGUAGES CXX)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if(NOT WIN32 OR NOT CMAKE_SIZEOF_VOID_P EQUAL 8)
  message(FATAL_ERROR "This add-on supports Windows x64 only.")
endif()
set(VTRPON_NETWORK_VIDEO_SDK_DIR "" CACHE PATH "External NDI SDK directory")
if(NOT EXISTS "${VTRPON_NETWORK_VIDEO_SDK_DIR}/Include/Processing.NDI.Lib.h")
  message(FATAL_ERROR "Set VTRPON_NETWORK_VIDEO_SDK_DIR to the NDI SDK directory.")
endif()
add_library(vtr-pon-network-video-addon SHARED src/network_video_addon.cpp)
target_include_directories(vtr-pon-network-video-addon PRIVATE
  include "${VTRPON_NETWORK_VIDEO_SDK_DIR}/Include")
target_compile_definitions(vtr-pon-network-video-addon PRIVATE
  NOMINMAX WIN32_LEAN_AND_MEAN VTRPON_NETWORK_VIDEO_ADDON_BUILD)
if(MSVC)
  target_compile_options(vtr-pon-network-video-addon PRIVATE /utf-8)
endif()
set_target_properties(vtr-pon-network-video-addon PROPERTIES
  RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/network-video-addons")
install(TARGETS vtr-pon-network-video-addon RUNTIME DESTINATION network-video-addons)
