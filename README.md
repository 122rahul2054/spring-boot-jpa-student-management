# Spring Boot JPA Student Management System

A REST API project built using Java, Spring Boot, Spring Data JPA, Hibernate, and PostgreSQL to manage student records and practice backend development.

## 🚀 Technologies Used

- **Java 23**
- **Spring Boot 3.5.6**
- **Spring Data JPA**
- **Hibernate ORM**
- **PostgreSQL**
- **Maven**
- **Lombok**
- **Spring Web**

## ✨ Features

- Create and save student records.
- Automatically generate student IDs.
- Map Java entities to database tables using JPA.
- Persist student data in PostgreSQL.
- Expose REST endpoints using Spring Boot.
- Reduce boilerplate code using Lombok annotations.

## 📂 Project Structure

```text
SpringJpaProject1/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── qspider/
│   │   │           ├── entity/
│   │   │           │   └── Student.java
│   │   │           ├── repository/
│   │   │           │   └── StudentRepository.java
│   │   │           ├── controller/
│   │   │           │   └── StudentController.java
│   │   │           └── SpringDataJpaDemoApplication.java
│   │   └── resources/
│   │       └── application.properties
│   └── test/
├── .gitignore
├── pom.xml
└── README.md
```

*Note: The package and file names above illustrate a typical structure. Adjust them to match your actual project.*

## 👨‍🎓 Student Entity

The `Student` entity represents a student record in the database.

| Field | Data Type | Description |
|---|---|---|
| `id` | `Long` | Automatically generated student ID |
| `name` | `String` | Student's name |
| `email` | `String` | Student's email address |
| `age` | `int` | Student's age |

The entity uses JPA annotations such as `@Entity`, `@Id`, and `@GeneratedValue`, along with Lombok annotations such as `@Getter`, `@Setter`, and `@NoArgsConstructor`.

## 🔗 Sample API Request

### Create Student

- **Method:** `POST`
- **Endpoint:** `/api/students`
- **Content-Type:** `application/json`

**Request Body**

```json
{
  "name": "Rahul Singh",
  "email": "rahul@gmail.com",
  "age": 22
}
```

**Example Response**

```json
{
  "id": 1,
  "name": "Rahul Singh",
  "email": "rahul@gmail.com",
  "age": 22
