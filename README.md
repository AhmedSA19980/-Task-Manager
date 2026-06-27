# -Task-Manager




 Task Manager with IndexedDB, Filtering, and Persistent Storage



 🧩 Project Overview

This project is a single-page task manager application that stores tasks locally in the browser using IndexedDB.


Users can add tasks, mark them as done or pending, delete them, filter by status, search by text, and safely refresh the page without losing data.
The UI updates instantly while all data operations are reliably persisted.



🧬 Core Concepts
🔹 IndexedDB for Persistent Storage

Tasks are stored inside the browser using IndexedDB, which allows structured, long-term data storage.

Unlike localStorage, IndexedDB supports large datasets, indexing, and asynchronous operations.



🔹 CRUD Operations (Create, Read, Update, Delete)
The project implements full CRUD functionality:

Create new tasks
Read all tasks on startup
Update task status (Pending ↔ Done)
Delete individual tasks or clear all tasks
This mirrors real production-grade data workflows.



🔹 Asynchronous Programming with async / await

IndexedDB is event-based by nature.

The project wraps IndexedDB requests inside Promises, allowing clean and readable async/await syntax—an essential modern JavaScript skill.



🔹 In-Memory State + Persistent Sync

Tasks are stored in two layers:

IndexedDB → long-term persistence
In-memory array → fast UI rendering
This separation ensures:

Fast UI updates
Safe rollback when database operations fail


🔹 Optimistic UI Updates

When updating or deleting tasks, the UI updates immediately (optimistic update) before the database confirms success.

If the database operation fails, the UI automatically rolls back to the previous state—exactly how professional apps behave.



🔹 Filtering by Task Status
Users can filter tasks using:

All
Pending
Done
This demonstrates how application state (currentFilter) directly controls UI rendering.



🔹 Live Search (Title & Description)
A real-time search input filters tasks as the user types.
The search works across both task titles and descriptions, showcasing efficient client-side filtering logic.



🔹 Event Delegation for Performance
Instead of attaching event listeners to every task button, the project uses event delegation:

One click listener on the task list container
Detects which task and action were clicked
This approach is scalable, efficient, and framework-ready.



🔹 User Feedback & UX Enhancements
The project includes:

Toast notifications for actions (add, update, delete)
Loading spinner during database operations
Confirmation dialogs before destructive actions
Visual color coding:
🟡 Pending tasks
🟢 Done tasks
These patterns improve usability and professionalism.



🔹 Keyboard Productivity Shortcut
Users can press Ctrl + Enter to quickly add a task.
This introduces accessibility and productivity concepts often missed in beginner projects.

