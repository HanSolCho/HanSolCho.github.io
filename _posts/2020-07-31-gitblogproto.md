---
title: 맨땅에 해당하기 Git Blog 시작하기
tags: gitHubBlog
categories : gitHubBlog
---

포스팅 테스트 겸 첫 포스팅입니다. 차후 가독성 보완 작업을 진행할것입니다.

첫 번째 포스팅! 깃 블로그 만들기

아무생각 없이 시간을 보내다보니 시간이 아까워서 블로그라도 시작해보자는 생각이 들어서 무작정 시작한 블로그만들기!!

내가 생각보다 git에 대해 모르고 사용하는데 미숙하다는 것을 생각한 순간 git blog로 시작하자고 마음을 먹었습니다;;

결과부터말하자면
<br>1.git repositories 만들기
<br>2.해당 repositories에 jekyll 추가하기
<br>3.Custom
<br>이 단계로 구분할 수 있고 필자는 현재 jekyll를 추가하고 개인적으로 Custom은 안하고 포스팅중임을 밝힙니다.

사실 이 포스팅은 스스로 복기할 겸 필자처럼 아예 처음부터하는 사람들에게 조금이나마 도움이 되기를 바라는 마음으로 시작하는 글임을 알립니다.

좀 더 정확하고 자세한 설명을 원하신다면 필자가 하단에 첨부한 참고한 블로그들을 읽어보시면 될것같습니다. 이 글을 제가 좀 더 막히거나 생각이 부족했던 부분을 기록하기 위한 포스팅입니다.


1. github repositories만들기

