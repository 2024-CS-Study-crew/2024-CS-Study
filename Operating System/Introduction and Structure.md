# 운영체제 소개

## 일상생활 속의 운영체제

### 운영체제

- 일반 컴퓨터, 노트북, 스마트폰의 전원을 켜먼 가장 먼저 만나게 되는 소프트웨어
- 컴퓨터 관리를 위한 기본적은 규칙과 절차를 규정하여 컴퓨터 내의 모든 하드웨어(컴퓨터 자원)와 응용 프로그램을 관리
- ex) pc 운용체제(윈도우, Mac OS, 유닉스, 리눅스 등), 모바일 운영체제(iOS, 안드로이드 등)

### 임베디드 운영체제

- CPU 성능이 낮고 메모리 크기도 작은 시스템에 내장하도록 만든 운영체제
- 임베디드 운영체제가 있는 기계는 기능을 계속 향상할 수 있음
    - 업그레이드가 가능하다 : 스마트폰처럼!
    - 요즘은 냉장고에서 노리고 있음

## 운영체제의 정의

- 응용 프로그램이나 사용자에게 컴퓨터 자원을 사용할 수 있는 인터페이스를 제공, 그 결과를 돌려주는 시스템 소프트웨어
- 응용 프로그램이나 사용자에게 모든 컴퓨터 자원을 숨기고 정해진 방법으로만 컴퓨터 자원을 사용할 수 있도록 제한
- 커널 : 운영체제의 핵심 기능만 모와 놓은 것


- 임베디드 시스템에도 운영체제가 필요하다. 유저가 하드웨어에 접근 가능하도록 하며 사용자 인터페이스도 가능하게 만듦, HW 관리, 즉 자원 관리도 할 줄 알아야 한다.

## 운영체제의 역할

1. 자원 관리 (효율성)
    - 컴퓨터 시스템의 자원을 **응용 프로그램**에 나눠줘 사용자가 원활하게 작업할 수 있도록 함
    - 자원을 요청한 프로그램이 여러 개라면 적당한 순서로 자원을 배분하고 적절한 시점에서 자원을 **회수**하여 다른 응용 프로그램에 나눠줌
        - 적당한 순서란? 컴퓨터 내부에 정책으로 정의되어 있다.
2. 자원 보호 (안정성)
    - 비정상적인 작업으로부터 컴퓨터 자원을 보호
    - 보안이 중요하다
    - ex) 정전시 어떻게 처리하냐? ATM기의 경우 돈 뺏길 때 어캄..?
3. 하드웨어 인터페이스 제공 (확장성)
    - 사용자가 복잡한 과정 없이 다양한 장치를 사용할 수 있도록 해주는 하드웨어 인터페이스 제공
    - CPU, 메모리, 키보드, 마우스와 같은 다양한 하드웨어를 일관된 방법으로 사용할 수 있도록 지원
4. 사용자 인터페이스 제공 (편리성)
    - 사용자가 운영체제를 편리하게 사용하도록 지원
    - ex) 윈도우의 그래픽 사용자 인터페이스 (GUI)

## 운영체제의 목표


1. 효율성
    - 자원을 효율적으로 관리하는 것
    - 같은 자원을 사용하여 더 많은 작업량을 처리하거나 같은 작업량을 처리하는 데 보다 적은 자원을 사용하는 것 (목표)
2. 안정성
    - 작업을 안정적으로 처리하는 것
    - 사용자와 응용 프로그램의 안전 문제와 하드웨어적인 보안 문제 처리
    - 시스템에 문제가 발생했을 때 이전으로 복구하는 fault-tolerance 기능
3. 확장성
    - 다양한 시스템 자원을 컴퓨터에 추가하거나 제거하기 편리하게 하는 것
    - 새로운 기능의 효과적인 개발을 허용하게 하는 것
        - HW 위주
4. 편리성
    - 사용자가 편리하게 작업할 수 있는 환경을 제공하고 편리한 인터페이스 제공

# 운영체제의 발전

1. 초창기 컴퓨터 (1940년대)
    - 에니악
        - 백열전구 같은 모양의 진공관이라는 소자를 사용하여 진공관이 켜지면 1, 꺼지면 0이라고 판단
        - 전선을 연결하여 논리회로를 구성하는 ‘하드와이어링’ 방식으로 동작
        - 운영체제가 없음
