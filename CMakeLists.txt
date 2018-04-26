# CMakeList.txt : Top-level CMake project file, do global configuration
# and include sub-projects here.
#
cmake_minimum_required (VERSION 3.8)

project ("Cmake_SFML2")

# project wide output directories
set(BIN_DIR ${CMAKE_CURRENT_SOURCE_DIR}/bin)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${BIN_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${BIN_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${BIN_DIR}/bin)

# SFML install path
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "E:/Programing/Programing/Cpp/SFML/SFML-2.4.1/cmake/Modules")
set(SFML_ROOT "E:/Programing/Programing/Cpp/SFML/SFML-2.4.1")

message("sfml lib: " $ENV{SFML_LIB})

if(DEFINED ENV{SFML_LIB})
	message("real env" $ENV{SFML_LIB})

else()

	message("not found real")

endif()

if(DEFINED ENV{fake_env})
	message("fake env" $env{fake_env})
else()
	message("not found fake")
endif()



# Include sub-projects.
add_subdirectory ("Cmake_SFML2")
