# 📝 Mini-Trello (Kanban) App

A simplified Trello-like Kanban application built using **Next.js**, **React**, **Node.js**, and **MongoDB**. This project implements core Kanban functionalities like authentication, workspace and board creation, list & card management, and drag-and-drop card movement. It also uses the Unsplash API to fetch board cover images.

-----

## ⚙️ Tech Stack

**Frontend**

  * [Next.js](https://nextjs.org/) – React-based framework for building the UI
  * [React](https://react.dev/) – Component-based UI library

**Backend**

  * [Express](https://expressjs.com/) – Node.js web framework to build REST APIs
  * [MongoDB](https://www.mongodb.com/) – NoSQL database for storing app data

**Other**

  * JWT-based Authentication
  * Unsplash API for fetching board images

-----

## 🚀 Features

  * User Authentication (Signup/Login/Logout)
  * Create Workspaces
  * Create Boards inside Workspaces
  * Create, Edit, Delete Cards
  * Drag & Drop Cards across Lists
  * Update Card details (title, description)
  * Persistent board data using MongoDB
  * Unsplash images for board covers


-----

## ⚡ Setup & Run Locally

### 1\. Clone Repository

```bash
git clone <your-repo-url>
cd <repo-folder>
```

-----

### 2\. Create `.env` File

Create a `.env` file in the root directory using the following template:

\<details\>
\<summary\>\<code\>.env.example\</code\>\</summary\>

```env
NODE_OPTIONS=--openssl-legacy-provider

MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/trello-clone?retryWrites=true&w=majority
MONGODB_DB=trello-clone
JWT_SECRET_KEY=your_jwt_secret_key

NEXT_PUBLIC_UNSPLASH_API=your_unsplash_access_key
```


> ⚠️ Replace placeholder values with your actual credentials.

-----

### 3\. Install Dependencies

#### Backend

```bash
cd backend
yarn install
yarn dev
```

#### Frontend

```bash
cd frontend
yarn install
yarn dev
```

-----

### 4\. Access App

Visit [http://localhost:3000](https://www.google.com/search?q=http://localhost:3000) in your browser.

-----

## 🗄️ Database Schema Overview

**Collections:**

  * **Users**: `{ _id, name, email, passwordHash, avatar }`
  * **Workspaces**: `{ _id, name, ownerId, members[] }`
  * **Boards**: `{ _id, title, workspaceId, imageUrl, visibility }`
  * **Lists**: `{ _id, title, boardId, position }`
  * **Cards**: `{ _id, title, description, listId, position }`

-----

## 📌 Known Limitations

  * No real-time updates between users
  * No invite/membership roles
  * No activity log, comments, search, or filters
  * No file uploads or attachments

-----

## 📍 Next Steps (Future Improvements)

  * Add real-time collaboration using
  * Implement comments & activity log
  * Add role-based access and invites
  * Add due dates, labels, and assignees

-----
🗄️ Database Schema Overview
Collections:

Users: { _id, name, email, passwordHash, avatar }

Workspaces: { _id, name, ownerId, members[] }

Boards: { _id, title, workspaceId, imageUrl, visibility }

Lists: { _id, title, boardId, position }

Cards: { _id, title, description, listId, position }

Comments: { _id, cardId, content, authorId }

-----

## 📸 Screenshots
<img width="1905" height="1062" alt="Screenshot 2025-09-14 173919" src="https://github.com/user-attachments/assets/18bf64f1-1cda-4fea-9759-35282b9d229e" />


<img width="1909" height="1069" alt="Screenshot 2025-09-14 173930" src="https://github.com/user-attachments/assets/b73b8e07-92a7-44ac-b27c-4c8b685f8f94" />

-----
<img width="1919" height="1079" alt="Screenshot 2025-09-14 174002" src="https://github.com/user-attachments/assets/366418df-d7c6-4a65-b11d-122974aa7100" />