2. 일괄작업 시스템 (1950년대)
    - 천공카드 시스템(홀러리스)
        - **천공카드 리더**를 입력 장치로 **라인 프린터를 출력장치**로 사용
        - 프로그램을 구성한 후 카드에 구멍을 뚫어 컴퓨터에 입력하면 프로그램이 실행되는 구조로서 프로그램의 실행 결과가 라인 프린터를 통해 출력
        - 혹은 일괄 처리 시스템 - batch job system
            - 작업 준비 시간을 중리기 위해 요구 사항이 비슷한 여러 개의 작업을 모아 한꺼번에 처리하는 것
        - 모든 작업을 한꺼번에 처리하고 프로그램 실행 중간에 사용자가 데이터를 입력하거나 수정하는 것이 불가능한 시스템
        - 운영체제 사용
            - 메인 메모리가 운영체제의 상주 영역과 사용자 영역으로 나뉨
        - 상주 모니터
            - 자동 작업 순서에서 하나의 작업에서 다른 작업으로의 진행을 자동으로 제어하는 프로그램
3. 대화형 시스템 - interactive system
    - 모니터와 키보드의 등장 : 프로그램이 진행되는 도중에 사용자로부터 입력을 받을 수 있어 입력값에 따라 작업 흐름을 바꾸는 것이 가능한 시스템
    - 온라인 시스템이라고도 함
    - 대화형 시스템의 등장으로 문서 편집기, 게임과 같은 다양한 종류의 응용 프로그램을 만들 수 있게 됨
    - 멀티프로그래밍 시스템
        - 동시에 기억 장치에 적재(load)시켜 CPU가 다른 프로그램을 수행할 수 있게 함 → CPU 유휴시간을 줄이고 처리량 극대화
        - 기억장치 관리 기법이나 CPU 스케줄링 기법 필요
        - **전반적인 시스템 성능은 향상!(목표)** but 하나의 프로그램의 실행 성능 향상은 불가능!
4. 시분할 시스템 (1960년대) time sharing system
    - cpu 사용 시간을 잘게 쪼개어 작업들에 나누어줌으로써 모든 작업이 동시에 처리 되는 것처럼 보임
    - 한 조각을 **타임슬라이스** 또는 **타임 퀀텀**
    - 시분할 **시스템의 목적은 응답 시간을 최소화하**고 사용자로 하여금 자신만이 컴퓨터 시스템을 독점하여 사용하고 있는 듯이 느끼게 만드는 것
    - 오늘 날의 컴퓨터에는 대부분 시분할 시스템이 사용
    
    **실시간 시스템(Real-Time System)**
    
    - 단말기나 제어 대상으로부터 처리를 요구하는 자료가 발생할 때마다 **즉시 처리하여 제한 시간 안에 응답**하는 방식
    - 대개 **은행**, 공장, 기차와 **비생기 좌석 예약** 등 **특수 목적** 외에 멀티미디어 로봇 제어, 가상 현실 등의 응용 분야에서의 **제어장치로 사용**
    - 특징
        - 자료가 발생한 지점에서 단말기를 통하여 직접 입출력 되는 형태
        - 자원을 효율적으로 사용하는 것보다 신속하게 응답하는 것이 중요
        - 자료가 무작위로 도착하므로 자료의 일시 저장과 대기가 필요
        - 특정 상태의 **재현 불가**
            - 오류 시 재현 불가, Script 대로 동작하지 않음
        - 시스템에 장애가 발생 할 때 단순한 재실행 불가
5. 분산 시스템 (1970년대 후반) Distributed system
    - 개인용 컴퓨터와 인터넷이 보급되면서 값이 싸고 크기가 작은 컴퓨터를 하나로 묶어서 대형 컴퓨터의 능력에 버금가는 시스템을 만들 수 있게 됨
    - 네트워크 상에 분산되어 있는 여러 컴퓨터로 작업을 처리하고 그 결과를 상호 교환 하도록 구성한 시스템
6. 클라이언트/서버 시스템 (1990~현재)
    - 웹 시스템이 보급된 이후 일반인들에게 알려짐
    - 작업을 요청하는 클라이언트와 거기에 응답하여 요청받은 작업을 처리하는 서버의 이중구조로 나뉨
    - 문제점 : 모든 요청이 서버로 집중되어 서버 과부하 됨. 이를 피하려면 많은 서버와 큰 용량의 네트워크가 필요
7. P2P 시스템(2000년대 초반~현재)
    - 클라이언트/서버 구조의 단점인 서버 과부하를 해결하기 위해 만든 시스템
    - 서버를 거치지 않고 사용자와 사용자를 직접 연결
    - 냅스터(mp3공유 시스템)에서 시작하여 현재는 메신저나 토렌트 시스템에서 사용
    - 불법 소프트웨어 기술 규제 때문에 발전하지 못하다가 메신저 프로그램에 도입되어 큰 발전을 이룸
    - 완전한 P2P 시스템의 예 : 블록 체인
        - 블록 체인 기술의 활용 : NFT -  자신의 유일성을 증명하는 수단
