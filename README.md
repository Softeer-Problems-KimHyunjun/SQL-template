### 버전 
v1

## 문제 제목
전담 에이전트 배정

## 문제 설명
소프티어 보험사에서는 고객의 전담 에이전트를 배정하려한다. 지금까지 연락을 했던 기록을 바탕으로 고객과 가장 많은 연락을 했던 에이전트를 점담으로 지정한다. 만약 연락 한 횟수가 동일하다면 연락 타입이 1(상담)이 많은 에이전트를, 그 또한 동일하다면 만족도 좋음이 더 많은 에이전트를 배정한다. 단, 연락을 한번도 하지 않은 고객과 회원탈퇴를 한 고객(is_active가 false), 퇴사한 에이전트는(is_active가 false) 제외 한다.

전담 에이전트가 배정된 고객의 이름, 전화번호, 전담 에이전트의 이름, 전화번호를 출력 하라. 고객 id를 기준으로 오름차순으로 정렬 해야 한다.

## 문제 해설
이 SQL 코드를 작성하기 위해서는 여러 고급 SQL 개념을 이해해야 합니다. 첫째로, 서브쿼리와 그룹화 함수(GROUP BY, COUNT, SUM 등)를 이해해야 ContactCounts를 생성할 수 있습니다. 둘째로, 윈도우 함수와 RANK()를 이용하여 파티션별 순위를 매기는 방법을 알아야 RankedAgents를 만들 수 있습니다. 셋째로, 조인(JOIN) 연산을 이해하여 여러 테이블의 데이터를 결합할 수 있어야 합니다. 마지막으로, WHERE 절과 ORDER BY를 활용하여 필터링과 정렬을 할 수 있어야 최종 결과를 얻을 수 있습니다.