![alt-text](https://hansolcho.github.io/assets/image/repo_new_icon.PNG "이미지입니다")

깃허브에 회원가입을 하고 나서 위와 같은 화면에서 New 버튼을 누르게되면 새로운 repositories를 만들 수 있습니다.

![alt-text](https://hansolcho.github.io/assets/image/create_repo.png "이미지입니다")

위 사진과 같은 화면이 나오는데 repositories name을 "name".github.io라고 지어줍니다.
<br>제 경우에는 HanSolCho.github.io가 되는 것입니다.  즉 “name"의 자리에 HanSolCho와 같은 자신의 이름을 적어주면 됩니다.

<br>이 작업을 수행하고 나면 여러분은 https://"name".github.io 의 주소에 자신의 블로그를 만들었습니다.
<br>* Initialize this repository with a README 의 경우 자동적으로 홈페이지 주소가 적힌 README파일을 만들어주는 것으로 큰 의미는 없습니다.
이렇게 완성을하고 해당 블로그로 들어가게되면 README파일의 name.github.io 라는 문구만 적혀있는 블로그 화면을 볼 수 있을겁니다.

2. 자 그럼 이제 jekyll라는 것을 사용해서 블로그에 생기를 불어넣어봅시다.

[http://jekyllthemes.org/](http://jekyllthemes.org/)
<br>[https://github.com/topics/jekyll](https://github.com/topics/jekyll) 와 같은 곳에서 테마를 구경하고 원하는 테마를 선택하면 되겠습니다.

우선 저는 [https://github.com/mmistakes/minimal-mistakes](https://github.com/mmistakes/minimal-mistakes) 테마를 선택하였는데 이 글을 쓰는 지금도 완성한 내용을 기억하고 그 과정을 기록하기 위함이기에 처음 만들어본 예제에 대해서 글을 작성하도록 하겠습니다.
<br> cf)위 링크를 들어가게되면 README파일에 자세한 설명이 적혀져 있습니다. 한번 읽어보시는것도 이해하는데 도움이 될거라고 생각합니다.


![alt-text](https://hansolcho.github.io/assets/image/minimal_repo.png "이미지입니다")


자 해당 링크를 들어가서 표시된 부분을 클릭하게되면 위와 같이 보여지는데 본인이 작업할 디렉토리를 만들어서 git을 이용해서 clone을 해주어도 되고 직접 Download ZIP을 통해 받아도 괜찮습니다.

->git에 관해서는 천천히 공부해서 포스팅을 다시 하도록 하겠습니다.

해당 파일은 위에서 만들어준 repositories  폴더 내부에 압축을 풀어주시면 됩니다.
그렇게되면 HanSolCho.github.io-master 이와 비슷한 형식의 폴더와 그 내부는  
[https://github.com/HanSolCho/HanSolCho.github.io ](https://github.com/HanSolCho/HanSolCho.github.io)비슷한 형식으로 구성이 될것입니다.

모든 작업을 바로 웹으로 적용시키기에는 위험부담이 있으니 로컬에서 먼저 작업을 진행하고 github에 올리도록 하려면 로컬에서 개발이 가능해야합니다.
[https://rubyinstaller.org/downloads/ ](https://rubyinstaller.org/downloads/)에서 최신버전을 다운받았고 jekyll 테마를 압축해제한 폴더에 가보면 Gemfile이 형성 되어있을것입니다.
cmd를 통해 Gemfile이 있는 폴더에서 아래 명령어를 차례로 입력해주면

![alt-text](https://hansolcho.github.io/assets/image/rocal_git.png "이미지입니다")

![alt-text](https://hansolcho.github.io/assets/image/jekyll_serve.png "이미지입니다")

이렇게 로컬 서버에서 적용됨을 확인 할 수있습니다.
(bundler를 통해 변경된 내용을 적용하고 jekyll serve를 통해 서버를 동작시키는것같습니다.)
이때 성공적으로 진행이되ᄋᅠᆻ다면  http://localhost:4000/ 로 접근하게 되면 선택한 테마의 기본 화면을 볼 수 있습니다.
minimal-mistakes 테마의 기본 화면입니다.

![alt-text](https://hansolcho.github.io/assets/image/minimal_theme.png "이미지입니다")

이제 원하는 형식으로 테마를 수정해야합니다.
제가 참고한 김석진 님의 포스팅을 따라서 디자인을 진행하였고 제가 막혔던 부분들도 설명을 적어둘 생각입니다.

자 일단 repositories의 최상단에 위치한 config.yml파일로 들어가봅시다.

첫 번째로 테마에 관련된 부분들입니다.

![alt-text](https://hansolcho.github.io/assets/image/configfile.png "이미지입니다")

천천히 읽어보시면 어느부분을 고치면 본인이 원하는 곳을 수정할 수 있을지 알 수 있고
minimal-mistakes github에 가서 읽어보셔도 도움이 됩니다.

추가적인 설명을 조금만 하자면 다음은 블로그 왼쪽에 위치한 나에 대해서 적은 공간입니다.

![alt-text](https://hansolcho.github.io/assets/image/site_author.png "이미지입니다")

navigation bar라고 불리는 상단의 목록표입니다.

![alt-text](https://hansolcho.github.io/assets/image/navigation_bar.png "이미지입니다")

이를 위해서 /data/navigation.yml과 /config.yml, /pages를 수정하겠습니다.


![alt-text](https://hansolcho.github.io/assets/image/navigation_yml.png "이미지입니다")
/data/navigation.yml

여기서 타이틀은 화면에 보이지는 이름이고 url값이 경로를 의미합니다. 이 부분에서 pages폴더에 필요한 페이지 정보들을 삽입합니다.

이는 pages/category-archive.md 파일인데 peramalink값으로 navigation의 Categories의 url이 연결되어있을것임을 알 수 있습니다. 즉 navigation의 Categories를 클릭하면 url을 통해 category-archive.md파일의 peramalink와 연결되고 이는 layout에 지정된 categories라는 html파일을 불러오도록 되어있습니다.

필자는 개인적으로 이 부분에서 헷갈림이 있ᄋᅠᆻ습니다.

이제 config.yml을 수정합시다

![alt-text](https://hansolcho.github.io/assets/image/defaults.png "이미지입니다")
<br>최하단의 defaults: 부분을 다음과 같이 바꿔줍니다.

이제 가장 기본적인 블로그의 구현이 끝났습니다.

이후 새로운 글을 작성하고 싶다면 최상단에_post라는 폴더에 yyyy-mm-dd-name.md라는 형식으로 파일을 만들시면 됩니다.
아래 사진과 같이 title:제목, tags: 태그 항목에 보이고 싶은 내용, categories : 카테고리 항목에 보이고 싶은내용, 아래는 본문 내용을 적으면 됩니다.

![alt-text](https://hansolcho.github.io/assets/image/test_file.png "이미지입니다")


아 애시당초 본 포스팅이 복습개념과 정말 처음부터하는 사람이 헷갈릴 수 있다는 생각으로 만들었기에 로컬에서 작업한 내용을 git으로 올리는 부분을 기능적으로만 적어두겠습니다.

보통 처음 repository를 만들고 그 안에 들어가보면 다음과 같은 화면을 볼 수 있습니다.

![alt-text](https://hansolcho.github.io/assets/image/repo_page.PNG "이미지입니다")

우리는 이미 repository를 만들어 둔 상태이기에 2번째 안내를 따라서 진행하면 될겁니다.

git remote add orgin "https://"
<br>-> orgin이라는 이름으로 해당 주소와 연결해준다고 생각해주면 될것같습니다.
git push -u origin master
<br>-> orgin이라고 이름붙인 저장소의 master branch에 넣는다라고 생각하면 되는데 이 부분은 훗날 더 공부해서 따로 포스팅하도록 하겠습니다.

이후에는 내용이 변경될때마다
<br>git add .
<br>git commit -m "변경된 내용을 표시“
<br>git push
<br>와 같이 해주시면 될 것 같습니다. 이 부분은 git을 모르는 분들이 일단 블로그를 만들고 직접 볼 수 있도록 기능만 적은것이기에 훗날 추가적인 공부를 통해서 다시 포스팅 해보도록하겠습니다.




댓글과위젯,adminpage와 같은 기능들은 김석진님의 블로그를 참고하시는 것을 추천드립니다.
<br> [https://honbabzone.com/jekyll/start-gitHubBlog/](https://honbabzone.com/jekyll/start-gitHubBlog/)
<br>Minimal Mistakes 참고 사이트
<br>[https://mmistakes.github.io/minimal-mistakes/docs/configuration/](https://mmistakes.github.io/minimal-mistakes/docs/configuration/)

추가 참고 블로그
<br>[https://jetalog.net/86?category=808871](https://jetalog.net/86?category=808871)
<br>[https://zoomkoding.github.io/gitblog/2019/08/15/git-blog-1.html](https://zoomkoding.github.io/gitblog/2019/08/15/git-blog-1.html)
