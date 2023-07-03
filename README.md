# 강호신 LIS 프로젝트와 본인 역할 소개

## 1. 프로젝트 개요

### 1.1. 프로젝트 시기

- Douzone 클라우드 ERD 개발자 양성 과정 Final 프로젝트
- 2022.12.xx ~ 2022.02.xx

### 1.2. 프로젝트 주제

**진단검사시스템(Laboratory Information System)**

  - 병원 진단검사 업무 보조 프로그램으로, 진단검사를 위한 채취 및 채혈 접수부터 검사 결과 입력까지의 일련의 과정을 관리하고 기록 할 수 있는 프로그램이다.
  - Douzone 헬스케어솔루션사업본부의 연계한 멘토링 프로젝트였다. LIS 프로그램의 비즈니스에 대한 이해, 현업에 쓰이는 비즈니스 구현 방식에 대한 멘토링을 받았다.
  
### 1.3. 프로젝트 팀 및 팀원 소개

나는 프로젝트의 팀장을 맡아 팀을 구성하고 팀 일정과 팀원 간의 역할분담을 계획하였다. 또한 팀의 팀장으로서, 메인 기획/설계자이고 메인 개발자였다.

- 팀명 **_강호신_**

  내가 나와 팀원들의 이름을 한글자씩 가져와서 임의로 지은 이름인데 팀원들의 반응이 좋아 사용하게 되었다. 

- 팀 구성과 맡은 역할
  
  <table>
    <tr>
      <th>직책</th>
      <th>팀장</th>
      <th colspan="2">팀원</th>
    </tr>
    <tr>
      <td>성명</td>
      <td>강현구</td>
      <td>류호진</td>
      <td>김동신</td>
    </tr>
    <tr>
      <td>역할</td>
      <td> 
        1. 일정 및 자원 관리 <br>
        2. 공통 개발 환경 구성 <br>
        3. 기획/설계 총괄 <br>
        4. 환자 등록, 진료 방문/예약 접수, 진료 및 검사 처방, 인사 관리, 보안 및 인증 기능을 설계하고 구현.
      </td>
      <td>
        1. 채취/채혈 기능을 설계하고 구현
      </td>
      <td>
        1. 검사 접수 및 결과 입력 기능을 설계하고 구현
      </td>
    </tr>
  </table>
  
### 1.4. 기술 스택
  
