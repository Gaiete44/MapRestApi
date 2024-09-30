cmake_minimum_required(VERSION 3.10)
project(MapRestApi)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(CURL REQUIRED)
find_package(nlohmann_json 3.11.2 REQUIRED)

add_executable(MapRestApi main.cpp MapRestApi.cpp)

target_include_directories(MapRestApi PRIVATE ${CURL_INCLUDE_DIRS})
target_link_libraries(MapRestApi PRIVATE ${CURL_LIBRARIES} nlohmann_json::nlohmann_json)