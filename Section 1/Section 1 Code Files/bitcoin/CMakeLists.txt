set(CMAKE_CXX_STANDARD 17)
project(bitcoin)
cmake_minimum_required(VERSION 3.23)

#endforeach( testsourcefile ${APP_SOURCES} )
#set(CURL_LIBRARY "-lcurl")
#find_package(CURL REQUIRED)
#add_executable(curl-demo convert.cpp)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -lcurl")
add_executable(bitcoin bitcoin.cpp)
#include_directories(${CURL_INCLUDE_DIR})
target_include_directories(bitcoin PUBLIC curl)
#target_include_directories(bitcoin ${CURL_LIBRARY})
#add_library(${CMAKE_CURRENT_SOURCE_DIR})













