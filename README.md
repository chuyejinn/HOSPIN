# 🏥 HOSPIN - 병원 웹사이트 프로젝트

## **📌 1. 프로젝트 개요**

•	**프로젝트명:** HOSPIN

•	**목표:** 환자 중심의 진료 예약 및 의료 정보 확인이 가능한 병원 웹사이트 개발

•	**주요 대상 사용자:** 환자, 의료진(관리자)

•	**핵심 기능:**

•	환자: 회원가입/로그인, 진료 기록 열람, 예약 시스템

•	의료진: 진료 스케줄 확인, 예약 관리, 공지사항 작성, 사용자 관리

---

## **👥 2. 팀 소개**

| **이름** | **역할** | **주요 업무** | **GitHub** |
| --- | --- | --- | --- |
| 추예진 | 백엔드 | DB 설계, API 개발 | https://github.com/chuyejinn |
| 최지원 | 프론트엔드 | UI 구현, 사용자 흐름 설계 | (링크 입력) |

---

## **🧠 3. 기술 스택 & 개발 환경**

•	**Frontend:** React, HTML/CSS, JavaScript

•	**Backend:** Spring Boot, Java

•	**Database:** MySQL

•	**Deployment:** Render / AWS EC2

•	**협업 도구:** Notion, GitHub, Figma

---

## **🗂 4. 기능 리스트**

| **기능** | **설명** | **대상 사용자** | **우선순위** |
| --- | --- | --- | --- |
| 회원가입/로그인 | JWT 인증 기반 로그인 구현 | 환자/의료진/관리자 | ⭐️⭐️⭐️⭐️⭐️ |
| 진료 기록 확인 | 본인 진료 이력 조회 기능 | 환자 | ⭐️⭐️⭐️⭐️ |
| 예약 시스템 | 진료과, 의료진, 시간 선택 | 환자 | ⭐️⭐️⭐️⭐️⭐️ |
| 예약 관리 | 의료진이 예약 목록 확인 | 의료진 | ⭐️⭐️⭐️⭐️ |
| 공지사항 | 관리자 공지 등록 및 열람 | 전체 사용자 | ⭐️⭐️⭐️ |

---

## **📄 5. API 명세서 (예시 일부)**

| **Method** | **Endpoint** | **설명** | **요청 예시** | **응답 예시** |
| --- | --- | --- | --- | --- |
| POST | /api/auth/login | 로그인 | username, password | JWT token |
| GET | /api/user/me | 내 정보 조회 | Header: JWT | JSON(user) |
| POST | /api/reservation | 예약 등록 | doctorId, date, time | 예약정보 |
| GET | /api/records | 진료 기록 조회 | Header: JWT | 기록 목록 |

---

## **📊 6. ERD 요약**

•	**User** (id, username, password, name, role)

•	**Doctor** (id, name, department, schedule_info)

•	**Reservation** (id, user_id, doctor_id, date, time, status)

•	**MedicalRecord** (id, user_id, diagnosis, treatment, date)

•	**Notice** (id, title, content, created_at)
