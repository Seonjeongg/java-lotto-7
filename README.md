# java-lotto-precourse

## 로또 발매기

1. 로또 구입 금액 입력 받기
- 출력: 구입금액을 입력해 주세요.
- 입력: 8000
- **1000원 단위**로 입력 
- 1000원 단위가 아닐경우 에러 처리 **([ERROR] 구입 금액은 1000원 단위로 입력해주세요.)** 후 다시 입력 받기
- 음수일 경우 에러 처리 **([ERROR] 구입 금액은 양의 정수로 입력해주세요.)** 후 다시 입력 받기

2. 당첨 번호 입력 받기
- 출력: 당첨 번호를 입력해 주세요.
- 입력: 1,2,3,4,5,6
- 번호는 *쉼표 기준*으로 구분
- 1~45 사이의 숫자가 아니면 **([ERROR] 로또 번호는 1부터 45 사이의 숫자여야 합니다.)** 에러 처리 후 다시 입력 받기
- 쉼표로 구분 안했으면 에러 처리 **([ERROR] 당첨 번호는 쉼표로 구분되어야 합니다.)** 후 다시 입력 받기
- 중복된 숫자인 경우 에러 처리 **([ERROR] 당첨 번호는 중복된 숫자일 수 없습니다..)** 후 다시 입력 받기

3. 보너스 번호 입력 받기
- 출력: 보너스 번호를 입력해 주세요.
- 입력: 7
- 1~45사이의 숫자 *1개* 입력 받기
- 범위 넘어가면 에러 처리 **([ERROR] 로또 번호는 1부터 45 사이의 숫자여야 합니다.)** 후 다시 입력 받기

4. 구입 금액에 해당하는 로또 발행 개수 파악
- 구입금액에서 나누기 1000 해서 개수 넘겨줌

5. 로또 발행
- 중복되지 않는 6개 숫자 선택
- `Randoms.pickUniqueNumbersInRange(1, 45, 6);`

6. 당첨 통계 계산
- 당첨 번호, 보너스 번호를 통해 발행한 로또 번호 비교 후 1등~5등 당첨 개수 파악

7. 수익률 계산
 - 당첨 통계를 통한 수익률 계산

8. 로또 발행 출력 하기
- 발행한 로또 리스트 출력

9. 로또 발행 개수 출력
- 출력: n개를 구매했습니다.

10. 당첨 통계 출력
- 출력 : 
~~~
당첨 통계
---
3개 일치 (5,000원) - 1개
4개 일치 (50,000원) - 0개
5개 일치 (1,500,000원) - 0개
5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
6개 일치 (2,000,000,000원) - 0개
~~~

11. 수익률 출력
- 출력: 총 수익률은 62.5%입니다.
- (총 당첨금/구입금액)%100