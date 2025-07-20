# *️⃣ Git 문법

<br>

### ✅ Git 의 3가지 영역

1. Working Directory (WD) : 내가 작업하는 영역

2. Staging Area (Stage) : 작업 내역을 올려놓는 곳 (가상)

3. Repository (Repo) : 작업 내역을 저장하는 곳

<br>

### ✅ 로컬저장소 설정

| | |
|:---:|:---:|
|git init|git 영역 설정|

<br>

* 해당 폴더 밑으로 하나의 프로젝트임을 선언

* 해당 폴더에 Repository를 만들기 위한 토목공사 실행

* 오른쪽에 (master) 단어가 뜨거나 `ls -a` 해서 git/ 이 뜨면 토목공사 완료

<br>

### ✅ 작업내역 이동하기

| | |
|:---|:---|
|git add|WD→Stage 로 작업 내역 올리기|
|git commit|Stage→Repo 로 작업 내역 저장하기|
|git commit -m '메시지'|Stage→Repo 로 작업 내역과 메시지 저장하기|

<br>

### ✅ 작업내역 확인하기

| | |
|:---|:---|
|git status|Stage 에 올라온  작업 내역 확인하기  (commit 하기 전 사용)|
|git log|Repo 에 저장된 작업 내역 확인하기 (commit 한 후 사용)|

<br>

### ✅ 작업내역 비교하기

| | |
|:---|:---|
|git diff|Stage 에 올라온 작업 내역 비교하기|
|git log --oneline|Repo 에 저장된 작업 내역 비교하기(한줄로 요약)|

<br>
<br>
<br>

### ▶️ 원격저장소 만들기

1. Github 에 로그인하고 New Repository 를 생성한다

2. Repository name 을 작성한다 (로컬저장소의 이름과 일치시켜야 한다)

3. Public / Private 을 선택한다

4. 로컬저장소에서 먼저 프로젝트를 만든 경우에는 README.md 를 로컬저장소에서 먼저 만들고, <br> 원격저장소에서 먼저 프로젝트를 만든 경우에는 README.md 를 원격저장소에서 추가를 한다

5. 나머지 설정은 그대로 유지한 상태로 생성한다.

<br>

### ▶️ 원격저장소 계정 등록하기

| | |
|:---|:---|
|git config|git에 사용자 정보 전달|
|git config --global user.email "이메일주소"|github 아이디 등록|
|git config --global user.name "사용자이름"|github 사용자 등록|

<br>

### ▶️ 로컬저장소와 원격저장소 연동하기

| | |
|:---|:---|
|git remote add 별칭 원격저장소링크|로컬저장소를 원격저장소로 업로드|
|git clone remote 원격저장소링크|원격저장소를 로컬저장소로 다운로드|

<br>

| | |
|:---|:---|
|git remote -v|원격저장소로 올린 내용 확인|
|git remote remove 별칭|원격저장소로 올린 내용 삭제|

<br>

### ▶️ 변경사항 업로드하고 다운로드하기

| | |
|:---|:---|
|git push 별칭 master|로컬저장소 변경사항을 원격저장소에 업로드|
|git pull 별칭 master|원격저장소 변경사항을 로컬저장소에 다운로드|

<br>

### ▶️ 원격저장소에 올리면 안되는 로컬저장소 파일

| | |
|:---:|:---:|
|touch .gitignore|.gitignore 파일 생성|

    원격저장소에 push를 해도 업로드가 되지 않는 파일이다
    공개하면 안되는 key와 같은 파일과 폴더경로를 .gitignore 파일 안에 적어두면
    해당 파일과 폴더 경로는 push할떄 무시된다 

<br>
<br>
<br>

### ☑️ 가장 최신 버전을 수정해야 할떄

| | |
|:---|:---|
|git commit --amend -m "새 메시지"|가장 최신 버전의 메시지 변경하기|
|git add 변경사항 <br>git commit --amend|가장 최신 버전을 덮어씌우기|
|git add 변경사항 <br>git commit --amend -m "새 메시지"|가장 최신 버전을 덮어씌우고, 메시지 변경하기|

<br>

### ☑️ 타임라인 특정 지점(버전)을 수정해야 할때

| | |
|:---|:---|
|git revert #|특정 변경사항을 없애고, 저장됨. 직접 메시지 남겨야함|
|git revert no-edit #|특정 변경사항을 없애고, 저장됨. 자동으로 메시지를 남겨줌|
|git revert no-commit #|특정 변경사항을 없앰. 직접 저장하고 메시지 남겨야함|

<br>

### ☑️ 타임라인 특정 지점(버전)까지 모든 작업을 취소해야할 때

| | |
|:---|:---|
|git reset --soft #|Repo→SA 으로, 저장 직전(commit 직전)까지 시간을 되돌림|
|git reset --mixed #|Repo→WD 로, 작업 직후(add 직전)까지 시간을 되돌림(기본옵션)|
|git reset --hard #|Repo→WD 로, 작업 직전까지 시간을 되돌림|

<br>

### ☑️ 그 외 타임라인 수정 방법

| | |
|:---|:---|
|git restore|SA→WD 으로, add 한 상태를 되돌릴 수 있다<br>ctrl z와 같은 역할이지만, ctrl shrt z을 할 수 없다(비추)|
|git rm --cached|(1) SA에서 사용하면 WD로 내린다 (git restore와 같음) <br>(2) Repo에서 사용하면 작업은 그대로 남고 타임라인 기록만 삭제된다|

<br>
<br>
<br>
