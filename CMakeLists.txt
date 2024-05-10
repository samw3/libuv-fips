#
# project: libuv-fips
#
cmake_minimum_required(VERSION 3.21)
project(libuv-fips)
# include the fips main cmake file
get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")

include_directories(libuv/include)
fips_setup()
fips_begin_lib()
add_subdirectory(libuv)
fips_end_lib()
# add_subdirectory(src/...)
