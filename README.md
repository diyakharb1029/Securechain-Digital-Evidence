SecureChain – Digital Evidence Integrity & Chain-of-Custody System
SecureChain is a Java-based digital evidence preservation system developed during an IBM Internship, designed to ensure the integrity, authenticity, and verifiability of digital evidence using cryptographic hashing techniques.
The system simulates real-world chain-of-custody workflows commonly used in cybersecurity, digital forensics, and legal investigations, enabling tamper detection and secure evidence validation.

Key Objectives
- Preserve integrity of digital evidence
- Detect tampering using cryptographic hashes
- Simulate forensic chain-of-custody workflows
- Provide secure access through authentication

System Overview
SecureChain allows authenticated users to upload digital evidence files. Each file is processed using the SHA-256 hashing algorithm, and its hash is stored as a permanent integrity record. When a file is re-uploaded, the system verifies whether the evidence remains unchanged.

Technology Stack
- Backend: Java Servlets, java.security.MessageDigest
- Frontend: JSP, HTML, CSS, JavaScript
- Database: MySQL
- Server: Apache Tomcat
- Database Connectivity: JDBC (MySQL Connector/J)


Core Features
1. Secure Authentication
- User registration and login
- Passwords securely stored using SHA-256 hashing
  
2. Evidence Upload
- Authenticated users can upload digital evidence
- Files are stored securely on the server
- SHA-256 hash generated using HashUtil.java
- Hash records stored for future verification

3. Evidence Verification
- Re-upload an evidence file to validate integrity
- Verification results:
  VERIFIED – File remains unchanged
  TAMPERED – Hash mismatch detected
  NOT FOUND – No existing hash record

System Architecture
- Authentication Layer
- Secure File Upload Module
- SHA-256 Hashing Engine
- Integrity Verification Module
- MySQL-backed Metadata Storage

How to Run the Project
1. Database Setup
- Ensure MySQL server is running
- Create a database named securechaindb
- Import securechaindb.sql to create required tables
  
2. Server Setup
- Deploy the project on Apache Tomcat
- Add MySQL Connector/J (.jar) to apache-tomcat/lib/

3. Configuration
- Update database credentials in:
- src/main/java/com/securechain/util/DBConnection.java

4. Run the Application
- Start Tomcat server
- Access the application at:
- http://localhost:8080/Secure_Chain/

Future Enhancements
- Blockchain-based immutable hash ledger
- Role-Based Access Control (RBAC)
- Timestamped evidence logging
- Audit trail visualization


Author- Diya Kharb
Developed during IBM Internship with focus on security architecture, cryptographic hashing, and backend implementation.

Disclaimer
This project is intended for educational and academic purposes and demonstrates secure digital evidence handling concepts.
