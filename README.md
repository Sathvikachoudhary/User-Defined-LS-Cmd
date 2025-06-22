# LS -LIAS USER DEFINED COMMAND

## 📚 PROJECT OVERVIEW:
This project is a user-defined version of the Linux ls command written in the C language. It mimics functionalities like listing files with details such as inode number, permissions, file size, block size, and including hidden files using -l, -i, -a, and -s options.
The project uses Linux system calls such as opendir, readdir, stat, and structures like dirent and stat to extract and display file metadata.

## 📋 KEY FEATURES:
- 📄 Display files and directories from a given path
- 🕶️ Supports -a flag to show hidden files
- 🔍 Supports -i flag to print inode numbers
- 📦 Supports -s flag to display file sizes in blocks
- 📝 Supports -l flag for long-format listing (permissions, links, UID, GID, size, modification time)
- 🧮 Handles combination of flags like -lias
- 📂 Uses system calls: stat(), ctime(), opendir(), readdir(), strchr(), etc.

## 📂 FILE STRUCTURE:
- myls.c → Complete implementation of ls -lias logic
- (Optional) makefile → Automates compilation (if needed)
## ⚙️ HOW TO COMPILE AND RUN:
### ✅ METHOD 1: Manual Compilation (Recommended):
gcc -o myls myls.c
- ./myls                 # List current directory files
- ./myls -a              # Show all including hidden files
- ./myls -l              # Long listing format
- ./myls -li             # Long + inode numbers
- ./myls -lias           # Long + inode + all + block size
- ./myls /etc -lis       # Apply flags to a specific directory
### ✅ METHOD 2: Using Makefile (Optional):
- myls: myls.c
	- cc -o myls myls.c
- To compile: make
- To run: ./myls
## 🖥️ COMMAND OPTIONS:
- -l	Long format listing
- -i	Show inode numbers
- -a	Show hidden files
- -s	Show size in blocks
## 📌 SAMPLE OUTPUT:
- ./myls -lias
- in function . lias
- 56789 d rwxr-xr-x  2 1000 1000 4096 Jun 21  Documents
- 12345 - rw-r--r--  1 1000 1000  123 Jun 19  README.txt
## 🧠 CONCEPTS USED:
- Bitwise permissions display
- Recursive directory reading
- File metadata extraction
- Time formatting using ctime()
- Use of stat, dirent, strchr, strlen, etc.


# Happy Coding....!
