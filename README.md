# Storm_Of_Time_And_Space

# Stormy_Six

![image](https://github.com/user-attachments/assets/6a0fb8e4-182b-49ec-9759-a696257ef5ef)



## 📖 목차
1. [프로젝트 소개](#프로젝트-소개)
2. [주요기능](#주요기능)
3. [개발기간](#개발기간)
5. [Trouble Shooting](#trouble-shooting)

## 👨‍🏫 프로젝트 소개
2D협동 슈팅 프로젝트입니다.

1~4인까지 멀티플레이가 가능 하며

4개의 스포너와 1마리의 보스를 잡고 엔딩을 볼 수 있습니다.


## 👨‍🏫 조작법

좌우 화살표를 사용해 좌우 조작 

C를 사용하여 상호작용

SpaceBar를 통해 점프 및 상호작용 중인 오브젝트를 사용하실 수 있습니다.
    
## 💜 핵심기능

프로젝트의 핵심 기능들 입니다


### 📁 Photon  
멀티플레이를 구현하기위한 프레임워크입니다.
  
### 👤 Interface  
플레이어가 다양한 오브젝트와 상호작용 할수있도록
결합도감소와 유연성을 확보하기 위한 기능입니다.
  
### 🕹️ Objectpooling  
수많은 투사체오브젝트와 파티클 생성 제거시 풀링을 사용해
자원을 절약하기위한 기능입니다.
  
### 🤖 ScriptableObject, Enum
데이터를 효율적으로 관리하고 위한 기능입니다.
  
### 💻 FSM  
각 상태별 동작을 분리해 유지보수를 쉽게 해주는 기능입니다.
  
### 💬 OverlapCircle  
물체 생성 전 해당위치에 물체가 겹치는지 체크해주는 기능입니다.



## 트러블 슈팅


문제> 
스포너 각각이 갖고 있는 Spawner 스크립트의 기체 미참조 현상


문제 발생 출처 및 시도 > 
스포너의 생성 지점과 기체의 생성 지점의 거리를 계산해야 되는 상황에서 
기체 오브젝트 참조가 되지않아 스포너가 자신의 역할(기체와 스포너의 거리가 좁혀졌을 때 몬스터를 생성한다.)을 수행하지 못한 문제 발생

해결 방법 > 
기체의 생성 시점과 Spawner 스크립트의 Ship 오브젝트 참조 시점이 
Awake()여서 Ship 오브젝트에 참조가 되지 않았고, 
스포너가 생성되는 시점을 Start() 로 늦췄더니 정상작동 하였다.

![image](https://github.com/user-attachments/assets/d5602aed-815f-499c-91b3-fcbe260cdc93)


![image](https://github.com/user-attachments/assets/05da0791-aa45-400d-b17a-595e0af8ff63)


![image](https://github.com/user-attachments/assets/a98a271c-2f39-4ff6-85ed-a46434526086)

![image](https://github.com/user-attachments/assets/0601bd38-94e8-41b5-9eb1-c4641f07a557)

![image](https://github.com/user-attachments/assets/74be001b-b2d2-4a2d-bf03-bd6323bc27d5)




## ⏲️ 개발기간
2025.06.12 ~ 2025.06.18
    
### ✔️ Language
- C#
