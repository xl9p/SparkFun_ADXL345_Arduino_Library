cmake_minimum_required(VERSION 3.13)

if(ESP_PLATFORM)
  file(GLOB_RECURSE SPARKFUN_ADXL345
    "src/*.*"
  )

  idf_component_register(
    SRCS ${SPARKFUN_ADXL345}
    INCLUDE_DIRS src
    REQUIRES arduino
  )

  return()
endif()
