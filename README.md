# TFLITE 모빌리티팀



## 1. Raspberry Pi 설치





## 2. 개발 사양 & Packages

- Linux Ubuntu 

- RAM

- python 3.7 higher 버전이 필요

- Packages Install

  #### 설치 Package list

  - edgetpu @ file:///home/pi/Downloads/edgetpu-2.12.1-py3-none-any.whl
  - imutils==0.5.3
  - numpy==1.19.1
  - opencv-contrib-python==4.1.0.25
  - picamera==1.13
  - Pillow==7.2.0
  - simpleaudio==1.0.4
  - tflite-runtime @ https://dl.google.com/coral/python/tflite_runtime-2.1.0.post1-cp37-cp37m-linux_armv7l.whl

  ####  ※ requirements.txt에 명시된 Package를 설치하는 방법

  ```bash
  pip3 install -r requirements.txt
  ```



		#### 		※ 혹시라도 가상환경(Virtual environment) 생성을 모른다면? 

```bash
# 1 코드를 실행 할 디렉토리에 들어가서 venv라는 이름의 가상환경을 생성한다.
python3 -m venv venv

# 2 가상환경을 실행시켜준다.
(디렉토리에 들어갔다는 가정) source bin/activate

# 3 가상환경 실행 후, pip를 설치해준다.
pip3 -r install requirements.txt


# ** 가상환경을 끄는 방법도 있다.
source deactivate

```





		#### 		Opencv 설치법

```

```







