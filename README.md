# 목차
- [**프로그램 설치**](#프로그램-설치)
- [**나만의 Power Tower Fractal을 만들어보자**](#나만의-power-tower-fractal을-만들어보자)

## 프로그램 설치
- mytetration 챌린지에 필요한 프로그램은 총 4가지 입니다 : Visual Studio[^1], Python, NumPy, Matplotlib
- 아래 설치과정에서 문제가 생길시, 문제상황을 [chat GPT](https://chatgpt.com/)에 설명하면 쉽게 해결할 수 있을 겁니다.

---
**Visual Studio 설치 (Window)**
1. [Visual Studio 공식 웹사이트](https://visualstudio.microsoft.com/)에 접속합니다.
2. 'Downloads' 섹션을 찾아 'Community 2024' 버전을 클릭합니다. 이 버전은 무료로 사용할 수 있으며 개인 개발자나 소규모 팀에 적합합니다.
3. 다운로드 페이지에서 'Download' 버튼을 클릭하여 설치 파일을 내려받습니다.
4. 다운로드한 설치 파일을 실행하면 설치 마법사가 시작됩니다.
5. 설치가 완료되면, 컴퓨터를 재시작하라는 메시지가 나타날 수 있습니다. 재시작 후 Visual Studio를 실행할 수 있습니다.

**Visual Studio 설치 (Mac)**
1. [Visual Studio 공식 웹사이트](https://visualstudio.microsoft.com/)에 접속합니다.
2. 화면 상단의 'Download for Mac' 버튼을 클릭합니다.
3. 'Visual Studio 2024 for Mac' 버튼을 클릭하여 Mac용 설치 파일을 다운로드합니다.
4. 다운로드한 .dmg 파일을 열어 설치 프로세스를 시작합니다.
5. 열린 창에서 Visual Studio 아이콘을 'Applications' 폴더로 드래그하여 설치합니다.
---
**Python 설치 (Window)**
1. [파이썬 공식 웹사이트](https://www.python.org/) 상단 메뉴에서 "Downloads"를 클릭한 후, 윈도우 운영체제용 파이썬을 클릭합니다. 보통 "Download Python 3.x.x" (x는 버전 번호) 형식으로 표시됩니다.
2. 다운로드 페이지에서 "Download" 버튼을 클릭하여 설치 파일을 내려받습니다.
3. 다운로드한 설치 파일을 실행합니다. 설치 시작 화면에서 "Add Python 3.x to PATH" 체크박스를 선택하는 것을 잊지 마세요. 이 옵션은 파이썬과 pip을 시스템의 PATH에 자동으로 추가해 줍니다.
4. "Install Now" 버튼을 클릭하여 파이썬 설치를 시작합니다.
5. Visual Studio 실행 후 상단에 보기(View) 메뉴에서 터미널(Terminal)을 클릭하면 화면하단에 터미널 창이 나타납니다.
6. 터미널창에 `python3 --version`과 `pip3 --version`을 입력하여 파이썬과 pip이 정상적으로 설치되었는지 확인할 수 있습니다.

**Python 설치 (Mac)**
1. [파이썬 공식 웹사이트](https://www.python.org/) 상단 메뉴에서 "Downloads"를 클릭한 후, macOS 운영체제용 파이썬을 클릭합니다.
2. "Download Python 3.x.x" 버튼을 클릭하여 맥용 설치 파일을 내려받습니다.
3. 다운로드한 .pkg 파일을 더블 클릭하여 설치 마법사를 실행합니다.
4. 화면의 지시에 따라 설치를 진행합니다. 대부분 '계속', '동의', '설치' 버튼을 순서대로 클릭하면 됩니다.
5. Visual Studio 실행 후 상단에 보기(View) 메뉴에서 터미널(Terminal)을 클릭하면 화면하단에 터미널 창이 나타납니다.
6. 터미널창에 `python3 --version`과 `pip3 --version`을 입력하여 파이썬과 pip이 정상적으로 설치되었는지 확인할 수 있습니다.
---
**NumPy, Matplotlib 설치**
- 다음명령어를 터미널에 입력하여 NumPy와 Matplotlib를 설치합니다 : `pip3 install numpy matplotlib`
- 설치가 완료되면 터미널에 다음 명령어를 입력하여 각각의 버젼을 확인하여 설치완료여부를 확인 할 수 있습니다 :
  - `python3 -c "import numpy; print(numpy.__version__)"`
  - `python3 -c "import matplotlib; print(matplotlib.__version__)"`

## 나만의 Power Tower Fractal을 만들어보자
### 샘플이미지 출력
- 우선, 모든 프로그램들이 잘 설치되었는지 확인하기 위해 test 이미지를 출력해보겠습니다.
- Visual Studio (이하 VS) 상단에서 File > New Text File 을 클릭하여 새로운 text 창을 띄우세요.
- [첫번째 코드](Power Tower Fractal (static)/PTF_static_1by1_H.py) 전체를 그대로 복사해서 VS에 띄어진 text창에 붙여넣기 하세요.
- 이 text 파일을 바탕화면에 `PTF_static_1by1_H.py`라는 이름으로 지정하세요.
- 터미널에 다음과 같은 명령어를 입력하면 코드가 실행됩니다 : `python3 PTF_static_1by1_H.py`
- 실행이 완료되면 결과 이미지가 'Figure 1'이라는 이름의 창으로 뜨고, 바탕화면에는 `mytetration_x_0_y_0_eps_5.png`라는 이름의 이미지 파일이 생성됩니다 :![Sample Result](Power%20Tower%20Fractal%20(static)/sample/mytetration_x_0_y_0_eps_5.png)
---
### PTF세계로의 여행
- 원하는 이미지를 출력하기 위한 주요변수들의 역할을 살펴보겠습니다.
  - `n`은 x축 화소수를 결정합니다. 16:9 비율에서 `n=3840`으로 설정하면 4K화질로 출력할 수 있습니다. rendering시간은 컴퓨터 사양에 따라 상당한 차이가 있으며, 원하는 화질과 rendering시간을 고려하여 적절한 `n`값을 설정하세요.
  - `x0`와 `y0`는 이미지 중심의 (x,y)좌표이며 `eps`는 출력범위를 설정합니다. x축방향으로의 출력범위는 x0-eps부터 x0_eps까지 입니다.
- rendering이 끝났을때 뜨는 'Figure 1'창에서 확대를 원하는 부분의 좌표를 확인 할 수 있습니다. 해당창을 클릭하고 마우스로 이미지를 훑어보면, 우측하단에 해당위치의 (x,y)좌표가 표시됩니다. 원하는 부분의 좌표를 원래코드의 변수 `x0`, `y0`에 입력하고, 확대정도는 `eps`변수를 통해 정합니다. 만약 10배 확대하고 싶으면 `eps=1e-1` 100배 확대하고 싶으면 `eps=1e-2`로 설정하면 됩니다.
- 이미지 비율과 회전
  - 이미지의 가로세로 비율은 `eps_y`를 통해 변경 할 수 있습니다. 1:1, 16:9, 4:5비율에 대해서는 [Power Tower Fractal (static)](Power_Tower_Fractal_(static))폴더에 별도의 code를 만들어 두었습니다. 원하는 비율에 맞게 선택하세요.
  - 가로를 허수축, 세로를 실수축으로 하고 싶으시다면 파일이름 끝에'R (rotated)'이 붙은 코드를 이용하세요. 'H(horizontal)'은 가로가 실수축, 세로가 허수축 입니다.
  - 16:9비율은 일반적인 유튜브영상이나 PPT화면의 비율입니다. 4:5는 인스타그램 화면에서 crop되지 않고 가장 크게 display 될 수 있는 비율입니다.
  - 다른 비율을 원하신다면 `eps_y`를 조절하시면 됩니다.
---
### SNS 업로드 규칙

---
### 다른 변수들에 대한 코멘트
- 

---
### 또 다른 미지의 세계를 향해..
- 



[^1]: 다른 IDE를 사용하셔도 됩니다. 초보자분들을 위해 대표적인 프로그램을 선정한것입니다.
