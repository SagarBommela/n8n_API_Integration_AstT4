
# N8N API Integration – Topic 4: API Authentication and Security

## 1. Project Overview

**Project Name:** N8N API Authentication Workflow

**Course:** N8N Hands-On API Integration

**Topic:** Topic 4 – API Authentication and Security

**Platform:** n8n

## 2. Objective

The objective of this project is to understand different API authentication methods and how to securely connect APIs using n8n.

This project demonstrates:

- Basic Authentication using username and password.
- Header Authentication using Bearer Tokens.
- OAuth 2.0 authentication using GitHub.
- Understanding and decoding JSON Web Tokens (JWT).

## 3. Workflow Structure

The workflow contains the following nodes:

### 1. Manual Trigger
Starts the workflow manually.

### 2. Basic Auth Request
- Uses Basic Authentication.
- Connects to the Postman Echo API.
- Verifies username and password.
- Checks the authenticated response.

### 3. Header Auth Request
- Uses Header Authentication.
- Sends a Bearer Token through the Authorization header.
- Verifies the received request headers.

### 4. GitHub OAuth Request
- Uses GitHub OAuth 2.0 credentials.
- Connects to the GitHub REST API.
- Retrieves authenticated user information.

## 4. Authentication Methods

### Basic Authentication

Username: postman

Password: password

API:
https://postman-echo.com/basic-auth

Expected result:

```json
{
  "authenticated": true,
  "user": "postman"
}
```

### Header Authentication

Authorization Header:

```text
Bearer my_secret_token_9988
```

API:
https://postman-echo.com/headers

Expected result: The API returns the Authorization header received.

### OAuth 2.0 Authentication

Provider: GitHub

API:
https://api.github.com/user

OAuth configuration includes:

- Client ID
- Client Secret
- Redirect URL
- Authorization Code
- Access Token

Expected result: GitHub returns authenticated user information.

**Note:** Client secrets and access tokens are stored securely in n8n credentials and are not included in this repository.

## 5. JSON Web Token (JWT)

JWT contains three sections:

1. Header
2. Payload
3. Signature

Example decoded Header:

```json
{
  "alg": "HS256",
  "typ": "JWT"
}
```

Example decoded Payload:

```json
{
  "sub": "1234567890",
  "name": "John Doe",
  "admin": true
}
```

Tool used:
https://jwt.io/


Git URL:
https://github.com/SagarBommela/n8n_API_Integration_AstT4

Loom Video:

https://www.loom.com/share/5a644b45722e443e888e7c9540fa4853
