INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR})
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/include)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/include/exports)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/include/imports)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/infra/log/)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/infra/utils/)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/infra/utils/digest)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/infra/utils/misc)

FILE (GLOB src_infra_log_SRCS
    ${PROJECT_SOURCE_DIR}/src/infra/log/*.c
)

ADD_LIBRARY (iot_log OBJECT
    ${src_infra_log_SRCS}
    ${EXTRA_C_SOURCES}
)

