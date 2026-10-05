# IAI-SLE-3-
# SLE-3: Architectural Design using Full C4 Model

## Course

**02AML204 – Introduction to Artificial Intelligence**

## Student Details

* **Name:** Anushri Appaso Shinde
* **PRN:** 25UAM013
* **Division:** A

---

## 1. Project Title

### Search System – BFS and DFS Graph Search

This project represents the architectural design of a graph search system using the **Full C4 Model**.

The system allows a user to provide a graph, start node, and goal node and search for a path using:

* Breadth-First Search (BFS)
* Depth-First Search (DFS)

The project continues the work completed in **SLE-2**, where BFS and DFS were implemented and profiled.

---

## 2. SLE-3 Objective

The objective of SLE-3 is to represent the BFS and DFS Graph Search System using all four levels of the **C4 Model**:

1. Context Diagram
2. Container Diagram
3. Component Diagram
4. Code Level Overview

The architecture shows how the user interacts with the system and how the different parts of the search system work together.

---

## 3. System Description

The Search System finds a path between a start node and a goal node in a graph.

**BFS** explores the graph level by level using a queue, while **DFS** explores one branch as deeply as possible using a stack.

The system returns the path found and the number of nodes expanded during the search.

The same BFS and DFS system was used in SLE-2 for performance profiling and comparison.

---

## 4. C4 Model Architecture

### Level 1 – Context Diagram

The Context Diagram shows the complete Search System as one main system and the user as the external actor.

The user provides:

* Graph
* Start node
* Goal node
* Search method

The system processes the request using BFS or DFS and returns the search result.

---

### Level 2 – Container Diagram

The system is divided into the following main containers:

| Container             | Responsibility                              |
| --------------------- | ------------------------------------------- |
| **Input Module**      | Accepts the graph, start node and goal node |
| **Search Controller** | Selects BFS or DFS                          |
| **BFS Search**        | Performs Breadth-First Search               |
| **DFS Search**        | Performs Depth-First Search                 |
| **Result Module**     | Displays the path and nodes expanded        |

---

### Level 3 – Component Diagram

The **BFS Search Engine** is selected as the main container for the detailed component view.

Its major components are:

* **Frontier Manager** – Manages the BFS queue.
* **Visited Manager** – Keeps track of visited nodes.
* **Goal Checker** – Checks whether the current node is the goal.
* **Neighbor Expander** – Finds and processes neighboring nodes.
* **Path Reconstructor** – Reconstructs the path from start to goal.

---

### Level 4 – Code Level Overview

The Code Level shows the main functions involved in the BFS search process.

Important functions include:

```text
bfs(graph, start, goal)
get_neighbors(graph, node)
is_goal(node, goal)
update_visited(node)
reconstruct_path(parent, goal)
return_result(path)
```

These functions represent the main logic used by the BFS Search Engine.

---

## 5. Graph Used

The graph used in the previous SLE-2 profiling experiment contains **7 nodes**:

```text
        A
       / \
      B   C
     / \   \
    D   E   F
         \ /
          G
```

* **Start Node:** A
* **Goal Node:** G

The graph is represented using an adjacency list.

---

## 6. BFS and DFS

### Breadth-First Search (BFS)

BFS explores nodes level by level.

It uses a **queue (FIFO)** to manage the frontier.

### Depth-First Search (DFS)

DFS explores one branch as deeply as possible before backtracking.

It uses a **stack (LIFO)** to manage the frontier.

Both algorithms can be used to find a path from the start node to the goal node.

---

## 7. Design Decisions

The system is divided into separate modules to keep the architecture simple and easy to understand.

BFS and DFS are represented as separate search containers because they use different search strategies and data structures.

The graph input is shared by both algorithms so that their performance can be compared fairly.

A common Result Module provides the search result to the user.

---

## 8. Relation to SLE-2

SLE-2 focused on **performance profiling** of BFS and DFS.

The following aspects were measured in SLE-2:

* Execution time
* Nodes expanded
* Best case
* Average case
* Worst case
* Search path
* Flame graphs using py-spy

SLE-3 extends the same system by showing its **software architecture using the C4 Model**.

Therefore:

```text
SLE-1 → Code / Search Implementation
SLE-2 → Performance Profiling
SLE-3 → Architectural Design
```

---

## 9. Tools Used

* **Python** – Implementation of BFS and DFS
* **draw.io / diagrams.net** – C4 architecture diagrams
* **GitHub** – Project repository and version control
* **ChatGPT** – Assistance with C4 architecture understanding and documentation

---

## 10. AI Contribution

### AI Tool Used

ChatGPT

### What AI Helped With

* Understanding the C4 Model
* Organizing the system into Context, Container, Component and Code levels
* Improving architecture documentation
* Structuring the README and explanations

### What I Did Myself

* Selected the BFS + DFS Graph Search System from SLE-2
* Implemented and ran the BFS and DFS programs
* Performed the profiling work in SLE-2
* Designed and checked the architecture
* Created the C4 diagrams
* Managed the GitHub repository

---

## 11. Conclusion

This SLE-3 activity helped me understand how a BFS and DFS search program can be represented as a complete software architecture.

The Full C4 Model helped me view the system at different levels, from the overall user interaction to the internal components and functions.

This activity improved my understanding of software architecture, modular design and the relationship between different parts of an AI search system.

---

## Repository Contents

```text
SLE-3/
│
├── README.md
├── Context_Diagram.png
├── Container_Diagram.png
├── Component_Diagram.png
├── Code_Level.png
└── SLE3_25UAM013_Anushri_Shinde.docx
```

---

## Author

**Anushri Appaso Shinde**
PRN: **25UAM013**
B.Tech CSE (AI & ML)
Division: **A**
