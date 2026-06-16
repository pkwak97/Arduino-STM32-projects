# Car Follow
초음파 센서 기반 PID 거리 추종 RC카 (Arduino Uno)

# project_outline
초음파 센서(YB-SG90)로 전방 장애물과의 거리를 측정하고,
PID 제어 알고리즘을 통해 목표 거리 30cm를 유지하며
장애물의 이동과 상관없이 자동으로 추종하는 RC카 입니다.

- 목표거리 30cm 유지
- 제어 방식 PID

# Composition of HardWare
|
부품
|
모델
|
-----
메인보드
----
Arduino Uno Board

모터 드라이버
----
PCA9685 PWM Driver

거리 센서 
----
YB-SG90 초음파 센서
구동방식 메카넘 휠 

# FSM
<img width="748" height="612" alt="Image" src="https://github.com/user-attachments/assets/f8630f74-4b60-4bd9-8301-f0a54ec40488" />



#PID 제어
----
- P : 현재 오차에 비례한 반응 I : 누적 오차  D : 오차 변화율에 따른 제동
- pid_output = (error * Kp) + (integral * Ki) + (derivative * Kd)

----
# PID 튜닝 과정



|
최종 파라미터 Kp = 7 , Ki = 0 Kd = 0
|
 정상상태 오차 : 약 0.6cm (목표 30cm , 실측 29.4cm)

----
# 작동영상