8. 기타 컴퓨팅 환경 (2000년대 초반~현재)
    - 클라우드 컴퓨팅
        - 언제 어디서나 응용프로그램과 데이터를 자유롭게 사용할 수 있는 컴퓨팅 환경으로 그리드 컴퓨팅과 SaaS를 합쳐 놓은 형태
        - 클라우드 컴퓨팅은 PC, 핸드폰, 스마트 기기 등을 통하여 인터넷에 접속하고 다양한 작업을 수행하며 데이터 도한 기기들 사이에서 자유롭게 이동이 가능한 컴퓨팅 환경
        - 하드웨어를 포함한 시스템이 구름에 가려진 것처럼 사용자에게 보이지 않는 컴퓨팅 환경이라는 의미
    - 사물 인터넷
        - 사물에 센서와 통신 기능을 내장하여 인터넷에 연결하는 기술
        - 예 : 전철이나 버스의 도착 예정시간을 표기, 각종 전자제품을 스마트폰으로 제어
        - 인터넷으로 연결된 사물들이 데이터를 주고 받아 스스로 분석하고 학습한 정보를 사용자에게 제공하거나 새로운 서비스를 창출

# 운영체제의 구성

## 커널과 인터페이스

1. 커널
    - 프로세스 관리, 메모리 관리, 저장장치 관리와 같은 운영체제의 핵심적인 기능을 모아놓은 것
2. 인터페이스
    - 커널에 사용자의 명령을 전달하고 실행 결과를 사용자에게 알려주는 역할
    - 그래픽을 사용한 인터페이스를 GUI라고 부름

## 시스템 호출과 디바이스 드라이버

1. 시스템 호출
    - 응용 프로그램이 커널에 접근할 수 있도록 커널이 제공하는 인터페이스는 API라고도 함
    - 커널이 제공하는 시스템 자원의 사용과 연관된 함수
    - 응용 프로그램이 하드웨어 자원에 접근하거나 운영체제가 제공하는 서비스를 이용하려 할 때는 시스템 호출을 사용해야 함
    - 운영체제는 커널이 제공하는 서비스를 시스템 호출로 제한하고 다른 방법으로 커널에 들어오지 못하게 막음으로써 컴퓨터 자원을 보호
2. 드라이버
    - 커널과 하드웨어의 인터페이스 담당하며 디바이스 드라이버라고도 불림
    - 마우스와 같이 간단한 제품은 드라이버를 커널이 가지고 있으나, 그래픽카드와 같이 복잡한 하드웨어의 경우 제작자가 드라이버를 제공함

## 커널의 역할과 종류

1. 커널
    
    
    | 핵심 기능 | 설명 |
    | --- | --- |
    | 프로세스 관리 | 프로세스에 CPU를 배분하고 작업에 필요한 제반 환경을 제공한다. |
    | 메모리 관리 | 프로제스에 작업 공간을 배치하고 실제 메모리보다 큰 가상공간을 제공한다 |
    | 파일 시스템 관리 | 데이터를 저장하고 접근할 수 있는 인터페이스를 제공한다 |
    | 입출력 관리 | 필요한 입력과 출력 서비스를 제공한다 |
    | 프로세스 간 통신관리 | 공동 작업을 위한 각 프로세스 간 통신 환경을 지원한다. |
2. 단일형 구조 커널
    - 초창기 운영체제 구조
    - 커널의 핵심 기능을 구현하는 모듈들이 구분 없이 하나로 구성
    - 장점
        - 모듈 간의 통신 비용이 줄어들어 효율적인 운영이 가능
    - 단점
        - 모든 모듈이 하나로 묶여 있기 때문에 버그나 오류를 처리하기가 어려움
        - 운영체제의 여러 기능이 서로 연결되어 있어 상호 의존성이 높기 때문에 기능상의 작은 결함이 시스템 전체로 확산될 수 있음
        - 다양한 환경의 시스템에 적용하기 어려움
            - HW의 환경 변화시 유연한 대처 불가능
        - 현대의 운영체제는 매우 크고 복잡하기 때문에 완전 단일형 구조의 운영체제를 구현하기가 어려움
3. 계층형 구조 커널 == Layered 아키택처
    - 비슷한 기능을 수행하는 모듈을 묶어서 하나의 계층으로 만들고 계층 간의 통신을 통해 운영체제를 구현하는 방식
    - 시스템을 계층으로 나누면 시스템 설계나 구현 단순해짐
    - 계층의 정의가 쉽지 않음, 표준안이 없다.
4. 마이크로 구조 커널
    - 커널에는 프로세스 관리, 메모리 관리, 프로세스 간 통신 관리 등 가장 기본적인 기능만 포함하고 기타 기능은 사용자 영역에서 수행
    - 커널의 각 모듈은 세분화되어 존재하고(모듈화 정도가 높음), 모듈 간의 정보 교환은 프로세스 간 통신을 이용하여 이루어짐
    - 커널 내부에서의 지연이 적고 예측 가능하여 실시간 시스템에 활용
    - 모듈간 통신이 빈번하여 성능이 떨어질 수 있음
    - 현대 운영체제에서 가장 많이 사용된다.
