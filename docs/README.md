# 다리 건너기

## 기능 목록

### 입력
- [x] 자동으로 생성할 다리길이를 입력받는다.
- [x] 라운드마다 플레이어가 이동할 칸을 입력 받는다.
- [x] 게임 재시작/종료 여부를 입력 받는다.

### 출력
- [x] 게임 종료 문구를 출력한다.
- [x] 게임 시작 문구를 출력한다.
- [x] 사용자가 이동할 때마다 다리 건너기 결과를 출력한다.
  - 이동할 수 있는 칸을 선택한 경우 O 표시
  - 이동할 수 없는 칸을 선택한 경우 X 표시
  - 선택하지 않은 칸은 공백 한 칸으로 표시
  - 다리의 시작은 [, 다리의 끝은 ]으로 표시
  - 다리 칸의 구분은 |(앞뒤 공백 포함) 문자열로 구분
  - 현재까지 건넌 다리를 모두 출력
- [x] 예외 상황 시 에러 문구 출력한다.

### 핵심 기능
- [x] 입력받은 길이로 다리를 생성한다.
  - 0과 1 중 무작위 값으로 생성
  - 0을 아래칸 D로 1을 위칸 U로 변환한다.
- [x] 플레이어가 이동한 칸이 건널 수 있는지 확인한다.
  - 건널 수 있다면 O, 건널 수 없다면 X
- [x] 다리를 끝까지 건너면 게임 성공이다.
- [x] 다리를 건너다 실패하면 재시작하거나 종료할 수 있다.
  - 재시작해도 처음에 만든 다리로 재사용한다.
  - 게임 결과의 총 시도한 횟수는 첫 시도를 포함해 게임 종료까지 시도한 횟수를 나타낸다.

## 예외
- 다리길이 입력이 올바르지 않을 경우
  - [x] 입력값이 숫자가 아닌 경우
  - [x] 입력값이 3이상 20이하의 숫자가 아닌 경우
- 이동할 칸 입력 시
  - [x] 입력값이 U or D가 아닌 경우
- 게임 재시작/종료 여부 입력 시
  - [x] 입력값이 R or Q가 아닌 경우

### 주의사항
- 사용자가 잘못된 값을 입력할 경우 예외처리 후 그 부분부터 입력을 다시 받는다.