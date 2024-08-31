# oop2024fall
OOP course @ HNU CE (2024 fall)

## Links
수업 노트 관련
  - https://github.com/forax/java-guide 이 온라인 강의노트를 참고로 내용 선택 및 더 필요한 내용 추가

프로그래밍 환경 관련
  - [GitHub Codespace 문서](https://docs.github.com/ko/codespaces) 깃헙 코드스페이스는 클라우드를 통해 제공되는 개발환경
  - https://github.com/jupyter-java 주피터 환경에서 자바를 사용하기 위한 환경 설정 관련 내용 정리
    - [JBang: 자바 개발 환경 설치를 간편하게 해주는 관리 도구](https://www.jbang.dev/)
    - [rapaio-jupyter-kernel 1.3.0 깃헙 저장소](https://github.com/padreati/rapaio-jupyter-kernel/tree/fd3a64a483b6b731783818395deb677fbfbe208c) 수업시간에 활용하는 자바 커널 버전
  - https://blog.jetbrains.com/ko/datalore/ Datalore 관련 JetBrains사의 블로그 글들
    - [Datalore란 무엇인가요?](https://blog.jetbrains.com/ko/datalore/2020/11/02/what-is-datalore/)

프로그래밍 언어 관련
  - https://docs.oracle.com/en/java/javase/21/ JDK 21 문서
    - [JDK 21이 출시되었다. 최신 문법 보고 가요](https://velog.io/@dongvelop/JDK-21%EC%9D%B4-%EC%B6%9C%EC%8B%9C%EB%90%98%EC%97%88%EB%8B%A4.-%EC%B5%9C%EC%8B%A0-%EB%AC%B8%EB%B2%95%EC%9D%80-%EC%82%B4%ED%8E%B4%EB%B4%90%EC%95%BC%EC%A7%80) 
  - https://kotlinlang.org/docs/ Kotlin 2.0.x 문서

## Installing the programming environment
기본적으로 Codespace 안에서 설치하는 것을 기준으로 한다.
다른 리눅스 호환 환경에 코드스페이스와 대략 비슷한 버전의 python, jupyter를 설치한다면 마찬가지 방법으로 프로그래밍 환경을 구성할 수 있다.
### Before installing
학기 초에 시험해 본 바에 따르면 Codespace에 기본적으로 python, jupyter가 설치되어 있다 것
```
@~ ➜ /workspaces/oop2024fall (main) $ python --version
Python 3.12.1
@~ ➜ /workspaces/oop2024fall (main) $ jupyter --version
Selected Jupyter core packages...
IPython          : 8.26.0
ipykernel        : 6.29.5
ipywidgets       : not installed
jupyter_client   : 8.6.2
jupyter_core     : 5.7.2
jupyter_server   : 2.14.2
jupyterlab       : 4.2.4
nbclient         : 0.10.0
nbconvert        : 7.16.4
nbformat         : 5.10.4
notebook         : not installed
qtconsole        : not installed
traitlets        : 5.14.3
```

### Installation steps
```
curl -Ls https://sh.jbang.dev | bash -s - app setup
```
위와 같이 실행 후 터미널을 닫고 새로운 터미널 열어서 다음으로 진행한다.
(성공적으로 설치되면 영문으로 새로운 터미널을 열라는 내용이 포함된 메시지가 출력될 것이다.)

```
jbang --java 22 io.github.padreati:rapaio-jupyter-kernel:2.1.0 -i -auto
```

여기까지 성공적으로 rapaio 자바 커널(런타임)을 설치하면 끝!

### How to run
```
jupyter-lab --no-browser --IdentityProvider.token='x'
```
이렇게 실행하여 새로운 웹브라우저 창/탭에서 주피터 환경에 접속

로컬 환경에 설치한 경우에는 아무런 없이 `jupyter-lab` 으로만 실행해도 됨
