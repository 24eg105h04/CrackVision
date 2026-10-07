# CrackVision

## Structural Crack Detection and Monitoring System

CrackVision is a web-based system designed to detect and monitor visible cracks in structures such as buildings, walls, bridges, columns, and beams. The system uses computer vision to analyze structural images, identify visible cracks, classify their severity, and maintain inspection history for monitoring changes over time.

## Problem Statement

Manual structural crack inspection can be time-consuming and may make it difficult to maintain consistent inspection records. CrackVision provides a digital platform where structural images can be uploaded, analyzed, reviewed by engineers, and tracked across multiple inspections.

## Main Objective

The main objective of CrackVision is to assist construction teams and engineers in identifying and monitoring visible structural cracks through image-based computer vision while maintaining organized inspection records and engineer reviews.

## Technology Stack

* **Frontend:** React + Vite
* **Backend:** Spring Boot
* **Database:** Aiven Cloud MySQL
* **API:** REST APIs
* **Authentication:** JWT
* **Authorization:** Role-Based Access Control
* **AI Service:** Python Computer Vision
* **Containerization:** Docker
* **Version Control:** Git + GitHub
* **Development Environment:** Google Antigravity

## Main Modules

1. User Authentication
2. Role-Based Access Control
3. User Management
4. Project Management
5. Building Management
6. Floor and Component Management
7. Structural Image Upload
8. Crack Detection
9. Crack Severity Classification
10. Crack Highlighting
11. Engineer Review
12. Inspection History
13. Crack Monitoring
14. Previous and Current Inspection Comparison
15. Inspection Reports
16. Project Dashboards

## User Roles

### Admin

* Manage users
* Assign roles
* Manage projects
* View system activity
* View all inspections and reports

### Site Worker

* View assigned projects
* Select building, floor, and component
* Upload structural images
* Submit inspections
* View inspection status

### Site Engineer

* Review uploaded inspections
* View original and analyzed images
* Review crack detection results
* Add comments
* Approve inspections
* Mark inspections for further inspection
* Mark cracks for monitoring
* Track crack history

### Project Manager

* View project dashboards
* Monitor inspections
* View crack statistics
* Track unresolved cracks
* View inspection history
* View reports

## Crack Severity Classes

The computer vision component uses the following project-defined visual categories:

* Normal
* Minor Crack
* Moderate Crack
* Severe Crack

These categories are intended for visual screening within the project and do not replace professional structural engineering assessment.

## Planned Workflow

1. User logs into CrackVision.
2. Site worker or engineer selects a project.
3. Building, floor, and structural component are selected.
4. A structural image is uploaded.
5. The computer vision service analyzes the image.
6. Visible cracks are detected and highlighted.
7. Crack severity and confidence are returned.
8. The analysis result is stored.
9. An engineer reviews the result.
10. The engineer adds comments and selects an appropriate review status.
11. Inspection history is maintained.
12. Future inspections can be compared with previous inspections.
13. Crack changes can be monitored over time.
14. Inspection reports can be generated.

## Planned Project Structure

```text
CrackVision/
│
├── frontend/
│   └── React + Vite application
│
├── backend/
│   └── Spring Boot REST API
│
├── ai-service/
│   └── Python Computer Vision service
│
├── docs/
│   └── Project documentation
│
└── README.md
```

## System Architecture

```text
                    CrackVision
                         │
          ┌──────────────┴──────────────┐
          │                             │
          ▼                             ▼
   React + Vite                    Spring Boot
    Frontend                         Backend
          │                             │
          └──────── REST + JWT ─────────┘
                                        │
                              ┌─────────┴─────────┐
                              │                   │
                              ▼                   ▼
                       Python AI Service     Aiven MySQL
                              │
                              ▼
                     Computer Vision Model
                              │
                    ┌─────────┼─────────┐
                    ▼         ▼         ▼
                 Detect    Highlight   Classify
                  Crack      Crack      Severity
                              │
                              ▼
                       Engineer Review
                              │
                              ▼
                       Crack Monitoring
                              │
                              ▼
                            Reports
```

## Future Deployment

The application is planned to be containerized using Docker and deployed to a cloud environment.

The final deployment architecture will contain:

* React frontend container
* Spring Boot backend container
* Python computer vision container
* Aiven Cloud MySQL database

## Project Status

**Current Stage:** Initial project setup

The project will be developed incrementally, with each major module tested before moving to the next stage.
