---
layout: archive
lang: kr
ref: ollo_bugkit
read_time: true
share: true
author_profile: false
permalink: /docs/kr/edu/ollo/bugkit/
sidebar:
  title: 버그 키트
  nav: "ollo_bugkit"
---

# [버그 키트](#버그-키트)

올로 버그 키트에서는 센서 일체형 제어기([CM-100])와 [감속모터]가 포함되어 있습니다. 사용자가 직접 버그 로봇을 제어하는 프로그램을 제작 및 다운로드 하기 위해서는 [USB 다운로더(LN-101)]를 구매하셔야 합니다.
프로그래밍 방법은 [프로그래밍 학습]을 참고하세요.  
{: .notice}


※ 올로 버그 기트는 현재 단종되어 더 이상 판매되지 않습니다.  
{: .notice--warning}

## 버그 키트에 포함된 설명서로 만든 4 가지 형태의 버그 로봇 예제

 ![](/assets/images/edu/ollo/bug_kr.png)


## 올로 버그 로봇으로 할 수 있는 게임 예제

`올로 버그 게임 1` 버그 배틀
1. 동그란 원 안에 로봇을 올려 놓습니다.
2. 심판의 시작 신호와 함께 게임을 시작합니다.
3. 로봇을 조종하여 상대방 로봇을 원 밖으로 밀어내면 승리~!!

![](/assets/images/edu/ollo/bug_battle_kr.png)

`올로 버그 게임 2` 버그 라인트레이싱
1. 버그 로봇을 선 위에 올려 놓습니다.
2. 전원을 켜면 버그 로봇이 스스로 선을 따라 움직입니다.
3. OLLO 버그 라인트레이스용 라인 인쇄물 : [OLLO_LineTrace.pdf]

![](/assets/images/edu/ollo/bug_line_kr.png)

동봉된 여러가지 모양의 퍼즐판을 이용해 올로 버그가 따라갈 길을 만들어 주세요.  
버그 로봇은 어디든지 갈 수 있습니다.  
OLLO 버그 퍼즐 레이스용 라인 인쇄물 :
[OLLO_PuzzleRacing.zip]

![](/assets/images/edu/ollo/bug_line_2_kr.png)

# [시작하기](#시작하기)

## [부품 리스트](#부품-리스트)

올로 버그 부품 리스트

![](/assets/images/edu/ollo/bug_partlist_kr.png)

- [CM-100]
- [RC-100]
- [감속모터]

## [버그 작동하기](#버그-작동하기)

올로 버그 키트는 기본적으로 제품 출하 시 [버그 기본 프로그램]이 들어 있습니다. 버그 기본 프로그램의 동작 방법은 아래와 같습니다.

버그 전원 켜기

시작 버튼을 한 번 누르면 전원이 켜지고, 다시 한 번 누르면 전원이 꺼집니다.  
버그 제어기 CM-100은 절전 기능이 있어서 별다른 입력이 없다면 약 5분 뒤에 자동으로 전원이 꺼집니다.  
이 절전 기능은 태스크 코드로 제어할 수 있으며, 기본 프로그램에는 5분으로 설정되어 있습니다.([태스크 코드로 제어하는 방법보기])

![](/assets/images/edu/ollo/cm100_partname_kr.png)

리모컨 조종 모드

![](/assets/images/edu/ollo/tutorial_6_goal_kr.png)

- 시작 버튼을 1~2회 누르면 실행됩니다.(1회는 적외선 채널 1, 2회는 적외선 채널 2)
- 무선 조종을 위해서는 RC-100 리모컨의 적외선 채널이 일치해야 합니다. ([RC-100 적외선 채널 바꾸는 방법 보기])
- RC-100 의 U / L / D / R 버튼을 이용하여 버그 로봇의 이동 방향을 조종합니다.
- 포트 3 에 서보 모터가 연결되어 있는 경우 1, 3 버튼으로 서보 모터를 조종합니다.
- 포트 4 에 서보 모터가 연결되어 있는 경우 2, 4 버튼으로 서보 모터를 조종합니다.
 ([서보모터]는 버그 키트에 기본으로 들어 있지 않습니다. 별도 구매 후 연결하셔야 합니다.)

라인트레이서 모드

![](/assets/images/edu/ollo/tutorial_4_goal_kr.png)

- 시작 버튼을 3회 누르면 실행됩니다.
- 흰 바닥에 검은 색 라인을 따라 다닙니다.
- 전방에 물체가 감지되면 멈추고, 박수를 치면 다시 라인을 따라 다닙니다.

## [지그비 무선 조종](#지그비-무선-조종)

### 지그비(ZIGBee)

![](/assets/images/edu/ollo/zig_100_110_kr.png)

[ZIG-100/110]은 로봇용 무선 통신 장치로서 ZIGBee 방식을 사용합니다. ZIGBee 는 Bluetooth 와 같이 PAN(Personal Area Network) 통신에 많이 사용되는 통신 기술입니다.  
적외선 방식에 비해서 통신 품질이 매우 좋고, 여러 명이 동시에 조종하여도 각자 자신의 로봇을 조종할 수 있는 장점이 있습니다.

