# Git

> Git은 소스코드 형상(버전)관리 도구이다.



## 기본명령어

1. 저장소(`repository`) 만들기

   ```bash
   $git init
   Initialized empty Git repository in /Users/baky/TIL/.git/
   
   TIL git:(master)
   ```

   내가 원하는 폴더를 git으로 관리하는 저장소로 초기화한다.

   (master) 라는 표기를 통해 해당 폴더가 git repository라는 것을 확인 할 수 있다.(더 정확하게는 해당 폴더에 숨김폴더로 .git이 있다.)

2. `git add` - 커밋할 목록에 추가하기

   ```bash
   $git add .
   
   $git status
   On branch master
   
   No commits yet
   
   Changes to be committed:
     (use "git rm --cached <file>..." to unstage)
   
   	new file:   Git.md
   ```

   `git add git.md` 라고 하면, 특정 파일만 올릴 수 도 있고, `git add myFolder/` 라고 하면, 특정폴더를 모두 담아둘 수 도 있다.

3. 커밋

   ```bash
   $git commit -m '커밋메시지'
   
   #오류나면
   git config --global user.email '유저이메일'
   git config --global user.name '유저아이디명'
   해서 git 설정합시당.
   
   ```

   커밋은 버전의 이력을 남기는 것이다. 커밋할 목록에 있는 내용들을 버전에 포함시킨다.(untracked / 목록에 없는 것은 포함 안됨.)

   

4. 커밋 이력 확인하기

   ```bash
   $git log
   
   commit fcf6b702082fd75a8955ba9d2dffd332b1a354cb (HEAD -> master)
   Author: baky94 <baky94@naver.com>
   Date:   Tue May 21 12:37:32 2019 +0900
   
       커밋메세지
       
   ```

   

5. **git 상태 확인하기**

   ```bash
   $git status
   ```

   CLI(Command Line Interface)에서는 현재 상태를 확인 하기 위해서 지속적으로 확인해야 한다.

6. 