# azure-pipeline-self-hosted-runner-deployment
Azure DevOps CI/CD Pipeline – Spring Boot (Self-Hosted Linux Agent)
1. Overview

This repository implements a two-stage Azure DevOps CI/CD pipeline for building and deploying a Spring Boot application using a self-hosted Linux agent.
The pipeline is triggered by changes to the main branch and deploys the application as an executable JAR to Azure App Service (Linux) running Java 17.

The design prioritizes:

Deterministic build environments

Full control over runtime tooling

Artifact-based deployment

Production-grade release flow

2. High-Level Architecture
CI/CD Flow

```text
Git Push (main)
     ↓
Azure DevOps Pipeline
     ↓
Self-Hosted Linux Agent
     ↓
Build Stage (Java 17, Maven)
     ↓
Pipeline Artifact (JAR)
     ↓
Deploy Stage
     ↓
Azure App Service (Linux, Java 17)
```

