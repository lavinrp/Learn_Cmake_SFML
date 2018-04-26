# CMakeList.txt : CMake project for Cmake_SFML2, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

# Add source to this project's executable.
add_executable (CmakeSFML2 "Cmake_SFML2.cpp" "Cmake_SFML2.h")

find_package(SFML 2 REQUIRED network audio graphics window system)
if(SFML_FOUND)
  include_directories(${SFML_INCLUDE_DIR})
  target_link_libraries(CmakeSFML2 ${SFML_LIBRARIES} ${SFML_DEPENDENCIES})
endif()

# TODO: Add tests and install targets if needed.
