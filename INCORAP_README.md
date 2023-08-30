# yolov5 - INCORAP

Installation:

1) Follow normal yolov5 installation instructions
2) Download INCORAP smartfactory truck weights:

https://drive.google.com/file/d/1bbBkHheDWCiUt-DWqk9ZGgUNApEtRUZq/view?usp=drive_link

place them on the root folder (.../yolov5/yolov5mbest.pt)

3) test

Place objects in front of your camera, then run:

    roscore
    python3 detect.py --weights yolov5mbest.pt --conf-thres 0.8 --source 0

    replace --source 0 with the number of your camera, e.g.

    --source 4

    rosrun rqt_image_view rqt_image_view
    rostopic echo /detections
