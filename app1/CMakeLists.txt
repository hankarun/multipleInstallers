add_executable(app1 main.cpp)

OPTION(BUILD_PACK1 "Used to build package1" OFF)

include(${CMAKE_SOURCE_DIR}/cmake/CMakeLists.txt)


if (BUILD_PACK1)
    install(TARGETS app1 DESTINATION app1)
    set(CPACK_COMPONENTS_ALL app1)
    set(CPACK_PACKAGE_FILE_NAME "App1")
    create_cpack_config(CPackConfig-App1.cmake)
endif()

include(${CMAKE_SOURCE_DIR}/cmake/CMakeLists.txt)