구매한 제품에 지그비 모듈이 포함되지 않을 수 있습니다. 이 경우에는 별도로 구매해야 합니다.  
{: .notice--warning}

BT-210도 사용법은 동일 합니다.  
{: .notice--warning}

### 제어기와 지그비

RC-100 을 이용한 올로와 바이올로이드의 조종은 기본적으로 적외선 방식의 무선 통신을 이용하도록 되어 있습니다. 이것을 ZIGBee 방식의 무선 통신을 이용하도록 하기 위해서는 [ZIG-110 set] 를 별도로 구매하여 [RC-100] 에 ZIG-100 을 장착하고, [제어기]에 ZIG-110 을 장착해야 합니다.  (자세한 장착 방법은 각 부품의 설명 페이지를 참고하세요.)


지그비 셋트는 제품 출하시 서로 통신이 가능하도록 설정이 맞춰져 있습니다. 만약, 다른 지그비 셋트와 혼용하면 무선 조종이 되지 않으니 섞이지 않도록 주의하시기 바랍니다.   
{: .notice--warning}

|ZIG-100 installed in RC-100|ZIG-110 installed in CM-100|
|:-----:|:-----:|
|![](/assets/images/edu/ollo/rc-100_zig-100_insert4_kr.jpg)|![](/assets/images/edu/ollo/cm100_zig110_kr.jpg)|

|ZIG-110 installed in CM-510|ZIG-100 installed in CM-5|
|:-----:|:-----:|
|![](/assets/images/edu/ollo/cm510_zig110_kr.png)|![](/assets/images/edu/ollo/cm5_zig100_kr.png)|

# [응용하기](#응용하기)


## [배틀 버그 만들기](#배틀-버그-만들기)
올로 버그 키트에 [서보모터]를 추가 구매하여 장착하면 다양한 형태의 배틀 버그를 만들 수 있습니다.  
올로 [버그 기본 프로그램]에는 포트 3 이나 포트 4 에 서보 모터를 연결했을 때 RC-100 으로 조종이 가능하도록 프로그래밍 되어 있습니다.  
포트 3 에 서보 모터가 연결되어 있는 경우 1, 3 버튼으로 서보 모터를 조종합니다.  
포트 4 에 서보 모터가 연결되어 있는 경우 2, 4 버튼으로 서보 모터를 조종합니다.

![](/assets/images/edu/ollo/battlebug_kr.png)

## [자동차 만들기](#자동차-만들기)
올로 버그 키트에 [큰타이어 세트]를 추가 구매하시면 바퀴를 달아 자동차를 만드실 수 있습니다.

![](/assets/images/edu/ollo/linetracer_kr.png)

## [그 외의 장치 활용하기](#그-외의-장치-활용하기)
올로(OLLO) 의 제어기([CM-100]) 에는 배틀 버그 만들기와 자동차 만들기에서 소개한 부품 외에도 아래와 같은 여러 가지 부품들을 연결하여 다양한 형태의 로봇을 만들 수 있습니다.

|적외선 센서|접촉 센서|LED 모듈|
| :-----: | :-----: | :-----: |
|![](/assets/images/edu/ollo/ir_kr.jpg)|![](/assets/images/edu/ollo/touch_kr.jpg)|![](/assets/images/edu/ollo/led_kr.jpg)|



# [프로그래밍 학습](#프로그래밍-학습)

## [화면 출력하기](#화면-출력하기)

### 학습목표

프로그램 출력용 모니터 창에 제어기(CM-100)의 중앙 적외선 센서 값을 출력하여 확인하는 프로그램을 작성합니다.

![](/assets/images/edu/ollo/tutorial_2_goal_kr.png)

### 준비 사항

학습 목표를 달성하기 위해서는 우선 태스크 코드를 작성하고, 프로그램 출력용 모니터 창을 띄워줄 로보플러스(RoboPlus) 소프트웨어가 필요하며, 태스크 코드를 실행하여 중앙 적외선 센서 값을 PC 로 보내줄 [제어기(CM-100)]가 필요합니다. 또한 PC 와 제어기 사이의 연결을 위해 [USB 다운로더(LN-101)]가 필요합니다.

### 태스크 코드 작성

1. [RoboPlus Task] 프로그램 실행

    ![](/assets/images/edu/ollo/print-scr-01_kr.png)

2. [제어기 선택]  
  빈 줄을 선택한 후 더블클릭 하거나 Enter 키를 누르면 제어기 선택 대화창이 나타납니다.  제어기를 선택 후 확인 버튼을 누릅니다.

    ![](/assets/images/edu/ollo/print-scr-02_kr.jpg)

3. [프로그램 시작]만들기  
  이어서 뜨는 명령어 종류 선택 창에서 프로그램 시작을 마우스로 더블클릭 하거나 선택 후 Enter 키를 누릅니다.

    ![](/assets/images/edu/ollo/print-scr-03_kr.png)

