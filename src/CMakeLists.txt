set(SRCS 
    ihex_parser.c
)

add_library(${PROJECT_NAME} ${SRCS})

install(TARGETS ${PROJECT_NAME} EXPORT ${PROJECT_NAME}Targets
        DESTINATION bin/${PROJECT_NAME} COMPONENT Runtime
        DESTINATION lib/${PROJECT_NAME} COMPONENT Runtime
        DESTINATION lib/${PROJECT_NAME} COMPONENT Development)

install(EXPORT ${PROJECT_NAME}Targets DESTINATION lib/${PROJECT_NAME})