![핵심기술](https://user-images.githubusercontent.com/18836863/210029513-ba13f53a-9a6b-40c6-bc6f-62776ad841d6.jpg)

| 분류 | 소분류 | 기술 | 기술 상세 |
| -- | -- | -- | -- |
| 프론트엔드 | 주요기술 | ReactJS | 18.2.0, CRA 기반 SPA |
| | UI | MaterialUI |  5.11.2, icon 5.11.0 |
| | 상태관리 | @reduxjs/toolkit | 1.9.1, 8.0.5 |
| | 개발환경 | npm+yarn | vsc 사용 |
| 백엔드 | 주요기술 | Spring Boot | Spring Boot 2.7.7 |
| |     | Spring Framework | Spring Framework 5.3.24 |
| | Model Boilerplate | lombok | lombok 1.18.24 |
| | 빌드 툴 | Gradle | 7.6 |
| | 메시징 | MQTT | 미정 |
| | 영속성 | MyBatis | MyBatis Spring 2.0.7 |
| | WAS | Tomcat | Tomcat 9.0.70 | 
| | IDE | Eclipse+STS | STS 3.9.18, Eclipse 4.21.0 | 
데이터베이스 | 주요기술 | MariaDB | MariaDB 10.5.18
형상관리 | 주요기술 | Git | Git 2.37.1

## 2. 본인 역할 소개

### 2.1. 일정 및 자원 관리

- 전체 일정을 주 단위로 계획, 각 주마다 주어지는 Todo List 를 각 팀원의 역량에 맞춰 분담시키고 각 업무 산출물들을 Issue에 업로드 하게함. Issue에 남긴 기록을 토대로 업무 성과를 확인하고 성취율을 추후 계획에 반영.
- git project의 milestone과 todo list 기능을 활용하여, 각 업무의 진행 종료 상황을 한눈에 파악하고 공유할 수 있게 함.

### 2.2 공통 개발환경 구성

#### 2.2.1. 기술 스택 선정 방식 

- Douzone 헬스케어솔루션사업본부 또는 기타 현업의 개발 환경과, 나의 개발 경험과 팀원들의 개발 역량을 고려하여 프로젝트에 사용될 프론트엔드/백앤드의 개발 스택을 구성.
- 나의 개발 경험과 현업의 공통분모가 존재하는 기술들 위주로 구성하면서, 기술의 버전을 헬스케어솔루션사업본부에서 사용하는 특정 버전으로 맞춤.
- 팀원과 나의 역량차이가 있기 때문에, 팀원 스스로가 프로젝트를 통해 부족한 기술들을 공부하면서 진행할 수 있게끔 기획함.

#### 2.2.2. 공통 개발환경 구성

- 공통 개발 환경은 내가 직접 구성해서 배포하면, 팀원들이 git을 통해 배포된 작업 환경 위에서 자신의 작업물을 업데이트 하는 방식으로 개발을 진행.
- 본인이 구성해서 배포한 내용은 다음과 같다.
  <table> 
    <tr>
      <th>백엔드</th>
      <td>
  - 디렉토리 구조 및 파일 생성 규칙 지정<br>
  &nbsp;• 구현 기능별로 구분된 REST API와 페이지 라우팅 Controller, Service와 Model등 각 소스파일의 명명 규칙과 그에 맞는 디렉토리 구조 생성.<br>
  - git 브렌치 생성, 커밋, 병합 관리 규칙, gitignore 설정<br>
  &nbsp;• codeowner기능을 활용하여 코드 리뷰 없는 병합을 방지하는 등의 버전 관리상의 사고 방지와 보안성, 로그성 파일의 업로드 방지가 주 목적.<br>
  - Spring Boot 프레임워크 설치 및 필요 종속성 설치 <br>
  &nbsp;• mybatis+mariadb의 구성과, Mapper, DO, DAO 의 생성 규칙 정의 <br>
  &nbsp;• hibernate validator를 통한 validation 구성, Controller및 Service에서의 Validation 규칙 정의<br>
  &nbsp;• 각 기능 파트별 루트 라우팅 설정과 Spring Security 기초 보안 설정(테스트용 host 설정, 특정 경로 외 리소스 접근 제한). 보안 인증은 개발 주기에 구현.<br>
      </td>
    </tr>
    <tr>
      <th>프론트엔드</th>
      <td>
        - 프로젝트 종속성 라이브러리 설치 및 구성파일 작성<br>
        &nbsp;• React + Redux Toolkit + RTK Query 데이터 패치/캐싱 및 상태관리 라이브러리 종속성을 추가하고 구성파일을 작성.<a href="#411-Redux-Toolkit--RTK-Query">[1]</a><br>
        &nbsp;• Prettier + ESLint + typescript 종속성을 추가하고 구성파일을 작성<br>
        &nbsp;• MUI 컴포넌트 라이브러리와 sass, axios 등 기타 라이브러리 종속성을 추가.<br>
        - 프론트엔드 개발에 사용될 JS의 문법과 코딩 스타일을 제한<br>
        &nbsp;• Prettier + ESLint 종속성을 추가하고 구성파일을 작성<br>
        &nbsp;• 팀에서 사용하는 문법과 코딩스타일을 제한함으로서 코드 리뷰와 형상관리를 용이하게함(diff에 불필요한 부분이 제외됨).<br>
        &nbsp;• Typescript를 종속성에 추가하고 구성하여, Typescript에 대한 VSC 더욱 강력한 intellisense기능을 활용하여 개발의 효율성을 추구함.<a href="#402-Typescript">[2]</a><br>
      </td>
    </tr>
  </table>


## 4. 아쉬운점
### 4.1 프로젝트 완성도
#### 4.1.1. Redux Toolkit + RTK Query
Redux Toolkit + RTK Query 사용 환경을 구성해서 팀원 들에게 배포했으나 팀원들이 활용을 아예 못한 점이 아쉽다. 팀원들이 공부를 병행했지만 활용까지는 실패하고 자신들의 컴포넌트 내에서 axios로 처리했다고 한다. 결과적으로 팀장인 나 혼자 Redux Toolkit+RTK Query를 통해 상태관리와 데이터 패칭을 구현했기 때문에 내가 개발한 기능 내에서만 활용되는 등의 활용성이 제한되었다. 그래도 내가 개발한 기능에 대해서는 개발 효율성이 올라갔으니 프로젝트 단위로 봐도 없는 것보다는 효과적이었다고 할 수 있다. 
#### 4.1.2. Typescript
Typescript도 1번과 마찬가지 이유로 나혼자 사용하였으나 프로젝트 단위로보면 꽤나 큰 비율을 차지하는데 이는 내가 작성한 코드가 절반 이상이기 때문이다.
   



