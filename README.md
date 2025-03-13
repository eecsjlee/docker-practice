# 도커 실습
<img src="https://github.com/user-attachments/assets/83a8969b-9a8a-4ef9-af44-9b123d122297" width="300px" alt="Docker 로고">

## 도커 구조
<img src="https://github.com/user-attachments/assets/6bafc5bb-02fd-4d1b-9396-93f49677f031" width="300px" alt="Docker 구조 설명">

## MSA
**MSA(Microservices Architecture)**는 애플리케이션을 하나의 큰 시스템으로 구축하는 대신, 독립적인 기능을 수행하는 작고 자율적인 서비스들로 쪼개어 구성하는 소프트웨어 아키텍처
하나의 거대한 소프트웨어를 여러 작은 서비스(마이크로서비스)로 나누어 개발하고 운영하는 방식

### MSA와 Docker, Kubernetes의 관계
MSA(Microservices Architecture)는 컨테이너 기술(Docker)과 쿠버네티스(Kubernetes) 같은 오케스트레이션 플랫폼과 궁합이 매우 잘 맞음
마이크로서비스들은 보통 컨테이너(Docker)에 담아 관리하며, Kubernetes를 이용해 컨테이너의 배포와 관리, 운영을 자동화함

## 단점
1. 컨테이너 침입과 같은 새로운 보안이슈를 챙겨야함
2. 컨테이너를 많이 사용하면 관리 시간과 서버비용이 증가함 
3. 안정적인 DB같은거 띄울 땐 컨테이너로 만드는게 딱히 이점이 없음
4. 컨테이너간 완전한 격리를 원하면 컨테이너 말고 가벼운 VM쓰는게 나을 수 있음


## 자주겪는 에러
1. 윈도우는 The network name cannot be found. 에러
시작 - 검색 - powershell 실행 후
wsl --unregister docker-desktop
입력하고 docker desktop 껐다가 다시 켜보도록 합시다.

2. 시스템 리소스 부족 에러가 뜨면
아마 램 부족일 수 있어서
램을 잡아먹는 프로그램을 끄거나, 윈도우 재부팅 후 Docker desktop만 실행해봅시다.
아니면 강의에서 소개하는 식으로 터미널에서 명령어들을 실행하는 식으로 docker를 사용합시다.
터미널 켜려면 윈도우는 검색에서 "powershell" 검색해서 실행하고
맥북은 런치패드에서 "터미널" 검색해서 실행하면 됩니다.

## 참고자료
https://www.docker.com/products/docker-desktop/
