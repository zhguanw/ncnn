NCNN = /home/henry/projects/cnn/ncnn/

OPENCV = /home/henry/projects/cnn/ncnn/opencv-2.4.13

INCPATH =       -I${NCNN}/build/install/include \
                -I${OPENCV}/modules/objdetect/include \
                -I${OPENCV}/modules/highgui/include \
                -I${OPENCV}/modules/imgproc/include \
                -I${OPENCV}/modules/core/include

LIBS = -lopencv_core -lopencv_highgui -lopencv_imgproc  -fopenmp -pthread

LIBPATH = -L${OPENCV}/build/lib

# ALL TARGET
all: squeezenet

squeezenet:squeezenet.cpp
	$(CXX) $(INCPATH) $(LIBPATH) $^ ${NCNN}/build/install/lib/libncnn.a $(LIBS) -o $@
