# 🐚 MyShell — Custom Linux Shell (OS Project)

## 🌟 Overview

**MyShell** is a lightweight custom shell developed in **C++**, simulating essential functionalities of a Linux terminal.  
It demonstrates **core operating system concepts** such as process creation, execution, piping, and synchronization using:

- `fork()`
- `execvp()`
- `waitpid()`
- `pipe()`
- `dup2()`

---

## 👥 Team Members

| Name            | Contact                                      |
|------------------|----------------------------------------------|
| **Ghulam Qadir** | 📧 gqitspecialist@gmail.com <br> 🔗 [LinkedIn](https://www.linkedin.com/in/ghulam-qadir-07a982365) |
| **Noor Malik**   | 🔗 [LinkedIn](https://www.linkedin.com/in/noormalik56500) |
| **Ishrat Ali**   | —                                            |
| **Muqeem Ahmed** | —                                            |

---

## 🧠 Project Objectives

The main goal is to create a **basic Linux shell** that supports:

- Command parsing and execution  
- Process creation using `fork()`  
- Execution of commands using `execvp()`  
- Command pipelining using `pipe()` and `dup2()`  
- Synchronous execution with `waitpid()`  
- Continuous shell loop and clean termination

---

## 🛠️ Technologies Used

| Component     | Purpose                           |
|---------------|-----------------------------------|
| **C++**        | Core logic and shell control flow |
| `fork()`       | Create child processes            |
| `execvp()`     | Execute external commands         |
| `pipe()`       | Create communication channels     |
| `dup2()`       | Redirect file descriptors         |
| `waitpid()`    | Wait for child process completion |
| `getline()`    | Read CLI input                    |

---

## 📜 License

This project is open-source and available for **educational and academic use** under the **MIT License**.

---

## 📧 Contact

For inquiries or feedback:

- **Ghulam Qadir** — 📧 gqitspecialist@gmail.com  
- **Noor Malik** — 🔗 [LinkedIn](https://www.linkedin.com/in/noormalik56500)
## 🚀 Features

### 🔹 Command Execution

execute standard Linux commands:

```shell
MyShell> ls -l
MyShell> pwd

🔹 Process Creation & Management
Each command is executed in a child process via fork() and execvp().

🔹 Pipelined Commands
Supports piped commands:

shell
Copy
Edit
MyShell> ls -l | grep .cpp | wc -l
🔹 Lifecycle Management
quit command for graceful termination

Basic input validation and error handling

🧪 Example Commands
bash
Copy
Edit
MyShell> whoami
MyShell> ps aux | grep bash
MyShell> cat file.txt | sort | uniq
MyShell> quit
📂 File Structure
bash
Copy
Edit
├── myshell.cpp       # Main shell implementation
├── README.md         # Project documentation
🔄 Program Flow
mermaid
Copy
Edit
flowchart TD
    A[User enters command] --> B{Contains pipe?}
    B -- Yes --> C[Split using '|']
    C --> D[Execute piped commands with fork(), pipe(), dup2()]
    B -- No --> E[Parse and execute with execvp()]
    D --> F[Wait for all child processes]
    E --> F
    F --> G[Loop continues]
🏁 How to Compile & Run
🔧 Compile
bash
Copy
Edit
g++ myshell.cpp -o myshell
▶️ Run
bash
Copy
Edit
./myshell



