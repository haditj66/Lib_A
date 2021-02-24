cmake_minimum_required(VERSION 3.17.3) 
project(LibA)


# Use this snippet *after* PROJECT(xxx):
message("before-------------------")
#IF(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)
message("asdasd-------------------${CMAKE_CURRENT_BINARY_DIR}")
#SET(CMAKE_INSTALL_PREFIX "c:/Program Files/${PROJECT_NAME}" CACHE PATH ${PROJECT_BINARY_DIR}  FORCE)
#ENDIF(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)
message("asdasd-------------------${CMAKE_INSTALL_PREFIX}")

# ${PROJECT_SOURCE_DIR}/out/bla
# Include sub-projects.
#add_subdirectory ("LibraryA") 

add_library (LibA SHARED "Adder.cpp" "Adder.h")
 

install(TARGETS LibA
		LIBRARY DESTINATION ${PROJECT_NAME}/bin)


#add_executable(${PROJECT_NAME} main.cpp)