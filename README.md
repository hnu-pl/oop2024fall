# oop2024fall
OOP course @ HNU CE (2024 fall)

## Links
  - https://github.com/forax/java-guide 이 온라인 강의노트를 참고로 내용 선택 및 더 필요한 내용 추가
  - https://docs.github.com/ko/codespaces 온라인으로 제공되는 깃헙 제공 리눅스 개발 환경
  - https://github.com/jupyter-java 자바 프로그래밍 환경과 관련된 다양한 정보
    - https://www.jbang.dev/ 자바 개발 환경 설치를 간편하게 해주는 관리 도구
    - https://github.com/padreati/rapaio-jupyter-kernel/tree/fd3a64a483b6b731783818395deb677fbfbe208c 수업에서 사용할 버전의 자바 커널

## Installing the programming environment
기본적으로 Codespace 안에서 설치하는 것을 기준으로 한다.
다른 리눅스 호환 환경에 코드스페이스와 같은 버전의 python, java, jupyter를 설치한다면 마찬가지 방법으로 프로그래밍 환경을 구성할 수 있다.
### Before installing
학기 초에 시험해 본 바에 따르면 Codespace에 기본적으로 다음과 같은 버전의 python, java, jupyter가 설치되어 있을 것
```
@~ ➜ /workspaces/oop2024fall (main) $ python --version
Python 3.12.1
@~ ➜ /workspaces/oop2024fall (main) $ java --version
openjdk 21.0.4 2024-07-16 LTS
OpenJDK Runtime Environment Microsoft-9889606 (build 21.0.4+7-LTS)
OpenJDK 64-Bit Server VM Microsoft-9889606 (build 21.0.4+7-LTS, mixed mode, sharing)
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
jbang io.github.padreati:rapaio-jupyter-kernel:1.3.0 -i -auto
```
여기까지 성공적으로 rapaio 자바 커널(런타임)을 설치하면 끝!

만일 자바 버전이 맞지 않는 문제러 설치가 실패한 상황이라면 버전에 맞는 JDK가 설치되도록 다음과 같이 `--java 21` 옵션을 추가하여 rapio 자바 커널 설치를 시도해 보라.
```
jbang --java 21 io.github.padreati:rapaio-jupyter-kernel:1.3.0 -i -auto
```

### How to run
```
jupyter-lab --no-browser --IdentityProvider.token='x'
```
이렇게 실행하여 새로운 웹브라우저 창/탭에서 주피터 환경에 접속
