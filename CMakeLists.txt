cmake_minimum_required(VERSION 3.7)

project(VulkanTest)

set (CMAKE_CXX_STANDARD 17)

include_directories(include)

find_package(glfw3 3.3 REQUIRED)
find_package(vulkan REQUIRED)


file(GLOB VulkanTest_SRC
    "src/*.cpp"
)

file(GLOB VulkanTest_INC
    "include/*.hpp"
)

add_executable(VulkanTest ${VulkanTest_SRC} ${VulkanTest_INC})
target_link_libraries(VulkanTest glfw Vulkan::Vulkan)
