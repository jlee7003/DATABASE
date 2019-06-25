항목-> 필드명 자료형<p>

자료형 -> int ,char ,text
3.데이터 관리하기(입력,수정,분류,삭제)
//물건들은 예를 들어 물건테이블에 있는 것이고 물건을 등록하고 그후에 출력하는 것

명령어
show -> show databases;-데이터 베이스를 보여달라
drop -> 삭제(table)
create-> 생성 (데이터베이스 혹은 테이블) 
desc 테이블명 (필드보기)
select*from member; 테이블의 구조 보기
insert into 테이블명(필드명, 필드명, 필드명, 필드명) values('값', '값', '값', '값');
insert into member(name, phone, age, pay) values('anthony','01032757003',24,100000);

입력: insert
ex) insert into 테이블명(필드,필드) values('값',값);
보기: select*from member; 테이블의 구조 보기

create table imsi(id int auto)
//record => 한명의 정보
*수정과 삭제는 where가 무조건 필수
수정: update
ex) update 테이블명 set 필드명='바꿀값',필드명=바꿀값
    where 필드=값

삭제: delete
ex) delete from 테이블명 where 필드=값;
delete from "table name" where "field"='값'; 선택한 레코드만 삭제 !따옴표도 없애는 것!
ex) delete from guest where i

테이블 수정-> alter

use DB명 -> 사용할 DB결정

add column 항목 추가
ex) alter table friend add column id int auto_increment primary key;
 alter table friend drop column id int auto_increment primary key;
-> 중복허용 불가 

1.데이터베이스 생성, 접근
  show databases;-> 데이터베이스의 종류확인
create database; -> 생성



2.테이블의 생성, 수정
 생성전에 use 데이터 명을 입력
select : 검색
select 
resultset 데이터베이스의table 내용을 그대로 복사하여 가져오는것 


3.테이블 만들기
  create table명령을 실행
  create table member(id int auto_increment primary key, name char(10), title char(100), content text);

간단계시판

//레코드 데이터베이스에서의 한줄
rs.next()

1.테이블명 -> guest

2.항목 - id int auto_increment primary key -> 기본키
       - name char(10) -> 이름
       - tittle char(100) ->제목
       - content text -> 내용

3.select*from 테이블명 
 ->테이블에 입력한 정보 보는 법

-select 할때 조건을 붙이는 방법

  select * from guest where id="number"; //<,> 등도 사용가능 //아이디 값은 중복이 안되는 유일한 값
select * from member order age desc(내림차), name asc(오름차);
