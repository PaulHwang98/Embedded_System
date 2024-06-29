## Subject

---

- FRDM-K64F보드와 HUZZAH ESP8266보드 이용 하드웨어 구성 및 다양한 실습 및 ALARM CLOCK 미니 프로젝트

---

## Key Point

---

- FRDM-K64F보드와 Mbed Application shield이용 아날로그 및 디지털 입출력
- HUZZAH ESP8266보드 이용 인터넷 통신
- 임베디드 시스템인 ALARM CLOCK 구현

---

## Role

---

- ARM Keli Studio 아날로그 및 디지털 입출력, 인터넷 통신 실습
- 알람 시계 동작을 위한 주요 C/C++ 코드 작성(main.cpp, thread.cpp, clock.cpp, ISR.cpp)

---

## **Capabilities**

---

- 임베디드 시스템 아날로그 및 디지털 입출력 실습 경험
- 임베디드 시스템 인터넷 통신 실습 경험
- Thread와 ISR을 이용한 ALARM CLOCK 구현 경험

---

## ALARM_CLOCK

---

**Demonstration**
    - https://www.youtube.com/watch?v=1yp4uvCmZsc
**Functional description**
    
[SW1]
    
- 누를 때마다 MainScreen, Alarm1SetScreen, Alarm2SetScreen, Alarm3SetScreen으로 순서대로 이동(화면 순환)
    
[SW2]
    
- SW2 누르면 ClockSet Mode로 진입
- Mbed Application Shield(이하 Shield) joystick으로 시간 설정
- MainScreen ClockSet Mode :
    
    > joystick up : 시(HH) 1씩 증가
    > 
    > 
    > joystick down : 시(HH) 1씩 감소
    > 
    > joystick left : 분(MM) 1씩 증가
    > 
    > joystick right : 분(MM) 1씩 감소
    > 
    > joystic center : 초(SS) 리셋\n
    >
     
AlarmSetScreen ClockSet Mode :
    
    > joystick up : 시(HH) 1씩 증가\n
    > 
    > joystick down : 시(HH) 1씩 감소\n
    > 
    > joystick left : 분(MM) 1씩 증가\n
    > 
    > joystick right : 분(MM) 1씩 감소\n
    
[SW3]
    
1. 설정한 알람이 울리고 있으면 알람 중지
2. AlarmSetScreen에서 SW3 누르면 해당 알람 해제
    
> ex) Alarm1SetScreen에서 SW3 누르면 설정된 알람이 해제됨
 
    
[LCD]
1. MainScreen : 현재 시각 Display
2. Alarm1SetScreen : 첫 번째 알람 설정 화면
3. Alarm2SetScreen : 두 번째 알람 설정 화면
4. Alarm3SetScreen : 세 번째 알람 설정 화면
    
[Buzzer]
    
1. 알람 설정한 시각이 되면 소리가 출력
    
[LED]
    
1. 알람 설정한 시각이 되면 LED 점멸

---

<img width="910" alt="스크린샷 2023-11-08 오후 3 03 41" src="https://github.com/actorjung/Embedded_System/assets/112843229/317e1c3f-9fb5-498c-a505-a527b8fb561f">


---
