cmake_minimum_required(VERSION 3.15)
project(HE_kv_store_server)

set(CMAKE_CXX_STANDARD 17)

include_directories(/usr/local/include)
add_executable(HE_kv_store_server main.cpp hash.hpp)
target_link_libraries(HE_kv_store_server /usr/local/lib/librpc.a)
find_package(SEAL 3.6 REQUIRED)
target_link_libraries(HE_kv_store_server SEAL::seal)