# Security Policy

## Supported Versions

We release patches for security vulnerabilities. Currently supported versions:

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |

## Reporting a Vulnerability

We take the security of our real-time chat application seriously. If you discover a security vulnerability, please follow these steps:

### How to Report

**DO NOT** open a public issue for security vulnerabilities.

Instead, please report security vulnerabilities by emailing:
- **Email**: [agarwalhimanshu136.com]
- **Subject**: Security Vulnerability in real-time-chat-app

### What to Include

Please provide as much information as possible:
- Type of vulnerability (e.g., XSS, SQL injection, authentication bypass)
- Full paths of affected source files
- Location of the affected source code (tag/branch/commit or direct URL)
- Step-by-step instructions to reproduce the issue
- Proof-of-concept or exploit code (if possible)
- Impact of the vulnerability

### Response Timeline

- **Initial Response**: Within 48 hours
- **Status Update**: Within 7 days
- **Fix & Disclosure**: Coordinated disclosure after patch is released

### Security Best Practices

When deploying this application:
1. Always use environment variables for secrets (never commit `.env` files)
2. Enable HTTPS in production
3. Keep dependencies up to date (`npm audit` regularly)
4. Use strong JWT secrets (minimum 32 characters)
5. Implement rate limiting on authentication endpoints
6. Regularly rotate AWS credentials and database passwords
7. Use parameterized queries to prevent SQL injection
8. Sanitize all user inputs
9. Enable CORS only for trusted origins
10. Use secure WebSocket connections (wss://)

### Hall of Fame

We appreciate security researchers who help improve our security. Contributors will be acknowledged here (with permission).

---

Thank you for helping keep this project secure!
