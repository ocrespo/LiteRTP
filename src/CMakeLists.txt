


set (LITERTP_HEADERS ${LITERTP_HEADERS} liteRTP.h ) #Add .h here, just for standalone headers

set (LITERTP_SOURCES ${LITERTP_SOURCES} liteRTP.cpp)


add_library(LiteRTP STATIC ${LITERTP_SOURCES} ${LITERTP_HEADERS})
 
install (TARGETS LiteRTP DESTINATION release/lib)
install (FILES ${LITERTP_HEADERS} DESTINATION release/include)

################## TESTS ############################
#add_executable(serverTest ServerTest.cpp)
#target_link_libraries(serverTest ConnectionManager)
#target_include_directories(serverTest PUBLIC release/include)

#add_executable(clientTest ClientTest.cpp)
#target_link_libraries(clientTest ConnectionManager)
#target_include_directories(clientTest PUBLIC release/include)



