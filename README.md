# 🚀 Team 22 — CSCI361 Project Guidelines

Welcome to the central repository for **Team 22**. This document serves as the master guide for our development workflow, branching strategies, and project management setup across all our codebases.

---

## 🛠️ Repository Overview

Our system is divided into three core components:
* **`backend`**: Core API and database services.
* **`web-frontend`**: Web application client.
* **`mobile-app`**: Cross-platform mobile client.

> **Note:** For specific local environment setup, dependencies, and execution commands, refer directly to the `README.md` file inside each respective repository.

---

## 📋 Project Management Workflow

We track all progress using our **CSCI361 Master Board**. 

### Board Columns
1. **Todo**: Tasks ready to be picked up.
2. **In Progress**: Tasks actively being worked on.
3. **In Review**: Pull Requests waiting for code review.
4. **Done**: Fully merged and completed features.

### Moving Tasks
* **Todo ➔ In Progress**: Drag your assigned task manually when you start working on it.
* **In Progress ➔ In Review**: Automatically triggers when you push a feature branch and open a Pull Request (PR).
* **In Review ➔ Done**: Automatically triggers when your PR is approved and merged into `main`.

---

## 🌿 Git Branching Strategy

We follow a simple feature-branch workflow. **Direct pushes to `main` are strictly prohibited.**

### Branch Naming Convention
Create feature branches off `main` using the following naming structure:
* `feature/short-description` (e.g., `feature/user-login`, `feature/database-schema`)
* `bugfix/short-description` (e.g., `bugfix/fix-auth-header`)

### Developer Terminal Steps

1. **Sync `main` and create a branch:**
   ```bash
   git checkout main
   git pull origin main
   git checkout -b feature/your-feature-name
