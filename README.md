# Database Library System

Kiosk-based library table management system using Oracle SQL.  
This project is a comprehensive database management system designed to digitize and optimize study table reservations in a library environment. It focuses on fair usage, real-time tracking, and automated session management through Oracle Live SQL.

## Features

- **Multi-Category User Management:** Support for students, staff, and guests.  
- **Real-Time Occupancy Control:** Automated table status updates ('Empty' or 'Occupied') using database triggers.  
- **Automated Session Management:** Implements a strict 90-minute session limit to ensure fair access for all users.  
- **Integrity Constraints:** Prevents multiple active reservations for a single user and blocks attempts to sit at already occupied tables.  

## Database Structure

Designed following 3rd Normal Form (3NF) principles to ensure data integrity and eliminate redundancy.

- **KULLANICI_TIPLERI:** Defines user categories such as student, personnel, and guest.  
- **KULLANICILAR:** Stores personal data and linked category IDs.  
- **KONUMLAR:** Manages physical locations and floor information.  
- **MASALAR:** Tracks real-time status, location, and the current occupant of each table.  
- **FIS_KAYITLARI:** Central logging system for all reservation activities, timestamps, and active session status.  

## Technologies and Tools

- **Engine:** Oracle Live SQL  
- **Language:** SQL and PL/SQL (Procedures, Triggers, Loops)  
- **Modeling:** ER/ERD Diagrams designed via excalidraw.com  

## Contributors and Responsibilities

- **Nisanur GÖREN:** Database design, table release trigger (`trg_masa_bosalt`), seating procedure (`OTURT_KULLANICI`), location management  
- **Zeynep Işıl PELİT:** User entity management, ER/ERD diagram design, initial test data implementation  
- **Elif Nur AYDIN:** Table entity management, normalization control, automated table generation scripts  
- **Beyza AYAN:** Receipt records management, status update trigger (`trg_fis_kayit_ekle`), ER/ERD design contribution  

## Files in this Repository

- **database.sql:** Full schema creation, triggers, procedures, and test data  
- **project_report.pdf:** Detailed documentation of system logic, ER diagrams, and normalization analysis  
