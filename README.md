#  Java Maven Project Task 8

This is a simple **Java HelloWorld** application built using **Maven** and integrated with **Jenkins CI/CD**.

## Objective
Learn how to:
- Build a simple Java application using **Maven**
- Configure a **Jenkins Freestyle job**
- Automate builds and view console output

----
##  Project Structure
hello-java-maven/ <br>
├── pom.xml <br>
└── src/ <br>
└── main/ <br>
└── java/ <br>
└── HelloWorld.java <br>

---

## 💻 Source Code

src/main/java/HelloWorld.java
java

public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Jenkins + Maven!");
    }
}

-----

## Maven Configuration
pom.xml
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 
         http://maven.apache.org/xsd/maven-4.0.0.xsd">

  <modelVersion>4.0.0</modelVersion>
  <groupId>com.example</groupId>
  <artifactId>hello</artifactId>
  <version>1.0</version>

  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-compiler-plugin</artifactId>
        <version>3.8.1</version>
        <configuration>
          <source>1.8</source>
          <target>1.8</target>
        </configuration>
      </plugin>
    </plugins>
  </build>
</project>

-----
## Steps to Run
1️⃣ Clone the repository
git clone https://github.com/<your-username>/hello-java-maven.git
cd hello-java-maven

2️⃣ Build with Maven
mvn clean package

3️⃣ Run the application
java -cp target/classes HelloWorld

------

## Output:

Hello, Jenkins + Maven!

## Jenkins Integration

Start Jenkins (Docker recommended):

docker run -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts-jdk11


Open Jenkins: http://localhost:8080
--- 
Go to:

1) Manage Jenkins → Global Tool Configuration

2) Add Maven (e.g., Maven 3.8.6)

3)Create a new Freestyle Job

4)Source Code Management: Git → https://github.com/<your-username>/hello-java-maven.git

5)Build → Invoke top-level Maven targets → Goals: clean package
------

## Click Build Now
------

Check Console Output — should show:
[INFO] BUILD SUCCESS
----
Cansole output 
---
## screenshorts
---
Access from browser
----
![Branches](https://github.com/gawali-priyanka/Monitor-System-Resources-Using-Netdata/blob/main/screenshots/Access-dashbord1.png?raw=true)
---

