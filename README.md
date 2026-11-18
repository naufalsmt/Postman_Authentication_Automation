# Postman Authentication Automation

![Newman](https://img.shields.io/badge/Newman-6.2.3-orange?style=for-the-badge)
![Postman](https://img.shields.io/badge/Postman-API_Automation-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-CI%2FCD-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

[![Postman Authentication API Tests](https://github.com/naufalsmt/Postman_Authentication_Automation/actions/workflows/postman-auth-tests.yml/badge.svg)](https://github.com/naufalsmt/Postman_Authentication_Automation/actions/workflows/postman-auth-tests.yml)

## Project Overview

This project demonstrates API authentication testing and automation using Postman, JavaScript, Newman, and GitHub Actions.

It covers positive and negative authentication scenarios using public demo APIs, with automated test execution locally and through a CI/CD pipeline.

## Tools & Technologies

- Postman
- JavaScript (Postman Tests)
- REST API
- Newman CLI
- Git & GitHub
- GitHub Actions (CI/CD)

## Authentication Test Scenarios

| No. | Test Scenario | Expected Result |
|---|---|---|
| 01 | API Key Authentication | 200 OK |
| 02 | Basic Authentication – Valid Credentials | 200 OK |
| 03 | Basic Authentication – Invalid Credentials | 401 Unauthorized |
| 04 | Bearer Token Login | 200 OK |
| 05 | Access Protected API using Bearer Token | 200 OK |
| 06 | Access Protected API without Authentication | 401 Unauthorized |

## Automation Features

- HTTP status code validation
- Response body and JSON assertions
- Positive and negative authentication testing
- API key authentication header validation
- Basic Authentication credential validation
- Automatic access-token extraction after login
- Dynamic Bearer token reuse across requests
- Environment variable management
- Cookie management for unauthenticated testing
- Automated execution using Newman

## Project Structure

```text
Postman_API_Auth_Tests/
│
├── .github/
│   └── workflows/
│       └── postman-auth-tests.yml
│
├── collections/
│   └── Postman Authentication Automation.postman_collection.json
│
├── environments/
│   └── QA_Environment.postman_environment.json
│
├── .gitignore
└── README.md
```

Note: The environment JSON file is maintained locally and excluded from Git to protect credentials.

## Running Tests Locally

### Prerequisites

- Node.js
- Newman
- Exported Postman collection
- Local Postman environment file

### Install Newman

```bash
npm install -g newman
```

### Execute the Collection

```bash
newman run "collections/Postman Authentication Automation.postman_collection.json" -e "environments/QA_Environment.postman_environment.json"
```

Newman executes all six authentication scenarios and displays the test results in the terminal.

## CI/CD – GitHub Actions

The project integrates Newman with GitHub Actions for automated API test execution.

### Workflow Features

- Automatically triggers on pushes to the `main` branch.
- Executes on pull requests targeting `main`.
- Supports manual execution through GitHub Actions.
- Installs Newman in the GitHub Actions runner.
- Executes the Postman authentication collection.
- Reports test results and failures in the workflow logs.

### Credential Management

- GitHub Repository Secrets are used to provide credentials securely.
- Environment variables are passed to Newman during execution.
- Access tokens are generated dynamically during login.
- Local Postman environment files are excluded from Git.

## Security Practices

- Credentials are managed through Postman environment variables.
- Environment JSON files are excluded using `.gitignore`.
- GitHub Actions uses repository secrets for credentials.
- Access tokens are generated dynamically rather than hardcoded.

## Purpose

To demonstrate practical API authentication testing, JavaScript-based assertions, token management, command-line automation, version control, and CI/CD implementation for Software QA Engineering.

---

**Author:** Naufal Shamsudeen  
**GitHub:** https://github.com/naufalsmt
