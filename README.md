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

  #### ※ requirements.txt에 명시된 Package를 설치하는 방법



  ```bash
  pip3 install -r requirements.txt
  ```





  #### ※ 혹시라도 가상환경(Virtual environment) 생성을 모른다면?

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

  ```bash
  // 우선 업데이트와 업그레이드 해주기
  sudo apt-get update
  sudo apt-get upgrade

  sudo apt-get install build-essential
  sudo apt-get install cmake

  // 특정 포멧의 이미지 파일을 Read, Write 하기 위한 필요 패키지 설치
  sudo apt-get install libjpeg-dev libtiff5-dev libjasper-dev libpng12-dev

  // 특정 코덱의 비디오 파일을 Read, Write 하기 위한 필요 패키지 설치
  sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libxvidcore-dev libx264-dev libxine2-dev

  // Video4Linux  리눅스에서 실시간 비디오 캡처 및 비디오 디바이스 제어를 위한 API 패키지 설치
  sudo apt-get install libv4l-dev v4l-utils

  // GStreamer는 리눅스 기반에서 영상 스트리밍을 쉽게 처리할 수 있더록 만든 오픈 소스 프레임워크 이다.
  sudo apt-get install libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev

  // OpenCV에서 윈도우 생성 등의 GUI를 위해 gtk 또는 qt를 선택해서 사용가능하며 여기서는 gtk2를 지정해준다.
  sudo apt-get install libgtk2.0-dev

  // OpenGL 지원하기 위해 필요한 라이브러리 설치
  sudo apt-get install mesa-utils libgl1-mesa-dri libgtkgl2.0-dev libgtkglext1-dev

  // OpenCV 최적화를 위해 사용되는 라이브러리 설치
  sudo apt-get install libatlas-base-dev gfortran libeigen3-dev

  // python 패키지는 OpenCV-Python 바인딩을 위한 패키지이며, Numpy는 매트릭스 연산등을 빠르게 처리할 수 있다.
  // 물론 이미 설치되어 있음.
  sudo apt-get install python3-dev python3-numpy

  ~/Desktop$ mkdir opencvtemp
  ~/Desktop$ cd opencvtemp

  wget -O opencv.zip https://github.com/opencv/opencv/archive/4.1.2.zip
  unzip opencv.zip

  wget -O opencv_contrib.zip https://github.com/opencv/opencv_contrib/archive/4.1.2.zip
  unzip opencv_contrib.zip


  ~/Desktop/opencvtemp/$ cd opencv-4.1.2
  ~/Desktop/opencvtemp/opencv-4.1.2$ mkdir build
  ~/Desktop/opencvtemp/opencv-4.1.2$ cd build

  ~/Desktop/opencvtemp/opencv-4.1.2/build$
  cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local  -D WITH_TBB=OFF -D WITH_IPP=OFF -D WITH_1394=OFF -D BUILD_WITH_DEBUG_INFO=OFF -D BUILD_DOCS=OFF -D INSTALL_C_EXAMPLES=ON -D INSTALL_PYTHON_EXAMPLES=ON -D BUILD_EXAMPLES=OFF -D BUILD_TESTS=OFF -D BUILD_PERF_TESTS=OFF -D ENABLE_NEON=ON -D ENABLE_VFPV3=ON -D WITH_QT=OFF -D WITH_GTK=ON -D WITH_OPENGL=ON -D OPENCV_ENABLE_NONFREE=ON -D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib-4.1.2/modules -D WITH_V4L=ON -D WITH_FFMPEG=ON -D WITH_XINE=ON -D ENABLE_PRECOMPILED_HEADERS=OFF -D BUILD_NEW_PYTHON_SUPPORT=ON -D OPENCV_GENERATE_PKGCONFIG=ON ../

  ```
