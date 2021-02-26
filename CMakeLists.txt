cmake_minimum_required(VERSION 3.14.3) 
project(LibA)

set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)

# Use this snippet *after* PROJECT(xxx):
message("before-------------------")
#IF(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)
message("CMAKE_SOURCE_DIR-------------------${CMAKE_SOURCE_DIR}")
#SET(CMAKE_INSTALL_PREFIX "c:/Program Files/${PROJECT_NAME}" CACHE PATH ${PROJECT_BINARY_DIR}  FORCE)
#ENDIF(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)
message("CMAKE_INSTALL_PREFIX-------------------${CMAKE_INSTALL_PREFIX}")

message("CMAKE_CURRENT_SOURCE_DIR-------------------${CMAKE_CURRENT_SOURCE_DIR}")

# ${PROJECT_SOURCE_DIR}/out/bla
# Include sub-projects.
#add_subdirectory ("LibraryA") 


add_library (LibA STATIC "Adder.cpp" "Adder.h")
 target_include_directories(LibA PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

#install(TARGETS LibA		LIBRARY DESTINATION ${PROJECT_NAME}/bin)


#add_executable(${PROJECT_NAME} main.cpp)