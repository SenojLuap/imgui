cmake_minimum_required(VERSION 3.17)
project(imgui LANGUAGES C CXX)

set(IMGUI_SOURCE_FILES imgui.cpp
                        imgui_draw.cpp
                        imgui_widgets.cpp)

add_library(imgui ${IMGUI_SOURCE_FILES})
target_include_directories(imgui PUBLIC ${CMAKE_SOURCE_DIR}/include)
target_precompile_headers(imgui PUBLIC <float.h>
                                       <stdarg.h>
                                       <stddef.h>
                                       <string.h>
                                       <assert.h>
                                       <ctype.h>
                                       <stdio.h>
                                       <stdint.h>)
