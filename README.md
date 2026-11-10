# JOY-RIDE — Bike Rental & Ride Sharing System

A Java-based web application developed as a six-member Year 1, Semester 2 group project at the Sri Lanka Institute of Information Technology (SLIIT) for the Object-Oriented Programming (OOP) and Data Structures & Algorithms (DSA) modules.

JOY-RIDE provides a platform for users to browse bikes, check availability, submit rental requests, manage their profiles, and interact with bike reviews. Administrators can manage bikes, users, rental requests, payments, and reviews.

> **Academic project:** This repository contains a university group project. It is intended for learning and portfolio demonstration, not production use.

## Features

### User features
- User registration and login
- Password hashing with BCrypt
- Session-based profile management
- Browse bikes and view bike details
- Check bike availability and submit rental requests
- Upload payment-slip files for rental processing
- Submit and view reviews

### Administrator features
- Admin login and profile management
- Add, update, and delete bikes
- View and manage users
- Review and process rental requests and payment records
- Manage reviews

### Data structures and algorithms
- Circular queue implementation for handling rental requests
- Quick Sort implementation in the bike-list workflow

## Technology stack

- **Backend:** Java, JSP, Servlets
- **Frontend:** HTML, CSS, JavaScript
- **Web/application server:** Apache Tomcat
- **Build/dependency management:** Maven
- **Libraries:** JSTL, Gson, jBCrypt, Commons FileUpload, Commons IO
- **Data storage in the original coursework version:** Text files
- **IDE used:** IntelliJ IDEA

## Project structure

```text
Joy_Rides/
├── pom.xml
├── src/
│   └── main/
│       ├── java/                 # Java models, servlets and management logic
│       ├── resources/            # Runtime text-file data (keep real/private data out of Git)
│       └── webapp/               # JSP pages, CSS, JavaScript and web assets
│           └── WEB-INF/
│               └── web.xml
└── README.md
```

## Requirements

- JDK 11 (or a compatible JDK configured for the project)
- Apache Maven
- Apache Tomcat 9.x (the project uses the `javax.servlet` API; Tomcat 10+ uses the incompatible `jakarta.servlet` namespace unless the application is migrated)
- IntelliJ IDEA or another Java IDE

## Setup and running

1. Clone the repository:

   ```bash
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
   cd YOUR-REPOSITORY
   ```

2. Open the project in IntelliJ IDEA and load it as a Maven project.

3. Configure JDK 11 and a local Tomcat 9 server in your IDE.

4. **Configure the data files and upload directory before running.** The coursework version originally used local absolute file paths and local text-file storage. Replace those paths with portable paths (for example, paths derived from the application data directory or configuration) and create empty/sample data files. Do not use real user records, passwords, payment records, identity details, or payment-slip uploads.

5. Build the web application after configuring the Maven project as a WAR:

   ```bash
   mvn clean package
   ```

6. Deploy the generated WAR from `target/` to Tomcat 9, or configure a Tomcat 9 run configuration in IntelliJ IDEA.

7. Start Tomcat and open the local application URL shown by your server configuration, usually:

   ```text
   http://localhost:8080/YOUR-CONTEXT-PATH/
   ```

> **Important setup note:** Check `pom.xml` and ensure it declares `<packaging>war</packaging>`. The supplied project uses a web application layout, but the supplied POM did not explicitly declare WAR packaging. Also review every file-storage path before expecting the application to run on another computer.

## Data and privacy

The original project uses TXT files for application data. For a public repository:

- Commit only empty templates or clearly fictional sample data.
- Never commit real user names, email addresses, student IDs, phone numbers, password hashes, rental/payment records, or uploaded payment slips.
- Keep runtime data and user-uploaded files outside the source-controlled project, or exclude them using `.gitignore`.
- Do not publish credentials, local machine paths, or private configuration.
- BCrypt hashes are not plaintext passwords, but real users' hashes and account records are still private and must not be published.

## Screenshots

Add selected, sanitized screenshots to a folder such as `docs/screenshots/` and embed them here. Suggested screenshots:

- Home / landing page
- Bike listing and bike details
- Registration or login page (without real credentials)
- Rental request / booking flow (using dummy data)
- User profile (with fictional details)
- Admin dashboard
- Bike management page
- Rental request or payment management page (with all personal/payment information removed)
- Reviews page

Example:

```markdown
![JOY-RIDE home page](docs/screenshots/home.png)
```

## Group project and contributions

This was completed by a team of six students. Add the six members' names and, if appropriate, their GitHub profile links below. Describe each person's actual contribution; do not imply that one member independently developed the entire application.

| Team member | Contribution |
|---|---|
| IT24100816 | User management |
| IT24104217 | Bike management |
| IT24100658 | Admin management |
| IT24103553 | Bike rental management |
| IT24104116 | Billing & Payment management |
| IT24102308 | Reviews & Feedback management |

## Learning outcomes

This project provided practical experience with object-oriented programming, Java web application development, JSP and Servlets, session handling, password hashing, file-based persistence, data structures, sorting, and collaborative software development.

## Disclaimer

This project was created for academic purposes. Any sample accounts or data added to this repository should be fictional. The application has not been represented as production-ready or security-audited.
