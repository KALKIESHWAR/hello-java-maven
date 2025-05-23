# Hello Java Maven

This is a simple Java application built using **Maven** and integrated with **Jenkins** for continuous integration. The purpose of this project is to demonstrate how to run a basic Maven build job inside Jenkins.

---

## 💡 Project Description

This project contains a Java program that greets the user. It is structured using Maven’s standard directory layout and built using the Maven lifecycle (`clean`, `package`).

The project is intended as a learning exercise for:

- Java application structure
- Maven build configuration
- Jenkins CI pipeline setup

---

## 🧱 Project Structure

```
hello-java-maven/
├── pom.xml
├── README.md
└── src/
    └── main/
        └── java/
            └── com/
                └── example/
                    └── HelloWorld.java
```

---

## 🚀 How to Run Locally

### Prerequisites

- Java JDK 8 or 11
- Maven 3.6 or above

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/KALKIESHWAR/hello-java-maven.git
   cd hello-java-maven
   ```

2. Build the project:
   ```bash
   mvn clean package
   ```

3. Run the program:
   ```bash
   java -cp target/hello-1.0.jar com.example.HelloWorld
   ```

---

## ⚙️ Jenkins Setup

### Jenkins Job Configuration:

1. **Create a New Job**:  
   Freestyle project → `HelloWorld-Maven-Build`

2. **Source Code Management** (Optional):  
   Use Git if hosted on GitHub

3. **Build Step**:  
   Add → `Invoke top-level Maven targets`  
   Goals: `clean package`

4. **Run the Job**:  
   Click **Build Now** and check for `BUILD SUCCESS` in console output

---

## ✅ Output Example

```
Enter your name: Kalki
Hello, Kalki! Welcome to Jenkins and Maven!
```

---

## 📝 Notes

- Make sure Maven is correctly configured in Jenkins under **Global Tool Configuration**
- The build creates a JAR file at `target/hello-1.0.jar`

---
