# Task Manager API

A production-style backend API for managing **workspaces, projects, and tasks**.  
This project is designed to demonstrate **real-world NestJS backend architecture**, clean module boundaries, and modern database integration using **Prisma v7**.

This is **not** a tutorial or starter project.

---

## Why This Project Exists

The goal of this project is to showcase:

- Clean, scalable **NestJS modular architecture**
- Proper separation of concerns (controllers vs services)
- Database integration using **Prisma v7** with MySQL
- Production-ready configuration and structure
- Engineering decisions suitable for real teams

The focus is on **backend engineering quality**, not UI or frontend development.

---

## Tech Stack

- **NestJS** (TypeScript)
- **MySQL**
- **Prisma ORM (v7)** — custom generated client
- **JWT Authentication** (planned)
- **Docker** (planned)
- **Jest** (planned)

---

### Why Prisma v7?

This project uses **Prisma v7** following the **official Prisma v7 configuration model**:

- Database connection configuration is handled via `prisma.config.ts`
- Prisma Client is generated explicitly (not legacy `@prisma/client`)
- Aligns with Prisma’s latest architectural changes

This avoids legacy patterns and reflects current best practices.

---

## Architecture Overview

High-level modules:

- **PrismaModule** — database access layer
- **AuthModule** — authentication & authorization *(planned)*
- **UsersModule** — user management *(planned)*
- **WorkspaceModule** — multi-tenant workspace support *(planned)*
- **ProjectModule** — project management *(planned)*
- **TaskModule** — task lifecycle management *(planned)*

### Design Principles

- Controllers are thin and handle HTTP concerns only
- Business logic lives in services
- Infrastructure (database, config) is isolated
- Modules have clear ownership and boundaries

---

## Getting Started

### Requirements

- Node.js **>= 18**
- MySQL running locally
- npm

---

### Environment Variables

Create a `.env` file in the project root:

```env
DATABASE_URL="mysql://user:password@localhost:3306/task_manager"


## Install & Run

```bash
npm install
npx prisma migrate dev
npm run start:dev

