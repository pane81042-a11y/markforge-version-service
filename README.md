# MarkForge Version Service

## Overview

The MarkForge Version Service is a serverless backend microservice responsible for managing document revision history within the MarkForge platform.

It enables version tracking, historical comparisons, and rollback functionality while enforcing secure access through Amazon Cognito JWT authorization.

This service operates fully within the AWS Always Free Tier.

---

## Architecture

- AWS Lambda (Version management logic)
- Amazon API Gateway (REST API endpoints)
- Amazon DynamoDB (Version history storage)
- Amazon Cognito (Authentication and JWT validation)
- IAM roles with least privilege access

---

## Responsibilities

- Store document revisions
- Retrieve document version history
- Support rollback to previous versions
- Track change metadata and timestamps
- Enforce document ownership validation

---

## Security

- Cognito User Pool integration
- JWT-based authorization via API Gateway
- User identity extraction from token claims
- User-scoped revision access control
- IAM least privilege permissions

---

## Deployment Model

Deployed independently within a distributed serverless microservices architecture.

All API requests must include a valid Cognito access token in the Authorization header.

---

## Tech Stack

- Node.js
- AWS Lambda
- DynamoDB
- API Gateway
- Amazon Cognito

---

## Status

Initial versioning service scaffolding and architecture setup.
