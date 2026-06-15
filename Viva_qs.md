Here is a highly targeted set of Viva questions covering all the experiments you've prepared. They are structured with the exact, short answers examiners look for so you can recall them instantly.

### Category 1: Docker Basics & OS Containers

**Q1: What is the difference between a Docker Image and a Docker Container?**

* **Answer:** An image is a read-only template/blueprint containing the application and its environment. A container is a live, isolated, running instance of that image.

**Q2: Why do OS images like Ubuntu or Alpine exit immediately if you run them without the `-it` flag?**

* **Answer:** Containers require an active background process to stay alive. Running them with `-it` (Interactive Terminal) attaches a shell process (`bash` or `sh`), which keeps the container running.

**Q3: What is unique about the Alpine Linux image, and why is it preferred in production?**

* **Answer:** Alpine is an ultra-lightweight Linux distribution (~5MB). It is preferred because it reduces disk space, speeds up download times, and minimizes security vulnerabilities.

---

### Category 2: Jenkins & SonarQube Integration

**Q4: Why do we create a custom Docker Network (`docker network create`) for Jenkins and SonarQube?**

* **Answer:** It enables safe network communication between the containers, allowing Jenkins to reach SonarQube using its container name (`http://sonar:9000`) instead of tracking changing IP addresses.

**Q5: What is the significance of the `-Dsonar.sources=.` property in the pipeline script?**

* **Answer:** The dot (`.`) tells the SonarQube scanner to analyze all source files located in the current root workspace directory.

**Q6: In a Jenkins pipeline, when would you use `sh` vs. `bat`?**

* **Answer:** Use `sh` for Linux-based environments (like standard Docker containers) and `bat` for Windows-based host environments.

---

### Category 3: Maven & Gradle Build Tools

**Q7: What are the primary configuration files for Maven and Gradle?**

* **Answer:** Maven uses `pom.xml` (written in XML). Gradle uses `build.gradle` (written in Groovy or Kotlin DSL).

**Q8: Explain the term "Dependency Management" in Maven.**

* **Answer:** It is the automated process of declaring external libraries (like JUnit) in the `pom.xml`. Maven automatically downloads and updates them from the online Maven Central Repository, eliminating manual JAR management.

**Q9: How do you migrate an existing Maven project to Gradle without rewriting the configuration?**

* **Answer:** Navigate to the project root folder containing the `pom.xml` and execute the `gradle init` command. Gradle automatically reads the POM file and generates the corresponding Gradle configuration files.

---

### Category 4: Microservices & Docker Compose

**Q10: What is the core purpose of Docker Compose?**

* **Answer:** Docker Compose is a tool used to define, deploy, and manage multi-container applications (microservices) simultaneously using a single YAML configuration file (`docker-compose.yml`).

**Q11: How do microservices within a `docker-compose.yml` file discover and talk to each other?**

* **Answer:** Docker Compose automatically creates a shared network for all services listed in the file. Services can find and talk to each other using their service names (e.g., a web app connecting to a host named `redis`).

**Q12: What is the difference between `docker-compose up` and `docker-compose down`?**

* **Answer:** `docker-compose up` builds, creates, and starts all defined services. `docker-compose down` stops and completely removes the containers, networks, and volumes created by `up`.

### Last-Minute Strategy:

If an examiner asks a question you aren't 100% sure about, anchor your answer back to the fundamentals: **Docker is about isolation/portability, Maven/Gradle are about automation, and SonarQube is about code security/quality.** Good luck—you have mastered the material!
