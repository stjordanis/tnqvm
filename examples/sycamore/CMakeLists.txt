include_directories(${XACC_INCLUDE_DIRS})
include_directories(${PROJECT_SOURCE_DIR})

add_executable(sycamore_circ_contract_flops sycamore_circ_contract_flops.cpp)
target_link_libraries(sycamore_circ_contract_flops PRIVATE xacc::xacc tnqvm)
target_compile_definitions(sycamore_circ_contract_flops PRIVATE RESOURCE_DIR="${CMAKE_CURRENT_SOURCE_DIR}/resources")

add_executable(sycamore_circ_mps sycamore_circ_mps.cpp)
target_link_libraries(sycamore_circ_mps PRIVATE xacc::xacc tnqvm)
target_compile_definitions(sycamore_circ_mps PRIVATE RESOURCE_DIR="${CMAKE_CURRENT_SOURCE_DIR}/resources")

