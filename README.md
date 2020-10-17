# MLOps Workshop

## 실습환경

- OS: ubuntu 20.04
- root user (sudo)
- CPU 2 core / MEM 4G / Disk 50G
- Public IP 권장 (EC2 / GCE / Azure VM)

## 사전지식
- 리눅스 기본 지식이 필요합니다. (ssh, vim, apt, curl 등)
- 간단한 프로그래밍 지식을 요구합니다. 언어는 무관하지만 이 책에서는 파이썬을 주로 다룹니다. 파이썬을 모르시더라도 전반적인 프로그래밍 지식만으로도 충분히 이해할 수 있습니다.
- 간단한 클라우드 지식이 필요합니다.
- `tmux`, `screen`과 같은 터미널 멀티플랙서를 사용하면 편리합니다.

## 클라우드 계정 만들기

준비한 서버가 없다면 다음 클라우드 플랫폼을 이용하여 무료로 서버를 생성하시기 바랍니다.

- `GCP`: https://cloud.google.com/free/
- `AWS`: https://aws.amazon.com/ko/s/dm/landing-page/start-your-free-trial/
- `Azure`: https://azure.microsoft.com/ko-kr/free


## MobaXterm 설치

---

**참고** 윈도우 운영체제 사용자에 한해서 설치합니다. 리눅스나 맥 운영체제를 사용하시는 경우 MobaXterm을 설치할 필요 없이 바로 각 운영체제에서 지원하는 터미널 프로그램을 사용하면 됩니다.

---

리눅스 서버로 접속할 터미널을 윈도우 서버에 설치합니다. `putty` ([https://www.putty.org](https://www.putty.org/)) 등 선호하는 터미널을 사용해도 무방합니다.

1. MobaXterm 다운로드: [https://mobaxterm.mobatek.net/download.html](https://mobaxterm.mobatek.net/download.html)
2. `Home Edition` > `Download now` 클릭
3. `MobaXterm Home Edition (Portable edition)` 다운로드
4. 다운로드 완료된 파일 압축 해제
5. `Session` 버튼 > `SSH` 버튼 클릭
6. 다음 정보 입력:
	- Remote host: -
	- User: `ubuntu`
7. (Optional) Advanced SSH settings > Use private key (체크) > PEM키 등록

![[그림 3-3] MobaXterm](https://github.com/hongkunyoo/handson-k8s/raw/master/03-install/03-03.png)

---

**참고** Remote host는 독자별 준비한 서버 정보를 입력합니다.

## Workshop

1. Model Generation
	- [01-도커 실행](workshop/01/01.md)
	- [02-학습 이미지 생성하기](workshop/01/02.md)
2. Orchestration
	- [01-명령도구 마스터](workshop/02/01.md)
	- [02-Pod 살펴보기](workshop/02/02.md)
	- [03-Job 리소스](workshop/02/03.md)
3. Deployment
	- [01-배치 예측](workshop/03/01.md)
	- [02-모델 서빙](workshop/03/02.md)
	- [03-모델 배포를 위한 CI/CD](workshop/03/03.md)
4. Kubeflow
	- [01-Pipeline](workshop/04/01.md)
	- [02-Fairing](workshop/04/02.md)
5. [Project (Optional)](workshop/05/01.md)

