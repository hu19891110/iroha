
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/test_bin)

SET(AERON_PATH  "${PROJECT_SOURCE_DIR}/core/vendor/Aeron")

include_directories(
  ${AERON_PATH}/aeron-client/src/main/cpp
)
link_directories(
  ${AERON_PATH}/cppbuild/Release/lib
)

# Aeron connection Test
add_executable(connection_test
  connection_with_aeron_test.cpp
)
target_link_libraries(connecti on_test
  connection_with_aeron
  aeron_client
  pthread
)
