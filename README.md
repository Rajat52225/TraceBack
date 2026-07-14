# TraceBack

**TraceBack** is a full-stack cloud-native Lost & Found platform designed to simplify the process of reporting, finding, claiming, and returning lost items.

The idea for TraceBack came from a problem observed in college. When a student loses an item or finds someone else's item, they usually contact the Dean or a faculty member, who then sends an email to students regarding the item.

This process can be slow, dependent on faculty involvement, and difficult to track.

TraceBack provides a centralized platform where users can directly post Lost or Found items, upload images, browse Active and Resolved items, submit ownership claims with proof, and manage the complete claim verification process.

## Live Application

The application is publicly deployed and accessible at:

https://traceback-frontend-wine.vercel.app

> **Note:** The backend is hosted on Render's free tier, so the first request after a period of inactivity may take some time while the service starts.

## Source Code

The application is divided into separate frontend and backend repositories.

### Backend Repository

The backend contains the REST APIs, authentication and authorization, business logic, database integration, cloud storage integration, Docker Compose configuration, and Kubernetes manifests.

**Repository:**

https://github.com/Rajat52225/traceback-backend

### Frontend Repository

The frontend contains the React user interface, API integration, authenticated requests, Docker configuration, Nginx configuration, and Vercel deployment configuration.

**Repository:**

https://github.com/Rajat52225/traceback-frontend

## Tech Stack

### Frontend

- React
- Vite
- JavaScript
- CSS

### Backend

- Java 17
- Spring Boot
- Spring Security
- JWT Authentication
- BCrypt Password Hashing
- Maven

### Database and Cloud Storage

- MongoDB
- MongoDB Atlas
- AWS S3

### DevOps and Deployment

- Git and GitHub
- Docker
- Docker Compose
- Kubernetes
- Render
- Vercel

## Main Features

- User Registration and Login
- JWT-Based Authentication and Authorization
- BCrypt Password Hashing
- Post Lost and Found Items
- Upload Item Images
- Browse Active and Resolved Items
- Submit Ownership Claims
- Upload Proof Images
- Accept or Reject Claims
- Automatically Mark Items as Resolved After Claim Acceptance
- AWS S3 Image Storage
- MongoDB Atlas Cloud Database
- Docker Containerization
- Docker Compose Multi-Container Setup
- Local Kubernetes Deployment
- Public Cloud Deployment

## Application Workflow

```text
User Registration / Login
           |
           v
    JWT Authentication
           |
           v
  Post Lost / Found Item
           |
           v
  Upload Images to AWS S3
           |
           v
     Browse Items
           |
           v
 Submit Ownership Claim
           |
           v
    Upload Proof Images
           |
           v
    Owner Reviews Claim
           |
           v
      Accept / Reject
           |
           v
 Item Marked as Resolved
```

## Production Architecture

```text
                         User
                           |
                           v
                  React Frontend
                       Vercel
                           |
                           v
                       REST API
                           |
                           v
                 Spring Boot Backend
                        Render
                       /      \
                      v        v
             MongoDB Atlas    AWS S3
             Application      Image
                 Data         Storage
```

## Containerization and Kubernetes

The frontend and backend applications were containerized using Docker.

Docker Compose was used to run the frontend, backend, and MongoDB together as a multi-container application.

The complete containerized application was also deployed locally using Docker Desktop Kubernetes.

The Kubernetes configuration includes:

- Frontend Deployment and Service
- Backend Deployment and Service
- MongoDB Deployment and Service
- PersistentVolumeClaim for MongoDB storage
- Kubernetes Secrets for application credentials

## Production Deployment

| Component | Platform |
|---|---|
| Frontend | Vercel |
| Backend | Render |
| Database | MongoDB Atlas |
| Image Storage | AWS S3 |

## Application Screenshots

### TraceBack Application

![TraceBack Screenshot 1](Screenshot%20(427).png)

![TraceBack Screenshot 2](Screenshot%20(428).png)

![TraceBack Screenshot 3](Screenshot%20(429).png)

![TraceBack Screenshot 4](Screenshot%20(430).png)

## Project Presentation

The complete TraceBack project presentation is available in this repository.

**Presentation File:**

[Download / View TraceBack Presentation](traceback_corrected.pptx)

## Challenges and Learning

During the development of TraceBack, I gained practical experience in:

- Implementing JWT authentication using Spring Security
- Integrating AWS S3 for cloud-based image storage
- Connecting Spring Boot with MongoDB Atlas
- Developing and consuming REST APIs
- Connecting separately deployed frontend and backend applications
- Configuring CORS for local and production environments
- Containerizing applications using Docker
- Running multiple services using Docker Compose
- Deploying containerized services locally using Kubernetes
- Deploying a full-stack application to public cloud platforms

## Future Scope

- Enhance application security with Two-Factor Authentication (2FA)
- Add User Profiles
- Develop personalized User Dashboards
- Add an In-App Chat System for communication between users
- Improve the UI and overall user experience
- Make further improvements based on user feedback and real-world usage

## Author

**Rajat Sharma**

B.Tech Computer Science and Engineering
