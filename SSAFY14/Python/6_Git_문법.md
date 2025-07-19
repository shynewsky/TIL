# *️⃣ Git 문법

<br>

### ✅ Git 의 3가지 영역

1. Working Directory (WD) : 내가 작업하는 영역

2. Staging Area (Stage) : 작업 내역을 올려놓는 곳 (가상)

3. Repository (Repo) : 작업 내역을 저장하는 곳

<br>

### ✅ 작업 영역 설정

| | |
|:---:|:---:|
|git init|git 영역 설정|

<br>

* 해당 폴더 밑으로 하나의 프로젝트임을 선언

* 해당 폴더에 Repository를 만들기 위한 토목공사 실행

* 오른쪽에 (master) 단어가 뜨거나 `ls -a` 해서 git/ 이 뜨면 토목공사 완료

<br>

### ✅ 사용자 등록하기

| | |
|:---:|:---:|
|git config|git에 사용자 정보 전달|
|git config --global user.email "이메일주소"|github 아이디 연동|
|git config --global user.name "사용자이름"|github 사용자 연동|

<br>

### ✅ 작업내역 이동하기

| | |
|:---:|:---:|
|git add|WD→Stage 로 작업 내역 올리기|
|git commit|Stage→Repo 로 작업 내역 저장하기|
|git commit -m '메세지'|Stage→Repo 로 작업 내역과 메세지 저장하기|

<br>

### ✅ 작업내역 확인하기

| | |
|:---:|:---:|
|git status|Stage 에 올라온  작업 내역 확인하기  (commit 하기 전 사용)|
|git log|Repo 에 저장된 작업 내역 확인하기 (commit 한 후 사용)|

<br>

### ✅ 작업내역 비교하기

| | |
|:---:|:---:|
|git diff|Stage 에 올라온 작업 내역 비교하기|
|git log --oneline|Repo 에 저장된 작업 내역 비교하기|

<br>
<br>
<br>