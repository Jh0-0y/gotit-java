<div align="center">
 <img src="https://github.com/user-attachments/assets/8bd1a3ea-5b29-4f1c-80de-6cdfc66b6bc1">
</div>
<br/>

# 온라인 학습 커뮤니티

**고등교육 학습자들이 효율적으로 지식과 정보를 공유할 수 있는 온라인 커뮤니티 게시판 플랫폼**

<br/>

![Java](https://img.shields.io/badge/java-007396?style=flat-square&logo=java&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-2496ED?style=flat-square&logo=jpa&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariaDB&logoColor=white)

</div>

---

# 📋 목차

- [기술 스택](#-기술-스택)
- [주요 기능](#-주요-기능)
- [프로젝트 구조](#-프로젝트-구조)
- [아키텍처](#-아키텍처)
- [실행 방법](#-실행-방법)
- [데이터베이스](#-데이터베이스-구조)

---

# 기술 스택

| 구분         | 기술                              |
| ------------ | --------------------------------- |
| **Language** | Java 17                           |
| **Platform** | Jakarta EE (Servlet 6.0, JSP 3.1) |
| **Build**    | Maven                             |
| **Database** | MariaDB                           |
| **View**     | JSP, JSTL                         |
| **Security** | jBCrypt (비밀번호 해싱)           |
| **Logging**  | SLF4J                             |

# 주요 기능

- **회원 시스템** - 회원가입, 로그인, 프로필 이미지 업로드
- **게시판** - 다중 보드 및 카테고리별 게시물 관리
- **Q&A** - 답변 채택 기능이 있는 질문/답변 시스템
- **반응** - 좋아요, 스크랩(북마크) 기능
- **댓글** - 게시물에 대한 댓글 작성 및 답변 채택
- **마이페이지** - 내 게시물, 스크랩 목록, 계정 설정
- **포인트/뱃지** - 사용자 활동 기반 게이미피케이션
- **검색** - 제목 기반 게시물 검색
- **페이지네이션** - 최신순, 조회수, 좋아요, 댓글수 정렬

<br/>

### 🔐 로그인 · 회원가입

> 구글 소셜 로그인 · 이메일 인증 · 비밀번호 강도 검증

<div>
  <img src="https://github.com/user-attachments/assets/6fbe6623-a86e-40f7-8a4f-efea121ca634">
</div>

<br/>

### 🏠 메인페이지

<div align="center">
  <img src="https://github.com/user-attachments/assets/c2645804-15de-43b4-aa6a-4bf9cdef9f16" />
</div>

<br/>

### 👤 게시글

> 좋아요 및 스크랩 · 마크다운 에디터 · 정렬

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/c15bab88-1bed-4157-9eb4-f5ecada65410">
      <br/><sub><b>게시글 상세보기</b></sub>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/de185b50-6c86-4b8c-9e5d-38ba12246b68">
      <br/><sub><b>정렬</b></sub>
    </td>
  </tr>
</table>

### 💻 댓글

> 댓글 채택

<table>
  <tr style="vertical-align:bottom;">
    <td align="center">
     <img width="430px" src="https://github.com/user-attachments/assets/ed76042d-72d0-4877-856a-763f7aecb22f">
      <br/><sub><b>댓글 작성</b></sub>
    </td>
    <td align="center">
      <img width="430px" src="https://github.com/user-attachments/assets/ff7af2cf-37b3-407d-a48f-007bb6541d03">
      <br/><sub><b>댓글 채택</b></sub>
    </td>
  </tr>
</table>

### 💬 유저 시스템

> 활동 기반 포인트 적립 (게시글 작성, 댓글 작성 등)

<div align="center">
 <img width="60%" src="https://github.com/user-attachments/assets/589b1ccd-337e-4deb-934b-8f74570d9a51" />
</div>

<br/>

### 🛠️ 반응형 해상도

> PC 및 모바일 등 모든 해상도 완벽 지원

<table style="display:flex;">
  <tbody style="margin:0 auto;">
    <tr style="vertical-align:bottom">
    <td align="center">
      <img width="941" height="1147" alt="스크린샷 2025-12-26 오후 12 33 38" src="https://github.com/user-attachments/assets/484352ea-ef7c-46a7-af9c-2fb273006958" />
    </td>
    <td align="center">
      <img width="960" height="1156" alt="스크린샷 2025-12-26 오후 12 33 17" src="https://github.com/user-attachments/assets/8f738d37-cbed-4ea5-bf49-870afb58f66e" />
    </td>
    <td align="center">
      <img width="937" height="1145" alt="스크린샷 2025-12-26 오후 12 33 27" src="https://github.com/user-attachments/assets/5e1e7943-ce6b-497b-94f2-91a710311eb1" />
    </td>
  </tr>
</tbody>
</table>

# 프로젝트 구조

```
src/main/
├── java/gotit/
│   ├── core/          # FrontController, ViewPaths (핵심 프레임워크)
│   ├── model/         # Entity 클래스 (User, Post, Board, Comment 등)
│   ├── auth/          # 인증 (로그인, 회원가입)
│   ├── post/          # 게시물 CRUD
│   ├── board/         # 게시판 목록 및 탐색
│   ├── comment/       # 댓글 및 답변
│   ├── reaction/      # 좋아요, 스크랩
│   ├── mypage/        # 마이페이지
│   ├── file/          # 파일 업로드 (프로필 이미지)
│   ├── page/          # 페이지네이션 유틸리티
│   └── common/util/   # 공통 유틸리티
└── webapp/
    ├── WEB-INF/
    │   ├── views/     # JSP 파일 (post, board, auth, mypage 등)
    │   └── web.xml    # 서블릿 설정
    └── assets/        # CSS, JS, 이미지
```

# 아키텍처

**Front Controller 패턴** 기반 MVC 구조를 사용합니다.

```
요청 (*.do)
    └── FrontController
            ├── /auth.do   → AuthController
            ├── /board.do  → BoardController
            ├── /post.do   → PostController
            ├── /mypage.do → MyPageController
            └── /admin.do  → AdminController
```

각 Controller는 Service → DAO 레이어를 통해 DB와 통신하며, 결과를 JSP View로 포워딩합니다.

# 실행 방법

### 사전 요구사항

- JDK 17+
- Apache Tomcat 10.x+
- MariaDB 10.x+
- Maven 3.x+

### 1. 데이터베이스 설정

MariaDB에 데이터베이스를 생성하고 스키마를 적용합니다.

```sql
CREATE DATABASE gotdb CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

### 2. Tomcat JNDI DataSource 설정

`context.xml`에 아래 DataSource를 추가합니다.

```xml
<Resource name="jdbc/gotDB"
          auth="Container"
          type="javax.sql.DataSource"
          driverClassName="org.mariadb.jdbc.Driver"
          url="jdbc:mariadb://localhost:3306/gotdb"
          username="your_username"
          password="your_password"
          maxTotal="20"
          maxIdle="10" />
```

### 3. 빌드 및 배포

```bash
# 빌드
mvn clean package

# 생성된 WAR 파일을 Tomcat webapps에 배포
cp target/gotit.war $TOMCAT_HOME/webapps/
```

### 4. 접속

```
http://localhost:8080/gotit/
```

# 데이터베이스 구조

| 테이블             | 설명                  |
| ------------------ | --------------------- |
| `users`            | 회원 정보             |
| `boards`           | 게시판 정보           |
| `board_categories` | 게시판 카테고리       |
| `posts`            | 게시물                |
| `post_comments`    | 댓글 (답변 채택 포함) |
| `post_likes`       | 좋아요                |
| `post_scraps`      | 스크랩                |
| `user_badges`      | 뱃지 정의             |
