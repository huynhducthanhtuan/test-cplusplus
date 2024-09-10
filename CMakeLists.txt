# Minimum version of CMake required
cmake_minimum_required(VERSION 3.10)

# Project name and version
project(test-cplusplus VERSION 1.0)

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add source files
# If your sources are located in a different folder (e.g., src/), adjust the path accordingly
set(SOURCES
    src/main.cpp
)

# Add an executable target (replace 'MyExecutable' with the desired executable name)
add_executable(MyExecutable ${SOURCES})

# Include directories if you have header files in a separate folder
# include_directories(include)

# Link libraries if needed (e.g., pthread, etc.)
# target_link_libraries(MyExecutable pthread)
