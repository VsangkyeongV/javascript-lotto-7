# javascript-lotto-precourse
# 로또 발매기

이 프로젝트는 우아한테크코스 프리코스 3주차 과제인 **간단한 로또 발매기**입니다.

### 기능 목록
- [x] 로또 구입 금액 입력
- [x] 입력받은 로또 구입 금액만큼 로또 발행
- [x] 당첨, 보너스 번호 입력
- [x] 발행 횟수, 발행된 로또 출력
- [x] 기준에 따라 당첨 값 반환
- [x] 수익률 반환
- [ ] Error handling
  - 입력 틀리면 그 지점부터 다시 입력

#### ERROR CASE   
- 로또 구입 금액 입력
  - 입력 X  
  - 숫자 X
  - 천 원 단위 X
- 당첨 번호 문자열 입력
  - 입력 X
  - 숫자 X
  - 정수 X
  - 1 ~ 45 범위 X
  - 구분자 쉼표 X
  - 공백 포함
- 보너스 번호 입력
  - 입력 X
  - 숫자 X
  - 1 ~ 45 범위 X
  - 정수 X





### 피드백 반영 개인 목표
- [오류를 찾을 때 출력 함수 대신 디버거를 사용한다.](https://code.visualstudio.com/docs/editor/debugging)
  - 디버거를 잘 학습하고 활용해보자.
- 이름을 통해 의도를 드러낸다.
  - 숫자 덧붙이기X(aN), 불용어X(Info, data, a, an, the)  
  - 사용할 상수 이름, 함수 이름, 클래스 이름을 `README.md`에 미리 작성한다.
- 축약하지 않는다.
  - 클래스와 메서드 이름을 한 두 단어로 유지하려고 노력한다.
  - 문맥을 중복하는 이름을 자제하자.
    - `X: Order.shipOrder()`
    - `O: Order.ship()`
- JavaScript에서 제공하는 API를 적극 활용한다.
  - 함수를 구현하기 전에 API에서 해당 함수를 제공하는지 확인한다.
- 구현할 기능 목록을 잘 정리하고 변경사항이 있을 때 바로 최신화한다.
- 클래스는 필드, 생성자, 메서드 순으로 작성한다.
- 1메서드 1기능 (ex: 15라인 넘지 않도록 의식적으로 분리, 나만의 기준 세우기)
- 값을 하드 코딩하지 않는다. (대신 상수를 정의)   

### 학습 목표
- 관련 함수를 묶어 클래스를 만들고, 객체들이 협력하여 하나의 큰 기능을 수행하도록 한다.
- 클래스와 함수에 대한 단위 테스트를 통해 의도한 대로 정확하게 작동하는 영역을 확보한다.
- 2주 차 공통 피드백을 최대한 반영한다.

  ## 기능 요구 사항
- 로또 번호의 숫자 범위는 1~45까지이다.
- 1개의 로또를 발행할 때 중복되지 않는 6개의 숫자를 뽑는다.
- 당첨 번호 추첨 시 중복되지 않는 숫자 6개와 보너스 번호 1개를 뽑는다.
- 당첨은 1등부터 5등까지 있다. 당첨 기준과 금액은 아래와 같다.
  - 1등: 6개 번호 일치 / 2,000,000,000원
  - 2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원
  - 3등: 5개 번호 일치 / 1,500,000원
  - 4등: 4개 번호 일치 / 50,000원
  - 5등: 3개 번호 일치 / 5,000원
- 로또 구입 금액을 입력하면 구입 금액에 해당하는 만큼 로또를 발행해야 한다.
- 로또 1장의 가격은 1,000원이다.
- 당첨 번호와 보너스 번호를 입력받는다.
- 사용자가 구매한 로또 번호와 당첨 번호를 비교하여 당첨 내역 및 수익률을 출력하고 로또 게임을 종료한다.
- 사용자가 잘못된 값을 입력할 경우 "[ERROR]"로 시작하는 메시지와 함께 Error를 발생시키고 해당 메시지를 출력한 다음 해당 지점부터 다시 입력을 받는다.

### 실행 결과 예시
```js
구입금액을 입력해 주세요.
8000

8개를 구매했습니다.
[8, 21, 23, 41, 42, 43] 
[3, 5, 11, 16, 32, 38] 
[7, 11, 16, 35, 36, 44] 
[1, 8, 11, 31, 41, 42] 
[13, 14, 16, 38, 42, 45] 
[7, 11, 30, 40, 42, 43] 
[2, 13, 22, 32, 38, 45] 
[1, 3, 5, 14, 22, 45]

당첨 번호를 입력해 주세요.
1,2,3,4,5,6

보너스 번호를 입력해 주세요.
7

당첨 통계
---
3개 일치 (5,000원) - 1개
4개 일치 (50,000원) - 0개
5개 일치 (1,500,000원) - 0개
5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
6개 일치 (2,000,000,000원) - 0개
총 수익률은 62.5%입니다.
```
