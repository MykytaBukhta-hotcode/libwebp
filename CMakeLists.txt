cmake_minimum_required(VERSION 3.16)
set(PROJECT_NAME libwebp)
project(${PROJECT_NAME})

add_library(${PROJECT_NAME} INTERFACE)

target_include_directories(
  ${PROJECT_NAME}
  INTERFACE
  ${CMAKE_CURRENT_SOURCE_DIR}/include
)

target_link_directories(${PROJECT_NAME} INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(
  ${PROJECT_NAME} 
  INTERFACE 
  ${CMAKE_CURRENT_SOURCE_DIR}/lib/libwebp.lib 
  ${CMAKE_CURRENT_SOURCE_DIR}/lib/libwebpdemux.lib 
  ${CMAKE_CURRENT_SOURCE_DIR}/lib/libwebpmux.lib
)