4. [무조건 반복] 명령어 입력  
  반복해서 적외선 센서 값을 읽어와서 화면에 출력하기 위해 무조건 반복 명령어를 사용합니다.  
  프로그램 시작의 { 와 } 사이 구간의 빈 줄을 선택하고 Enter 키를 누르거나 더블클릭하면 명령어 선택 창이 뜹니다. 반복문 -> 무조건 반복 (while(1)) 을 선택합니다.

    ![](/assets/images/edu/ollo/print-scr-04_kr.png)

5. [로드] 명령어 입력  
  적외선 센서의 값을 읽어와 화면 표시로 입력하기 위해 로드 명령어를 사용합니다.  
  무조건 반복의 { 와 } 사이 구간의 빈 줄에 실행문 -> 로드 (값 입력하기) 를 선택하여 입력합니다.

    ![](/assets/images/edu/ollo/print-scr-05_kr.png)

6. [중앙 적외선 센서] 값을 [화면 출력]으로 로드
  로드 명령어의 파라미터 중 좌측의 파라미터( ? )를 선택합니다. ([파라미터에 대한 설명])
  ? 를 더블클릭 하거나 클릭 후 Enter 를 누르면 아래와 같은 파라미터 선택 창이 뜹니다. 제어기 -> 화면 출력 후 줄 바꿈 을 선택하고 확인 버튼을 누릅니다.

    ![](/assets/images/edu/ollo/print-scr-06-1_kr.png)

    같은 방법으로 우측의 파라미터( ? )에는 제어기 -> 중앙 적외선 센서를 입력해 줍니다.

    ![](/assets/images/edu/ollo/print-scr-06-2_kr.png)

    로드 명령어의 파라미터를 모두 입력한 화면은 아래와 같습니다.

    ![](/assets/images/edu/ollo/print-scr-06-3_kr.png)

7. 태스크 코드 저장 하기  
  Ctrl + S 를 누르거나 도구 모음의 저장 버튼을 눌러 저장합니다.

    ![](/assets/images/edu/ollo/print-scr-07_kr.png)

### [태스크 코드 다운로드](#태스크-코드-다운로드)

위에서 작성한 태스크 코드를 제어기에 다운로드 합니다. ( [태스크 코드 다운로드 방법] )


### 프로그램 실행 및 결과보기

1. 프로그램 출력용 모니터 창 띄우기  
  프로그램 실행 시 화면 출력을 보기 위해서는 반드시 프로그램 실행 전에 프로그램 출력용 모니터 창을 먼저 띄워야 합니다.  
  프로그램 출력용 모니터 창을 띄우는 방법은 프로그램 다운로드 창에서 프로그램 출력 보기 버튼을 클릭하거나 도구 모음에서 프로그램 출력 보기 버튼 클릭 혹은 프로그램(P) 메뉴의 프로그램 출력 보기(V) 메뉴 선택 혹은 단축키 F5 버튼을 누르면 됩니다.

2. 프로그램 실행하기  
  프로그램 출력용 모니터 창을 띄웠으면 제어기에 다운받은 프로그램을 실행합니다. 제어기 상단의 시작 버튼을 눌러 켜면 내부의 LED 가 켜지며 제어기에 다운로드 한 프로그램이 실행됩니다.  
  제어기의 중앙 적외선 센서 앞에 손을 가까이, 멀리 움직이며 프로그램 출력용 모니터 창에 숫자 값이 변화하는 것을 확인합니다.

![](/assets/images/edu/ollo/print-scr-result_kr.png)


## [버그 움직이기](#버그-움직이기)

### 학습 목표

버그 키트로 만들어진 버그 로봇을 전진/좌회전/우회전/후진으로 움직여 봅시다. (버그 로봇은 교육키트 2단계/3단계로도 만들 수 있습니다.)

![](/assets/images/edu/ollo/tutorial_3_goal_kr.png)

### 준비물

PC([RoboPlus Task] 프로그램), 조립된 버그 로봇, USB 다운로더([LN-101]),

### 태스크 코드 작성

#### 버그 로봇 전진

1. [RoboPlus Task] 실행 및 프로그램 시작 만들기 ([화면 출력하기 참조])
  RoboPlus Task를 실행하면 다음과 같은 화면을 볼 수 있습니다.

    ![](/assets/images/edu/ollo/print-scr-01_kr.png)

2. 직진 함수 만들기 ([함수에 대한 보다 자세한 설명은 여기를 참고하세요.])
  함수는 프로그램 시작의 { 와 } 바깥에 만들어야 합니다. 따라서 6 번째 줄 부터 함수를 만들도록 하겠습니다.  
  먼저 6 번 줄을 선택하면 뜨는 명령어 선택창에서 함수 (Sub routine) 에서 함수 만들기를 선택합니다.

    ![](/assets/images/edu/ollo/2-1_kr.jpg)

    함수가 아래와 같이 만들어 집니다.

    ![](/assets/images/edu/ollo/2-2_kr.png)

    함수 이름을 지정하기 위해 "이름을_입력하세요" 부분을 더블클릭하거나 선택된 상태로 Enter 키를 눌러 함수 이름을 "직진" 으로 입력하고 다시 Enter 키를 누릅니다.

    ![](/assets/images/edu/ollo/2-3_kr.png)

