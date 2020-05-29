# 1. SQL 기본 및 활용

### 1. SQL 문장들의 종류

- 데이터 조작어(DML : Data Manipulation Language)
  - SELECT : 데이터베이스에 들어 있는 데이터를 조회하거나 검색 하기 위한 명령어를 말하는 것으로 RETRIEVE 라고도 한다.
  - INSERT, UPDATE, DELETE : 데이터베이스의 테이블에 들어 있는 데이터에 변형을 가하는 종류의 명령어들을 말한다. 예를 들어 데이터를 테이블에 새로운 행을 집어넣거나, 원하지 않는 데이터를 삭제하거나 수정하는 것들의 명령어들을 DML이라고 부른다.
- 데이터 정의어(DDL : Data Definition Language)
  - CREATE, ALTER, DROP, RENAME : 테이블과 같은 데이터 구조를 정의하는데 사용되는 명령어들로 그러한 구조를 생성하거나 변경하거나 삭제하거나 이름을 바꾸는 데이터 구조와 관련된 명령어들을 DDL이라고 부른다.
- 데이터 제어어(DCL : Data Control Language)
  - GRANT, REVOKE : 데이터베이스에 접근하고 객체들을 사용하도록 권한을 주고 회수하는 명령어를 DCL이라고 부른다.
- 트랜잭션 제어어(TCL : Transaction Control Language)
  - COMMIT, ROLLBACK : 논리적인 작업의 단위를 묶어서 DML에 의해 조작된 결과를 작업단위(트랜잭션) 별로 제어하는 명령어를 말한다.

### 2. 데이터 유형

- CHARACTER(s)
  - 고정 길이 문자열 정보 (Oracle, SQL Server 모두 CHAR로 표현)
  - s는 기본 길이 1바이트, 최대 길이 Oracle 2,000바이트, SQL Server 8,000바이트
  - s만큼 최대 길이를 갖고 고정 길이를 가지고 있으므로 할당된 변수 값이 길이가 s보다 작을 경우에는 그 차이 길이만큼 공간으로 채워진다.
- VARCHAR(s)
  - CHARACTER VARYING의 약자로 가변 길이 문자열 정보 (Oracle은 VARCHAR2로 표현, SQL Server는 VARCHAR로 표현)
  - s는 최소 길이 1바이트, 최대 길이 Oracle 4,000바이트, SQL Server 8,000바이트
  - s만큼의 최대 길이를 갖지만 가변 길이로 조정이 되기 때문에 할당된 변수값의 바이트만 적용된다. (Limit)
- NUMERIC
  - 정수, 실수 등 숫자 정보 (Oracle은 NUMBER로, SQL Server는 10가지 이상의 숫자타입을 가지고 있음)
  - Oracle은 처음에 전체 자리 수를 지정하고, 그 다음 소수 부분의 자리 수를 지정한다.
- DATETIME
  - 날짜와 시각 정보 (Oracle은 DATE로 표현, SQL Server는 DATETIME으로 표현)
  - Oracle은 1초 단위, SQL Server는 3.33ms(millisecond) 단위 관리