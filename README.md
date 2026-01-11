📱 Social Media Feed Management System (C++ / SFML 3.0)

A fully-featured social media backend + GUI system built in C++17 using SFML 3.0, designed as an academic + portfolio-grade project.
The system models core functionality similar to Instagram / Twitter with real data structures, file persistence, and a modular architecture.

🎯 Project Overview

This project implements a Social Media Feed Management System where users can:

Register and login

Create posts

Follow and unfollow other users

View a personalized feed

Like and comment on posts

Receive notifications

Browse profile history

Search users

Persist all data between runs

The project emphasizes clean architecture, data structures, and real-world design, not shortcuts or toy examples.

🧱 Architecture & Design Principles

Language: C++17

GUI Framework: SFML 3.0 (Graphics + Window)

Architecture: Modular, OOP-based

Separation of Concerns:

Core logic (data & algorithms)

GUI screens (presentation)

App controller (navigation)

No global variables

Const-correctness

Header / Source separation

Scalable & extensible design

📂 Project Structure
/SocialMediaSystem
│
├── core/
│   ├── User.h / User.cpp
│   ├── UserBST.h / UserBST.cpp
│   ├── Post.h / Post.cpp
│   ├── PostList.h / PostList.cpp
│   ├── Comment.h
│   ├── Notification.h
│   ├── NotificationQueue.h / .cpp
│   ├── HistoryStack.h / .cpp
│   ├── FeedManager.h / .cpp
│   ├── FileManager.h / .cpp
│
├── gui/
│   ├── Screen.h
│   ├── LoginScreen.h / .cpp
│   ├── FeedScreen.h / .cpp
│   ├── ProfileScreen.h / .cpp
│   ├── NotificationScreen.h / .cpp
│   ├── SearchScreen.h / .cpp
│
├── app/
│   ├── App.h / App.cpp
│
├── data/
│   ├── users.txt
│   ├── posts.txt
│   ├── connections.txt
│   ├── notifications.txt
│
├── main.cpp
└── README.md

🧩 Core Modules
👤 User Management (BST)

Users stored in a Binary Search Tree (key = userID)

Unique usernames

Secure login validation

Followers & following lists

Profile viewing

📝 Posts System

Posts stored in doubly linked lists

Supports:

Create / delete posts

Likes

Comments

Timestamp-based ordering

📰 Feed Generation

Feed shows posts from followed users only

Sorted by newest first

Efficient merging of post lists

🔔 Notifications (Priority Queue)

Implemented using a heap

Priority levels:

Comment

Like

Follow

Read / unread tracking

🕘 Browsing History (Stack)

Tracks visited profiles

Back navigation support

Clear history option

💾 File Persistence

Data saved in plain text files:

users.txt

posts.txt

connections.txt

notifications.txt

Automatically loads on startup

Automatically saves on exit and data changes

🖥️ GUI Features (SFML 3.0)

Login & Register Screen

Feed Screen (scrollable)

Profile Screen (follow / unfollow)

Notifications Screen

Search Screen

Mouse-based interaction

Text input handling

Clean SFML 3 event system (pollEvent() + getIf<T>())

⚙️ Build & Run Instructions
🔧 Requirements

C++17 compatible compiler

SFML 3.0

Windows (32-bit or 64-bit)

🛠️ Build (Visual Studio)

Open the project in Visual Studio

Add all .cpp files to the project

Set Working Directory to:

$(ProjectDir)


Build → Run

🛠️ Build (g++)
g++ -std=c++17 main.cpp app/*.cpp core/*.cpp gui/*.cpp \
    -lsfml-graphics -lsfml-window -lsfml-system

📌 Key Learning Outcomes

Advanced C++ OOP design

Data structures in real applications

SFML 3.0 modern event handling

File-based persistence systems

GUI-backend integration

Debugging linker & runtime issues

Industry-style project organization

🚀 Future Improvements

Password hashing

Pagination & infinite scrolling

Image posts

Better UI styling

Networked multi-user version

SQLite database integration

📜 License

This project is intended for educational and portfolio use.
Free to modify, extend, and learn from.

🙌 Author

Developed by: Hikmatyar and Team
Purpose: Academic Project / Portfolio
Tech Stack: C++17 · SFML 3.0 · Data Structures
