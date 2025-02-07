1. 관계형 데이터베이스(RDBMS)와 비관계형 데이터베이스(NoSQL)의 장단점 비교

- **관계형 데이터베이스는** 정해진 스키마에 따라 데이터를 저장해서 명확한 데이터 구조를 보장하고, 데이터가 중복 저장되지 않는 장점이 있지만, 스키마로 인해 데이터가 유연하지 못하고 테이블간 관계로 인해 DB의 복잡성이 높아질 수 있는 단점이 있습니다.
- **비관계형 데이터베이스는** 일반적으로 관계형 데이터베이스보다 빠르고 유연하며 자유로운 데이터 구조를 가질 수 있는 장점이 있지만, 데이터 중복이 발생할 수 있으며 중복된 데이터가 변경 될 경우 수정을 모든 컬렉션에서 수행해야하는 단점이 있습니다.

2. 트랜잭션(transaction)이란 무엇인가요?

- **트랜잭션이란** 데이터베이스에서 트랜잭션이란 더 이상 쪼갤 수 없는 최소한의 작업 단위로, 오류로부터 안전하게 복구하여 데이터베이스의 일관성을 유지하기 위하여 사용한다. 데이터베이스의 트랜잭션이 안전하게 수행되기 위해서는 ACID 조건을 충족해야합니다.
    - ACID
        - 원자성: 트랜잭션은 DB에 모두 반영 or 모두 반영되지 않아야한다.
        - 일관성: 트랜잭션의 실행 이전과 이후의 데이터베이스의 상태는 동일해야 한다.
        - 고립성: 트랜잭션은 수행중일 때 다른 트랜잭션이 해당 작업에 끼어들지 못하도록 고립시켜야 한다.
        - 지속성: 트랜잭션이 성공적으로 완료되었으면 결과는 영구적으로 반영되어야 한다.

3. MySQL에서 조인(join)의 역할은 무엇인가요? 다양한 join의 방식에 대해 설명해주세요.

- **조인이란** 데이터베이스에서 두 개 이상의 테이블을 연결하여 데이터를 검색하는 방법입니다. 크게 내부조인, 외부조인이 있습니다.
    - (INNER) JOIN: 두 테이블의 중복되는 값(교집합)을 검색합니다. 표준 SQL과는 달리 MySQL에서는 JOIN, INNER JOIN, CROSS JOIN이 모두 같은 의미로 사용된다.
    - LEFT / RIGHT OUTER JOIN: 첫 번째(LEFT)or 두 번째(RIGHT)테이블 중 하나를 기준으로 join된 테이블과 중복되는 값을 검색합니다.

4. MySQL에서 인덱스(index)란 무엇인가요?

- **인덱스란** 추가적인 쓰기 작업과 저장 공간을 활용하여 데이터베이스 테이블의 검색 속도를 향상시키기 위한 자료구조로서 B+Tree가 일반적으로 사용됩니다.
