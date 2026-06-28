# Automating the Recruitment Process

![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)
![Redux](https://img.shields.io/badge/redux-%23593d88.svg?style=for-the-badge&logo=redux&logoColor=white)
![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Turborepo](https://img.shields.io/badge/Turborepo-%230F0813.svg?style=for-the-badge&logo=Turborepo&logoColor=white)

## Overview

Automating the Recruitment Process is a third-year university dissertation project built to explore how the University of Sheffield's recruitment workflows could be modernised. The prototype focuses on replacing heavily manual recruitment tasks with a web-based system for publishing roles, managing applicants, and supporting role-specific access for candidates, staff, and administrators.

The application is built as a Turborepo monorepo with a React/Vite frontend, an Express backend, and MongoDB for persistence. It includes public job browsing, authenticated user accounts, applicant profiles, job applications, staff dashboards for listing and application management, and administrator tooling for user role management.

Dissertation report: TODO - add hosted report link.

## Getting Started

### Dependencies and Prerequisites

- Node.js 18 or newer
- npm 10 or newer
- A MongoDB Atlas database using an SRV connection string
- JWT access and refresh token secrets

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/CitharaYote/uni-com3610-project.git
   cd uni-com3610-project/turborepo
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create local environment files from the examples:

   ```bash
   cp apps/backend/.env.example apps/backend/.env
   cp apps/web/.env.example apps/web/.env
   ```

4. Update `apps/backend/.env` with your MongoDB and JWT values:

   ```env
   MONGODB_USERNAME=username
   MONGODB_PASSWORD=password
   MONGODB_ENDPOINT=endpoint
   MONGODB_APPNAME=appname
   BACKEND_URL=http://localhost:3000
   BACKEND_PORT=3000
   ACCESS_TOKEN_SECRET=youraccesstokensecret
   REFRESH_TOKEN_SECRET=yourrefreshtokensecret
   NODE_ENV=development
   ```

5. Check `apps/web/.env` points to the backend:

   ```env
   VITE_REACT_APP_BASE_URL=http://localhost:3000
   ```

### Usage

Run the full development stack from the `turborepo` directory:

```bash
npm run dev
```

By default, the frontend runs at `http://localhost:5173` and the backend runs at `http://localhost:3000`.

The main user flows are:

- Browse and search public job listings.
- Register and log in as an applicant.
- Save listings, maintain profile information, and submit applications.
- Use staff-only pages to create, edit, search, and manage job listings and applications.
- Use administrator-only pages to manage user roles.

Initial administrator access needs to be created directly in MongoDB. The role values used by the app are `2001` for users, `1984` for staff, and `5150` for administrators.

## Notes

This project was produced as a dissertation prototype during the third year of a four-year university course. It was intended to explore a deployable recruitment platform, but the production deployment was not fully realised, mainly due to time constraints.

Some parts of the repository still reflect the project's prototype status, including starter Turborepo documentation and development-only helper content. Treat this as an academic proof of concept rather than a production-ready recruitment system.

## Get in Touch

<p align="center">
  <i>Built with <b>code</b>, <b>caffeine</b>, and 💜 by CitharaYote</i>
</p>

<p align="center">
  <a href="https://citharayote.xyz">
    <img src="https://img.shields.io/badge/Portfolio-Visit%20my%20site-8A2BE2?style=for-the-badge&logo=firefoxbrowser&logoColor=white" alt="Portfolio" />
  </a>
  <a href="https://github.com/CitharaYote">
    <img src="https://img.shields.io/badge/GitHub-CitharaYote-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
  <a href="https://www.linkedin.com/in/theo-cruddace/">
    <img src="https://img.shields.io/badge/LinkedIn-Connect%20with%20me-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:theocruddace@gmail.com">
    <img src="https://img.shields.io/badge/Email-Say%20hello-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>

<p align="center">
  <i>Like what I’m building? Feel free to support my work!</i>
</p>
<p align="center">
  <a href="https://www.buymeacoffee.com/citharayote">
    <img src="https://img.shields.io/badge/Buy%20me%20a%20coffee-Fuel%20my%20addiction-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=black" alt="Buy Me a Coffee" />
  </a>
</p>
