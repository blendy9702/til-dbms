# 데이터베이스 모델링 및 ERD 및 MySQL 활용하기

- MySQL (DBMS 8.x.ver)
  : RDBMS 를 다룬다. (Ralation : 관계)

## 1. 요구사항 분석

- 회의를 참석하면 (회의록)
- 회의록 검토 후 각 사항을 요구 사항 분석 (요구사항 정의서, 업무지시서)

## 2. 요구사항 분석을 하는 이유

- 각 내용의 속성을 찾고, 분류
- 분류 된 내용을 모아서 Entity 를 생성한다.
- Entity 는 Entity 간의 관계를 찾는다.
- 요구사항 정의서 작성

### 2.1. 요구사항 분석 예

- 고객은 고객코드 , 고객명 , 전화번호 , 이메일, 주소(기본주소 , 상세주소), 지역 , 가입일로 되어있다
- 고객은 지역별로 관리되도록 한다 .
- 지역은 지역코드와 지역명으로 되어 있고 지역명은 대한민국의 지역코드 (02:서울특별시)를 이용한다
- 한 지역에는 여러 고객이 있을 수 있다
- 제품은 제품코드 , 제품명 , 제품색상 , 가격으로 되어있다
- 하나의 제품은 여러 색상을 가질 수가 있다
- 고객은 등록된 제품을 구매 할 수 있다
- 한 명의 고객은 여러 제품을 구매 할 수 있고 , 하 나의 제품은 여러 고객이 구매 할 수 있다
- 고객이 제품을 구매 시 구매수량과 구매일자를 기록한다

### 2.2. 요구사항 정의서 또는 업무 기술서 (회사마다 포맷이 다르다.)

![Image](https://github.com/user-attachments/assets/0e7b4767-88fb-4376-b149-544b2f40c84e)

### 2.3. 속성(Attribute) 찾기 후 Entity 정의하기

- 설계 전문가는 Entity 정의 후 속성을 선별해 나간다.
- 신입 데이터 베이스 설계자는 Arribute를 선별 후 Entity 를 정의함.

#### 2.3.1. Entity 항목정리

: 명사소문자 추천
![Image](https://github.com/user-attachments/assets/193054d3-5190-4eac-bf37-e8785b673ce6)

#### 2.3.2. Entity 와 Entity 의 관계 정리

: 동사소문자 추천
![Image](https://github.com/user-attachments/assets/0e462426-eb64-493c-81b5-810288b9184e)

## 3. ERD 그리기

### 3.1. 개념적 모델링

- Entity-Relationship-Diagram
- E-R 다이어그램

![Image](https://github.com/user-attachments/assets/ca593cfa-eae0-4283-abf0-bb6d1a9d9332)

- 고객
  ![Image](https://github.com/user-attachments/assets/63881746-a650-4797-9148-3c20c6f4368a)

- 고객 PK 후보
  ![Image](https://github.com/user-attachments/assets/1d090d23-0264-4834-a68a-804e04674385)

- 지역
  ![Image](https://github.com/user-attachments/assets/417da956-10de-4811-96fd-5381ac7a72bf)

- 제품
  ![Image](https://github.com/user-attachments/assets/62372148-8ef5-4eb8-bd68-6897a5aa7caf)

### 3.2. Relation 표현하기

- 개체와 개체가 맺고 있는 연관성을 표현
  ![Image](https://github.com/user-attachments/assets/7ab6e272-28cb-432f-b653-086cc914327e)

#### 고객은 제품을 구매한다.

![Image](https://github.com/user-attachments/assets/19e3aa97-b5b8-4c11-866c-a2b474110ed8)

![Image](https://github.com/user-attachments/assets/52580bc0-f446-4c1f-a239-d034cb654fcb)

## 4. Logical Data Modeling(논리적 모델링)

- 개념적 스키마를 표형식 또는 테이블 형식으로 표현
- Entity 의 속성 데이터 타입, 길이, null 허용여부, 기본값, 제약 조건 등을 세부적으로 작성 후 문서화
- 즉 `테이블정의서` 를 생성함 (도구는 다양함)
  ![Image](https://github.com/user-attachments/assets/3022ae94-ee28-4c29-b1e5-1fbd84ee4854)
