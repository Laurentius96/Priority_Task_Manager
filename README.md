<div align="center">  <h1> Priority Task Manager </div>

<div align="center">
  <h3>Python Task Management System with Priority Levels</h3>
  <p><i>An educational Jupyter notebook project developed by DNC to teach fundamental Python concepts through practical task management implementation.</i></p>
</div>

<p align="center">
  <a href="#-overview">Overview</a> •
  <a href="#-features">Features</a> •
  <a href="#-installation">Installation</a> •
  <a href="#%EF%B8%8F-usage">Usage</a> •
  <a href="#-notebook-structure">Notebook Structure</a> •
  <a href="#-learning-objectives">Learning Objectives</a> •
  <a href="#%EF%B8%8F-technologies">Technologies</a> •
  <a href="#-contributing">Contributing</a> •
  <a href="#-license">License</a>
</p>

## 🔍 Overview

This project is a comprehensive task management system implemented in Python using Jupyter notebooks as part of DNC's (Digital Nation Course) educational curriculum. The system demonstrates essential programming concepts through a practical application that allows users to manage tasks with different priority levels.

The project serves as an interactive learning experience, combining theoretical concepts with hands-on implementation in a notebook environment that facilitates experimentation and learning.

## 🚀 Features

### Core Functionalities
- **Add Tasks**: Create new tasks with descriptions and priority assignments
- **Remove Tasks**: Delete specific tasks from the system
- **List Tasks**: Display all current tasks with their priority levels
- **Save Tasks**: Persist task data to files for future sessions
- **Interactive Menu**: User-friendly command-line interface

### Priority System
- **High Priority**: Critical tasks requiring immediate attention
- **Medium Priority**: Important tasks with moderate urgency
- **Low Priority**: Tasks that can be completed when time permits

### Educational Components
- **Step-by-step Implementation**: Code broken down into digestible sections
- **Concept Explanations**: Detailed explanations of Python concepts used
- **Interactive Examples**: Live code cells for experimentation

## 💾 Installation

### Prerequisites
- Python 3.7 or higher
- Jupyter Notebook or JupyterLab
- Basic understanding of Python syntax

### Setup Instructions

1. **Clone the repository:**
```bash
git clone https://github.com/Laurentius96/Priority_Task_Manager.git
```

2. **Navigate to project directory:**
```bash
cd Priority_Task_Manager
```

3. **Run the `main.ipynb` notebook in a Jupyter environment:**
```bash
jupyter notebook main.ipynb
```

4. **Alternatively, run the script directly:**
```bash
python -m main.py
```

## ⚙️ Usage

### Running the Notebook

The notebook is structured in sequential cells that build upon each other. Execute cells in order using `Shift + Enter`.

### Sample Code Examples

**Task Data Structure:**
```python
# Example task structure used in the notebook
tasks = [
    {"description": "Study Python", "priority": "High"},
    {"description": "Go to gym", "priority": "Medium"},
    {"description": "Buy groceries", "priority": "Low"}
]
```

**Adding a Task Function:**
```python
def add_task(tasks, description, priority):
    """
    Add a new task to the task list
    
    Parameters:
    tasks (list): Current list of tasks
    description (str): Task description
    priority (str): Task priority level
    """
    new_task = {"description": description, "priority": priority}
    tasks.append(new_task)
    print(f"Task '{description}' added with {priority} priority!")
    return tasks
```

**Expected Output:**
```
Task 'Study Python' added with High priority!
Current tasks: 3
```

### Interactive Menu System

```python
def display_menu():
    print("\n=== TASK MANAGER ===")
    print("1. Add Task")
    print("2. Remove Task") 
    print("3. List Tasks")
    print("4. Save Tasks")
    print("5. Exit")
    return input("Choose an option (1-5): ")
```

**Sample Execution Result:**
```
=== TASK MANAGER ===
1. Add Task
2. Remove Task
3. List Tasks
4. Save Tasks
5. Exit
Choose an option (1-5): 3

=== CURRENT TASKS ===
1. Study Python - Priority: High
2. Go to gym - Priority: Medium
3. Buy groceries - Priority: Low
```

## 📓 Notebook Structure

