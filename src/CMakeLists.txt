# Properties->C/C++->General->Additional Include Directories
include_directories ("../deps")

file (GLOB SOURCES
      "*.cpp"
      "*.cc")

# Create named folders for the sources within the project
source_group("src" FILES ${SOURCES})

# build
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
add_executable(${PROJECT_NAME} ${SOURCES})
