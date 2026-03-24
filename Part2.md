<div align="center">

# 🐧 Linux Bootcamp – Part 2

### 📘 Advanced Commands & System Utilities

![Linux](https://img.shields.io/badge/Linux-Terminal-black?style=for-the-badge&logo=linux)
![Status](https://img.shields.io/badge/Status-Learning-blue?style=for-the-badge)
![Level](https://img.shields.io/badge/Level-Intermediate-green?style=for-the-badge)

*A continuation of Linux Bootcamp: exploring advanced commands, permissions, searching, processes, and networking.*

</div>

---

## 📖 Key Concepts

- **Permissions:** Define who can read (`r`), write (`w`), or execute (`x`) a file.  
- **Owner / Group / Others:** Users controlling file access.  
- **Processes:** Programs running in the background or foreground.  
- **Commands Execution:** Using `find`, `grep`, `chmod`, `chown`, etc. to manipulate files & system.  
- **Shortcuts:** Keyboard combinations to improve command-line efficiency.  

---

## 💻 Linux Commands Reference

### 🔹 File Search & Filtering

| Command | Description |
|---------|-------------|
| `find . -type f -iname "filename.txt"` | Find file ignoring case. |
| `find . -type f -mmin -20` | Files modified **less than 20 minutes ago**. |
| `find . -type f -mmin +20` | Files modified **more than 20 minutes ago**. |
| `find . -type f -mmin -20 -mmin +10` | Files modified **between 10 and 20 minutes ago**. |
| `find . -type f -mtime -10` | Files modified in last 10 days. |
| `find . -type f -mtime +10` | Files modified more than 10 days ago. |
| `find . -type f -maxdepth 1` | Limit search to current directory only. |
| `find . -type f -size +1k` | Files larger than 1 kilobyte. |
| `find . -empty` | Empty files. |
| `find . -perm 777` | Files with permission 777. |
| `find . -type f -iname "*.txt" -exec rm -f {} +` | Find all `.txt` files and delete them. |

---

### 🔹 Permissions & Ownership

| Command | Description |
|---------|-------------|
| `ls -l names.txt` | Show detailed file info, including permissions. |
| `chmod u=rwx,g=rw,o=x names.txt` | Set custom permissions for owner, group, others. |
| `chmod 777 cars.txt` | Full read/write/execute for all. |
| `chmod 055 cars.txt` | Only group & others can read/execute, owner has none. |
| `chmod 500 cars.txt` | Owner can read/execute, others none. |
| `whoami` | Show current username. |
| `sudo chown root names.txt` | Change file owner to `root`. |
| `find . -perm 777` | Find all files with 777 permission. |

---

### 🔹 Searching with `grep`

| Command | Description |
|---------|-------------|
| `grep "berlin" cities.txt` | Search for “berlin” in file. |
| `grep -w "Washington" cities.txt` | Search **whole word only**. |
| `grep -i "berlin" cities.txt` | Case-insensitive search. |
| `grep -n "berlin" cities.txt` | Show line numbers with matches. |
| `grep -win "berlin" cities.txt` | Whole word, case-insensitive, with line numbers. |
| `grep -B 3 "mul" cities.txt` | Show 3 lines **before** match. |
| `grep -win "mul" ./*` | Search multiple files. |
| `grep -rwin "mul" .` | Recursive, whole word, case-insensitive. |
| `grep -rwic "mul" cities.txt` | Count matches recursively, case-insensitive. |
| `history \| grep "ls"` | Search command history for “ls”. |

---

### 🔹 Shortcuts (Keyboard)

| Shortcut | Function |
|----------|---------|
| `Ctrl + A` | Go to beginning of line. |
| `Ctrl + E` | Go to end of line. |
| `Ctrl + K` | Delete from cursor to end of line. |
| `Ctrl + U` | Delete from cursor to beginning. |
| `Tab` | Auto-complete file or directory names. |
| `Arrow Up` | Previous command. |
| `Arrow Down` | Next command. |
| `Ctrl + R` | Reverse search in history. |
| `Ctrl + L` | Clear screen. |

---

### 🔹 Command Execution & Chaining

| Command | Description |
|---------|-------------|
| `!361` | Re-run command by history ID. |
| `!command_name` | Re-run last occurrence of a command. |
| `echo "hello"; echo "how are you"` | Execute multiple commands sequentially. |
| `echo "one" && echo "two"` | Run second only if first succeeds. |
| `invalid_command || valid_command` | Run second only if first fails. |

---

### 🔹 Sorting & Processing Files

| Command | Description |
|---------|-------------|
| `sort -n numbers.txt` | Sort numerically. |
| `sort names.txt` | Sort alphabetically. |
| `sort -r names.txt` | Reverse sort. |
| `sort -f names.txt` | Case-insensitive sort. |

---

### 🔹 Processes & Background Jobs

| Command | Description |
|---------|-------------|
| `jobs` | Show processes started by the shell. |
| `ping google.com` | Send ICMP packets to test network. |
| `ping google.com &` | Run ping in background. |
| `top` | Show active processes in real-time. |
| `kill processId` | Terminate process by ID. |
| `ps aux` | List all running processes. |

---

### 🔹 System Info & Networking

| Command | Description |
|---------|-------------|
| `uname` | Show system information. |
| `uname -o` | OS name. |
| `uname -m` | Machine architecture. |
| `uname -r` | Kernel version. |
| `hostname` | Show hostname. |
| `hostname -i` | Show IP address. |
| `id` | Show user ID and groups. |
| `id -g` | Primary group ID. |
| `id -G` | All group IDs. |
| `id -ru` | Real user ID. |
| `id username` | Show info for specified user. |
| `getent passwd username` | Show passwd info of user. |
| `getent group username` | Show group info of user. |
| `lsof` | List open files. |
| `nslookup google.com` | Resolve domain to IP. |
| `netstat` | Show network connections. |
| `cut -c 1-2 names.txt` | Extract characters from columns 1-2. |

---

### 🔹 Archiving & Compression

| Command | Description |
|---------|-------------|
| `zip file.zip names.txt` | Create zip archive. |
| `zip twos.zip name1.txt names2.txt` | Zip multiple files. |
| `unzip twos.zip` | Extract files from zip archive. |

---

### 🔹 User Management

| Command | Description |
|---------|-------------|
| `sudo useradd username` | Create new user. |
| `sudo passwd username` | Set/change user password. |
| `sudo userdel username` | Delete user account. |

---

### 🔹 System Monitoring

| Command | Description |
|---------|-------------|
| `cat /etc/os-release` | Show OS release info. |
| `lscpu` | CPU architecture & cores. |
| `free -h` | Memory usage in human-readable form. |
| `vmstat` | System performance statistics. |
| `vmstat -S m` | Memory stats in megabytes. |

---

## 🧠 Important Notes

* Use `chmod` & `chown` carefully — affects security.  
* `grep -w` vs `grep` → whole word match vs substring match.  
* Background processes (`&`) must be managed with `kill` or `jobs`.  
* `history` and shortcuts make terminal usage efficient.  
* `find` is extremely versatile for searching by **name, type, size, time, permissions**.  

---

## 🚀 Learning Progress

* ![x](https://img.shields.io/badge/Basic%20Commands-blue) Basic Commands  
* ![x](https://img.shields.io/badge/Navigation-blue) Navigation  
* ![x](https://img.shields.io/badge/File%20%26%20Directory%20Management-blue) File & Directory Management  
* ![x](https://img.shields.io/badge/File%20Viewing%20%26%20Writing-blue) File Viewing & Writing  
* ![x](https://img.shields.io/badge/Environment%20Variables-blue) Environment Variables  
* ![x](https://img.shields.io/badge/Aliases-blue) Aliases  
* ![x](https://img.shields.io/badge/Utilities-blue) Utilities  
* ![x](https://img.shields.io/badge/Permissions-blue) Permissions  
* ![x](https://img.shields.io/badge/Processes-blue) Processes  
* ![x](https://img.shields.io/badge/Networking-blue) Networking  
* ![x](https://img.shields.io/badge/Shell%20Scripting-blue) Shell Scripting  
* ![x](https://img.shields.io/badge/File%20Search%20%26%20Filtering-blue) File Search & Filtering  
* ![x](https://img.shields.io/badge/Permissions%20%26%20Ownership-blue) Permissions & Ownership  
* ![x](https://img.shields.io/badge/Searching%20with%20grep-blue) Searching with grep  
* ![x](https://img.shields.io/badge/Shortcuts%20%26%20Keyboard%20Efficiency-blue) Shortcuts & Keyboard Efficiency  
* ![x](https://img.shields.io/badge/Command%20Execution%20%26%20Chaining-blue) Command Execution & Chaining  
* ![x](https://img.shields.io/badge/Sorting%20%26%20File%20Processing-blue) Sorting & File Processing  
* ![x](https://img.shields.io/badge/Processes%20%26%20Background%20Jobs-blue) Processes & Background Jobs  
* ![x](https://img.shields.io/badge/System%20Info%20%26%20Networking-blue) System Info & Networking  
* ![x](https://img.shields.io/badge/Archiving%20%26%20Compression-blue) Archiving & Compression  
* ![x](https://img.shields.io/badge/User%20Management-blue) User Management  
* ![x](https://img.shields.io/badge/System%20Monitoring-blue) System Monitoring  

---

<div align="center">

⭐ **echo "Done with Linux"**

</div>