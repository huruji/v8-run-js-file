cmake_minimum_required(VERSION 3.20)
project(demo)

set(CMAKE_CXX_STANDARD 14)
SET(ROOT_DIR ${CMAKE_SOURCE_DIR})
SET(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR})

include_directories(deps/v8/include)
include_directories(deps/v8)

link_directories(${ROOT_DIR}/deps/v8/out/x64.release/obj)
link_libraries(v8_monolith)



add_executable(demo main.cpp)
