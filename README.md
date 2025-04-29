A real-time Banking Application built with Java, Spring Boot, Spring Data JPA (Hibernate), and MySQL.
This project provides RESTful APIs for core banking operations like account creation, balance deposit, withdrawal, fetching account details, and deleting accounts.

🚀 Tech Stack -->
Java 17,
Spring Boot,
Spring Data JPA (Hibernate),
MySQL Database,
Maven

📚 Features --> 
Create a new bank account
Get account details by ID
View all existing accounts
Deposit money into an account
Withdraw money from an account (with balance validation)
Delete an account

📂 Project Structure
src/main/java/net/java/banking

src ── controller        # REST Controllers,
src ── dto               # Data Transfer Objects,
src ── entity            # Database Entities,
src ── mapper            # DTO-Entity Mapping,
src ── repository        # Spring Data JPA Repositories,
src ── service           # Service Layer Interfaces,
src ── service/impl      # Service Layer Implementations,
src ── BankingAppApplication.java  # Main Application Runner


🛠 How to Run

Clone the repository
git clone https://github.com/saqibnihal07/banking-app.git
cd banking-app
Configure the Database
Set up a MySQL database named banking_app (or update the application.properties file accordingly).

Update application.properties
spring.datasource.url=jdbc:mysql://localhost:3306/banking_app
spring.datasource.username=your_mysql_username
spring.datasource.password=your_mysql_password
spring.jpa.hibernate.ddl-auto=update

Build the project
mvn clean install
Run the application

mvn spring-boot:run
Access the APIs
The application will be available at:
http://localhost:8080/api/accounts

🧩 API Endpoints
Method	Endpoint	Description
POST	/api/accounts	Create a new account
GET	/api/accounts/{id}	Get account details by ID
GET	/api/accounts	Get all accounts
POST	/api/accounts/{id}/deposit	Deposit money into an account
PUT	/api/accounts/{id}/withdraw	Withdraw money from an account
DELETE	/api/accounts/{id}	Delete an account
