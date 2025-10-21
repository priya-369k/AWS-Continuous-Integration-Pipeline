# AWS-Continuous-Integration-Pipeline
Serverless CI/CD pipeline using AWS CodePipeline, CodeBuild, CodeArtifact, SonarCloud, and SNS

## 🎯 Overview

This project implements a **fully automated Continuous Integration pipeline** using AWS managed services, eliminating the operational overhead of maintaining traditional CI tools like Jenkins, Nexus, and SonarQube servers. The pipeline automatically builds, tests, analyzes code quality, and stores artifacts for every code commit.

### Problem Statement

Traditional CI/CD setups face several challenges:
- Manual build and release processes are time-consuming
- Server management overhead (Jenkins, Nexus, SonarQube)
- Delayed bug detection due to infrequent testing
- Inter-team dependencies causing bottlenecks

### Solution

Cloud-based CI pipeline that:
- ✅ Triggers automatically on every commit
- ✅ Performs static code analysis with quality gates
- ✅ Builds and stores artifacts in S3
- ✅ Sends real-time notifications
- ✅ Requires zero server maintenance

## 🏗️ Architecture


## 🛠️ Technologies Used

| Category | Technology | Purpose |
|----------|-----------|---------|
| **Source Control** | Bitbucket | Git repository hosting |
| **Build Service** | AWS CodeBuild | Managed build and test execution |
| **Orchestration** | AWS CodePipeline | CI/CD workflow automation |
| **Artifact Repository** | AWS CodeArtifact | Maven dependency management |
| **Code Quality** | SonarCloud | Static code analysis and quality gates |
| **Storage** | AWS S3 | Build artifact storage |
| **Notifications** | AWS SNS | Email notifications |
| **Secrets Management** | AWS Systems Manager Parameter Store | Secure credential storage |
| **Build Tool** | Maven | Java project build automation |
| **Runtime** | Amazon Corretto 11 | Java runtime environment |

## ✨ Features

- **Automated CI Pipeline**: Triggers on every commit to main branch
- **Code Quality Analysis**: SonarCloud integration with customizable quality gates
- **Secure Dependency Management**: Private Maven repository using AWS CodeArtifact
- **Artifact Versioning**: Timestamped artifacts stored in S3 with lifecycle policies
- **Real-time Notifications**: Email alerts for build success/failure via SNS
- **Zero Server Maintenance**: Fully serverless architecture
- **Infrastructure as Code**: Buildspec files for reproducible builds
- **Security Best Practices**: Credentials stored in Parameter Store with encryption

## 📦 Prerequisites

Before setting up this project, ensure you have:

- **AWS Account** with appropriate IAM permissions
- **Bitbucket Account** for source code hosting
- **SonarCloud Account** for code quality analysis
- **AWS CLI** installed and configured (`aws --version`)
- **Git** installed (`git --version`)
- **Maven** installed locally for testing (`mvn --version`)
- **Java 11** or higher (`java -version`)

### Required AWS IAM Permissions

Your IAM user/role needs permissions for:
- CodePipeline (create, update, execute)
- CodeBuild (create projects, start builds)
- CodeArtifact (create repositories, manage packages)
- S3 (create buckets, upload objects)
- SNS (create topics, publish messages)
- Systems Manager Parameter Store (put/get parameters)
- IAM (create service roles)
