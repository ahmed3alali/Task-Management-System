<h1 align="center">🧠 Task Management System (C++ Console Application)</h1>

<p align="center">
  <b>A lightweight, file-based Task Management System written in C++</b><br>
  Manage projects, users, and tasks efficiently through an interactive console interface.
</p>

---

## 📘 Overview

This project is a **console-based Task Management System** built in **C++**.  
It allows users to **create, read, update, and delete** (CRUD) tasks, projects, and users, while maintaining persistence through a simple **text file database (`database.txt`)**.

The program demonstrates key concepts of **Object-Oriented Programming (OOP)** such as **encapsulation, composition, and class relationships** between `User`, `Project`, and `Task`.

---

## 🧩 Project Structure

📦 TaskManagementSystem
┣ 📜 main.cpp
┣ 📜 FileHandler.cpp
┣ 📜 ptasksystem.h
┗ 📜 database.txt


- **main.cpp** → Entry point with UI and main menu logic.  
- **FileHandler.cpp** → Handles file operations (read, write, update, delete).  
- **ptasksystem.h** → Class definitions for `Task`, `User`, `Project`, and `FileHandler`.  
- **database.txt** → Persistent storage for tasks data.

---

## ⚙️ Features

✅ **Add Tasks** – Create new tasks and link them with users and projects.  
✅ **Update Tasks** – Modify existing task details or status dynamically.  
✅ **Delete Tasks** – Remove tasks safely and update the file automatically.  
✅ **User Management** – Register new users with roles and unique IDs.  
✅ **Project Tracking** – Assign and search tasks by project name.  
✅ **File Persistence** – Store all data in a local file (`database.txt`).  
✅ **Reports** – Generate usage statistics for system overview.  
✅ **Cross-Platform** – Works on both Windows and Linux (uses `system("cls")` or `system("clear")`).

---

## 🏗️ Object Model

### 🧑‍💻 **User**
Represents a user in the system.

| Property | Type | Description |
|-----------|------|-------------|
| `name` | string | Name of the user |
| `userID` | int | Unique identifier |
| `hisRole` | string | Role or position |
| `projects` | vector\<Project*\> | Projects assigned |
| `tasks` | vector\<Task*\> | Tasks assigned |

---

### 🏢 **Project**
Represents a project with tasks and assigned users.

| Property | Type | Description |
|-----------|------|-------------|
| `name` | string | Project name |
| `tasks` | vector\<Task*\> | Tasks under this project |
| `users` | vector\<User*\> | Users assigned to this project |

---

### 📋 **Task**
Represents an individual task.

| Property | Type | Description |
|-----------|------|-------------|
| `name` | string | Task title |
| `description` | string | Task details |
| `category` | string | Task category (e.g., Work, Gym) |
| `time` | string | Deadline or day |
| `label` | string | Label such as “Urgent” or “High” |
| `status` | string | Task status (`F` = Finished / `UF` = Unfinished) |
| `assignedUser` | User* | Pointer to assigned user |
| `assignedProject` | Project* | Pointer to related project |

---

### 💾 **FileHandler**
Handles file I/O and core management.

| Function | Description |
|-----------|-------------|
| `writeTasksIntoFile()` | Writes all tasks to `database.txt` |
| `readTasksFromFile()` | Reads tasks, users, and projects from file |
| `addTaskAndHandleFiles()` | Adds tasks interactively |
| `deleteTask()` | Deletes a task by name |
| `updateTaskInfo()` | Edits task name, description, or status |
| `UpdateTaskStatus()` | Quickly changes task status |
| `fullSystemReport()` | Displays total counts of users, tasks, and projects |
| `findTaskByName()` | Searches tasks by project name |
| `newUser()` | Registers a new user |

---

## 💻 How to Run

### 🧱 Requirements
- C++ compiler (e.g., **g++**, **clang**, or **MSVC**)
- Basic terminal access

### ▶️ Run Commands

#### **Windows (CMD / PowerShell)**
```bash
g++ main.cpp -o taskmanager
taskmanager.exe


```
### ▶️ Linux Run  Commands
```
g++ main.cpp -o taskmanager
./taskmanager
```


🧠 Example Usage

===== Task Management System =====
1. Add Task for Your Project
2. Delete Task
3. Update Task
4. Short Usage Report
5. New User Registration
6. Tasks Search Engine By Name
9. Fast Task STATUS Update


Enter Task Name: Code Review
Enter Project Name: TMTC Web
Enter User Name: Ahmed
Enter Task Description: Review the backend APIs
Enter Task Category: Work
Enter Task Label: Urgent
Enter Task Day: Monday
Enter Task Status: UF
Task info written into the file.


<h3 align="center">⭐ If you like this project, give it a star on GitHub!</h3> 