```
task_manager.ipynb
├── 1. Introduction & Setup
│   ├── Project overview
│   ├── Learning objectives
│   └── Import statements
├── 2. Data Structures
│   ├── Task representation
│   ├── List operations
│   └── Dictionary usage
├── 3. Core Functions
│   ├── add_task()
│   ├── remove_task()
│   ├── list_tasks()
│   └── save_tasks()
├── 4. Control Flow
│   ├── Menu system
│   ├── User input handling
│   └── Conditional logic
├── 5. File Operations
│   ├── Saving to file
│   ├── Loading from file
│   └── Error handling
├── 6. Main Program Loop
│   ├── Interactive execution
│   ├── Menu navigation
│   └── Program termination
└── 7. Exercises & Extensions
    ├── Practice problems
    ├── Enhancement ideas
    └── Further learning resources
```

## 🎯 Learning Objectives

This notebook teaches the following Python concepts through practical implementation:

### 1. Data Structures
- **Lists**: Managing collections of tasks
- **Dictionaries**: Storing task attributes
- **Data manipulation**: Adding, removing, and modifying data

### 2. Control Flow
- **Conditional statements**: Menu navigation and decision making
- **Loops**: Iterating through task collections
- **Function definitions**: Code organization and reusability

### 3. File I/O Operations
- **Writing files**: Persisting task data
- **Reading files**: Loading saved tasks
- **Error handling**: Managing file operations safely

### 4. User Interaction
- **Input validation**: Ensuring data integrity
- **Menu systems**: Creating user-friendly interfaces
- **Output formatting**: Presenting information clearly

## 🛠️ Technologies

- **Python 3.x**: Core programming language
- **Jupyter Notebook**: Interactive development environment
- **Built-in Libraries**: 
  - `os`: File system operations
  - `json`: Data serialization (optional enhancement)
- **Pandas**: Data manipulation (for advanced features)

## 📊 Code Examples with Results

### Task Listing Function
```python
def list_tasks(tasks):
    """Display all tasks with their priorities"""
    if not tasks:
        print("No tasks available.")
        return
    
    print("\n=== CURRENT TASKS ===")
    for i, task in enumerate(tasks, 1):
        print(f"{i}. {task['description']} - Priority: {task['priority']}")
```

**Execution Result:**
```python
# Sample execution in notebook cell
tasks = [
    {"description": "Complete Python project", "priority": "High"},
    {"description": "Review code documentation", "priority": "Medium"}
]

list_tasks(tasks)
```

**Output:**
```
=== CURRENT TASKS ===
1. Complete Python project - Priority: High
2. Review code documentation - Priority: Medium
```

### File Save Operation
```python
def save_tasks_to_file(tasks, filename="tasks.txt"):
    """Save tasks to a text file"""
    try:
        with open(filename, "w") as file:
            for task in tasks:
                file.write(f"{task['description']},{task['priority']}\n")
        print(f"Tasks saved to {filename} successfully!")
    except Exception as e:
        print(f"Error saving tasks: {e}")
```

**Expected Result:**
```
Tasks saved to tasks.txt successfully!
File created: tasks.txt
Content preview:
Complete Python project,High
Review code documentation,Medium
```

## 🚀 Enhancement Ideas

The project can be extended with additional features:

- **Task Categories**: Group tasks by work, personal, etc.
- **Due Dates**: Add deadline tracking functionality
- **Task Status**: Implement completed/pending status
- **Data Visualization**: Create charts showing task distribution
- **Export Options**: Save tasks in different formats (CSV, JSON)

## 🤝 Contributing

This educational project welcomes contributions to improve the learning experience:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/educational-enhancement`)
3. Make your changes with clear documentation
4. Add examples and explanations for new concepts
5. Submit a pull request with detailed description

## 📜 License

This project is part of DNC's educational curriculum and is available for learning purposes.

<details open>
<summary><b>CC BY-NC-ND 4.0 License</b></summary>

This repository is licensed under the [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](https://creativecommons.org/licenses/by-nc-nd/4.0/).

### What this means:

- ✅ **You can share** — You are free to copy and redistribute the material in any medium or format
- ❌ **No commercial use** — You may not use the material for commercial purposes
- ❌ **No derivatives** — You may not remix, transform, or build upon the material
- ✅ **Attribution required** — You must give appropriate credit, provide a link to the license, and indicate if changes were made

For the complete license terms, please see the [LICENSE.md](LICENSE.md) file.
</details>

## 🎓 Educational Resources

- **Python Documentation**: [python.org](https://docs.python.org/)
- **Jupyter Notebook Guide**: [jupyter.org](https://jupyter.org/documentation)
- **Data Structures Tutorial**: Additional learning materials in the notebook

---

<div align="center">
  <p><b>Developed with 💙 by <a href="https://github.com/Laurentius96">Lorenzo C. Bianchi</a> feat. DNC Educational Team</b></p>
  <p><i>Learning through practice - building real solutions with code!</i></p>
</div>
