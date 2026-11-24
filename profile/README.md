<!-- PROJECT LOGO -->
<br />

<div align="center">
  <a href="https://ssok.store">
    <img
      src="https://raw.githubusercontent.com/200ok-Hongik/.github/main/profile/assets/temp-logo.png"
      alt="SSOK Logo"
      width="120"
    />
  </a>

  <h1 align="center">SSOK</h1>

  <p align="center">
    헷갈리는 분리배출 정보를 사진 한 장으로 쏙!<br />
    AI 이미지 분석과 지역별 배출 정보를 활용한 맞춤형 분리배출 서비스
  </p>

  <p align="center">
    <a href="https://ssok.store"><img src="https://img.shields.io/badge/SSOK_서비스_바로가기-22C55E?style=for-the-badge&logoColor=white" alt="SSOK 서비스 바로가기"></a>
    <a href="https://github.com/200ok-Hongik/200ok-FE"><img src="https://img.shields.io/badge/Frontend-181717?style=for-the-badge&logo=github&logoColor=white" alt="Frontend"></a>
    <a href="https://github.com/200ok-Hongik/200ok-BE"><img src="https://img.shields.io/badge/Backend-181717?style=for-the-badge&logo=github&logoColor=white" alt="Backend"></a>
    <a href="https://github.com/200ok-Hongik/200ok-AI"><img src="https://img.shields.io/badge/AI-181717?style=for-the-badge&logo=github&logoColor=white" alt="AI"></a>
  </p>

  <p align="center">홍익대학교 컴퓨터공학과 졸업 프로젝트 · 팀 200 OK</p>
</div>

<p align="center">
  <img src="https://raw.githubusercontent.com/200ok-Hongik/.github/main/profile/assets/main.jpg" alt="사진 한 장으로 해결하는 AI 분리배출 판정 서비스 SSOK" width="100%" />
</p>

<br />


<!-- 프로젝트 소개 -->
## 프로젝트 소개

**SSOK(쏙)** — 버리려는 물건을 촬영하면 AI가 품목·재질·상태를 분석하고, 거주 지역 기준의 분리배출 방법과 일정을 안내하는 서비스

- **문제**: 지역·품목마다 분리배출 기준이 달라 매번 검색 필요, 라벨·뚜껑·오염 여부에 따라 배출 방법도 달라짐
- **해결**: 사진 한 장 → 물건별 품목·상태 판정 → 지역 규칙에 맞는 배출 방법 안내 → 배출 일정·기록 관리
- **기간**: 2026.03 ~ 진행 중

<p align="center">
  <img src="https://raw.githubusercontent.com/200ok-Hongik/.github/main/profile/assets/scan-photo.jpg" alt="재활용품을 촬영하면 품목·상태·지역 기준을 분석해 올바른 배출 방법을 안내" width="100%" />
</p>

<br />


## 주요 기능

<p align="center">
  <img src="https://raw.githubusercontent.com/200ok-Hongik/.github/main/profile/assets/features.png" alt="주요 기능: AI 분리배출 분석, 지역 맞춤 가이드, 배출 일정 관리, 알림·설정, 사용자 피드백" width="100%" />
</p>

<table>
<tr>
<td width="50%" valign="top">

**AI 기반 분리배출 분석**

- 이미지 업로드 → 물건별 품목·재질·상태 분석
- 분석 결과 기준 분리배출 방법 제공
- 잘못 분석된 결과는 사용자가 직접 수정

</td>
<td width="50%" valign="top">

**지역 맞춤형 분리배출 가이드**

- 품목별 분리배출 방법·주의 사항
- 거주 지역 기준 배출 규칙 안내
- 품목명·연관 단어 검색

</td>
</tr>
<tr>
<td width="50%" valign="top">

**분리배출 일정 관리**

- 캘린더에 배출 일정 등록
- 일정 완료 여부 관리
- 오늘의 배출 일정을 홈 화면에 표시

</td>
<td width="50%" valign="top">

**알림 및 사용자 설정**

- 배출 일정 푸시 알림
- 카카오 로그인
- 거주 지역·알림 수신 여부 설정

</td>
</tr>
<tr>
<td colspan="2" valign="top">

**사용자 피드백**

- AI 분석 결과에 대한 의견 등록
- 사용자 수정·피드백 결과를 분석 정확도 개선에 활용

</td>
</tr>
</table>

<br />


## 사용 흐름

<table>
<tr>
<td width="36%" align="center"><img src="https://raw.githubusercontent.com/200ok-Hongik/.github/main/profile/assets/app-scan.jpg" alt="SSOK 앱 시작 화면: 카메라로 페트병을 비추면 품목을 알려 줌" width="280" /></td>
<td valign="middle">

1. **로그인 · 지역 설정** — 카카오 로그인, 거주 지역 등록
2. **촬영** — 버릴 물건 촬영 (한 장에 여러 물건 가능)
3. **결과 확인 · 수정** — 물건별 품목·상태(라벨·뚜껑·오염 등) 확인, 틀린 항목 수정 후 확정
4. **배출 방법 안내** — 품목·상태·지역 기준 배출 방법·주의 사항
5. **기록 · 일정** — 배출 기록, 지역별 배출 일정 (캘린더·홈 화면)

