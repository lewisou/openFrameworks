cmake_minimum_required(VERSION 3.10.2)

project(openFrameworks VERSION 0.11.0)

#set(CMAKE_CXX_STANDARD 14)
#set(CMAKE_CXX_STANDARD_REQUIRED True)

set(source_list1 
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/3d/ofCamera.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/3d/ofNode.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/3d/of3dPrimitives.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/3d/ofEasyCam.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/3d/of3dUtils.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/video/ofVideoPlayer.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/video/ofVideoGrabber.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/types/ofRectangle.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/types/ofBaseTypes.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/types/ofParameterGroup.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/types/ofColor.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/types/ofParameter.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/app/ofBaseApp.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/app/ofMainLoop.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/app/ofAppNoWindow.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/app/ofAppRunner.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/utils/ofThread.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/utils/ofFpsCounter.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/utils/ofURLFileLoader.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/utils/ofSystemUtils.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/utils/ofLog.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/utils/ofTimer.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/utils/ofFileUtils.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/utils/ofMatrixStack.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/utils/ofUtils.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/utils/ofXml.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/math/ofVec2f.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/math/ofVec4f.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/math/ofMath.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/math/ofMatrix3x3.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/math/ofQuaternion.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/math/ofMatrix4x4.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/gl/ofMaterial.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/gl/ofFbo.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/gl/ofShader.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/gl/ofBufferObject.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/gl/ofVboMesh.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/gl/ofGLUtils.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/gl/ofLight.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/gl/ofGLProgrammableRenderer.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/gl/ofVbo.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/gl/ofTexture.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/gl/ofGLRenderer.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/communication/ofSerial.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/communication/ofArduino.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/events/ofEvents.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/graphics/ofBitmapFont.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/graphics/ofTessellator.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/graphics/ofGraphics.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/graphics/ofGraphicsBaseTypes.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/graphics/ofRendererCollection.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/graphics/ofPath.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/graphics/ofPixels.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/graphics/of3dGraphics.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/graphics/ofTrueTypeFont.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/graphics/ofImage.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/sound/ofSoundStream.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/sound/ofSoundBaseTypes.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/sound/ofSoundPlayer.cpp"
"${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/sound/ofSoundBuffer.cpp"
# "../../../openFrameworks/sound/ofOpenALSoundPlayer.cpp"
# "../../../openFrameworks/sound/ofRtAudioSoundStream.cpp"
# "../../../openFrameworks/graphics/ofCairoRenderer.cpp"
# "../../../openFrameworks/app/ofAppGLFWWindow.cpp"
# "../../../openFrameworks/app/ofAppGlutWindow.cpp"
# "../../../openFrameworks/app/ofAppEGLWindow.cpp"
# "../../../openFrameworks/video/ofGstVideoGrabber.cpp"
# "../../../openFrameworks/video/ofDirectShowGrabber.cpp"
# "../../../openFrameworks/video/ofDirectShowPlayer.cpp"
# "../../../openFrameworks/video/ofGstUtils.cpp"
# "../../../openFrameworks/video/ofQuickTimePlayer.cpp"
# "../../../openFrameworks/video/ofQtUtils.cpp"
# "../../../openFrameworks/video/ofQuickTimeGrabber.cpp"
# "../../../openFrameworks/video/ofGstVideoPlayer.cpp"
# "../../../openFrameworks/sound/ofFmodSoundPlayer.cpp"

)

file(GLOB_RECURSE source_list2 "${CMAKE_CURRENT_SOURCE_DIR}/../../../../addons/ofxAndroid/*.cpp")
file(GLOB_RECURSE source_list3 "${CMAKE_CURRENT_SOURCE_DIR}/../../../../addons/ofxGui/*.cpp")
file(GLOB_RECURSE source_list4 "${CMAKE_CURRENT_SOURCE_DIR}/../../../../addons/ofxNetwork/*.cpp")
file(GLOB_RECURSE source_list5 "${CMAKE_CURRENT_SOURCE_DIR}/../../../../addons/ofxAccelerometer/*.cpp")
file(GLOB_RECURSE source_list6 "${CMAKE_CURRENT_SOURCE_DIR}/../../../../addons/ofxXmlSettings/*.cpp")

set(lib_list 
${CMAKE_CURRENT_SOURCE_DIR}/../../../freetype/lib/android/${ANDROID_ABI}/libfreetype.a
${CMAKE_CURRENT_SOURCE_DIR}/../../../boost/lib/android/${ANDROID_ABI}/libboost_system.a
${CMAKE_CURRENT_SOURCE_DIR}/../../../boost/lib/android/${ANDROID_ABI}/libboost_filesystem.a
${CMAKE_CURRENT_SOURCE_DIR}/../../../curl/lib/android/${ANDROID_ABI}/libcurl.a
${CMAKE_CURRENT_SOURCE_DIR}/../../../tess2/lib/android/${ANDROID_ABI}/libtess2.a
${CMAKE_CURRENT_SOURCE_DIR}/../../../pugixml/lib/android/${ANDROID_ABI}/libpugixml.a
${CMAKE_CURRENT_SOURCE_DIR}/../../../openssl/lib/android/${ANDROID_ABI}/libcrypto.a
${CMAKE_CURRENT_SOURCE_DIR}/../../../openssl/lib/android/${ANDROID_ABI}/libssl.a
${CMAKE_CURRENT_SOURCE_DIR}/../../../FreeImage/lib/android/${ANDROID_ABI}/libfreeimage.a
${CMAKE_CURRENT_SOURCE_DIR}/../../../uriparser/lib/android/${ANDROID_ABI}
)

set(head_file_list 
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../FreeImage/include
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../curl/include
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../glm/include
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openssl/include
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../tess2/include
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../utf8/include
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../boost/include
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../freetype/include
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../freetype/include/freetype2
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../json/include
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../pugixml/include
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../uriparser/include
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/3d
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/app
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/communication
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/events
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/gl
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/graphics
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/math
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/sound
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/types
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/utils
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/video
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks/types
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../openFrameworks
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../../addons/ofxAndroid/src
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../../addons/ofxAccelerometer/src
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../../addons/ofxGui/src
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../../addons/ofxNetwork/src
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../../addons/ofxXmlSettings/src
            ${CMAKE_CURRENT_SOURCE_DIR}/../../../../addons/ofxXmlSettings/libs
            )

add_library(openFrameworks STATIC ${source_list1} ${source_list2} ${source_list3} ${source_list4} ${source_list5} ${source_list6})

target_link_libraries(openFrameworks PRIVATE
                        ${lib_list}
                        ${log-lib})

target_include_directories(openFrameworks PUBLIC ${head_file_list})

find_library(log-lib log)
#find_library(OpenSLES-lib OpenSLES)
#find_library(android-lib android)
#find_library(z-lib z)
#find_library(GLESv1_CM-lib GLESv1_CM)
#find_library(GLESv2-lib GLESv2)
