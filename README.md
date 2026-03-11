# Database Library System

SQL-based database system designed to manage users, tables, and sessions in a library kiosk.

## Project Description

This project is a relational database system developed using Oracle SQL to manage a library study area table system.  
The database tracks users, user types, table locations, and seating sessions.  

Users can sit at a table for a limited time, and the system automatically updates table status through triggers and procedures.

## Features

- Management of different user types (student, staff, guest)  
- Tracking library tables and their locations  
- Automatic table status updates using triggers  
- Seating procedure for assigning users to tables  
- Session tracking with start and end times  
- Automatic table release after a specified duration  

## Database Structure

Main tables:

- **KULLANICI_TIPLERI:** Stores different types of users  
- **KULLANICILAR:** Stores user information  
- **KONUMLAR:** Stores library floor or location information  
- **MASALAR:** Stores table information and current status  
- **FIS_KAYITLARI:** Stores table usage sessions  

## Automation

- **Triggers:** Automatically updates table status when a session is created and clears table info when the session expires  
- **Procedure (`OTURT_KULLANICI`):** Assigns a user to a table and ensures no active session exists for the user  

## Technologies Used

- Oracle SQL  
- PL/SQL  
- Relational Database Design  

## Sample Data

- Multiple user types  
- 100+ tables across different floors  
- Sample users and table session records for testing  

## Purpose of the Project

Demonstrates database design, relational modeling, and automation using SQL and PL/SQL.

## Author

Database project developed as part of a university coursework.
