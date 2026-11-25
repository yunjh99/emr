# 의료 EMR

**환자 등록부터 예약·방문 접수·진료 기록 작성까지, 병원 직원의 업무 흐름을 구현한 웹 애플리케이션입니다.**

백엔드 개발 포트폴리오로, 예약 중복 방지와 상태 전이, 진료 기록 원본 보존, 업무 트랜잭션과 감사 로그의 일관성에 집중했습니다. React 화면에서 실제 API를 호출해 역할별 업무를 수행할 수 있습니다. 시연 데이터는 가상 정보입니다.

---
## 기술 스택

| 구분 | 기술 |
| --- | --- |
| Backend | ![Java](https://img.shields.io/badge/Java-21-ED8B00?style=flat-square) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-4.1.2-6DB33F?style=flat-square) ![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square) ![QueryDSL](https://img.shields.io/badge/QueryDSL-5.1-0769AD?style=flat-square) ![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square) ![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square) ![Gradle](https://img.shields.io/badge/Gradle-02303A?style=flat-square) |
| Database | ![MySQL](https://img.shields.io/badge/MySQL-8-4479A1?style=flat-square) |
| Frontend | ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square) ![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=flat-square) ![React Router](https://img.shields.io/badge/React_Router-CA4245?style=flat-square) ![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=flat-square) ![Axios](https://img.shields.io/badge/Axios-5A29E4?style=flat-square) |
| Test | ![JUnit 5](https://img.shields.io/badge/JUnit-5-25A162?style=flat-square) ![Spring Boot Test](https://img.shields.io/badge/Spring_Boot_Test-6DB33F?style=flat-square) ![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square) ![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square) |
| Deployment — 준비 중 | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square) ![nginx](https://img.shields.io/badge/nginx-009639?style=flat-square) ![AWS EC2](https://img.shields.io/badge/AWS_EC2-FF9900?style=flat-square) |
---

## 대표 화면

아래 화면은 가상 환자와 데모 계정을 사용한 시연입니다.

### 예약 관리 · STAFF

날짜·의사·상태별로 예약 현황을 조회하고 예약 등록, 방문 접수, 예약 취소를 처리합니다. 취소된 예약도 목록에 보존해 상태를 확인할 수 있습니다.

![원무과 예약 관리 화면 — 날짜·의사·상태 필터와 예약별 방문 접수·취소](docs/images/appointments-management.png)

### 접수·진료 대기 · DOCTOR

담당 의사가 본인의 접수 목록과 대기·진료 중·완료·취소 상태를 확인합니다. 접수 상태에 따라 진료 보기, 기록 작성, 진료 기록 조회 버튼을 제공합니다.

![의사 접수·진료 대기 화면 — 상태별 현황과 담당 환자 진료 시작·기록 작성](docs/images/doctor-visit-queue.png)

---

## ERD

환자·예약·접수·진료 기록과 직원·의사·진료과, 감사 로그·수정 이력의 관계를 정리한 설계도입니다. 예약 슬롯과 업무 버전 등 일부 구현 상세는 이 이미지에 생략되어 있습니다.

[![의료 EMR 주요 도메인 ERD](docs/images/emr-erd.png)](docs/images/emr-erd.png)

이미지를 클릭하면 원본 크기로 확인할 수 있습니다.

---