3. 버그 직진을 위한 모터 제어
  버그에는 2개의 감속모터가 좌측과 우측의 관절로 된 다리를 움직이도록 되어 있습니다.  
  버그 직진을 위해서는 다리를 움직이는 양쪽 모터가 모두 전진 방향으로 회전을 해야 합니다.  
  감속모터 제어를 위해서는 로드 명령어를 사용하여 모터 제어 값을 넣어줘야 합니다.
  함수 직진의 { 와 } 사이 빈 줄을 더블클릭하여 뜨는 명령어 선택 창에서 실행문 → 로드 (값 입력하기)를 선택합니다.

    ![](/assets/images/edu/ollo/5-1_kr.jpg)

    포트 1 에 연결된 감속모터(좌측 모터) 제어를 위해 첫 번째를 선택하여 감속모터 포트 1 을 입력합니다.

    ![](/assets/images/edu/ollo/3-1_kr.png)

    좌측 모터의 회전 방향과 속도를 지정하기 위해 두 번째를 선택하여 방향 : CCW 와 출력 : 1023 을 입력합니다.(CCW 는 반시계 방향을 나타내며, 좌측모터의 전진방향입니다. 출력 1023 은 감속 모터의 최대 출력 값이며, 출력이 강하면 회전력도 강하고, 속도도 빠릅니다.)

    ![](/assets/images/edu/ollo/3-2_kr.png)

    포트 1 의 감속모터에 제어값 CCW:1023 입력을 완료한 모습입니다.

    ![](/assets/images/edu/ollo/3-3_kr.png)

    포트 2 의 감속모터 제어를 위해 방금 입력한 명령줄 아래에 빈 줄을 삽입합니다. 빈 줄을 삽입하기 위해서는 원하는 위치에서 Space 키를 누르면 됩니다. 아래는 함수 직진의 } 위치를 클릭한 후 Space 키를 누른 모습입니다.

    ![](/assets/images/edu/ollo/3-4_kr.png)

    위에서 포트 1 의 감속모터 제어문을 입력한 것과 동일한 방법으로 포트 2 의 감속모터에 CW 방향(시계방향)으로 1023(최대출력) 으로 회전하도록 명령줄을 입력합니다. (오른쪽 모터의 경우 CW 가 전진방향입니다.)

    ![](/assets/images/edu/ollo/3-5_kr.png)

4. 함수 호출 ([함수에 대한 보다 자세한 설명은 여기를 참고하세요.])
  CM-100 의 프로그램을 실행 시키면 직진 함수가 실행되도록 하기 위해서는 프로그램 시작에서 직진 함수를 호출해 주어야 합니다.  
  프로그램이 종료되지 않고 계속 실행되도록 하기 위해 무조건 반복 명령어를 사용합니다. 프로그램 시작의 { 와 } 사이에 무조건 반복 명령어를 입력 합니다.

    ![](/assets/images/edu/ollo/4-1_kr.png)

    무조건 반복 구문 내에서 직진 함수를 호출합니다. 무조건 반복의 빈 줄 더블클릭 혹은 Enter 에서 함수 (Sub-routine) 의 함수 호출을 선택합니다.

    ![](/assets/images/edu/ollo/4-2_kr.png)

    이름을_입력하세요 부분을 더블클릭하거나 Enter 키를 누르면 현재 만들어진 함수의 목록이 나옵니다. 목록에서 직진 함수를 선택하거나 직접 입력합니다.

    ![](/assets/images/edu/ollo/4-3_kr.png)

    지금까지 입력한 최종 결과물은 아래와 같습니다.  

    ![](/assets/images/edu/ollo/4-4_kr.png)

#### 버그 로봇 후진

후진은 직진에서 두 모터의 방향만 모두 반대로 바꿔주면 됩니다. 따라서 직진 함수를 가져다가 수정하여 후진 함수를 만들도록 하겠습니다.


1. 직진 함수 복사 후 붙여넣기 ([5. 복사/잘라내기/붙여넣기 참고])
  마우스로 드래그 혹은 Shift 키나 Ctrl 키를 누른 채로 직진 함수를 모두 선택합니다.

    ![](/assets/images/edu/ollo/b_1-1_kr.png)

    마우스 오른쪽 클릭 후 뜨는 팝업 메뉴에서 복사(C) 를 선택하거나 단축키 Ctrl + C 를 눌러 복사합니다.  

    ![](/assets/images/edu/ollo/b_1-2_kr.png)

    직진 함수 아래에 15 라인 클릭 후 마우스 오른쪽 클릭 팝업 메뉴에서 붙여넣기(P) 혹은 단축키 Ctrl + V 를 눌러 복사한 함수를 붙여 넣습니다.

    ![](/assets/images/edu/ollo/b_1-3_kr.png)

    아래는 직진 함수를 복사하여 아래에 붙여넣기를 완료한 화면입니다

    ![](/assets/images/edu/ollo/b_1-4_kr.png)

