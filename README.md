# 스파르타 GIT 강의 정리
<br/><br/>

## 1주차(git - 기본개념편)

<br/>

**GIT**
    
    버전 관리, 협업을 위한 관리 도구

**Github**
    
    원격 클라우드(컴퓨터)

---
<br/>

**버전 관리**

    cummit(커밋)을 통해 프로젝의 변경 정보(작성자, 시간, 변경내용) 저장

    (git은 가장 널리 쓰이는 버전관리 도구 중 하나, cummit을 사용)

**git 초기화(initialize)**

    프로젝트를 Git 관리하도록 만드는 것

**cummit**

    현재 프로젝트 상태 저장

    작성자(author), 시간, 프로젝트 변경 내용 으로 저장함.

    commit 마다 고유의 id값이 있어 조작가능함.
**cummit history**

    시간별 cummit
    
    프로젝트 cummit(버전)을 한번에 볼 수 있음.
    
![](https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F6811e22b-8abb-4831-8be8-512a704d5f73%2FUntitled.png?table=block&id=fa0600ad-754d-4e54-ba6a-1a1a3c384d29&spaceId=83c75a39-3aba-4ba4-a792-7aefe4b07895&width=1530&userId=&cache=v2)

------
<br/>

**repo**
    
    repository의 약자, 저장소

**로컬repo(local repo)**
    
    내 컴퓨터 저장소

**원격repo(remote repo)**   
    
    외부 컴퓨터 저장소, 다른 곳에서 접속 및 수정 가능

---

**추적(Tracking, branch Tracking)**
    
    로결repo에서 원격repo 연결, branch 단위로 연결한다. 
    (다른 branch의 commit들은 merge하지 않으면 서로 영향을 주지 않는다.)

    - 로컬repo와 원격repo 둘다 존재하는 경우
      -> Tracking(연결) 하면 됨.

    - 로컬 repo가 없고 원격repo에서 가져오는 경우
      -> 원격repo를 로컬repo에 clone함. 

    (원격repo와 로컬repo 존재 -> 하나의 원격repo에 여러 로컬repo를 연결 시켜 협업 가능하게 한다.)


**push(푸쉬)**
    
    로컬repo의 commit(커밋), 원격repo로 올림


**pull(풀)**
    
     원격repo의 commit(커밋), 로컬repo로 가져옴


**clone(클론)**:

    원격repo의 작업물 로컬repo에 복제함. (초기 다운로드), url을 통해 가져옴.

---
<br/>

**충돌(conflict)**<br>
    원격repo와 로컬repo에서 같은 파일 수정 시 발생
    (git에서 원격repo와 로컬repo의 파일 변경사항이 겹친다는 것을 알려주는 것이다.)

    1. - [pull]: 원격repo cummit내역, 로컬repo로 업데이트
       - 로컬 작업 진행(commit -> push)
    
    2. merge conflict(병합 충돌)
       -  두 branch에 하나의 file을 각각 수정 후 merge 시 발생
          -> commit에 저장된 file내역이 다르기 때문에 gitd에서 걸러주는 것임.

       - conflict 난 부분을 git에서 표시해줌 -> 확인 후 수정해 다시 merge하면 됨.
---
<br/><br/>


## 2주차(협업을 위한 git - 기본편)
---
<br/>

협업을 위한 Git 기본개념, 협업 Git 프로젝트, 기능별 작업내역 나누어 담기

원격 repo cummit, git graph로 확인 테스트

--- 

<br/><br/>

## 3주차(협업을 위한 git - 활용편)

### **목표)**

    1. 협업을 위한 작업 관리 스킬을 익힌다. - PR, commit 되돌리기(amend, revert, reset), 작업내역 임시저장 - stash

    2. 의사 소통이 잘 되는, 협업하기 좋은 사람이 되는  기본 협업 매너를 익힌다.

    3. Github로 다른 사람과 소통한다. - 포토폴리오, 오픈소스

    개발자스럽게 정보를 활용하고 의사소통하는 법을 배운다.

----

<br/><br/>

### 1) 협업을 위한 작업(commit)관리

    내 작업을 반영해달라고 요청하는 PR,

    commit을 되돌리기  - amend, revert, reset

    작업내역 임시 저장 - stash

<br/>

### 2) Git 프로젝트 관리 - 협업 매너

    좋은 작업내역을 남기기 위한 방법

     commit 단위 관리, 메세지 작성 - commit 메세지 컨벤션, gitignore
     
     다른사람에게 프로젝트 소개하는 방법 - README

<br/>

### 3) 오픈소스로 정보탐색 및 참여
    github에서 참고하기 좋은 코드, 기술 트랜드 정보 얻기 - github exprore

    오픈소스 - 오픈소스(open source)

<br/>

### 4) Github로 개발자인 나를 나타내자 - 포토폴리오


    Github로 profile, 프로젝트 소개, 개발 블로그 작성 방법 알기 
    - github profile, repo 소개, github page

---
<br/><br/>


## PR(Pull Request)

### 설명)

내 작업내역을 바로 merge하지 않고, 참여하고 있는 프로젝트에 
<span style="color:tomato">**내 작업내역(branch)를 merge해달라고 요청(Request)를 먼저 보내는 것**</span>이다. 

![](https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F7d02caad-ce28-4183-abb9-ca675ef3e3b6%2F3week.001.jpeg?table=block&id=cb9f793c-0cc7-4c33-bdc2-b693ef16a09d&spaceId=83c75a39-3aba-4ba4-a792-7aefe4b07895&width=1530&userId=&cache=v2)
**
작업한 내용에 대해 <span style="color:tomato">**코드 리뷰를 하거나 같이 토론하면서 개선**</span>시킬 수 있으며,<span style="color:tomato"> **프로젝트의 기준에 맞지 않을 시 reject(거부)</span>** 될 수 있다.

![](https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Ff77ad59a-3b71-4ec4-8582-6da031a6322a%2F3week.002.jpeg?table=block&id=0c123841-85c3-4374-9d67-ce87d2cb831a&spaceId=83c75a39-3aba-4ba4-a792-7aefe4b07895&width=1530&userId=&cache=v2)

이렇게 리뷰 후 작업을 최종 반영하면, 프로젝트 퀄리티가 놓아진다.<br>
기본적으로 프로젝트 품질을 관리하는 **회사**나, 여러 사람들이 참여하는 **오픈소스**에서는 작업 내역을 반영하기 위해 <span style="color:tomato">**PR 후 merge하는 과정**</span>을 거친다.
![](https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F03f8b856-6f99-46da-8435-115ead6c5a3a%2F3week.003.jpeg?table=block&id=40bdb70b-9d05-43e3-9dd5-b2da1bf5efac&spaceId=83c75a39-3aba-4ba4-a792-7aefe4b07895&width=1530&userId=&cache=v2)

<br/>

사용) <br/>
github페이지에서 PR날림.


