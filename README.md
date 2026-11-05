<div align="center">

# 🤖 AI Study Group

**AI 도구와 자동화를 직접 만들어 보며 배우는 스터디**

Cursor AI · MCP · A2A · Docker · n8n

<br/>

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)
![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)

<br/>

[📖 전체 스터디 정리 (Wiki)](https://github.com/tacoya03/AI-Study_Group/wiki)

</div>

---

## 📌 소개

**AI Study Group**은 최신 AI 도구의 개념을 익히고, **Docker와 n8n으로 실제 동작하는 자동화 워크플로우를 만들어 보는** 스터디입니다.

---

## 🎯 스터디 목표

| 구분 | 내용 |
| :--- | :--- |
| 🧠 **개념 학습** | API, JSON, Docker, Apache 등 자동화에 필요한 기초 다지기 |
| 🛠️ **AI 도구 이해** | Cursor AI, MCP(Model Context Protocol), A2A(Agent2Agent) 알아보기 |
| ⚙️ **자동화 실습** | n8n으로 메일 · 공공데이터 · 알림이 연결되는 워크플로우 직접 구축 |

---

## 🗓️ 주차별 실습

| 주차 | 주제 | 실습 내용 | 정리 |
| :---: | :--- | :--- | :---: |
| **0주차** | Study Group OT | Cursor AI 체험, MCP · A2A · n8n 개념 소개 | [📄 보기](https://github.com/tacoya03/AI-Study_Group/wiki/0%EC%A3%BC%EC%B0%A8_Study-group-OT) |
| **1주차** | Docker와 n8n | Docker 개념 학습, n8n 컨테이너 설치 및 실행 | [📄 보기](https://github.com/tacoya03/AI-Study_Group/wiki/1%EC%A3%BC%EC%B0%A8_Docker%EC%99%80-n8n) |
| **스터디 정리** | API | REST API 구조, 인증 방식, 공공데이터 · 날씨 · 지도 API 정리 | [📄 보기](https://github.com/tacoya03/AI-Study_Group/wiki/1_%EC%8A%A4%ED%84%B0%EB%94%94-%EC%A0%95%EB%A6%AC) |
| **2주차** | n8n 활용 1 | 매일 아침 8시 Gmail 알림 · Docker Apache로 정적 사이트 띄우기 | [📄 보기](https://github.com/tacoya03/AI-Study_Group/wiki/2%EC%A3%BC%EC%B0%A8_n8n-%ED%99%9C%EC%9A%A9-1) |
| **3주차** | n8n 활용 2 | 공공데이터(에어코리아) API로 미세먼지 이메일 알림 | [📄 보기](https://github.com/tacoya03/AI-Study_Group/wiki/3%EC%A3%BC%EC%B0%A8_n8n-%ED%99%9C%EC%9A%A9-2) |
| **4주차** | n8n 활용 3 | Gmail 키워드 감지 후 Discord 알림 | [📄 보기](https://github.com/tacoya03/AI-Study_Group/wiki/4%EC%A3%BC%EC%B0%A8_n8n-%ED%99%9C%EC%9A%A9-3) |

---

## ✨ 프로젝트 하이라이트

### ⏰ 1. 매일 아침 Gmail 알림 `2주차`
> 매일 오전 8시에 자동으로 인사 메일을 보내는 워크플로우

```
Schedule Trigger  ➜  Code (한국 시간 보정)  ➜  Send Email (Gmail SMTP)
```

### 🌫️ 2. 미세먼지 알림 `3주차`
> 공공데이터포털 API로 실시간 대기질을 가져와 정해진 시간에 메일로 전송

```
Schedule Trigger  ➜  HTTP Request (에어코리아 API)  ➜  Send Email
```

- 측정소별 실시간 `PM10` · `PM2.5` · 측정 시각을 이메일 본문에 표시
- n8n에서는 URL 인코딩이 자동으로 적용되므로 **디코딩된 서비스 키**를 사용

### 🔔 3. 키워드 메일 → Discord 알림 `4주차`
> 읽지 않은 메일에 특정 키워드(책상, 의자, 칠판)가 있으면 Discord로 알림

```
Gmail Trigger  ➜  Code (키워드 매칭)  ➜  Discord (Webhook)
```

### 🌐 4. Docker Apache 정적 사이트 `2주차`
> `httpd` 이미지로 컨테이너를 띄우고 로컬 폴더를 연결해 `index.html` 서빙

---

## 🧰 사용 기술

| 분류 | 기술 |
| :--- | :--- |
| **컨테이너** | Docker, Docker Compose, Apache (`httpd`) |
| **자동화** | n8n (Schedule Trigger, HTTP Request, Code, Gmail, Discord) |
| **AI 도구** | Cursor AI |
| **외부 서비스** | Gmail (SMTP · OAuth 2.0), Discord Webhook, 공공데이터포털 (에어코리아) |
| **데이터 형식** | REST API, JSON |

---
