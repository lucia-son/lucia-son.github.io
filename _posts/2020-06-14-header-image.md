---
layout: article
title: 우당탕탕 블로그 만들기
tags: [Blog, GithubPage]
---

## Git hub

남들이 아이패드병에 걸릴 때
왜 나는 **깃허브 블로그 병**에 걸려서는
이틀에 걸쳐 만든 깃허브 블로그,
윈도우에서 여러 가지를 깔고 지우며 만든 과정을 기록하려고 한다

### Make Local Directory & Git hub repository

0. 일단 과정에 들어가기에 앞서! 본인의 운영체제에 맞는
   Git, Ruby 를 설치한다!
   Git을 설치하면 **Git bah**가
   Ruby를 설치하면 **Start Command Prompt with Ruby**를 실행할 수 있다.

1. Github에 로그인하여 'NEW repository'로 레파지토리를 만든다.
   이때 레파지토리명은 "본인의 github아이디명.io"로 설정한다.
2. 그리고 내 컴퓨터에 원하는 위치에 원하는 이름으로 폴더를 생성한다.
3. Git bash에서 다음과 같이 실행한다.

```
"내 로컬 컴퓨터에 만들어 놓은 로컬 디렉토리 주소로 이동"
$ cd C:\giblog

"git 시작하고 이메일과 이름 선언"
$ git init
$ git config --global user.name "(본인 이름)"
$ git config --global email 이메일
$ git clone "(해당 폴더에clone시키려는 깃허브 레파지토리 주소)"
"깃허브에 올라가 있는 링크 복사하여 git clone으로 가져오기/특별한 접근권한필요없음"
```

이 과정까지 끝나면
Git hub에 있는 빈 repo(repository)를
내 로컬 컴퓨터의 비어있는 디렉토리에
똑같이 동기화를 시키는 과정(clone)까지 마무리가 된 상태이다!

### jekyll과 Bundler

4. Start Command Prompt with Ruby 에서 내 로컬 컴퓨터의 디렉토리 위치로 이동한 다음,
   다음과 같이 실행한다.

```
$ gem install jekyll
$ gem install bundler
```

### 테마 적용

5. 블로그에 테마를 적용하려면, github에서 원하는 jekyll 테마를 골라서 해당 스타일의 최신 저번 zip 파일을 다운받고 내가 내 컴퓨터에 만들어 놓은 로컬 디렉토리 안에 압축을 푼 채로 넣어 놓는다.
   이 과정은 콘솔없이 흔히 알집으로 압축풀기 과정과 동일하게 진행하면 된다.

6. Start Command Prompt with Ruby 에서 내 로컬 컴퓨터의 디렉토리 위치로 이동한 다음, 다음과 같이 실행하여 jekyll을 실행시킨다.

```
$jekyll serve
```

이때 파일의 버전이 낮다고 하거나, 의존성(DEPENDANCY)문제가 발생했다는 메시지가
뜨기도 하는데, 이때 나는 RACK의 버전이 낮다고 했고 직접 수정하기 위해
GUI로 \_config.yml 파일에 들어가서 rack의 버전 관련 명령어를 수정했다.

```
server runnig
```

위와 같은 문구로 끝나면 성공되었다!
웹브라우저 주소창에 localhost:4000 을 입력하여 사이트를 확인할 수 있다.

### 완성된 블로그를 git으로 옮기기

7. 이제 다시 Git bash로 돌아와 다음과 같이 명령어를 실행한다.

```
git add .
git commit -m "making new blog"
git push
```

[Notion:Git toddler](https://www.notion.so/iamlucia/Git-Toddler-1-1f38831536684ed29f36aa99e3573ea5)
