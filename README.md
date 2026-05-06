# Automating the Recruitment Process

![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white) ![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB) ![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB) ![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white) ![CSS](https://img.shields.io/badge/css-%23663399.svg?style=for-the-badge&logo=css&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white) ![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white) ![Turborepo](https://img.shields.io/badge/Turborepo-%230F0813.svg?style=for-the-badge&logo=Turborepo&logoColor=white)

## Introduction

This was a project undertaken as my third-year dissertation at the University of Sheffield. The aim of the project was to improve upon the outdated recruitment software currently used by the University of Sheffield, which relies heavily on manual processes and lacks compatibility with modern systems.

## Setup and Installation

### Prerequisites

- Node.js
- NPM or Yarn
- MongoDB Atlas cluster

### Installation Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/CitharaYote/uni-com3610-project.git
   ```

2. Navigate to the turborepo directory:

   ```bash
    cd uni-com3610-project/turborepo
   ```

3. Install the dependencies:

   ```bash
   npm install
   ```

   or

   ```bash
   yarn install
   ```

4. Set up environment variables:

   - Rename `.env.example` to `.env` in both `turborepo/apps/backend` and `turborepo/apps/web`.
   - Update the environment variables with your MongoDB Atlas credentials and generate a pair of secure JWT secret keys in `turborepo/apps/backend/.env`.
   - All other options can be left as default for local development.

5. Start the development server:
   ```bash
    npm run dev
   ```
   or
   ```bash
   yarn dev
   ```
   - This will start both the backend and frontend applications concurrently through Turborepo.
   - The frontend will be accessible by default at `http://localhost:5173` and the backend at `http://localhost:3000`.

### Usage Information

- Admin accounts need be created through the MongoDB database directly.
- The job creation form can be autofilled with dummy data by clicking the info text at the top of the form.
