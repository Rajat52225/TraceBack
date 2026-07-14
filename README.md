# TraceBack

TraceBack is a cloud-native Lost & Found platform designed to simplify the process of reporting, finding, and claiming lost items.

The idea for TraceBack came from a problem observed in college. When a student loses an item or finds someone else's item, they usually contact the Dean or a faculty member, who then sends an email to students regarding the item.

TraceBack provides a centralized platform where users can directly post Lost or Found items, upload images, browse Active and Resolved items, submit ownership claims with proof, and manage the complete claim verification process.

## Live Application

TraceBack is deployed and publicly accessible at:

https://traceback-frontend-wine.vercel.app

> The backend is hosted on Render's free tier, so the first request after a period of inactivity may take some time while the service starts.

## Source Code

TraceBack is divided into separate frontend and backend repositories.

### Backend Repository

The backend repository contains:

- Spring Boot REST APIs
- Spring Security
- JWT Authentication
- MongoDB integration
- AWS S3 integration
- Docker configuration
- Docker Compose configuration
- Kubernetes deployment manifests

Repository:

https://github.com/Rajat52225/traceback-backend

### Frontend Repository

The frontend repository contains:

- React frontend
- Vite
- JavaScript and CSS
- REST API integration
- JWT-based authenticated requests
- Docker configuration
- Nginx configuration
- Vercel deployment configuration

Repository:

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
- JWT-Based Authentication
- BCrypt Password Hashing
- Post Lost and Found Items
- Upload Item Images
- Browse Active and Resolved Items
- Submit Ownership Claims
- Upload Proof Images
- Accept or Reject Claims
- Automatically Resolve Items After Claim Acceptance
- AWS S3 Image Storage
- Cloud Database using MongoDB Atlas
- Docker Containerization
- Docker Compose Multi-Container Setup
- Local Kubernetes Deployment
- Public Cloud Deployment

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
