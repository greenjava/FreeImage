include_directories ( ${FREEIMAGE_INCLUDE_DIRS} )
link_directories ( ${FREEIMAGE_LIBRARY_DIRS} )


set(TEST_SOURCES
MainTestSuite.cpp 
testHeaderOnly.cpp 
testChannels.cpp 
testImageType.cpp 
testJPEG.cpp 
testMemIO.cpp 
testMPage.cpp 
testMPageMemory.cpp 
testMPageStream.cpp 
testPlugins.cpp 
testThumbnail.cpp 
testTools.cpp 
TestSuite.h 
)

add_definitions(${FREEIMAGE_BUILD_FLAGS})

add_executable(Test ${TEST_SOURCES} )
target_link_libraries( Test ${FREEIMAGE_LIBRARIES} )
