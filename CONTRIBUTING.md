# Contributing to Real-Time Chat App

First off, thank you for considering contributing to this project! 

The following is a set of guidelines for contributing to this real-time chat application. These are mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Pull Requests](#pull-requests)
- [Development Setup](#development-setup)
- [Style Guidelines](#style-guidelines)
- [Commit Message Guidelines](#commit-message-guidelines)

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to [agarwalhimanshu136@gmail.com].

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates. When creating a bug report, include as many details as possible:

- **Use a clear and descriptive title**
- **Describe the exact steps to reproduce the problem**
- **Provide specific examples** (code snippets, screenshots)
- **Describe the behavior you observed and what you expected**
- **Include environment details** (OS, Node.js version, browser)

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion:

- **Use a clear and descriptive title**
- **Provide a detailed description of the suggested enhancement**
- **Explain why this enhancement would be useful**
- **Include mockups or examples if applicable**

### Pull Requests

1. **Fork the repository** and create your branch from `main`
2. **Follow the development setup** instructions below
3. **Make your changes** and ensure the code follows our style guidelines
4. **Test your changes** thoroughly
5. **Update documentation** if needed (README, comments)
6. **Write clear commit messages** following our guidelines
7. **Submit a pull request** with a comprehensive description

#### Pull Request Checklist

- [ ] Code follows the project's style guidelines
- [ ] Self-review of code completed
- [ ] Comments added for complex logic
- [ ] Documentation updated (if applicable)
- [ ] No new warnings or errors introduced
- [ ] Tests added/updated (if applicable)
- [ ] All tests pass locally
- [ ] Changes are backwards compatible (or documented)

## Development Setup

### Prerequisites

- Node.js (v18+ recommended)
- PostgreSQL database
- Redis instance
- AWS account (for S3 uploads)

### Backend Setup

```bash
cd chat-app-backend

# Install dependencies
npm install

# Copy environment template
cp .env.example .env

# Edit .env with your credentials
# DATABASE_URL, REDIS_URL, AWS credentials, JWT_SECRET, etc.

# Run Prisma migrations
npx prisma generate
npx prisma migrate dev

# Start development server
npm start
```

### Frontend Setup

```bash
cd chat-app-frontend

# Install dependencies
npm install

# Copy environment template (if exists)
cp .env.example .env

# Edit .env with backend API URL
# REACT_APP_API_URL=http://localhost:4000

# Start development server
npm start
```

### Running Tests

```bash
# Backend tests
cd chat-app-backend
npm test

# Frontend tests
cd chat-app-frontend
npm test
```

## Style Guidelines

### JavaScript Style

- Use **ES6+ features** (arrow functions, destructuring, async/await)
- Use **camelCase** for variables and functions
- Use **PascalCase** for React components and classes
- Add **JSDoc comments** for complex functions
- Keep functions **small and focused** (single responsibility)
- Use **meaningful variable names**

### Code Formatting

- **Indentation**: 2 spaces (no tabs)
- **Line length**: Max 100 characters
- **Semicolons**: Use them consistently
- **Quotes**: Single quotes for strings (unless template literals)
- **Trailing commas**: Use in multi-line objects/arrays

### React Guidelines

- Use **functional components** with hooks
- Keep components **small and reusable**
- Use **PropTypes** or TypeScript for type checking
- Extract **custom hooks** for reusable logic
- Follow **React best practices** (keys, state immutability)

### Git Workflow

1. Create a feature branch: `git checkout -b feature/my-new-feature`
2. Make your changes and commit: `git commit -m "feat: add new feature"`
3. Push to your fork: `git push origin feature/my-new-feature`
4. Open a pull request against `main`

## Commit Message Guidelines

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- **feat**: A new feature
- **fix**: A bug fix
- **docs**: Documentation only changes
- **style**: Code style changes (formatting, missing semicolons, etc.)
- **refactor**: Code change that neither fixes a bug nor adds a feature
- **perf**: Performance improvement
- **test**: Adding or updating tests
- **chore**: Changes to build process or auxiliary tools

### Examples

```
feat(auth): add JWT token refresh mechanism

Implements automatic token refresh when the access token expires.
Adds a new endpoint /api/auth/refresh and updates the middleware.

Closes #123
```

```
fix(chat): resolve message ordering issue

Messages were displaying out of order due to race condition.
Fixed by adding timestamp-based sorting in the reducer.
```

## Questions?

Feel free to open an issue with the `question` label, or reach out to the maintainers directly.

Thank you for contributing! 🚀
