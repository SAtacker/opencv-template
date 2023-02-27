cmake_minimum_required(VERSION 2.8)
PROJECT(sample-opencv)

find_package(OpenCV REQUIRED)

set(NAME_SRC
    src/main.cpp
)

# set(NAME_HEADERS
#     include/header.h
# )

# INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}/include)
add_executable(${PROJECT_NAME} ${NAME_SRC})

target_include_directories(${PROJECT_NAME} 
    PRIVATE ${OpenCV_INCLUDE_DIRS}
)
target_link_libraries(${PROJECT_NAME} 
    PRIVATE ${OpenCV_LIBS}
)