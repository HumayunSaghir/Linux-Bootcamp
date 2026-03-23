# 🐧 Linux Bootcamp – Part 1

**Comprehensive Reference Guide: Fundamental Concepts & Essential Commands**

---

## 📖 Key Concepts

- **Terminal Emulator:** Graphical interface to access the shell.  
- **Shell:** Command-line interpreter executing your instructions.  
- **Command Prompt:** Indicator showing the terminal is ready for input.  
- **Process:** Active instance of a program or command.  
- **Environment Variables:** Named system values that affect process behavior.  
- **Path (`$PATH`):** Environment variable listing directories where executables are searched.  

---

## 💻 Linux Commands Reference

### 🔹 Navigation & File System

| Command | Description |
|---------|-------------|
| `ls` | Lists files & directories in current directory. |
| `ls -a` | Includes hidden files (starting with `.`). |
| `ls -l` | Detailed listing (permissions, owner, size, date). |
| `ls -R` | Lists contents recursively in all subdirectories. |
| `cd` | Go to home directory. |
| `cd folder` | Navigate into `folder`. |
| `cd ..` | Move up one level to parent directory. |
| `cd ../folder` | Move up one level, then into `folder`. |
| `cd ~/Desktop/Linux` | Directly navigate to `Linux` folder on Desktop. |
| `open .` | Open current directory in GUI file manager. |
| `mkdir folder` | Create a new directory. |
| `mkdir folder/newfolder` | Create `newfolder` inside `folder`. |
| `mkdir -p folder1/folder2/folder3` | Create nested directories (parents auto-created). |
| `touch file.txt` | Create empty file or update timestamp. |
| `touch folder/file.txt` | Create file inside a folder. |

---

### 🔹 File Manipulation

| Command | Description |
|---------|-------------|
| `cp file1.txt file2.txt` | Copy file1 to file2. |
| `cp -R test random` | Copy directory `test` recursively to `random`. |
| `mv file.txt folder` | Move file to a directory. |
| `mv file.txt newFileName.txt` | Rename file. |
| `mv file.txt ../newname.txt` | Move & rename file to parent directory. |
| `mv folder newFolder` | Rename directory. |
| `mv folderToBeMoved targetFolder` | Move/rename folder into target. |
| `mv folder/folder .` | Move nested folder to current directory. |
| `rm file.txt` | Delete a file. |
| `rm -R folder` | Delete directory and all contents. |

---

### 🔹 Viewing & Editing Files

| Command | Description |
|---------|-------------|
| `cat file.txt` | Display file content. |
| `cat file1.txt file2.txt` | Display multiple files sequentially. |
| `cat > file.txt` | Create file & input content (Ctrl+D to save). |
| `cat file1.txt file2.txt > file3.txt` | Concatenate files into a new file. |
| `head file.txt` | Show first 10 lines. |
| `head -n 2 file.txt` | Show first 2 lines only. |
| `tail file.txt` | Show last 10 lines. |
| `tail -n 2 file.txt` | Show last 2 lines only. |
| `nano file.txt` | Open file in Nano text editor. |
| `diff file1.txt file2.txt` | Compare two files line by line. |

---

### 🔹 Searching & Output

| Command | Description |
|---------|-------------|
| `echo "hello world"` | Print text to terminal. |
| `echo "hello world" > file1.txt` | Write text to file (overwrite). |
| `cat file1.txt file2.txt \| tr a-z A-Z > file3.txt` | Concatenate files, convert to uppercase, save to new file. |
| `find .` | List all files and directories in current path. |
| `find ..` | List all files starting from parent directory. |
| `find ../folder` | List all files starting from specific folder. |
| `find . -type f` | Find only standard files in current directory. |
| `find . -type f -name "two.txt"` | Find a specific file by name. |
| `find . -type f -name "*.jsx"` | Find all files with `.jsx` extension. |
| `locate "*.txt"` | Quickly find all `.txt` files using prebuilt database. |
| `which python3` | Show full path of `python3` executable. |

---

### 🔹 System & Environment Variables

| Command | Description |
|---------|-------------|
| `echo $PATH` | Display the value of `$PATH`. |
| `export MY_PATH="aaxe"` | Set environment variable `MY_PATH`. |
| `alias det="ls -al"` | Create custom shortcut `det` for `ls -al`. |
| `man echo` | Open manual page for `echo`. |
| `sudo man echo` | Open manual page with root privileges. |
| `df` | Show available disk space. |
| `df -m` | Show disk space in megabytes. |
| `df -hg` | Show disk space in human-readable format (GB). |
| `du` | Estimate disk usage for current directory & subdirectories. |
| `clear` | Clear terminal screen. |