2. 후진 함수로 이름 바꾸기 및 모터 방향 바꾸기
  복사한 함수의 이름을 직진에서 후진으로 바꿔 줍니다. 함수 이름 부분을 더블클릭하거나 Enter 키를 누르면 수정이 가능합니다.

    ![](/assets/images/edu/ollo/b_2-1_kr.png)

    양쪽 모터의 회전 방향을 모두 반대방향으로 바꿔 줍니다. 역시 오른쪽 파라미터 (CW:1023 or CCW:1023) 부분을 더블클릭 하거나 Enter 키로 수정이 가능합니다.
    ![](/assets/images/edu/ollo/b_2-2_kr.png)

3. 프로그램 시작에서 호출 함수를 전진에서 후진으로 바꿔 줍니다.
  다음과 같이 프로그램 시작 시 계속 반복해서 후진 함수를 실행하게 됩니다.

    ![](/assets/images/edu/ollo/b_3-1_kr.png)

#### 버그 로봇 좌회전

좌회전 함수를 만들기 위해서 위의 후진에서와 동일하게 직진 함수를 복사한 후 함수 이름을 좌회전으로 바꾸고, 우측 모터(포트 2)는 그대로 전진방향으로 회전하도록 두고 좌측 모터(포트 1)만 정지 시켜 (CW/CCW  상관 없이 출력에 0 을 넣어 줌) 버그 로봇이 좌회전하도록 합니다.

![](/assets/images/edu/ollo/l-turn_kr.png)


#### 버그 로봇 우회전

우회전 함수를 만들기 위해서 위의 후진에서와 동일하게 직진 함수를 복사한 후 함수 이름을 우회전으로 바꾸고, 좌측 모터(포트 1)는 그대로 전진방향으로 회전하도록 두고 우측 모터(포트 2)만 정지 시켜 (CW/CCW  상관 없이 출력에 0 을 넣어 줌) 버그 로봇이 우회전하도록 합니다.

![](/assets/images/edu/ollo/r-turn_kr.png)

### 프로그램 다운로드

- 프로그램 다운로드 절차는 [프로그램 다운로드] 를 참고하세요.
- 프로그래밍 결과 파일 :  [bug_move.tsk]

### 프로그램 실행 및 결과

CM-100 상단 시작 버튼 눌러 켜면 프로그램 시작에서 호출하는 함수에 따라 버그 로봇이 계속해서 직진 또는 후진 또는 좌회전 또는 우회전 합니다.

## [버그 라인 따라가기](#버그-라인-따라가기)

### 목표

적외선은 물체의 색상에 따라 반사하는 정도가 다릅니다. 흰 색은 적외선을 많이 반사하고, 검은색은 적외선을 적게 반사합니다. 이러한 성질을 이용하여 CM-100 의 적외선 센서로 흰 바닥과 검은 선을 구분하고, 버그 로봇이 그 선을 따라 가도록 프로그래밍 해 보도록 하겠습니다.  
(앞 장의 [버그 움직이기]를 바탕으로 작성합니다.)

![](/assets/images/edu/ollo/tutorial_4_goal_kr.png)

### 준비물

PC([RoboPlus Task] 프로그램), 조립된 버그 로봇, USB 다운로더([LN-101]), 흰 바닥에 검은 선이 그어진 판

### 라인 트레이서

CM-100 의 바닥쪽 왼쪽 적외선 센서와 오른쪽 적외선 센서를 사용하여 흰 바닥과 검은 선을 구분한 다음 검은 선을 따라 버그가 움직이도록 하는 프로그래밍의 알고리즘은 아래와 같습니다.

![](/assets/images/edu/ollo/linetracer_kr.jpg)

- 오른쪽 검은 선 감지 (O), 왼쪽 검은 선 감지 (X) : 우회전  
오른쪽 적외선 센서에만 검은 선이 감지되었다는 것은 선이 오른쪽으로 휘어져 있다는 의미이므로 오른쪽 모터를 정지시켜서 로봇의 진행 방향을 오른쪽으로 바꿉니다.
- 오른쪽 검은 선 감지 (X), 왼쪽 검은 선 감지 (O) : 좌회전  
 위에서의 반대 경우로 왼쪽으로 선이 휘어져 있으므로 왼쪽 모터를 정지시켜 로봇의 진행 방향을 왼쪽으로 바꿉니다.
- 오른쪽 검은 선 감지 (X), 왼쪽 검은 선 감지 (X) : 직진  
 양 쪽 적외선 센서 모두 감지가 되지 않았으면 선이 왼쪽과 오른쪽 적외선 센서 사이에 있거나 선을 벗어난 상태로 방향 전환 없이 직진합니다.
