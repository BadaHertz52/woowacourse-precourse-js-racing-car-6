# 자동차 경주

### mission-utils 사용

- [x] 입력값은 @woowacourse/mission-utils의 Console.Async, 출력은 Console.print 사용

## 기능 목록

### 1. 게임 설정

#### 자동차 클래스 생성

- [x] 경주할 자동차에 대한 상태를 관리하는 클래스 생성
  - [x] property : name(이름), movement(전진 횟수)

#### 경주할 자동차 설정

- [x] 쉼표를 기준으로 이름을 구분하여 자동차 이름 설정
  - [x] 안내문구 출력 :"경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)"
  - [x] 입력값 유효성 검사 : 5자 이하의 글자
  - [x] 형식 오류 시 throw문("[ERROR] 숫자가 잘못된 형식입니다.")으로 예외 발생 후 애플리케이션 종료
  - [x] 유효성 검사 통과 시, 입력한 자동차 이름 출력

#### 게임 횟수

- [x] 안내 문구 출력 :"시도할 횟수는 몇 회인가요?"
- [x] 사용자가 이동 횟수를 입력
- [x] 이동 횟수에 대한 유효성 검사 : 0 이상의 숫자
- [x] 입력한 이동 횟수 출력
- [x] 총 이동 횟수(totalRound), 현재 이동 횟수(currentRound) 설정

### 2. 게임 실행

#### 무작위 수 생성

- [x] @woowacourse/mission-utils의 Random.pickNumberInRange() 을 이용해 0-9 사이의 무작위 수 생성

#### 전진 판단

- [x] 무작위 수가 4이상 일 경우 전진
  - 해당 car의 movement에 이동 횟수 추가

#### 이동 횟수

- [x] 총 이동 횟수 만큼 게임을 반복 진행
- [x] 게임 진행 후 현재 이동 횟수 +1

#### 실행 결과 출력

- [x] 결과 출력 시, 자동차 이름과 함께 전진 횟수대로 "-"을 표기
      (ex: pobi 2번 전진=> pobi : -- )

### 3. 우승자 선정

- [x] 우승자 판별
  - 제일 많이 전진한 횟수를 기준으로 우승자 판별
- [x] 우승자 출력
  - ex: "최종 우승자 : pobi"
  - 여러명일 경우 쉼표를 이용하여 구분
    - 우승자 호명 순서는 차 이름 입력 순서대로
    - ex:최종 우승자 : pobi, jun
