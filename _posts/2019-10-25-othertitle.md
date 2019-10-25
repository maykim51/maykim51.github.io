---
title: "TIL - Today I Learned"
categories: 
    - til
tags:
    - til
    - scc
---

**2019/10/25**
오늘 내가 배운 것 🌟

WIP✏️✏️✏️




## 1. MySQL
* [codeanywhere.com](https://codeanywhere.com)
* 첫 사용법 (서버접속)
    **-uroot : use root(관리자)** 
    e.g. -umaykim51 (maykim51란 사용자 이용)
    
    ```
    $ mysql -uroot
    $ SET PASSWORD FOR 'root'@'localhost' = PASSWORD('YourNewPassword');
    exit
    ```
    비밀번호 설정됐으면 그 다음부터는

    ```mysql -u root -p```
    
    
### 구성요소
: 데이버베이스, 스키마 > 표  

* table 표
* database / schema 데이터베이스/스키마 
  : 표들을 그룹핑한것. A group of tables
* database server 데이터베이스 서버 (프로그램)

### DB의 효용
* 보안 
* 권한 기능

### 스키마 사용
 * 생성/삭제/보기
    ```
    $ CREATE DATABASE toreta;
    $ DROP DATABASE toreta;
    $ SHOW DATABASES;
    $ SHOW TABLES;
    ```

* 'toreta'라는 database를 사용하겠다 = 다음 명령어들은 'toreta'에 대해서 실행한다
    ```
    $ USE toreta;
    ```

### SQL(Structured Query Language)
: Database Svr(e.g. MySQL Server)에 얘기할때 사용하는 언어

### table
* 표 table
    * column,열 = data type, 구조 / row,record,행 = data 하나하나
    * 
* 표 생성
    ```
    $ CREATE TABLE topic(
        id INT(11) NOT NULL AUTO_INCREMENT,
        title VARCHAR(100) NOT NULL,
        description TEXT NULL,
        created DATETIME NOT NULL,
        author VARCHAR(30) NULL,
        profile VARCHAR(100) NULL,
        PRIMARY KEY(id)
    );
    ```
    *INT(11)*: 숫자를 11자리까지 노출시킨다
    *NOT NULL*: 행에 반드시 있어야 하는 열 (NULL이면 없어도 됨)
    *AUTO_INCREMENT*: 마지막 입력값보다 자동으로 +1 해준다
    *PRIMARY KEY(###)*: 행을 식별하는 항목


### CRUD
**INSERT INTO / SELECT \* FROM**
CR이 주로 중요함. UD는 안되는 경우도 있음. (회계, 역사, etc.)

* CREATE
    ```INSERT INTO topic (column 1, column 2...) VALUES (val1, val2...);```
        * DESC topic; 을 치고 구조에 맞게 업데이트
        * DESC: describe
        * auto_increment, NULL  항목은 생략하고 작성가능
    ```
    $ INSERT INTO topic (title, description, created,author, profile) VALUES('MySQL', 'MYSQL is...', NOW(), 'May', 'developer');
    ```
    *NOW()*: 현재 시각
* READ
    * ```SELECT * FROM topic;```




## 2. 2020 가트너 10대 전략기술...
[http://www.itworld.co.kr/news/134527](http://www.itworld.co.kr/news/134527)



## Others
* 'Cheat sheet'라는 검색어를 잘 이용하자