- 오른쪽 검은 선 감지 (O), 왼쪽 검은 선 감지 (O) : 직진  
 양 쪽 적외선 센서 모두 감지가 되었으면 십자(+)로 된 교차점과 같은 가로로 된 검은 선이 있거나 검은 바닥이므로 방향 전환 없이 직진합니다.

앞서 작성한 [버그 움직이기] 예제에서 왼쪽/오른쪽 적외선 센서에 검은 선이 감지되는 조건에 따라 다른 함수를 호출하는 코드를 프로그램 시작에 넣어 버그 로봇을 움직이도록 합니다.

1. 왼쪽 적외선 센서에만 검은 선이 감지되면 좌회전 합니다.   
  프로그램 시작 내의 무조건 반복의 { 와 } 사이에 조건에 따라 다른 동작을 하기 위해 조건문의 만약 명령어를 입력합니다. ([만약 명령어에 대한 자세한 정보는 여기를 참고하세요.])  
  만약 명령어 입력 후 화면은 다음과 같습니다.

    ![](/assets/images/edu/ollo/1-2_kr.png)

    왼쪽 적외선 센서에만 검은 선이 감지되는 경우는 왼쪽 적외선 센서 값은 200 보다 작고, 오른쪽 적외선 센서 값은 200 보다 크게 됩니다. 이러한 조건을 찾기 위해 조건절의 비교 파라미터1(첫 번째 ?)에 왼쪽 적외선 센서를 입력합니다.

    ![](/assets/images/edu/ollo/1-3_kr.png)

    두 비교 파라미터 사이의 비교 연산자는 왼쪽 적외선 센서가 200 보다 작아야 하므로 < 를 입력합니다.

    ![](/assets/images/edu/ollo/1-4_kr.png)

    비교 파라미터2 (두 번째 ?) 에 숫자 200 을 입력합니다.

    ![](/assets/images/edu/ollo/1-5_kr.png)

    ( 왼쪽 적외선 센서 < 100 ) 그리고 ( 오른쪽 적외선 센서 > 200 ) 두 가지 조건이 모두 만족되어야 하므로 then 을 클릭하여 연결 연산자를 && (AND) 로 바꿉니다. 연결 연산자를 바꾸면 뒤에 조건절이 자동으로 하나 더 추가됩니다.

    ![](/assets/images/edu/ollo/1-6_kr.png)

    두 번째 조건절의 비교 파라미터1에 오른쪽 적외선 센서를 입력하고 비교 연산자는 > 를, 비교 파라미터2에 숫자 200 을 입력하여 만약 명령어를 완성합니다.

    ![](/assets/images/edu/ollo/1-7_kr.png)

    완성된 조건절이 참이면(왼쪽 적외선 센서에만 검은 선이 감지되면) 좌회전 함수를 호출합니다.

    ![](/assets/images/edu/ollo/1-8_kr.png)

2. 반대로 오른쪽 적외선 센서에만 검은 선이 감지되면 우회전 합니다.  
  1 의 만약 명령어에 이어 조건을 계속 검사하기 위해 조건문의 아니면 만약 명령어를 입력합니다.    
  1 의 만약 명령어 조건문이 참일 경우 아니면 만약 명령어는 실행되지 않습니다.  

    ![](/assets/images/edu/ollo/2-1_kr.png)

    1 에서와 반대로 오른쪽 적외선 센서에만 검은 선이 감지되는 경우는 왼쪽 적외선 센서 값은 200 보다 크고, 오른쪽 적외선 센서 값은 200 보다 작게 됩니다. 조건절은 1 을 참고하여 비교 연산자만 반대로 작성하면 됩니다. 이 경우에는 우회전 함수를 호출합니다.

    ![](/assets/images/edu/ollo/2-2-1_kr.png)

3. 1 과 2 외의 경우, 즉 양쪽 적외선 센서 모두에 검은 선이 감지되거나, 양쪽 모두 선이 감지되지 않은 경우 직진합니다.  
  위의 두 가지 조건절이 모두 아닌 경우 직진하기 위해 조건문의 아니면 명령어를 입력하고, 직진 함수를 호출합니다.

  ![](/assets/images/edu/ollo/3-1-1_kr.png)


### 프로그램 다운로드

- 프로그램 다운로드 절차는 [프로그램 다운로드 를 참고]하세요.
- 프로그래밍 결과 파일 :  [bug_linetracer.tsk]
- [라인트레이서용 인쇄물 다운 받기]


### 프로그램 실행 및 결과

 흰 바탕에 검은 선이 그려진 판 위에 버그를 올려놓고 실행시켜 보세요. 라인을 따라 버그가 움직이는지 확인하세요.

## [센서에 반응하는 버그](#센서에-반응하는-버그)

### 목표

앞 장의 라인 따라하기와 같이 흰 바닥의 검은 선을 따라 움직이다가 전방의 중앙 적외선 센서에 물체가 감지되면 제자리에 멈추고, 그 상태에서 박수 소리가 감지되면 다시 선을 따라 다니도록 프로그래밍 해 봅시다.  
(앞 장의 [버그 라인 따라가기] 를 바탕으로 작성합니다.)

