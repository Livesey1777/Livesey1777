# 👋 Hi, I'm Mikhail Sazhin

![Java Developer](https://img.shields.io/badge/Java_Backend_Developer-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Location](https://img.shields.io/badge/Omsk,_Russia-FFFFFF?style=for-the-badge&logo=google-maps&logoColor=red)

**Backend Java Engineer** with **~1 year 3 months** at Hexlet plus consistent hands-on projects (**~1.5 years** focused practice overall). I build server-side apps with **Java** and the **Spring** ecosystem, care about **clear architecture**, **tests**, and **working with databases** in a predictable way (migrations, transactions, sensible ORM usage). Recent work includes **event-driven microservices** and **Kafka** (see the **Saga** demo repo).

---

## 🛠️ Tech Stack

### **Core & Backend**
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=spring-boot&logoColor=white)
![Spring MVC](https://img.shields.io/badge/Spring_MVC-6DB33F?style=flat&logo=spring&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat&logo=springsecurity&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=flat&logo=apache-maven&logoColor=white)
![Gradle](https://img.shields.io/badge/Gradle-02303A?style=flat&logo=gradle&logoColor=white)

### **Messaging & distributed patterns**
![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=flat&logo=apache-kafka&logoColor=white)
![Spring Kafka](https://img.shields.io/badge/Spring_for_Apache_Kafka-6DB33F?style=flat&logo=spring&logoColor=white)

### **Databases & ORM**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white)
![H2 Database](https://img.shields.io/badge/H2-4479A1?style=flat&logo=h2&logoColor=white)
![JPA/Hibernate](https://img.shields.io/badge/JPA/Hibernate-59666C?style=flat&logo=hibernate&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat&logo=flyway&logoColor=white)
![Liquibase](https://img.shields.io/badge/Liquibase-2962FF?style=flat&logo=liquibase&logoColor=white)

### **Tools & DevOps**
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Docker Compose](https://img.shields.io/badge/Docker_Compose-2496ED?style=flat&logo=docker&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-E40521?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat&logo=postman&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ_IDEA-000000?style=flat&logo=intellij-idea&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=flat&logo=swagger&logoColor=black)

---

## 📁 Featured Projects

### **🔄 Saga orchestration (microservices, Kafka)** | [View Repository](https://github.com/Levasey/saga-pattern-spring-boot)
*Java 17, Spring Boot 3.2, Maven (multi-module), Spring Web, Spring Data JPA, Hibernate, PostgreSQL, Apache Kafka, Spring Kafka, Docker Compose, Testcontainers, JUnit 5, Jakarta Bean Validation, Jackson*

- **Saga orchestration**: **orders-service** drives **reserve → pay → approve** using Kafka **command/event** topics; on payment failure, **compensation** cancels the product reservation and rejects the order
- Shared **core** module (**DTOs**, **commands**, **events**); REST + JPA in each service; **HTTP** client to a mock **credit-card processor**
- **Kafka** (multi-broker **Docker Compose** stack), topics provisioned at startup; **PostgreSQL** for local runs
- **Testcontainers** where enabled in modules for integration-oriented tests

### **📚 Library — readers & books (Spring Data JPA)** | [View Repository](https://github.com/Levasey/com.springDataJPA.library)
*Spring Boot 3, Spring Data JPA, Hibernate 6, Flyway, Spring Security (CSRF), Thymeleaf, PostgreSQL, JUnit 5, Mockito*

- Web app for **lending/returning books**, **search**, **pagination/sorting**, validation and error handling
- **Flyway** migrations + JPA **`validate`** (schema matches entities in production-minded setup)
- **Spring Security** for forms; **Actuator** exposed in a controlled way (health for probes, etc.)
- **Repositories + service layer**; **`JOIN FETCH`** where it helps avoid **N+1**
- Tests with **Mockito** and **`@DataJpaTest`** (H2 profile for slices)

### **📋 Task Management System** | [View Repository](https://github.com/Levasey/java-project-99)
*Spring Boot, PostgreSQL, JWT, Thymeleaf, Spring MVC, Docker, GitHub Actions*

- **Task tracker** inspired by Redmine-style workflows (tasks, people, labels, comments)
- **JWT** auth and **role split** (e.g. user vs admin) where applicable in the project
- **Integration tests** for API/security-critical paths (**where implemented in repo**)
- **Docker** + **CI** via **GitHub Actions** (**if enabled in repo — link workflow in README**)

### **🔍 URL Inspection Tool** | [View Repository](https://github.com/Levasey/java-project-72)
*Java 21, Javalin, PostgreSQL/H2, Gradle, JTE Templates*

- **URL analysis** app: availability checks, titles, meta descriptions, stored runs/metadata
- **Async-friendly** request handling for HTML fetch/parse workflows
- **PostgreSQL** vs **H2** profiles; **JTE** for HTML; pooling with **HikariCP**
- Layering: controllers, services, repositories

### **✅ Data Validator Library** | [View Repository](https://github.com/Levasey/java-project-78)
*Java, Design Patterns, Validation Framework, Unit Testing*

- **Flexible validation** with multiple types and **nested/recursive** structures
- **Builder**-style fluent API; **strategy**-like composition for rules
- Strong **JUnit 5** coverage on validation paths

### **📊 File Differ (gendiff)** | [View Repository](https://github.com/Levasey/java-project-71)
*Java, Gradle, JSON/YAML, CLI (Picocli)*

- **CLI diff** for JSON/YAML with **recursive** structure comparison
- Multiple **output formats** (stylish / plain / JSON)
- Solid **error handling** and **Gradle**-based build

### **🎮 Brain Games Collection** | [View Repository](https://github.com/Levasey/java-project-61)
*Java, Gradle, Console, Algorithms*

- **Five** small **CLI games** (parity, calc, GCD, progression, prime)
- **Three-round** flow; emphasis on **clean structure** and **readable** modules

---

## 🚀 More on GitHub

| Project | Stack / note | Link |
|--------|----------------|------|
| **Saga + Kafka** | Spring Boot, PostgreSQL, Kafka, Saga orchestration, Docker Compose | [saga-pattern-spring-boot](https://github.com/Levasey/saga-pattern-spring-boot) |
| Spring blog (Hexlet) | Spring MVC, classic web | [hexlet-spring-blog](https://github.com/Levasey/hexlet-spring-blog) |
| Algorithms practice | Java drills | [grokking-algorithms](https://github.com/Levasey/grokking-algorithms) · [algorithms-project-69](https://github.com/Levasey/algorithms-project-69) |

---

## 📊 GitHub Stats

<div align="center">

![Mikhail's GitHub stats](https://github-readme-stats.vercel.app/api?username=Livesey1777&show_icons=true&theme=dark&hide_border=true&cache_seconds=86400)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Livesey1777&layout=compact&theme=dark&hide_border=true&langs_count=8&exclude_repo=github-readme-stats)

![GitHub Streak](https://streak-stats.demolab.com?user=Livesey1777&theme=dark&hide_border=true&date_format=j%20M%5B%20Y%5D)

</div>

---

## 🎓 Learning Path & Expertise

### **Core competencies**
- **Java**: OOP, collections, streams, exceptions, basic concurrency
- **Spring**: Spring Boot, MVC, Spring Data JPA, Spring Security basics
- **Databases**: PostgreSQL, schema design, migrations (**Flyway** / **Liquibase**), transactions
- **APIs**: REST principles, OpenAPI/Swagger where applicable
- **Testing**: JUnit 5, Mockito, integration tests for web layers
- **Messaging (learning / portfolio)**: Apache Kafka with **Spring Kafka** — topics, commands vs events, multi-service flow (**Saga** demo)

### **Currently deepening**
- **Docker Compose** and deployment-shaped setups (multi-service + Kafka cluster locally)
- **CI/CD** (GitHub Actions-first)
- **Distributed workflows**: saga-style **orchestration**, **compensation**, reliability basics — grounded in the Kafka demo
- **System design** foundations (reliability, scaling, caching — learning curve)

---

## 📝 Education

- **Hexlet** — Java Developer (**2025–2026**, Hexlet карьера)
- **СПбГУ ГА**, инженер по направлению аэронавигационное обслуживание (**2014**)
- **JavaRush** — Java Core (29 levels completed)

**Self-directed**
- Algorithms & structures (books + practice)
- **Designing Data-Intensive Applications** (selected chapters)
- Clean Code / maintainability habits in small projects

**Open source (when true, list PR URLs)**  
If you have merged PRs — add one line each, e.g. `Contributed to hexlet-cv: <pr-link>`.

---

## 📫 Connect

<div align="center">

[![Email](https://img.shields.io/badge/email-michail--s1988%40rambler.ru-D14836?style=for-the-badge&logo=minutemailer&logoColor=white)](mailto:michail-s1988@rambler.ru)
[![GitHub](https://img.shields.io/badge/GitHub-Livesey1777-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Livesey1777)
[![Telegram](https://img.shields.io/badge/Telegram-Livesey1777-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/Livesey1777)
[![LeetCode](https://img.shields.io/badge/LeetCode-Profile-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/Levasey/)

</div>

---

## 💼 Professional Highlights

```java
public final class AboutMe {

    private static final String NAME = "Mikhail Sazhin";
    private static final String ROLE = "Backend Java Engineer";

    /** Hexlet track + shipped learning projects (portfolio — see GitHub). */
    private static final String EXPERIENCE_NOTE = "~1 year 3 months Hexlet + ~1.5 years focused practice";

    private static final List<String> PRIMARY_SKILLS = List.of(
            "Java 17+",
            "Spring Boot",
            "Spring Data JPA",
            "PostgreSQL",
            "REST APIs",
            "Spring Security",
            "Docker / Docker Compose",
            "Apache Kafka / Spring Kafka",
            "JUnit 5 / Mockito"
    );

    private static final Map<String, String> CAREER = Map.of(
            "Status", "Open to opportunities",
            "Format", "Remote (preferred — résumé); Hybrid / On-site — discuss",
            "Location", "Russia (relocation — discuss)",
            "Commitment", "Full-time / part-time / project — discuss"
    );

    public String summary() {
        return """
                Backend-focused Java developer. Strongest public work: Spring Boot + JPA \
                library project (Flyway, Security, tests — pinned repo). Also shipping a \
                Kafka-based Saga orchestration demo (multi-module Spring Boot, Docker Compose). \
                Learning CI/CD and system design; comfortable with SQL and pragmatic API design.""";
    }
}
```
