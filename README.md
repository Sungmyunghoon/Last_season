# 이번 학기 총정리

## ROS2와 Jetson Nano를 사용하여 터틀봇의 라인트레이서 기능 및 라이다 센서를 활용한 자율주행 기능을 구현

![image](https://github.com/Sungmyunghoon/Last_season/assets/112747810/eaaf1fc2-992b-4833-9312-541758f00c40)

## 1. Jetson 보드의 Publisher노드에서 토픽전송
## 2. WSL2의 Subscriber 노드에서 에러계산
## 3. WSL2의 Publisher노드에서 에러토픽을 전송
## 4. Jetson보드의 Subscriber 노드에서 양쪽바퀴의 속도명령을 계산하여 다이내믹셀로전송

# Line Tracer
## Opencv를 사용하여 영상을 캡처하여 토픽 전송

## WSL2의 Subscriber 노드에서 영상처리하여 에러 계산