</td>
</tr>
</table>

<br />


## 서비스 흐름

<p align="center">
  <img src="https://raw.githubusercontent.com/200ok-Hongik/.github/main/profile/assets/service-flow.png" alt="서비스 흐름도: 카카오 로그인 → 촬영 → 백엔드가 RabbitMQ 작업 큐로 AI 서버 호출 → YOLO 탐지 → GPT 품목·상태 판단 → 결과 확인·수정·확정 → 배출 안내·기록" width="100%" />
</p>

- **비동기 분석**: 백엔드가 분석 요청을 작업 큐(RabbitMQ)에 등록 후 jobId 즉시 반환 → 앱은 상태 조회로 결과 수신
- **AI 분석**: YOLOv8 물체 탐지 → GPT 품목·상태 판단 (1차 저해상도, 애매한 경우만 2차 고해상도)
- **판정·기록**: 사용자 확정 결과 기준으로 백엔드가 품목·상태·지역별 배출 방법 판정, 결과·기록 저장

<br />


## 시스템 구성

<p align="center">
  <img src="https://raw.githubusercontent.com/200ok-Hongik/.github/main/profile/assets/system.png" alt="시스템 구성: SSOK 앱(Expo) → 백엔드(Spring Boot, RabbitMQ, MySQL, Redis, S3) → AI 서버(FastAPI, YOLOv8, GPT)" width="100%" />
</p>

| 저장소 | 역할 | 주요 기술 |
|---|---|---|
| [200ok-FE](https://github.com/200ok-Hongik/200ok-FE) | SSOK 앱 · 웹 | Expo, React Native, TypeScript, Vercel |
| [200ok-BE](https://github.com/200ok-Hongik/200ok-BE) | 인증, 분석 작업 관리, 배출 규칙 판정, 기록·일정 | Spring Boot, RabbitMQ, MySQL, Redis, AWS S3·EC2 |
| [200ok-AI](https://github.com/200ok-Hongik/200ok-AI) | 사진 속 재활용품 품목·상태 분석 | FastAPI, YOLOv8, OpenAI GPT, AWS EC2 |

<br />


## 팀원

| 이름 | 학교 | 역할 | 참여 기간 | 비고 |
|:---:|:---:|:---:|:---:|:---:|
| 유영주 | 홍익대학교 컴퓨터공학과 | `팀장` `AI 개발자` | MVP 개발 ~ 현재 | GitHub · Blog |
| 김지현 | 홍익대학교 컴퓨터공학과 | `백엔드 개발자` | MVP 개발 ~ 현재 | [![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/hyeoniss) [![Velog](https://img.shields.io/badge/Velog-20C997?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@hyeoniss/posts) |
| 김혜원 | 홍익대학교 컴퓨터공학과 | `AI 개발자` | MVP 개발 ~ 현재 | [![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/fkoeier) Velog |
| 최수민 | 홍익대학교 컴퓨터공학과 | `프론트엔드 개발자` | MVP 개발 ~ 현재 | Velog |
| 정유민 | - | `디자이너` | MVP 개발 ~ 현재 | - |
| 정용빈 | - | `디자이너` | MVP 개발 ~ 현재 | - |

<br />


## 기술 스택

#### **Frontend**

![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Expo](https://img.shields.io/badge/Expo-000020?style=for-the-badge&logo=expo&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)

#### **Backend**

![Java](https://img.shields.io/badge/Java_17-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![OAuth 2.0](https://img.shields.io/badge/OAuth_2.0-3C4043?style=for-the-badge&logo=auth0&logoColor=white)
![Kakao Login](https://img.shields.io/badge/Kakao_Login-FFCD00?style=for-the-badge&logo=kakao&logoColor=000000)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)

#### **AI**

![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![YOLOv8](https://img.shields.io/badge/YOLOv8-111F68?style=for-the-badge&logo=ultralytics&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI_GPT-412991?style=for-the-badge&logo=openai&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)

#### **Database**

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)

#### **Infra / CI·CD**

![AWS](https://img.shields.io/badge/AWS_EC2·S3·ECR-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Caddy](https://img.shields.io/badge/Caddy-1F88C0?style=for-the-badge&logo=caddy&logoColor=white)

#### **협업 도구**

![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white)

<br />


## 관련 링크

#### SSOK 프로젝트 레포지터리

- [SSOK 서비스](https://ssok.store)
- [GitHub - Frontend](https://github.com/200ok-Hongik/200ok-FE)
- [GitHub - Backend](https://github.com/200ok-Hongik/200ok-BE)
- [GitHub - AI](https://github.com/200ok-Hongik/200ok-AI)

<br />
<br />

<h2></h2>

<br />

<div align="center">

### 헷갈리는 분리배출, 이제 쏙 알아보세요.

사진 한 장이면 분리배출 방법부터 일정까지 한눈에.<br />
우리의 작은 실천이 더 나은 내일로 이어지도록, **SSOK**과 함께해요.

</div>

<br />
