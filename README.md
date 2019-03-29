Detection darknet, yolo: car, bus, motobike, bike, truck, traffic light
Using: Cuda 10, CUDNN 7.4

Visual Studio 2017

1. run video and export file: 
darknet.exe detector demo data/coco.data cfg/yolov3.cfg yolov3.weights 1.MOV -out_filename result.avi

2. run after train
darknet.exe detector demo data/obj.data cfg/yolov3-tiny-obj.cfg yolov3-tiny-obj_last.weights 1.mp4 -out_filename result1.avi
3. run photo:
darknet.exe detect cfg/yolov3.cfg yolov3.weights *image path*
4. run webcam and export file
darknet.exe detector demo cfg/coco.data cfg/yolov3.cfg yolov3.weights
tren darknet 

darknet.exe detector train data/obj.data yolov3-tiny-obj.cfg yolov3-tiny.conv.15 15
darknet.exe detector train data/obj.data yolov3-tiny-obj.cfg yolov3-tiny.conv.15

darknet.exe detector demo data/obj.data yolov3-tiny-obj.cfg backup/yolov3-tiny-obj_last.weights 1.MOV -out_filename result1.avi
darknet.exe detector test data/obj.data yolov3-tiny-obj.cfg backup/yolov3-tiny-obj_1000.weights 1.jpg

darknet.exe partial cfg/yolov3-tiny.cfg yolov3-tiny.weights yolov3-tiny.conv.15 15
darknet.exe detector train data/obj.data yolov3-tiny-obj.cfg yolov3-tiny.conv.15

darknet.exe detector demo data/obj.data yolov3-tiny-obj.cfg backup/yolov3-tiny-obj_2000.weights 1.MOV -out_filename result1.avi
