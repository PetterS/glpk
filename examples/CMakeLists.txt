
add_executable(glpsol glpsol.c)
target_link_libraries(glpsol glpk)

add_test(NAME glpsol_version COMMAND glpsol --version)
add_test(NAME glpsol_alloy COMMAND glpsol --mps ${CMAKE_CURRENT_SOURCE_DIR}/alloy.mps)
add_test(NAME glpsol_furnace COMMAND glpsol --mps ${CMAKE_CURRENT_SOURCE_DIR}/furnace.mps)
add_test(NAME glpsol_icecream COMMAND glpsol --mps ${CMAKE_CURRENT_SOURCE_DIR}/icecream.mps)
add_test(NAME glpsol_murtagh COMMAND glpsol --mps ${CMAKE_CURRENT_SOURCE_DIR}/murtagh.mps)
add_test(NAME glpsol_plan COMMAND glpsol --mps ${CMAKE_CURRENT_SOURCE_DIR}/plan.mps)
add_test(NAME glpsol_samp1 COMMAND glpsol --mps ${CMAKE_CURRENT_SOURCE_DIR}/samp1.mps)
add_test(NAME glpsol_samp2 COMMAND glpsol --mps ${CMAKE_CURRENT_SOURCE_DIR}/samp2.mps)
