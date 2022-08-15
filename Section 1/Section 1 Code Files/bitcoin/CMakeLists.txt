set(CMAKE_CXX_STANDARD 17)
project(bitcoin)
cmake_minimum_required(VERSION 3.23)
# If necessary, use the RELATIVE flag, otherwise each source file may be listed
# with full pathname. RELATIVE may makes it easier to extract an executable name
# automatically.
#file( GLOB APP_SOURCES RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} *.cpp )
## file( GLOB APP_SOURCES ${CMAKE_SOURCE_DIR}/*.c )
## AUX_SOURCE_DIRECTORY(${CMAKE_CURRENT_SOURCE_DIR} APP_SOURCES)
#foreach( testsourcefile ${APP_SOURCES} )
#    # I used a simple string replace, to cut off .cpp.
#    string( REPLACE ".cpp" "" testname ${testsourcefile} )
#    add_executable( ${testname} ${testsourcefile} )
#
#    set_target_properties(${testname} PROPERTIES LINKER_LANGUAGE CXX)
#    if(OpenMP_CXX_FOUND)
#        target_link_libraries(${testname} OpenMP::OpenMP_CXX)
#    endif()
#    install(TARGETS ${testname} DESTINATION "bin/strings")
#
#endforeach( testsourcefile ${APP_SOURCES} )
#set(CURL_LIBRARY "-lcurl")
#find_package(CURL REQUIRED)
#add_executable(curl-demo convert.cpp)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -lcurl")
add_executable(bitcoin.cpp)
#include_directories(${CURL_INCLUDE_DIR})
target_include_directories(bitcoin PUBLIC curl)
#target_include_directories(bitcoin ${CURL_LIBRARY})
#add_library(${CMAKE_CURRENT_SOURCE_DIR})













