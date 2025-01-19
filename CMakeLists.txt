cmake_minimum_required(VERSION 3.30.5)
project(myproject)
# Variables are used with ${...}
# cmake .. builds your make file / configures make file.
# make builds your executable
add_executable(${PROJECT_NAME} main.c)
# Install will copy your executable to /usr/local/bin. Making it easy to run on linux.
# install makes a target (sudo cmake install) in your makefile.
# cmake -S .. (-S .. is telling cmake where to look for CMakeLists.txt)
install(TARGETS ${PROJECT_NAME} DESTINATION bin)

# Link local libraries
# target_link_libraries(${PROJECT_NAME} ...) ... is your lib name.
# This will find libraries in your local directory.(/usr/local/lib)

# SUBMODULES
# Inable git (git INIT)
# Create a .gitignor file on the top level.
# add_subdirectory(external/...) ... is your submodule name
