**Social Network Management System**

## Overview

This project is a **console-based social network management system** implemented in C++. It models users, their profiles, friendships, posts, and chat functionalities using object-oriented programming and advanced data structures such as AVL trees, heaps, and stacks. The system supports user registration, friend management, posting, and chat features, and persists user data via file I/O.

## Features

- **User Profiles:**  
  - Store username, email, full name, status, and interests.
  - Edit user interests interactively from a predefined list.

- **Friendship Management:**  
  - Each user's friends are managed using an AVL tree for efficient search and insertion.
  - Supports finding mutual friends between users.

- **Posts and Comments:**  
  - Users can create posts, like posts, and add comments.
  - Posts and comments are managed using stacks for efficient access.

- **Chat System:**  
  - One-on-one and group chat functionalities.
  - Chat messages contain sender, receiver, and message content.
  - Singleton pattern ensures only one chat manager instance per user.

- **Data Persistence:**  
  - User data, friendships, and posts are persisted to files.
  - Directories are created for each user to store their data.

- **Heaps:**  
  - Includes MaxHeap and MinHeap implementations (provided in separate header files) for potential features such as trending posts or priority queues.

## Project Structure

| File Name         | Description                                                |
|-------------------|-----------------------------------------------------------|
| main.cpp          | Main application logic, core class definitions            |
| AVL_Tree.hpp      | AVL tree implementation for managing friends              |
| MaxHeap.hpp       | Max heap implementation (for advanced features)           |
| MinHeap.hpp       | Min heap implementation (for advanced features)           |
| users.txt         | User data storage (username, name, email, status, interests) |

## Getting Started

### Prerequisites

- C++17 compatible compiler (e.g., g++, MSVC)
- Standard C++ libraries

### Compilation

```bash
g++ main.cpp -o social_network
```

> Make sure all header files (e.g., `AVL_Tree.hpp`, `MaxHeap.hpp`, `MinHeap.hpp`) are present in the same directory as `main.cpp`[1][2][3].

### Running

```bash
./social_network
```

## Usage

- **Startup:**  
  The program loads users from `users.txt` and initializes the social network.
- **User Actions:**  
  - View and edit your profile and interests.
  - Add or remove friends.
  - View mutual friends.
  - Post content, like, and comment on posts.
  - Send and receive messages.

## Data Model

- **User_Information:**  
  Stores user credentials, status, and interests.
- **User:**  
  Inherits from `User_Information`, adds content and friends management.
- **Social_Network:**  
  Manages all users and their connections via an AVL tree.
- **DataBase:**  
  Handles file I/O, loading and saving user data and friendships.
- **ChatMessage, User_Chat, ChatBox, ChatGroup:**  
  Manage chat functionalities, using singleton patterns for session control.
- **Posts:**  
  Stores post text, likes, and comments using stacks.

## Example User Data (`users.txt`)

```
22
shakib123    ShakaShaka     shakibarslan@gmail.com    A    00000000
turk_eman    Eman Murtaza          murtazaeman651@gmail.com   A    10000110
...
```
- Columns: username, full name, email, status (A=Active, D=Deactivated), interests code[4].

## Extending the Project

- Implement GUI for better user interaction.
- Integrate MaxHeap/MinHeap for trending posts or notifications.
- Enhance security and error handling.

## License

This project is for educational purposes.
