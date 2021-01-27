cmake_minimum_required(VERSION "3.19.1")

project("HW")

add_executable("${PROJECT_NAME}" "main.cpp")

#install(TARGET "${PROJECT_NAME}" DESTINATION build)	#absolute path: ${CMAKE_INSTALL_PREFIX}/build
#install(FILES "main.cpp" DESTINATION source)		#absolute path: ${CMAKE_INSTALL_PREFIX}/source

enable_testing()
include(CTest)

add_test ("test1" "${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}")