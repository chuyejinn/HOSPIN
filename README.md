
HOSPIN - 병원 웹사이트 프로젝트
📌 프로젝트 개요
프로젝트명: HOSPIN
주요 기능: 환자 진료 예약, AI 진료과 추천, 마이페이지 조회, 의사 예약 관리
사용 기술: Spring Boot, JWT, REST API, MySQL
🎨 UI&UX (Figma) 
https://www.figma.com/design/ylHhPm73MlV3AoLsfJMb1V/Untitled?node-id=0-1&p=f&t=VNsi8uPCDugPhxww-0
🗃️ ERD 및 테이블 정의
📊 핵심 테이블 관계
User → Reservation, Symptom_Selection
Doctor → Reservation, MedicalRecord
Department → DoctorDepartment, Mapping
Symptom → Symptom_Selection, Mapping
🔗 연결 테이블
Symptom_Selection (id, user_id, symptom_id, selected_at)
Symptom_Department_Mapping (symptom_id, department_id, weight)

📂 API 명세서
🗓️ 여름방학 일정표
🔒 인증 / 보안 구조
구분
설명
로그인 방식
이메일 + 비밀번호 입력 → JWT 발급
인증 방식
모든 API 요청 시 Authorization 헤더 포함
권한 제어
/doctor/** → ROLE_DOCTOR / /my/** → 일반 사용자
실패 처리
401: 인증 실패 / 403: 권한 없음 / 401: 토큰 만료
🧪 테스트 계정 예시
계정 유형
이메일
비밀번호
환자 테스트 계정
patient1@example.com
test1234
의사 테스트 계정
doctor1@example.com
test1234
🧾 예외 코드 정리
상태 코드
의미
설명
400
Bad Request
필수값 누락
401
Unauthorized
토큰 누락 또는 만료
403
Forbidden
권한 없음
409
Conflict
중복 예약 존재
500
Internal Server Error
서버 오류
