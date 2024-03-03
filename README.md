# Library-Management-table-sql

CREATE TABLE Authors (
    AuthorID INT PRIMARY KEY,
    AuthorName VARCHAR(100)
);
INSERT INTO Authors (AuthorID,AuthorName)
VALUES (1001, 'James Joyce' ),
       (1002, 'Sir Thomas Moor' ),
       (1003, 'T.S Eliot'),
       (1004, 'H.G Wells' );

CREATE TABLE Books (
    BookID INT PRIMARY KEY,
    Title VARCHAR(100),
    AuthorID INT,
    Genre VARCHAR(100),
    ISBN VARCHAR(100),
    AvailableCopies INT,
    FOREIGN KEY (AuthorID) REFERENCES Authors(AuthorID)
);

INSERT INTO Books(BookID, Title, AuthorID, Genre,ISBN,AvailableCopies)
VALUES (232, 'Ulysses', 1001, 'Fiction','9-234-32-345',21),
       (233, 'Utopia',1002 , 'Memoir','9-234-33-345',56),
       (234, 'Waste Land',1003 , 'Mystery','9-234-34-345',43),
       (235, 'Time Machine',1004 , 'Biography','9-234-35-345',56);

CREATE TABLE Borrowers (
    StudentUID VARCHAR(100),
    StudentName VARCHAR(100),
    Email VARCHAR(255),
    PhoneNumber VARCHAR(20)
);

INSERT INTO Borrowers(StudentUID, StudentName, Email, PhoneNumber)
VALUES ('22BCA10318', 'Aryan','22BCA10318@cuchd.in', '9874563210'),
       ('22BCA10317', 'Akash','22BCA10317@cuchd.in','0321456987'),
       ('22BCA10192', 'Anish','22BCA10192@cuchd.in','7412589630'),
       ('22BCA00001', 'Badshah','22BCA00001@cuchd.in','9632587410');