5. 가상머신
    - 운영체제와 응용 프로그램 사이에서 작동하는 프로그램
    - 가상머신을 설치하면 응용 프로그램이 모두 동일한 환경에서 작동하는 것처럼 보임
    - 자바는 유닉스와 윈도우에서 작동하는 다양한 가상머신을 만들어 배포하는데 이를 자바 가상머신이라고 함
    - 서버 가상화: 물리적 서버 하나에 가상 서버를 여러 개 구성하는 방법

# 유닉스와 리눅스

1. 유닉스의 개발과 확산
    - 1969년 AT&T의 멀틱스 프로젝트에 참가 중이던 켄 톰프슨이 PDP-7 컴퓨터에 멀틱스와 비슷한 개념의 운영체제를 구현하고, 이 운영체제의 이름을 골치 아픈 멀틱스 대신 단순하다는 의미의 ‘유닉스’로 지음
    - 개발 후 소스코드가 공개되어 기능이 추가되었고 이식하기 쉬웠던 탓에 인기를 얻게 됨
2. 리눅스의 개발
    - 1991년에 리누스 토르발스가 PC에서 동작하는 유닉스 호환 커널을 작성하여 GPL로 배포하고 이어서 소스코드도 공개한 것이 리눅스의 시작
3. 안드로이드
    - GNU의 리눅스 커널을 사용하여 제작되었기 때문에 GPL을 따름
    - 누구나 공짜로 사용할 수 있고, 새로운 버전과 동시에 소스코드도 공개하기 때문에 누구나 수정·배포할 수 있음
4. 애플 II의 등장
    - 1977년에 애플에서 만든 애플 II는 개인용 컴퓨터의 시초로 키보드, 메인보드, 전원장치가 하나로 합쳐진 일체형 모델
    - 애플 II가 보급되면서 전문가만 사용하던 고가의 컴퓨터를 일반 대중도 사용할 수 있게 되고 다양한 하드웨어와 소프트웨어의 개발로 이어짐
5. Mac OS와 iOS
    - 마하 커널을 기반으로 하는 Mac OS를 사용한 컴퓨터 등장. Mac OS의 강점은 마우스를 이용하는 그래픽 사용자 인터페이스(GUI)를 처음 도입했다는 것
    - Mac OS를 수정한 iOS가 적용된 스마트폰인 아이폰 출시. 아이폰은 세계 최초로 멀티터치스크린 장착
    - 이것을 사용자 인터페이스보다 더 사용자 친화적이고 경험에 중심을 두는 기술로 UX(User eXperience)라고 부름
        - 행동으로 무엇인가 한다.
6. 윈도우의 출시
    - 마이크로소프트는 애플 Mac OS의 그래픽 사용자 인터페이스에 자극을 받아윈도우 운영체제를 출시하고 계속 업그레이드하여 현재는 버전 11까지 나와있음


---
# 예상 질문 List

## 1. 컴퓨터 시스템을 계층적으로 표현할 때, (상위) 사용자-> 응용프로그램 -> 유틸리티 프로그램 -> 하드웨어 (하위)입니다. 이 중 운영체제의 위치는 어느 부분에 해당되나요? 

유틸리티와 하드웨어 사이입니다.  

## 2. 운영체제 설계 시 계층적 접근 방법의 장점이 뭔가요?

계층적 접근 방식이란 비슷한 기능을 수행하는 모듈을 묶어서 하나의 계층으로 만들고 계층 간의 통신을 통해 운영체제를 구현하는 방식입니다. 이를 통해 시스템을 계층으로 나누면 시스템 설계나 구현 단순해질 수 있습니다.
하지만 계층의 정의가 쉽지 않으며 표준안이 없는 단점이 있습니다.

## 3. 가상 머신은 운영체제와 응용 프로그램 사이에서 작동하는 프로그램입니다. 이 때 가상머신의 장점을 예시와 함께 설명해주세요. 

가상 머신의 장점은 응용 프로그램이 다양한 운영 체제나 환경에서 실행할 수 있도록 하여 호환성과 일관성을 제공합니다.

자바 가상 머신의 경우 자바 프로그램이 유닉스와 윈도우 같은 다른 운영 체제에서도 실행될 수 있게 해줍니다. 이를 통해 개발자는 특정 운영 체제에 종속되지 않고 동일한 코드를 여러 플랫폼에 배포할 수 있으며 개발 생산성을 높이고 응용 프로그램의 이식성을 향상시킵니다.

또한, 가상 머신은 시스템 리소스를 분리하여 응용 프로그램 간의 간섭을 줄여주고 보안성을 향상시킬 수도 있습니다.
