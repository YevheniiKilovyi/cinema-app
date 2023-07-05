# :movie_camera: Cinema Service :movie_camera:
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=Hibernate&logoColor=white)
	![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
 	![Apache Maven](https://img.shields.io/badge/Apache%20Maven-C71A36?style=for-the-badge&logo=Apache%20Maven&logoColor=white)
  	![Apache Tomcat](https://img.shields.io/badge/apache%20tomcat-%23F8DC75.svg?style=for-the-badge&logo=apache-tomcat&logoColor=black)
   	![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
# About the application

That's a basic RESTful application, built with Spring Framework, which can perform all of basic resource methods.

# Features 
* registration like a "USER"
* registration like an "ADMIN"
* authentication system built with Spring Security
* creating a cinema hall / getting a list of all cinema halls
* creating a movie / getting a list of all movies
* create/update/remove a movie session / getting list of available sessions
* completing order / getting a history of all user orders
* creating shopping cart, add a product to movie cart, getting a shopping cart by user
* finding a user by an e-mail
* logout system

# Structure of the project

Application has basic structure with adherence to all SOLID principles and N-tier architecture :
* The package `config` contains all configuration classes, in particular AppConfig, WebConfig and Security Config for for correct functioning of Spring Framework, and this package has class DataInitiliazer for injecting default user.
* The package `controller` has controllers of all entities to perform resourse methods and AuthenticationConmtroller for correct registration of users.
* The package `dao` has all services and implementations for accessing data from DB. In this application, all DAOs are based on ORM-framework Hibernate.
* The package `dto` has models of request and response DTOs. DTO - Data Transfer Object - objects whose purpose is to collect data to be returned to the client by the server and increase performance of this app.
* The package `exception` has custom DataProcessingException 
* The package `lib` contains two custom annotations for checking user data during authentication and two validators for them.
* The package `model` all Spring entities for correct functioning of an app.
* The package `service` is responsible for working with the DAO and does not allow working with the DB at the controller level and `mapper` package contains mapper for DTOs.
* The package `util` has `DateTimePatternUtil` for standardization of date pattern.
* The directory `resources` has a `db.properties` file, that should be used to properly structure the database.

# Used technologies
* ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
* ![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
* ![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=Hibernate&logoColor=white)
*	![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)

# Required software versions
* Java SE Development Kit 17.0.6
* git 2.40.0
* Apache Maven 3.9.1
* MySQL 8.0.32
* Apache Tomcat 9.0.73

# Installation
1. IntelliJ IDEA <sub> [download link](https://www.jetbrains.com/idea/download/#section=windows) </sub>, JDK<sub> [download link](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html) </sub> should be installed on your PC

2. Install GIT <sub> [download link](https://git-scm.com/downloads) </sub> and setup it <sub> [setup instruction](https://githowto.com/setup)

3. Install Apache Maven <sub> [download link](https://maven.apache.org/install.html) </sub> and add `PATH` variables <sub> [adding variables instruction](https://stackoverflow.com/questions/45119595/how-to-add-maven-to-the-path-variable) </sub>

4. Install MySQL <sub> [download link](https://dev.mysql.com/downloads/installer/) </sub> and setup it <sub> [video guide](https://www.youtube.com/watch?v=6MvJsqloIco) </sub>

5. Setup your SSH key <sub> [GIThub guide](https://docs.github.com/ru/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) </sub>

6. Now you need to fork project to your repo, you can do it by clicking ![image](https://user-images.githubusercontent.com/118058456/227191760-e5238095-4b06-4076-ba0e-464717de2fcb.png)

7. Go to IntelliJ IDEA and create new project from Version Control  ![image](https://user-images.githubusercontent.com/118058456/227191922-30c60041-3181-470b-9ca9-e53e4aef7eaf.png)

8. From your recently made repository click Code button, choose SSH and paste the link into IntelliJ IDEA ![image](https://user-images.githubusercontent.com/118058456/227192265-c8d209e6-1ad6-4ac0-8827-1649eabd7c2a.png)

9. Now you need to go to `src/main/resources/db.properties` and insert your params for connection to DB, there you'll see such fields 


![image](https://github.com/YevheniiKilovyi/cinema-app/assets/118058456/f04a79a6-052e-404f-8f26-5c69725ccefb)



* Into `db.driver` field you need to insert driver `MySQL.com.mysql.cj.jdbc.Driver`
* Into `db.url` field you need to insert url for connection to your database, it will be presented as `jdbc:mysql://localhost:3306/<your_db_name>`
* Into `db.user` field you need to insert `root`, or you username that you have choosen while have been setting up MySQL.
* Into `db.password` field you need to insert password that you have choosen while have been setting up MySQL.

10. Install Apache Tomcat <sub> [download link](https://tomcat.apache.org/download-90.cgi) </sub>, add configuration for your project here ![image](https://user-images.githubusercontent.com/118058456/227192947-02e1e248-78d0-4085-a748-1ca2804f2409.png)

11. Run the project and check the result ! :see_no_evil:
