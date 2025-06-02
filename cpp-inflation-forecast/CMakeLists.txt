cmake_minimum_required(VERSION 3.10)
project(cpp_inflation_forecast)

set(CMAKE_CXX_STANDARD 17)

find_package(QuantLib REQUIRED)
find_package(matplot++ REQUIRED)

include_directories(/usr/local/include/DataFrame)

add_executable(main src/main.cpp)
target_link_libraries(main QuantLib::QuantLib matplot::matplot)
