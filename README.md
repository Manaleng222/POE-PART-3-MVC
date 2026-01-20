# mecca17  
## Lecturer Claims Management System

## Project Description

The **Lecturer Claims Management System** is an ASP.NET Core MVC web application designed to manage lecturer claims efficiently.  
Lecturers can submit claims for hours worked, while program coordinators and managers can review, approve, or reject those claims.

The system supports document uploads, claim status tracking, and feedback management using a SQL Server database.

---

## Features

### Lecturer Features
- Submit claims for hours worked
- Upload supporting documents (PDFs, images, etc.)
- View claim status (Pending, Approved, Rejected)

### Coordinator / Manager Features
- View all submitted claims
- Approve or reject claims with feedback
- Update claim status in real time

---

## Database

The system uses a **LecturerClaims** table to store claim information, documents, and statuses.

### Table Schema: `LecturerClaims`

```sql
CREATE TABLE LecturerClaims (
    id INT NOT NULL IDENTITY(1,1),
    username VARCHAR(200),
    email VARCHAR(255) NULL,
    module VARCHAR(200),
    rate VARCHAR(200),
    hours_worked VARCHAR(200),
    description VARCHAR(500),
    total VARCHAR(200),
    filename VARCHAR(200),
    filepath VARCHAR(500),
    status VARCHAR(200)
);

SELECT * FROM LecturerClaims;


## Technologies Used

- **Framework:** ASP.NET Core MVC  
- **Language:** C#  
- **Database:** SQL Server  
- **Frontend:** Razor Pages, HTML, CSS, Bootstrap  
- **File Storage:** Local storage for uploaded documents

---

## Configuration

### Database Connection

Update the connection string in `appsettings.json`:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=YOUR_SERVER_NAME;Database=mecca17;Trusted_Connection=True;TrustServerCertificate=True;"
}


