# java-lotto-precourse


## 요구사항
1. 함수의 길이가 15라인을 넘어가지 않도록 구현
    + 함수가 한 가지 일만 잘 하도록 구현

2. else, switch/case 사용 x

3. JAVA Enum 을 적용하기

4. 구현한 기능에 대한 단위 테스트
    + UI (System.out, System.in, Scanner) 로직은 제외

5. 제공된 Lotto 클래스를 사용하여 구현
    + numbers 이외의 필드를 추가할 수 없음
    + numbers의 접근 제한자 변경 불가
    + Lotto의 패키지 변경 가능

## 구현 기능 목록
1. 구입 금액을 입력받는다.
+ 숫자 앞에 공백이 있다면 제거한다.

2. 입력받은 금액을 검증한다.
+ 음수,0,그 외 문자열 입력에 대해서 '[ERROR] 정상적인 입력이 아닙니다.' 메시지를 넣어 IllegalArgumentException을 발생시킨다.
+ 1000원으로 나누어 떨어져야 한다. 
+ 10만원을 초과하는지 검증한다. (회차당 최대 10만원을 초과하여 판매 및 구매할 수 없음)

3. 입력받은 금액을 가공한다.
+ Amount 클래스로 래핑한다.

4. 몇 개를 구매했는지 구한다.
+ 복권 가격 으로 나눈 몫을 복권의 갯수로 한다.

5. 구매한 갯수를 출력한다.

6. 복권 수 만큼 1~45의 랜덤한 숫자 6개를 배열에 생성한다. 
+ 배열 내부의 숫자 6개는 중복되면 안된다.
+ 배열 내부를 오름차순으로 정렬한다.

7. 복권 숫자들을 출력한다.

8. 당첨 번호 6개를 입력받는다. 번호는 쉼표(,)를 기준으로 구분한다.
+ ,로 구분한 후 공백을 제거한다. 
+ 1~45사이의 숫자가 아닌 경우 '[ERROR] 정상적인 입력이 아닙니다.' 메시지를 넣어 IllegalArgumentException을 발생시킨다.
+ 중복 유무를 검사하고 중복인 경우, '[ERROR] 정상적인 입력이 아닙니다.' 메시지를 넣어 IllegalArgumentException을 발생시킨다.

9. 보너스 번호를 입력받는다.
+ 1~45사이의 숫자가 아닌 경우 '[ERROR] 정상적인 입력이 아닙니다.' 메시지를 넣어 IllegalArgumentException을 발생시킨다.
+ 입력한 보너스 번호가 입력한 당첨 번호에 존재할 경우, '[ERROR] 정상적인 입력이 아닙니다.' 메시지를 넣어 IllegalArgumentException을 발생시킨다.

10. 당첨을 구한다.
+ 3개 일치
+ 4개 일치
+ 5개 일치
+ 5개, 보너스 숫자 일치
+ 6개 일치

11. 수익률을 계산한다.

12. 당첨 결과와 수익률을 출력한다.

## To do
+ 에러 메시지 집중화
+ Enum 활용하기 (등수?)
+ 당첨 결과 출력 println 도배 해결
+ 리팩토링
+ 요구사항 충족 확인