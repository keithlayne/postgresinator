cmake_minimum_required (VERSION 3.0)
project (postgresinator)

# The version number.
set (postgresinator_VERSION_MAJOR 0)
set (postgresinator_VERSION_MINOR 1)
set (postgresinator_VERSION_PATCH 0)

# configure a header file to pass some of the CMake settings
# to the source code
configure_file (
  "${PROJECT_SOURCE_DIR}/include/postgresinator/config.h++.in"
  "${PROJECT_BINARY_DIR}/include/postgresinator/config.h++"
)

add_subdirectory(src)
add_subdirectory(test)
