# Dorosee - falldown(쓰러짐/낙상) 감지 / 음성, 제스쳐 인식 상호작용 시스템

Dorosee는 컴퓨터 비전과 음성 인식 기술을 활용하여 거리의 안전을 실시간으로 모니터링하는 시스템입니다. YOLOv8 딥러닝 모델을 통한 정확한 쓰러짐 감지와 MediaPipe 기반 실시간 모니터링 기능을 제공합니다.

## 주요 기능

### 1. 쓰러짐 감지 시스템 (Dorosee_falldown.ipynb)
- **정확한 쓰러짐 감지**: YOLOv8 모델을 사용한 높은 정확도의 쓰러짐 감지
- **지속적인 추적**: 바운딩 박스 추적을 통한 쓰러짐 상황 연속 분석  
- **시간 측정**: 쓰러짐 지속 시간 및 발생 시점 정확한 기록
- **이벤트 로깅**: 쓰러짐 발생 시간, 지속 시간 등 상세 정보 저장
- **비디오 분석**: 녹화된 영상 파일에서 쓰러짐 상황 자동 분석

### 2. 실시간 모니터링 시스템 (Dorosee_mp.audio.ipynb)
- **음성 활성화**: "도로시"라는 음성 명령으로 시스템 활성화
- **손 인식**: MediaPipe를 통한 실시간 손 동작 감지
- **자동 녹화**: 활성화 시 자동으로 영상 녹화 시작
- **실시간 피드백**: 화면을 통한 시스템 상태 실시간 표시

## 시스템 구성

```
dorosee-model/
├── Dorosee_falldown.ipynb     # 쓰러짐 감지 분석 시스템
├── Dorosee_mp.audio.ipynb     # 실시간 모니터링 시스템  
├── trained_yolov8m.pt         # YOLOv8 model
└── README.md         
```

## 기술 스택

- **DL**: YOLOv8 (Ultralytics)
- **CV**: OpenCV, MediaPipe
- **음성 인식**: SpeechRecognition, Google Speech API
- **개발 환경**: Python, Jupyter Notebook
- **비디오 처리**: OpenCV VideoCapture/VideoWriter

## 사용 방법

### 쓰러짐 감지 시스템 실행
1. `Dorosee_falldown.ipynb` 실행
2. 입력 비디오 파일 경로 설정
3. 모델 분석 시작
4. 결과 비디오 및 로그 확인

### 실시간 모니터링 시스템 실행  
1. `Dorosee_mp.audio.ipynb` 실행
2. 웹캠 연결 확인
3. "도로시"라고 말하거나 손을 화면에 보여 시스템 활성화
4. 자동 녹화 시작 및 실시간 모니터링

## 필요 라이브러리

```bash
pip install ultralytics opencv-python mediapipe speechrecognition pyaudio
```

## 활용 분야

- **도로시 시스템**: 거리의 응급환자 초동조치 지원
- **의료 시설**: 병원, 요양원에서의 환자 안전 모니터링
- **가정 케어**: 독거노인 또는 환자의 일상 안전 관리
- **재활 센터**: 환자의 움직임 패턴 분석 및 안전 관리
- **연구 목적**: 쓰러짐 패턴 분석 및 예방 연구

## 특징

이 시스템은 단순한 감지를 넘어서 지속적인 추적과 분석을 통해 실제 쓰러짐 상황을 정확히 판별합니다. 위치 추적, 시간 측정, 연속성 분석 등의 고급 기능을 통해 오탐지를 최소화하고 실제 응급 상황에서 신속한 대응이 가능합니다.

음성 인식과 손 인식을 통한 다중 활성화 방식으로 사용자의 편의성을 높였으며, 실시간 녹화 기능으로 상황 기록과 분석이 동시에 가능합니다.