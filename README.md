# Postman Authentication Automation

## Project Overview

This project demonstrates API authentication testing and automation using Postman, Newman, and JavaScript test scripts.

It covers positive and negative authentication scenarios using public demo APIs.

## Tools & Technologies

- Postman
- JavaScript (Postman Tests)
- REST API
- Newman
- Git & GitHub
- GitHub Actions (planned)

## Authentication Scenarios

| No. | Scenario | Expected Result |
|---|---|---|
| 01 | API Key Authentication | 200 OK |
| 02 | Basic Authentication – Valid Credentials | 200 OK |
| 03 | Basic Authentication – Invalid Credentials | 401 Unauthorized |
| 04 | Bearer Token Login | 200 OK |
| 05 | Access Protected API using Bearer Token | 200 OK |
| 06 | Access Protected API without Authentication | 401 Unauthorized |

## Automation Features

- HTTP status code validation
- Authentication response validation
- Response body assertions
- Automatic access-token extraction
- Environment variable management
- Bearer token reuse across requests
- Positive and negative authentication testing
- Cookie management for unauthenticated testing

## Project Structure

```text
Postman_Authentication_Automation/
├── collections/
│   └── Postman Authentication Automation.postman_collection.json
├── .gitignore
└── README.md
```

## Security Practices

- Credentials are managed using Postman environment variables.
- Environment files are excluded from Git.
- Access tokens are generated dynamically during login.
- Sensitive credentials are not committed to the repository.

## Test Execution

The collection can be executed using Postman or Newman.

Newman execution instructions will be added after CLI configuration.

## Purpose

To demonstrate practical API authentication testing, JavaScript-based assertions, token management, and API automation skills for Software QA Engineering.