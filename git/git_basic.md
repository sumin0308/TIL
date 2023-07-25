Git Basic
Git 코드 관리
git init, git commit, git push

1.git init
1) mkdir 디렉토리 생성
$ pwd -> 현재 위치 확인
$ mkdir practice -> practice 디렉토리 생성
$ ls -> 잘 생성되었는지 확인
$ cd practice -> practice 폴더로 이동
2) 'git init' 실행
$ git init
/practice/.git/ 안의 기존 깃 저장소를 다시 초기화했습니다.
$ git status -> git 상태 확인
3) 파일 생성
$ touch a.txt -> a.txt 파일을 practice 디렉토리 안에 생성
$ git add a.txt -> a.txt 파일을 stage 위에 올려놓음
$ git commit -m "add a.txt" -> a.txt 파일의 스냅샷을 "add a.txt" 라는 이름으로 찍음
 [master (최상위-커밋) 9c5e526] add a.txt
  1 file changed, 0 insertions(+), 0 deletions(-)
  create mode 100644 a.txt                        -> push 준비됨
2. repository 생성
GIthub 에서 + 버튼 클릭해서 New repository 생성
URL 복사 https://github.com/sin09135/practice
3. git remote
1) git remote add
% git remote add origin https://github.com/sin09135/My-first-Github-intro.git  -> github에서 생성한 repository 연결
2) git remote -v
% git remote -> remote 잘 되었는지 확인
origin -> 굿
% git remote -v   -> 자세히 알려줘
origin	https://github.com/sin09135/My-first-Github-intro.git (fetch)
origin	https://github.com/sin09135/My-first-Github-intro.git (push)
3) git push origin master
$ git push origin master 
 오브젝트 나열하는 중: 3, 완료.
 오브젝트 개수 세는 중: 100% (3/3), 완료.
 오브젝트 쓰는 중: 100% (3/3), 208 bytes | 208.00 KiB/s, 완료.
 Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
 To https://github.com/sin09135/practice.git
Git 협업
A,B 사람이 협업 한다고 가정

1. 폴더 지정(b)
1) cd ~  홈 폴더로 이동
$ cd ~
2) 팀 폴더 받아올 폴더 생성 후 다운로드
(1) git clone 폴더 받아오기

$ git clone 주소 지정폴더 이름
$ git remote -> 새로 등록할 필요 없음 이미 있음
origin 
2. 권한 부여 하기(a)
github 홈페이지 : collaboration -> 링크 전송

3. 파일 주고 받기
(1) git push 푸시 보내기
$ git add l.txt  -> 추가할 파일 stage에 추가
$ git commit -m "add l.txt" -> commit
[master 72e06c7] add z.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 z.txt

$ git push origin master -> push 보내기
(4) 폴더에 올려진 파일 받기
$ git pull origin master
같은 방식으로 번갈아 가면서 push,pull

Git 협업(파일)
1. 폴더 생성(a)
1) cd ~,mkdir
$ cd ~ 
$ mkdir wordchain  -> 끝말잇기 폴더 생성
2) git init
$ cd wordchain -> wordchain 폴더로 이동
$ git init -> git 시작
2. Visual Studio Code(a)
1) code . 열기
$ code . -> vscode 실행
2) 문서 편집 후 저장
README.md 파일 생성 후 저장

3) git push
$ git add README.md
$ git status -> git 상태 확인
$ git commit -m "데이터 추가"
$ git push origin master
3.폴더 지정(b)
1)git clone 폴더 받아오기
$ git clone 주소 지정폴더 이름
$ git remote -> 새로 등록할 필요 없음 이미 있음
origin 
2) 폴더 내에서 VScode 열기
$ cd 지정폴더
$ code .
4. 권한 부여하기(a)
github 홈페이지 : collaboration -> 링크 전송

5. 파일 주고 받기
1) 문서 편집 후 저장
README.md 파일 생성 후 저장

2) git
$ git add README.md
$ git status -> git 상태 확인
$ git commit -m "데이터 추가"
$ git push origin master
Git 주의 사항
프로젝트 받아올 때 현재 위치 확인
git 관리 받는 프로젝트 폴더 밑에 또 git 관리 파일,프로젝트 생성하지 않도록 주의
프로젝트 관리 시
프로젝트 복사 시에 git 해제 해야 함
