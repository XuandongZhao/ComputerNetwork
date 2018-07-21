cmake_minimum_required(VERSION 3.10)
project(client)
project(server)
find_package (Threads)

add_executable(client client.c client.h)
add_executable(server server.c server.h)
target_link_libraries (client ${CMAKE_THREAD_LIBS_INIT})
target_link_libraries (server ${CMAKE_THREAD_LIBS_INIT})