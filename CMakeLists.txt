cmake_minimum_required(VERSION 2.8)
project(TL)

find_package(catkin REQUIRED
        )

catkin_package(
        INCLUDE_DIRS Test
        LIBRARIES TL
)
include_directories(Test ${catkin_INCLUDE_DIRS})

set( SOURCES
	Test/share.cpp
)
add_library (TL SHARED ${SOURCES})
target_link_libraries(TL ${catkin_LIBRARIES})