![](/assets/images/edu/ollo/tutorial_5_goal_kr.jpg)

### 준비물

 PC([RoboPlus Task] 프로그램), 조립된 버그 로봇, USB 다운로더([LN-101]), 흰 바닥에 검은 선이 그어진 판

### 센서에 반응하는 버그

1. 정지 함수 추가  
  중앙 적외선 센서에 물체가 감지되면 이동을 멈추기 위해 정지 함수를 추가합니다.  
  함수 만들기는 [버그 움직이기]를 참고하여 작성하시면 됩니다.  
  포트 1, 2 에 연결된 좌/우측 감속모터에 모두 출력 0 을 넣어 정지 함수를 만듭니다.

    ![](/assets/images/edu/ollo/1-1_kr.png)

2. 중앙 적외선 센서에 물체가 감지되면 정지 함수 호출   
  프로그램 시작에 만약 명령어를 추가하여 중앙 적외선 센서 값이 200 보다 커지면(물체가 감지됨) 정지 함수를 호출합니다.

  ![](/assets/images/edu/ollo/2-1-kr.png)

3. 버그가 완전히 정지할 때까지 잠시 기다립니다.  
  소리 감지를 사용하기 위해서는 버그가 완전히 멈춰야 합니다. 버그의 모터 등이 움직이는 소리는 CM-100 의 마이크에 아주 크게 들리기 때문에 버그가 움직이고 있으면 소리가 감지되었다고 판단되기 때문입니다.  
  따라서 타이머를 사용하여 일정 시간 기다리는 코드를 추가해 줍니다. ([타이머의 자세한 설명은 여기 참조])

  로드 명령어로 타이머에 타이머 값 1초를 넣어줍니다.

    ![](/assets/images/edu/ollo/3-1-2_kr.png)

    ![](/assets/images/edu/ollo/3-1-3_kr.png)

    ![](/assets/images/edu/ollo/3-1-4_kr.png)

    타이머 시간이 줄어들어 0 이 될 때까지 기다리기 위해 조건 대기 명령어를 사용합니다. ([조건 대기 명령어에 대한 보다 자세한 정보는 여기를 참고하세요.])  
    조건 대기 명령어로 타이머 값이 카운트다운 되어 0 이 될 때까지(0 보다 큰 동안) 대기합니다.  

    ![](/assets/images/edu/ollo/3-4-1_kr.png)

    ![](/assets/images/edu/ollo/3-5-1_kr.png)

4. 마이크를 통해 박수소리가 날 때 까지 대기합니다.
  중앙 적외선 센서에 물체가 감지되어 움직임을 정지했으면 그 상태로 소리가 감지될 때까지 대기하는 코드를 작성합니다.  
  소리감지 횟수는 자동으로 0 으로 초기화 되지 않으므로 대기하기 전에 로드 명령어로 0 으로 초기화를 해 줍니다.  
  ([소리감지 횟수에 대한 자세한 설명은 여기를 참고하세요.])

    ![](/assets/images/edu/ollo/4-1-1_kr.png)

    ![](/assets/images/edu/ollo/4-1-2_kr.png)

조건 대기 명령어를 사용하여 소리감지 횟수가 0 인 동안에는 대기하도록 합니다.

### 프로그램 다운로드

- 프로그램 다운로드 절차는 [프로그램 다운로드 를 참고]하세요.
- 프로그래밍 결과 파일 :  [bug_sensor.tsk]

### 프로그램 실행 및 결과

프로그램을 실행 시킨 후 중앙 적외선 센서에 물체가 감지되면 버그가 멈추는지 확인합니다.  
그 후 박수를 쳐서 다시 버그가 움직이는지 확인합니다.

## [버그 조종하기](#버그-조종하기)

### 목표

RC-100 조종기를 사용하여 버그 로봇을 전/후/좌/우 로 조종할 수 있도록 프로그래밍을 해 봅시다.  
(앞 장의 [센서에 반응하는 버그] 를 바탕으로 작성합니다.)

![](/assets/images/edu/ollo/tutorial_6_goal_kr.png)

### 준비물

PC([RoboPlus Task] 프로그램), 조립된 버그 로봇, USB 다운로더([LN-101]), RC-100

### 버그 조종하기

1. 기존의 코드에서 프로그램 시작 내에 무조건 반복의 { 와 } 로 둘러쌓인 부분을 모두 삭제합니다.  

    ![](/assets/images/edu/ollo/1-1-1_kr.png)

2. RC-100 의 무선 조종 신호를 받기 위해 조건 대기 명령어를 사용하여 새 무선 데이터가 도착할 때까지 대기합니다.  
  ([새 무선 데이터 도착에 대한 자세한 설명은 여기를 참고하세요.])

    ![](/assets/images/edu/ollo/2-1-1_kr.png)
    
    ![](/assets/images/edu/ollo/2-1-2_kr.png)

