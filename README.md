# 스파르타 GIT 강의 정리
<br/><br/>

## 1주차(기본)

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

**cummit history**

    시간별 cummit 리스트
    
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
    
    로결repo에서 원격repo 연결

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

    1. [pull]: 원격repo cummit, 로컬에 업데이트
    2. 로컬 작업 진행(commit -> push)
        (초심자의 팁, 100%의 해결법이 아님, 추가 공부 필요)

---

    1. 원격repo, 로컬repo 연결

    - 로컬repo, 원격repo 연결: 로컬repo를 원격repo [tracking] 하도록 설정 

    -로컬 repo에 내용이 없는 경우: 원격 repo [clone]


    2. 원격repo와 로컬repo 존재 이유

    협업 시, 하나의 원격repo에 여러 로컬repo를 연결 시켜 하나의 프로젝트를 동시에 작업하는게 가능함.

---
<br/><br/>


## 2주차(협업)
---
<br/>

협업을 위한 Git 기본개념, 협업 Git 프로젝트, 기능별 작업내역 나누어 담기

****