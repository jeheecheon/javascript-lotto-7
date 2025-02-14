# javascript-lotto-precourse

## 프로젝트 개요
이 프로그램은 간단한 로또 발매기입니다. 로또 번호(1~45) 중 중복 없는 6개 번호를 추첨하며, 사용자가 입력한 금액에 따라 로또 티켓을 발행합니다. 당첨 번호와 구매한 로또 번호를 비교해 당첨 결과와 수익률을 출력하며, 잘못된 입력에는 에러 메시지를 출력하고 재입력을 받습니다.

## 프로젝트 구조
📦 project-root  
├─ 📂 tests  
│ ├─ 📜 ApplicationTest.js  
│ └─ 📜 LottoTest.js  
├─ 📂 src  
│ ├─ 📂 constants  
│ │ ├─ 📜 errorMessages.js  
│ │ ├─ 📜 prizeAmounts.js  
│ │ └─ 📜 userMessages.js  
│ ├─ 📂 models  
│ │ ├─ 📜 Lotto.js  
│ │ └─ 📜 LottoGame.js  
│ ├─ 📂 utils  
│ │ ├─ 📜 ErrorHandler.js  
│ │ ├─ 📜 UserInterface.js  
│ │ └─ 📜 Validator.js  
│ ├─ 📜 App.js  
│ └─ 📜 index.js  


## 기능 목록
- [x] 사용자의 지불 금액 입력
- [x] 지불 받은 금액만큼 로또 생성
- [x] 당첨 번호 6개 쉼표로 구분한 입력
- [x] 보너스 번호 입력
- [x] 당첨 여부 계산
- [x] 수익률 계산
- [x] 당첨 여부 출력
- [x] 수익률 출력
- [x] 잘못된 값이 입력된 경우 "[ERROR]"로 시작하는 Error를 던지고 에러 발생지점부터 재시작

## 테스트 목록
- [x] 구입 금액 사용자 입력 1,000 으로 나누어 떨어지는 값인지 검증
- [x] 사용자의 당첨 번호 입력이 쉼표로 구분되었는지 검증
- [x] 사용자의 당첨 번호 입력이 중복되지 않는 숫자들인지 검증
- [x] 사용자의 보너스 번호 입력이 6개의 당첨번호화 중복되지 않는지 검증
- [x] 출력된 당쳠 결과가 올바르게 계산되었는지 검증
- [x] 출력된 수익률이 올바르게 계산되었는지 검증

## Lotto 클래스 단위 테스트
- [x] 로또 번호가 6개가 맞으면 로또 객체가 생성된다.
- [x] 로또 번호의 개수가 6개 초과이면 예외가 발생한다.
- [x] 로또 번호의 개수가 6개 미만이면 예외가 발생한다.
- [x] 로또 번호에 중복된 숫자가 있으면 예외가 발생한다.
- [x] 로또 번호에 숫자가 아닌 값이 있으면 예외가 발생한다.
- [x] 로또 번호에 1이상 45이하가 아닌 값이 있으면 예외가 발생한다.

## 실행 결과 예시
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

