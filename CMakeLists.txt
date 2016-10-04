cmake_minimum_required(VERSION 3.3)

project(boost_rational)

add_library(boost_rational INTERFACE)

target_include_directories(boost_rational BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_rational DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::rational ALIAS boost_rational)
