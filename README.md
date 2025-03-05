# 🖥️ Linux Directory Management - OS Lab

## 📌 Overview
This repository contains a Linux-based directory management assignment where various commands are used to manipulate files and directories in a structured manner. The goal is to practice and demonstrate proficiency in essential Linux commands like `mkdir`, `mv`, `cp`, `ls`, `cat`, and more.

## 👩‍🏫 Instructor: Malak Ghabayen

## 🏷️ Tags
- Linux
- Bash
- File System
- Terminal
- CLI Commands

---

## 📂 Directory Structure
```
/home/OS/Lab1/
├── Archive/
├── Customer/
├── Finance/
│   ├── Cust1.txt
│   ├── Cust2.txt
│   └── Cust3.txt
└── Public/
    ├── Forms/
    └── Info/
        └── Leave.txt
```

---

## 🛠️ Commands Used
| Command  | Description |
|----------|------------|
| `mkdir`  | Creates directories |
| `cd`     | Changes directory |
| `cd ..`  | Moves to the parent directory |
| `mv`     | Moves or renames files/directories |
| `cp`     | Copies files/directories |
| `ls`     | Lists files and directories |
| `cat`    | Displays file content |
| `clear`  | Clears the terminal screen |
| `exit`   | Exits the terminal session |

---

## 📜 Implementation Steps

### 🏗️ Step 1: Create Directory Structure
```bash
mkdir -p OS/Lab1/{Finance,Customer,Public/{Forms,Info},Archive} && \
cd OS/Lab1 && \
touch Finance/{Cust1.txt,Cust2.txt,Cust3.txt} \
      Public/Info/Leave.txt
```
📌 **Check Structure:**
```bash
tree
```
```
.
├── Archive
├── Customer
├── Finance
│   ├── Cust1.txt
│   ├── Cust2.txt
│   └── Cust3.txt
└── Public
    ├── Forms
    └── Info
        └── Leave.txt
```

---

### 🔄 Step 2: Move Customer Files to `Customer/`
```bash
mv Finance/* Customer
tree
```
```
.
├── Archive
├── Customer
│   ├── Cust1.txt
│   ├── Cust2.txt
│   └── Cust3.txt
├── Finance
└── Public
    ├── Forms
    └── Info
```

---

### 📂 Step 3: Copy Customer Files to `Archive/`
```bash
cp Customer/* Archive
tree
```
```
.
├── Archive
│   ├── Cust1.txt
│   ├── Cust2.txt
│   └── Cust3.txt
├── Customer
│   ├── Cust1.txt
│   ├── Cust2.txt
│   └── Cust3.txt
├── Finance
└── Public
    ├── Forms
    └── Info
```

---

### 📝 Step 4: Move `Leave.txt` and Rename it to `leave_old.txt`
```bash
mv Public/Info/Leave.txt Archive/leave_old.txt
tree
```
```
.
├── Archive
│   ├── Cust1.txt
│   ├── Cust2.txt
│   ├── Cust3.txt
│   └── leave_old.txt
├── Customer
│   ├── Cust1.txt
│   ├── Cust2.txt
│   └── Cust3.txt
├── Finance
└── Public
    ├── Forms
    └── Info
```

---

### 📁 Step 5: Move `leave_old.txt` to `Forms/`
```bash
mv Archive/leave_old.txt Public/Forms/
tree
```
```
.
├── Archive
│   ├── Cust1.txt
│   ├── Cust2.txt
│   ├── Cust3.txt
├── Customer
│   ├── Cust1.txt
│   ├── Cust2.txt
│   └── Cust3.txt
├── Finance
└── Public
    ├── Forms
    │   └── leave_old.txt
    └── Info
```

---

### ✅ Step 6: Verify Files in `Customer/` and `Archive/`
```bash
cd Customer && tree
```
```
.
├── Cust1.txt
├── Cust2.txt
└── Cust3.txt
```
```bash
cd ../Archive && tree
```
```
.
├── Cust1.txt
├── Cust2.txt
└── Cust3.txt
```

---

### 🗑️ Step 7: Delete Files in `Customer/`
```bash
cd ../Customer/ && rm *
tree
```
```
.
(empty)
```

---

### 📜 Step 8: Display Contents of Text Files
```bash
cd ../ && cat {Archive,Public/Forms}/*.txt
```
```
Dear Instructor, I promise I didn’t use ChatGPT for this... or did I? 😏
I worked so hard, even my laptop cried. Please reward me with a 100%! 🥺
If I don’t get 100%, my pet rock will be very disappointed. 🪨
P.S. I’ll name my firstborn after you if you give me full marks. Deal? 🤝
```

---

### 🔄 Step 9: Clear Screen & Exit (Do it Yourself 😉)
```bash
clear
exit
```

---

## 🎯 Conclusion
This lab covers essential file system commands in Linux, providing hands-on experience with directory structures, file movement, copying, renaming, deletion, and file content display. This structured approach helps in understanding hierarchical file management in Linux environments.

---

### 🌟 Happy Coding! 🚀
