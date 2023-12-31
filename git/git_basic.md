# Git

코드를 관리하는 도구(버전을 통해)

* 코드 관리도구
* 코드 협업도구
* 코드 배포도구



## Git 명령어

`git [명령어]`

## (1) git init

Git으로 코드 관리를 시작

* 코드 관리 단위(기준): 폴더
* `(master)` : ~~~현재 브랜치명~~~
* `.git` 폴더 생성: Git이 관리와 관련된 파일



## (2) git status

현재 상태를 출력(Git에게 현재 상태를 물어봄)

* `git init` 직후

  ```
  On branch master
  -> master라는 브랜치 위에 있어요.
  No commits yet
  -> 아직 commit이 없어요.
  nothing to commit (create/copy files and use "git add" to track)
  -> commit할 것이 없어요. (설명충)
  ```

  

* `test.txt` 파일 생성 후,

  ```
  Untracked files:
  (use "git add <file>..." to include in what will be committed)
  test.txt
  -> 추적되지 않은 파일이 있어요.
  (파일명)
  nothing added to commit but untracked files present (use "git add
  -> commit 하기 위해 add된 것이 없어요. 그러나 추적되지 않은 파일은 있어요.
  ```

  

* `git add text.txt` 직후,

  ```
  Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
  new file: test.txt
  -> commit할 변경들이 있어요.
  (파일명)
  ```

  

* `git commit` 이후,

  ```
  nothing to commit, working tree clean
  -> commit 할 게 없어요. 작업 폴더는 깔끔해요.
  ```

  

* 파일 수정후,

  ```
  On branch master
  Changes not staged for commit:
  -> commit하기 위해 stage 되지 않은 변경 사항이 있어요.
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  modified: test.txt
  no changes added to commit (use "git add" and/or "git commit -a")
  ```

  

## (3) `git add [파일명]`

commit을 위한 stage

* `git add .` : 현재 폴더의 모든 변경 사항 stage



## (4) `git commit -m "커밋 메시지"`

> commit == 버전을 생성 == 현재상태의 스냅샷 촬영

* 처음으로 commit을 할 경우,

```
Author identity unknown
-> 작자미상
*** Please tell me who you are.
-> 당신이 누군지 알려주세요.
Run
-> 아래의 명령어를 실행주세요.
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```



* `git config` 설정 후( `vim` 에디터 창),

```
# Please enter the commit message for your changes.
-> 변경사항에 대한 commit message를 입렵해주세요.
# Lines starting with '#' will be ignored, and an empty message aborts the
commit.
-> #로 시작하는 라인은 무시됩니다. 아무것도 없는 메시지는 종료됩니다.
# On branch master
#
# Initial commit
#
# Changes to be committed:
# new file: test.txt
```



## (5) `git config`

Git에 관한 설정

* `git config --global user.email "이메일"` : global(전역으로) user의 email을 설정

* `git config --global user.email` : 설정값 확인



## (6) `git log`

현재까지의 commit을 출력

* `git log` 출력화면

```
commit 1a7d9384d2f9a064e2ddb4719306defeb51ac3cf (HEAD -> master)
Author: John Kang <hphk.john@gmail.com>
-> 작성자
Date: Tue Mar 16 15:55:10 2021 +0900
-> 날짜
first commit
-> 커밋 메시지
```



* `git log --oneline` : 한줄로 출력

  ```
  7c7abf0 (HEAD -> master) Add title
  1a7d938 first commit
  ```



## (7) `git remote`

* git remote add [저장소이름] [저장소주소] : git remote add origin https://github.com/hkeryfonttlxisdrlw/basic_git
  * git에게 원격저장소(remote) 추가(add)를 명령
* 저장소이름: `origin`
* 저장소주소: https://github.com/hkeryfonttlxisdrlw/basic_git

## add

`git add 파일명`

=> 깃허브에 올리고 싶은 파일명을 입력한다.(ex. git add a.txt 하면 a.txt가 만들어진다.)



## ls

ls를 쳐서 파일이 제대로 만들어졌는지 확인한다. 



## status

git status 를 쳐서 상태를 확인한다.

ex) $ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   c.txt
        new file:   d.txt
        new file:   e.txt
        new file:   f.txt
        new file:   g.txt
        new file:   h.txt
        new file:   i.txt
        new file:   j.txt
        new file:   k.txt





## commit

`git commit -m "Add 파일명"`

=> 커밋하고 싶은 파일을 입력한다.

## remote

`git remote` 를 해서 origin 이 뜨는 것을 확인한다.





## push

`git push origin master`

=> 마스터에 push 해서 올린다.(최종단계: 깃 해당 사이트에 f5를 눌러 파일이 올라갔는지 확인해본다.)