3. 새 무선 데이터가 도착하면 받은 무선 데이터를 로드 명령으로 받은데이터 라는 변수에 넣어줍니다.  
  ([변수에 대한 자세한 설명은 여기를 참고하세요.])

    ![](/assets/images/edu/ollo/3-1-5_kr.png)
    
    ![](/assets/images/edu/ollo/3-1-6_kr.png)
    
    ![](/assets/images/edu/ollo/3-1-7_kr.png)

4. 받은 무선 데이터의 값 중 RC-100 이동 조종 버튼값만 분리합니다.
  계산 명령어를 이용하여 받은데이터 값에 RC-100 의 U, L, D, R 버튼 값을 비트연산 & 를 통해 필요한 값만 분리하여 이동조종키 변수에 넣어줍니다.  
  계산 명령어 입력 ([계산 명령어에 대한 자세한 정보는 여기를 참고하세요.])
  
    ![](/assets/images/edu/ollo/4-5_kr.png)

    결과 란에 이동조종키 변수를 넣고, 연산 파라미터1 에 받은데이터 변수를 넣은 다음 연산자를 & (AND) 로 선택합니다.  
    
    ![](/assets/images/edu/ollo/4-5-1_kr.png)

    연산 파라미터2 에 RC-100 버튼 값으로 U/L/D/R 을 모두 선택하여 입력합니다. ([RC-100 버튼 값에 대한 자세한 정보는 여기를 참고하세요.])
    
    ![](/assets/images/edu/ollo/4-3-1_kr.png)

    입력을 완료하면 아래와 같습니다.
    
    ![](/assets/images/edu/ollo/4-3-2_kr.png)

5. 이동조종키 값에 따라 직진/후진/좌회전/우회전 합니다. 모든 이동조종키 버튼이 떼어지면 정지합니다.

    ![](/assets/images/edu/ollo/5-1_kr.png)

### 프로그램 다운로드

- 프로그램 다운로드 절차는 [프로그램 다운로드 를 참고]하세요.
- 프로그래밍 결과 파일 :  [bug_rc.tsk]

### 프로그램 실행 및 결과

프로그램을 실행 시킨 후 RC-100 조종기로 전/후/좌/우로 조종해 보세요.


[CM-100]: /docs/kr/parts/controller/cm-100/
[감속모터]: /docs/kr/parts/motor/gm-10a/
[USB 다운로더(LN-101)]: /docs/kr/parts/interface/ln-101/
[프로그래밍 학습]: ???
[OLLO_LineTrace.pdf]: ???
[OLLO_PuzzleRacing.zip]: ???
[RC-100]: /docs/kr/parts/communication/rc-100/
[버그 기본 프로그램]: ???
[태스크 코드로 제어하는 방법보기]: ???
[RC-100 적외선 채널 바꾸는 방법 보기]: /docs/kr/parts/communication/rc-100/
[서보모터]: /docs/kr/parts/motor/servo_motor/
[ZIG-100/110]: /docs/kr/parts/communication/zig-110/
[ZIG-110 set]: /docs/kr/parts/communication/zig-110/
[제어기]: ???
[큰타이어 세트]: ???
[제어기(CM-100)]: /docs/kr/parts/controller/cm-100/
[제어기 선택]: ???
[프로그램 시작]: ???
[무조건 반복]: ???
[로드]: ???
[중앙 적외선 센서]: ???
[화면 출력]: ???
[파라미터에 대한 설명]: ???
[태스크 코드 다운로드 방법]: ???
[RoboPlus Task]: /docs/kr/software/rplus1/task/getting_started/
[LN-101]: /docs/kr/parts/interface/ln-101/
[화면 출력하기 참조]: ???
[함수에 대한 보다 자세한 설명은 여기를 참고하세요.]: ???
[5. 복사/잘라내기/붙여넣기 참고]: ???
[프로그램 다운로드]: ???
[bug_move.tsk]: ???
[버그 움직이기]: ???
[만약 명령어에 대한 자세한 정보는 여기를 참고하세요.]: ???
[bug_linetracer.tsk]: ???
[라인트레이서용 인쇄물 다운 받기]: ???
[버그 라인 따라가기]: ???
[타이머의 자세한 설명은 여기 참조]: ???
[조건 대기 명령어에 대한 보다 자세한 정보는 여기를 참고하세요.]: ???
[소리감지 횟수에 대한 자세한 설명은 여기를 참고하세요.]: ???
[bug_sensor.tsk]: ???
[센서에 반응하는 버그]: ???
[새 무선 데이터 도착에 대한 자세한 설명은 여기를 참고하세요.]: ???
[변수에 대한 자세한 설명은 여기를 참고하세요.]: ???
[계산 명령어에 대한 자세한 정보는 여기를 참고하세요.]: ???
[RC-100 버튼 값에 대한 자세한 정보는 여기를 참고하세요.]: ???
[bug_rc.tsk]: ???