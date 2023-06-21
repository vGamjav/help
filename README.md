# 앱개발하는 감자 도움말

## 당부의 말

- 이해하는 것보다 익숙해지는 게 큽니다. 가능한 오랜 시간 컴퓨터로 삽질하십시오.
- 튜토리얼보다는 **무엇을 삽질해야 하는가**에 대한 글이라고 생각해주세요.
- 공부해야 할 키워드 위주로 작성했습니다.

## 오류가 발생하면

- **당황하지 않는 것이 가장 중요합니다. 절대 포기하지 마세요.**
- 영어로 나오는 오류문을 읽으세요. 해결책을 오류문 안에서 소개해주는 경우가 많습니다.
- 고민해도 안나오면 가장 중요한 부분을 구글에 복붙하십시오.
- 개발자스럽게 생각하십시오. 문제의 원인은 생각보다 간단할 수 있습니다.
  - 예) 192.168.XX.XX : Wifi 문제
- 다 해봤지만 안 되면 질문하십시오. 역으로 삽질 안 해보고 질문하지 마십시오. 개발과 친해질 수 없습니다.

> 1 ~ 9는 순서대로 하는 것을 권장하지만, 꼭 그럴 필요 없습니다. 그때 자기가 재미있어보이는 걸 하면 됩니다. React Native & Expo로 바로 개발해보고 싶다면 그렇게 해도 무방합니다. 하나를 꼭 끝내고 다른 걸 해야할 필요도 없습니다.

## 1. 깃허브와 친해지기

```shell
$ git init
$ git add .
$ git commit -m "XXXXX"
$ git remote add origin https://github.com/XXXXX
$ git remote -v
$ git remote remove origin
$ git push -u origin main
$ git pull
$ git clone https://github.com/XXXXX
```

- 처음이기 때문에 브랜치(`git branch`, `git checkout`, `git merge`, `git rebase` 등)과 관련된 글은 읽지 않으셔도 됩니다.
- 하루 개발의 처음과 끝은 반드시 `git pull`과 `git push`여야 합니다. pull & push를 두려워하지 마세요. 생활화하세요.

> 과제 : vGamjav Organization이나 개인 계정에 자신만의 토이 프로젝트(길어도 3일 안에 끝낼 수 있는 아주 간단한 주제. C, C++, Python, HTML, JavaScript, 백준, 프로그래머스 등 아무 주제나 괜찮음) 공부 레포를 파서 Github에 commit & push를 최대한 많이 해보십시오.

## 2. 마크다운과 친해지기

- 지금 쓰고 있는 `README.md` 파일이 마크다운입니다.
- 워드/한글을 간소화한 버전이라고 생각하십시오.

> 과제 1 : 자신이 판 레포에서 `README.md` 파일 _예쁘게_ 작성해보기

> 과제 2 : 깃허브의 View Raw 기능을 활용하여 지금 이 `README.md`가 실제로 어떻게 생겨먹은건지 보십시오.

> 과제 3 : 자신의 깃허브 계정 프로필을 예쁘게 꾸며보기

## 3. 쉘, Vim과 친해지기

### 쉘

- 쉘이란 검은색 명령어 창을 의미합니다.
- 다음의 명령어가 무슨 의미인지 찾아보세요.

```shell
$ ls
$ pwd
$ cd ..
$ mkdir DIRECTORYNAME
$ rm -rf DIRECTORYNAME # 삭제 명령어입니다. 휴지통에 가는게 아니라 영구삭제라 그냥 막 쓰진 마세요
```

```shell
$ echo $SHELL
$ source ~/.zshrc
$ source ~/.vimrc
```

### Vim

- Vim이란 개발자를 위한 메모장입니다.
- 사실 VSCode를 많이 쓰지만 `~/.zshrc`, `~/.vimrc`와 같이 설정 파일을 수정하는 경우에는 Vim을 사용합니다.

```shell
$ vi ~/.zshrc
$ vi ~/.vimrc
```

> 과제 : `~/.zshrc`에 각종 플러그인을 설치하여 **예쁘게** 꾸며보세요.

## 4. VSCode와 친해지기

- 사실 대부분의 개발은 VSCode에서 진행됩니다.
- zsh를 꾸민 것처럼 VSCode를 꾸밀 수도 있습니다. [노마드코더 프로처럼 VSC 세팅하기](https://www.youtube.com/shorts/cdqULOmORVU) 영상을 보고 한번 꾸며보세요!

```shell
$ code .
```

> 과제 : VSCode 예쁘게 꾸미기

## 5. (윈도우를 사용한다면) WSL과 친해지기

- WSL은 골치가 아픈 존재입니다. 하지만 웹이나 앱개발을 하고 싶다면 반드시 깨고 넘어가야 할 산입니다.

공부하면 좋은 키워드는 다음과 같습니다.

- 가상머신의 원리
- WSL이 돌아가는 원리

---

> 여기서부터는 사이트 개발과 연관된 내용입니다.

## 6. React와 친해지기

- **사실 단기간에 할 수 있는 일이 아닙니다. (잘 이해 안된다고 주눅들지 마세요. 저도 이 부분에서 빠르게 이해할 수 있을지 의문이네요.)**

React를 이해하기 위해서는 다음의 선수지식이 필요합니다.

- HTML, CSS로 페이지 짜보기
- JavaScript를 추가하여 페이지 짜보기 [노마드코더 Momentum 클론코딩](https://nomadcoders.co/javascript-for-beginners?utm_medium=website&utm_source=webpage&utm_campaign=roadmap)
- JSX가 무엇인지 이해하기 [노마드코더 ReactJS로 영화 웹 서비스 만들기](https://nomadcoders.co/react-for-beginners/lectures/3281)

### React 프로젝트 폴더 구조에 친해지기

- `package.json` 파일이 하는 일에 대해 이해하세요.
- Web Router가 작동하는 원리에 대해 이해하세요. (`index.XXX`)

> 과제 : 위의 링크에서 소개된 강의 들어보기

## 7. React Native와 친해지기

### expo

- react-native-cli의 쉬운 버전입니다.
- Expo Go를 이용하여 자신의 휴대폰으로 실시간으로 반영되는 걸 보면서 개발해보세요.
- _이런 기술이 있다니.. 늦게 태어난 것에 감사합니다._

> 과제 : React Native를 이용하여 TODO 앱을 개발해보세요. (이건 나도 해야됨)

## 나가며

- 막상 글로 적어보니 이걸 다 공부하는게 무리인 것 같네요. **앱 개발에 진짜로 관심이 있는 사람이 아니면 이걸 다 공부하는게 과연 앞으로의 커리어에 맞을지도 의문이 들고요. 결국 결정은 자기가 하는겁니다. 강요하지 않습니다.** 스스로 하고 싶으면 하세요.
- 절대 자신이 못한다고 생각하지 마세요. (삽질하면서 익숙해지는데에는 당연히 시간이 걸립니다.)
- 자신이 공부하거나 프로젝트하는 걸 반드시 vGamjav Organization이나 자신의 개인 레포지토리에 올려주세요. 자주 들어가서 진척도를 본 뒤 어느정도 익숙해졌다 싶으면 앱 개발 프로젝트를 이어나갈지, 앱 개발을 접고 다른 프로젝트를 할지 등등... 에 대해 고민해보도록 합시다.
