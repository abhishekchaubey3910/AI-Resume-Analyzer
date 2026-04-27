# 🧠 Resume Analyzer

<p align="center">
  <img src="https://img.shields.io/badge/Status-Live-brightgreen?style=for-the-badge" alt="Live Status" />
  <img src="https://img.shields.io/badge/AI-Google%20Gemini-blue?style=for-the-badge&logo=google" alt="Gemini AI" />
  <img src="https://img.shields.io/badge/Backend-Spring%20Boot-green?style=for-the-badge&logo=springboot" alt="Spring Boot" />
  <img src="https://img.shields.io/badge/Frontend-React.js-61DAFB?style=for-the-badge&logo=react" alt="React" />
  <img src="https://img.shields.io/badge/DB-MySQL-orange?style=for-the-badge&logo=mysql" alt="MySQL" />
  <a href="https://resume-analyser-kp0f.onrender.com/">
    <img src="https://img.shields.io/badge/🚀%20Live%20App-Click%20Here-purple?style=for-the-badge" alt="Live App" />
  </a>
</p>

---

## 📖 Description

**Resume Analyzer** is a full-stack AI-powered web application that analyzes resumes and provides actionable insights including:

- ✅ **Skill Extraction** — Automatically identifies key skills from your resume
- 📊 **Resume Evaluation** — Scores your resume based on quality and completeness
- 💡 **Improvement Suggestions** — AI-driven tips to strengthen your resume
- 💼 **Job Recommendations** — Relevant job listings matched to your profile

Powered by **Google Gemini AI** with secure authentication (email OTP verification & password reset) and a modern dark-themed glassmorphism UI.

---

## 🛠️ Tech Stack

| Layer     | Technology            |
|-----------|-----------------------|
| Frontend  | React.js, CSS Modules |
| Backend   | Spring Boot (Java)    |
| Database  | MySQL                 |
| AI Engine | Google Gemini AI      |
| Email     | Brevo (SendinBlue)    |
| Jobs API  | Adzuna API            |

---

## 🖼️ Preview

<p align="center">
  <img width="30%" src="https://github.com/user-attachments/assets/df7bb0c1-1f10-478d-b8c9-c2b1bf2369f4" />
  <img width="30%" src="https://github.com/user-attachments/assets/1c65a0cc-c915-4103-a7fe-30a975639ab0" />
  <img width="30%" src="https://github.com/user-attachments/assets/b8ca21ad-7c2f-470d-ad5d-73119b8fd9f1" />
</p>

<p align="center">
  <img width="30%" src="https://github.com/user-attachments/assets/3f945bf1-84dd-4052-9c65-709f512ae0a4" />
  <img width="30%" src="https://github.com/user-attachments/assets/d04af8b7-4e12-4948-94c6-3b1f15340180" />
  <img width="30%" src="https://github.com/user-attachments/assets/a0c6f513-2108-41c8-98b5-91e86d27d398" />
</p>

---

## 🚀 How to Run Locally

### 1. Clone the Repository

```bash
git clone https://github.com/Mohamed-Imran-12/Resume-Analyser.git
cd Resume-Analyser
```

### 2. Open in IDE

Open the project in **IntelliJ IDEA** or **Eclipse**, then open `pom.xml` and let Maven download all dependencies.

### 3. Configure `application.properties`

Create or update `src/main/resources/application.properties` with your credentials:

#### 🗄️ Database (MySQL)
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/your_db
spring.datasource.username=your_DB_USERNAME
spring.datasource.password=your_DB_PASSWORD
```

#### 🤖 Google Gemini AI
```properties
genKey=your_GEMINI_API_KEY
```

#### 📧 Mail Service (Brevo)
```properties
apiKey=your_BREVO_MAIL_API
```

#### 🔑 Google OAuth (Optional)
```properties
spring.security.oauth2.client.registration.google.client-id=your_GCP_ID
spring.security.oauth2.client.registration.google.client-secret=your_GCP_SECRET
```

#### 💼 Job Suggestions (Adzuna — Optional)
```properties
application-id=your_ADZUNA_APP_ID
application-api-key=your_ADZUNA_API_KEY
```

### 4. Run the Backend

Run `ResumeAnalyserApplication.java` from your IDE, or:

```bash
./mvnw spring-boot:run
```

### 5. Open in Browser

```
http://localhost:8080/
```

---

## 🎨 Frontend Development

The React frontend is built separately and served as static files by the Spring Boot backend.

### Run in Development Mode

```bash
cd "frontend src"
npm install
npm run dev
```

### Build for Production (Backend Deployment)

```bash
cd "frontend src"
npm run build
```

Then copy the contents of `dist/` into `src/main/resources/static/`:

```
static/
├── assets/
│   ├── *.css
│   └── *.js
└── index.html
```

> ⚠️ Delete old `index.html` and files inside `assets/` before copying new build files.

---

## 🔧 Architecture Notes

- The React app is **built and served by Spring Boot** as static files in production
- The `static/templates/` folder stores **email templates** used for OTP verification and password reset
- Only **Gemini AI** is configured by default — to switch providers, update `appservice.java`
- Email works **only with Brevo** — to switch providers, update `mailservice.java`

---

## ⚠️ Important Notes

- 🤖 AI models evolve rapidly. If the Gemini model is deprecated, update the model name in `appservice.java`
- 📧 Email OTP functionality requires a valid Brevo API key
- 💼 Job suggestions require Adzuna API credentials (omit to disable this feature)
- Do **not** edit files inside the backend `static/` folder directly — always rebuild from the frontend source

---

## 📄 Disclaimer

> This project is developed for **learning and demonstration purposes**.  
> AI-generated analysis results may vary and should **not** be considered professional career advice.

---

<p align="center">Made with ❤️ using Google Gemini AI + Spring Boot + React</p>
