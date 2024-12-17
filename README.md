# 증권사 OPEN API를 이용한 자동 매수/매도 서비스 

## 1. 프로젝트 : Rich Beagle
* 증권사 커뮤니티 기능과 OPEN API를 이용한 자체 제작 주식 자동 매수/매도 서비스

## 2. 구성
* **안드로이드 App(Kotlin)**
  * **나의 매수 금액 관리**
    * 매수 금액/투자금 설정 조회
    * 1회 최저 매수 금액 설정
    * 1회 최대 매수 금액 설정
    * 나의 총 투자금 규모 설정
  * **잔고 조회 관리**
    * 잔고 조회
    * 계좌 예수금 조회
    * 증권사 유저 보유 수량 수동 설정 
  * **안전 매도 모드 관리**
    * 안전 모드 ON 목록 조회
    * 안전 모드 STATUS 조회
    * 안전 매도 ON/OFF 설정
    * 전체 안전 매도 타입 조회
    * 안전 매도 타입 설정(ALL/HALF/QUARTER)
  * **양전(+) 매도 모드 관리**
    * 양전 매도 모드 상태 조회
    * 양전 매도 모드 ON/OFF
    * 양전 매도 타입 설정(ALL/HALF/QUARTER)
  * **손익 조회 관리**
    * 국내 주식 손익 조회
    * 해외 주식 손익 조회
  * **팔로우 유저 관리**
    * 팔로우 유저 조회
    * 국내 팔로우 유저 추가
    * 해외 팔로우 유저 추가
  * **거래 관리**
    * 팔로우 거래 ON/OFF 설정
    * 국내 주식 거래 ON/OFF 설정
    * 해외 주식 거래 ON/OFF 설정 
  * **수동 주문**
    * 커뮤니티 수동 주문
    * 한국투자증권 수동 주문
  * **보유 주식 조건 주문**
    * 조건 주문 내역 조회
    * 조건 주문 MODE ON/OFF
    * 조건 주문 설정 
* **텔레그램**
  * 안드로이드 App의 요청 수신
* **파이썬 서버(Flask)**
  * **Notification REST API 서버**
  * **Scheduler**
    * 주식 잔고 내역 update
    * 안전 매도
    * 양전 알림
  * **Telegram Message Reader**
    * 텔레그램 메시지 기반 REST API 전송
 
## 3. 대표 기능 
* **Telegram 서버**
* **자체 제작 한국투자증권 OpenAPI 라이브러리**
* **방어 로직**
  * 안전 매도
  * 투자금 대비 비율 보정
  * 오알림 필터링

## 4. 트러블 슈팅
* **안드로이드 앱->내부망 서버 요청 보안 처리**
* **REST API & Scheduler 간 동시성 문제**
* **안드로이드 알림 MQ**

