#
#  CMakeLists.txt
#  rapidxml
#
#  Created by Dmitrii Torkhov <dmitriitorkhov@gmail.com> on 20.09.2021.
#  Copyright © 2021 Dmitrii Torkhov. All rights reserved.
#

cmake_minimum_required(VERSION 3.14 FATAL_ERROR)

project(rapidxml
        VERSION 1.13
        LANGUAGES CXX)

#

add_library(rapidxml INTERFACE)
add_library(rapidxml::rapidxml ALIAS rapidxml)

target_include_directories(rapidxml INTERFACE
        $<BUILD_INTERFACE:${CMAKE_CURRENT_LIST_DIR}/include>)