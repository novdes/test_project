# 과제 프로젝트 이름

이 프로젝트는 과제 명세에 따라 제공된 기능을 Java로 구현한 결과물입니다.

## 개요

## 프로젝트 구조

본 프로젝트는 Java Vert.x로 구현되었습니다. 

Vert.x는 비동기 I/O 프로그래밍, 이벤트 기반 프로그래밍, 클러스터링, 
분산메시징 시스템, 마이크로서비스 아키텍처 등을 지원하여,
높은 성능과 확장성을 제공하는 프레임워크입니다.

## 프로젝트 구조 : 
Vert.x 프레임워크와 미국 무인자율주행 아키텍쳐에서 활용했던 
JAUS(Joint Architecture for Unmanned Systems) 일부 개념을 활용해서 설계하였습니다.

이를 통해 전체 아키텍쳐 구조를 노드와 인스턴스까지 분산화시켜 서비스 확장성을
극대화시키고 마이크로 서비스를 구현하여 확장성까지 갖출수 있도록 노력했습니다.

시스템 : 시스템 전체를 의미합니다(Blockchain)
서비스 : 시스템 내부의 하위 서비스를 의미합니다.(Auction)  
노드 : 서비스 내부의 독립적으로 실행 가능한 기능적인 블록을 의미합니다.(경매물,입찰)
인스턴스 : 노드의 구체적인 인스턴스를 의미합니다.(입찰 노드의 입찰 등록, 낙찰)

현 프로젝트에서는 vetx의 verticle로 노드를 생성했고, 
노드간의 inbound 통신은 vert.x의 evnet bus를 활용했습니다. 
외부 시스템과의 outbound 통신은 restful API를 활용했습니다. 

프로젝트 구조는 다음과 같습니다.
- com.blockchain : 블록체인시스템
- com.blockchain.acution :  블록체인시스템 내의 경매 서비스
- com.blockchain.auction.deploy : 경매 서비스의 노드 배포자
- com.blockchain.auction.driver : 경매 서비스의 노드 driver
- com.blockchain.auction.model : 경매 서비스의 도메일 모델
- com.io : 통신관련 모듈
- com.vertx : vert.x 관련 모듈

구현한 기능은 다음과 같습니다.
- 기능 1
- 기능 2
- 기능 3

## 설치 및 사용 방법

1. 이 프로젝트를 클론합니다
git clone https://github.com/username/project.git
2. 프로젝트 폴더로 이동합니다.
cd project
3. Maven을 사용하여 프로젝트를 빌드합니다.
mvn clean package
4. 프로젝트를 실행합니다.
java -jar target/project.jar
## 실행 결과

이 프로젝트는 다음과 같은 결과를 출력합니다.

### 결과 1

결과 설명

### 결과 2

결과 설명

### 결과 3

결과 설명

## 기술 스택

- Java 11
- Spring Boot
- Maven

## 기여 방법

1. 프로젝트를 포크합니다.
2. 새로운 기능을 개발하거나 버그를 수정합니다.
3. 변경 사항을 커밋합니다.
git commit -m 'Add some feature'
 
4. 변경 사항을 자신의 포크한 저장소에 푸시합니다.
git push 
5. 원본 저장소에 풀 리퀘스트를 작성합니다.

## 라이선스

이 프로젝트는 MIT 라이선스를 따릅니다. 자세한 내용은 `LICENSE` 파일을 참조하세요.
 

