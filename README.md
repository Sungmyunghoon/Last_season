# 이번 학기 총정리

## ROS2와 Jetson Nano를 사용하여 터틀봇의 라인트레이서 기능 및 라이다 센서를 활용한 자율주행 기능을 구현

![image](https://github.com/Sungmyunghoon/Last_season/assets/112747810/eaaf1fc2-992b-4833-9312-541758f00c40)

## 1. Jetson 보드의 Publisher노드에서 토픽전송
## 2. WSL2의 Subscriber 노드에서 에러계산
## 3. WSL2의 Publisher노드에서 에러토픽을 전송
## 4. Jetson보드의 Subscriber 노드에서 양쪽바퀴의 속도명령을 계산하여 다이내믹셀로전송


# Line Tracer
### Opencv라이브러리를 사용하여 영상을 캡처하여 토픽 전송
https://github.com/Sungmyunghoon/ros2_linetracer_Jetson/blob/main/src/pub.cpp

### WSL2의 Subscriber 노드에서 영상처리하여 에러 계산 및 에러토픽을 전송
https://github.com/Sungmyunghoon/ros2_linetracer_WSL/blob/main/src/psub_wsl.cpp

### Dxl로 에러값을 전송
https://github.com/Sungmyunghoon/ros2_linetracer_Jetson/blob/main/src/sub.cpp


# lidarDrive

### sllidar_node를 실행하여 라이다를 동작 및 토픽 전송
https://github.com/Sungmyunghoon/sllidar_ros2

### wsl에서 라이다가 측정한 거리를 sub하고 만들어져 있는 dxl에 topic 전송
https://github.com/Sungmyunghoon/ros2_lidardrive

### 에러값을 사용하여 dxl실행

### Ros2의 장점
### - 한 개의 publisher는 동일한 메시지를 여러 구독자에게 동시에 전송할 수 있다.
### - 각 subscriber는 독립적으로 동작하기 때문에, 특정 subscriber에서 발생하는 문제가 다른 subscriber에 영향을 미치지 않는다.
### - 여러 subscriber가 병렬로 데이터를 처리할 수 있어, 전체 시스템의 처리 성능을 향상시킨다.
### - 동일한 publisher의 데이터를 여러 용도로 활용할 수 있다, 따라서 코드를 재사용하는 데 유리하다.
