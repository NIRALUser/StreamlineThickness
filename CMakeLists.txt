PROJECT(ktools)
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

FIND_PACKAGE(VTK REQUIRED)
INCLUDE(${VTK_USE_FILE})

ADD_EXECUTABLE(StreamThickness klaplace.cpp klaplace.h kgeometry.cpp kgeometry.h kstreamtracer.cpp kstreamtracer.h kvolume.cpp kvolume.h kvtkutils.cpp kvtkutils.h vtkio.cpp vtkio.h piOptions.h piOptions.cpp csv_parser.cpp csv_parser.h SimpleOpt.h)
TARGET_LINK_LIBRARIES(StreamThickness ${VTK_LIBRARIES})
