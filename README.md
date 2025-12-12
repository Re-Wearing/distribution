<div align="center">

# 🧥 RE:WEAR

**입지 않는 옷에 새로운 가치를, 의류 기부 중개 플랫폼**

[![Java](https://img.shields.io/badge/Java-21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)

[🌐 데모 보기](http://ec2-13-209-64-97.ap-northeast-2.compute.amazonaws.com/)
[🌐 시연 영상](https://youtu.be/44GKcobj6Sg)

</div>

---

## 📋 목차

- [프로젝트 소개](#-프로젝트-소개)
- [주요 기능](#-주요-기능)
- [기술 스택](#-기술-스택)
- [프로젝트 구조](#-프로젝트-구조)
- [시작하기](#-시작하기)
- [환경 변수](#-환경-변수)
- [API 문서](#-api-문서)
- [스크린샷](#-스크린샷)
- [팀원](#-팀원)
- [라이선스](#-라이선스)

---

## 🎯 프로젝트 소개

**RE:WEAR**는 개인이 입지 않는 의류를 필요로 하는 기관(비영리단체, 복지기관 등)에 연결해주는 **의류 기부 중개 플랫폼**입니다.

### 왜 RE:WEAR인가요?

- 🌱 **환경 보호**: 버려지는 의류를 줄여 환경 오염 감소에 기여
- 💝 **나눔 문화**: 필요한 곳에 따뜻한 마음을 전달
- 🔄 **선순환 구조**: 기부자 → 플랫폼 → 기관 → 수혜자로 이어지는 투명한 기부 과정

### 기부 프로세스

```
📦 물품 등록 → ✅ 관리자 승인 → 🤝 기관 매칭 → 🚚 배송 → ✨ 완료
```

---

## ✨ 주요 기능

### 👤 일반 회원 (기부자)
| 기능 | 설명 |
|------|------|
| 🎁 기부 신청 | 의류 정보 입력 및 사진 업로드로 간편하게 기부 신청 |
| 📍 매칭 방식 선택 | 자동 매칭 또는 원하는 기관 직접 선택 |
| 📊 기부 현황 조회 | 실시간으로 기부 진행 상황 확인 |
| 📝 후기 작성 | 기부 완료 후 후기 게시판에 경험 공유 |

### 🏢 기관 회원 (수혜 기관)
| 기능 | 설명 |
|------|------|
| 📋 매칭 제안 확인 | 관리자로부터 받은 기부 매칭 제안 수락/거절 |
| 📢 요청 게시글 | 필요한 의류 종류를 게시판에 요청 |
| 📈 수령 내역 관리 | 받은 기부 물품 내역 확인 |

### 🛡️ 관리자
| 기능 | 설명 |
|------|------|
| ✅ 물품 승인 | 기부 물품 검토 및 승인/거절 |
| 🏛️ 기관 승인 | 신규 기관 회원 가입 승인 |
| 🔗 매칭 관리 | 기부 물품과 기관 간 최적 매칭 |
| 🚚 배송 관리 | 배송 정보 입력 및 상태 관리 |
| 👥 회원 관리 | 전체 회원 조회 및 관리 |

### 🔔 공통 기능
- 실시간 알림 시스템
- FAQ 및 1:1 문의
- 게시판 (공지사항, 기부 후기, 요청 게시글)

---

## 🛠 기술 스택

### Backend
| 기술 | 버전 | 설명 |
|------|------|------|
| Java | 21 | 메인 언어 |
| Spring Boot | 3.x | 웹 프레임워크 |
| Spring Security | - | 인증/인가 |
| Spring Data JPA | - | ORM |
| MySQL | 8.0 | 데이터베이스 |
| Thymeleaf | - | 서버사이드 템플릿 (관리자 뷰) |
| Gradle | - | 빌드 도구 |

### Frontend
| 기술 | 버전 | 설명 |
|------|------|------|
| React | 19 | UI 라이브러리 |
| Vite | 7 | 빌드 도구 |
| Express | 4 | 프로덕션 서버 |
| jsPDF | 2.5 | PDF 생성 |

### Infrastructure
| 기술 | 설명 |
|------|------|
| AWS EC2 | 서버 호스팅 |
| AWS EC2 Nginx | 프론트엔드 배포 |
| Gmail SMTP | 이메일 발송 |

---

## 📁 프로젝트 구조

```
📦 RE:WEAR
├── 📂 Back/                          # Spring Boot 백엔드
│   ├── 📂 src/main/java/com/rewear/
│   │   ├── 📂 admin/                 # 관리자 기능
│   │   ├── 📂 common/                # 공통 유틸, Enum
│   │   ├── 📂 config/                # 설정 (Security, CORS 등)
│   │   ├── 📂 delivery/              # 배송 관리
│   │   ├── 📂 donation/              # 기부 관리 (핵심 도메인)
│   │   ├── 📂 email/                 # 이메일 인증
│   │   ├── 📂 faq/                   # FAQ/문의
│   │   ├── 📂 notification/          # 알림
│   │   ├── 📂 organ/                 # 기관 회원
│   │   ├── 📂 post/                  # 게시판
│   │   ├── 📂 signup/                # 회원가입
│   │   └── 📂 user/                  # 사용자 관리
│   └── 📂 src/main/resources/
│       ├── 📄 application.properties # 설정 파일
│       └── 📂 templates/             # Thymeleaf 템플릿
│
├── 📂 Front/                         # React 프론트엔드
│   ├── 📂 src/
│   │   ├── 📂 components/            # 재사용 컴포넌트
│   │   ├── 📂 pages/                 # 페이지 컴포넌트
│   │   ├── 📂 styles/                # CSS 스타일
│   │   ├── 📂 constants/             # 상수 데이터
│   │   ├── 📂 utils/                 # 유틸리티 함수
│   │   └── 📄 App.jsx                # 메인 앱 컴포넌트
│   ├── 📄 package.json
│   └── 📄 vite.config.js
│
└── 📄 README.md
```

---

## 🚀 시작하기

### 필수 요구사항

- **Java** 21 이상
- **Node.js** 18 이상
- **MySQL** 8.0 이상
- **Gradle** 7.x 이상

### 1. 저장소 클론

```bash
git clone https://github.com/Re-Wearing/distribution.git
cd distribution
```

### 2. 데이터베이스 설정

```sql
-- MySQL에서 데이터베이스 생성
CREATE DATABASE rewear CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

-- 사용자 생성 및 권한 부여
CREATE USER 'rewear'@'localhost' IDENTIFIED BY 'your_password';
GRANT ALL PRIVILEGES ON rewear.* TO 'rewear'@'localhost';
FLUSH PRIVILEGES;
```

### 3. 백엔드 실행

```bash
cd Back

# 환경 변수 설정 (또는 application.properties 수정)
export DB_USERNAME=rewear
export DB_PASSWORD=your_password

# 빌드 및 실행
./gradlew bootRun
```

백엔드 서버: `http://localhost:8080`

### 4. 프론트엔드 실행

```bash
cd Front

# 의존성 설치
npm install

# 개발 서버 실행
npm run dev
```

프론트엔드 서버: `http://localhost:5173`

---

## ⚙️ 환경 변수

### Backend (application.properties)

| 변수명 | 설명 | 기본값 |
|--------|------|--------|
| `DB_URL` | 데이터베이스 URL | `jdbc:mysql://localhost:3306/rewear` |
| `DB_USERNAME` | DB 사용자명 | `rewear` |
| `DB_PASSWORD` | DB 비밀번호 | - |
| `MAIL_USERNAME` | 이메일 발송 계정 | - |
| `MAIL_PASSWORD` | 이메일 앱 비밀번호 | - |
| `UPLOAD_DIR` | 파일 업로드 경로 | `uploads` |
| `JPA_DDL_AUTO` | DDL 자동 생성 모드 | `update` |

### 기본 테스트 계정

| 역할 | 아이디 | 비밀번호 |
|------|--------|----------|
| 관리자 | `admin` | `admin` |
| 일반 회원 | `user01` | `user01` |
| 기관 회원 | `organ01` | `organ01` |

---

## 📚 API 문서

### 주요 API 엔드포인트

#### 인증
| Method | Endpoint | 설명 |
|--------|----------|------|
| POST | `/api/users/login` | 로그인 |
| POST | `/api/users/signup` | 회원가입 |
| POST | `/api/users/signup/organ` | 기관 회원가입 |
| GET | `/api/users/me` | 현재 사용자 정보 |

#### 기부
| Method | Endpoint | 설명 |
|--------|----------|------|
| POST | `/api/donations` | 기부 신청 |
| GET | `/api/donations` | 기부 목록 조회 |
| GET | `/api/donations/{id}` | 기부 상세 조회 |
| PUT | `/api/donations/{id}/status` | 기부 상태 변경 |

#### 기관
| Method | Endpoint | 설명 |
|--------|----------|------|
| GET | `/api/organs` | 승인된 기관 목록 |
| GET | `/api/organs/pending` | 승인 대기 기관 목록 |

#### 게시판
| Method | Endpoint | 설명 |
|--------|----------|------|
| GET | `/api/posts` | 게시글 목록 |
| POST | `/api/posts` | 게시글 작성 |

#### 알림
| Method | Endpoint | 설명 |
|--------|----------|------|
| GET | `/api/notifications` | 알림 목록 |
| GET | `/api/notifications/unread-count` | 읽지 않은 알림 수 |

---

## 👥 팀원

<div align="center">

| 이름 | 역할 | GitHub |
|------|------|--------|
| 김동욱 | Backend / PM | [@github](https://github.com/dw426) |
| 김가빈 | Backend | [@github](https://github.com/vinn81) |
| 고준영 | Frontend | [@github](https://github.com/rhwnsdud70) |
| 권석현 | Frontend | [@github](https://github.com/seokhyunkwon) |
| 석지윤 | Frontend | [@github](https://github.com/yooning8) |
| 박정은 | Frontend | [@github](https://github.com/parkje0323) |

</div>

---

## 📄 라이선스

이 프로젝트는 [MIT 라이선스](LICENSE)를 따릅니다.

---

<div align="center">

### 🌟 프로젝트가 마음에 드셨다면 Star를 눌러주세요!

Made with ❤️ by RE:WEAR Team

</div>
