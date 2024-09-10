cmake_minimum_required(VERSION 3.10)
project(MyProject VERSION 1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add your source files here
set(SOURCES 
    main.cpp
    main2.cpp
    main3.cpp
)

# Create the executable
add_executable(MyExecutable ${SOURCES})

# Enforce strict compiler flags to treat warnings as errors
if (CMAKE_CXX_COMPILER_ID MATCHES "GNU|Clang")
    target_compile_options(MyExecutable PRIVATE -Wall -Wextra -Werror)
elseif (CMAKE_CXX_COMPILER_ID MATCHES "MSVC")
    target_compile_options(MyExecutable PRIVATE /W4 /WX)
endif()
