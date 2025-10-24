# Assignment on Basic Linux Commands

**Student:** Kanishka Anand
**Roll Number:** 24122016

## Objective
To gain practical understanding of essential Linux commands for file management, system navigation, user and process handling, and system information retrieval.

---

## Part A: File and Directory Management

### 1. Directory Structure Creation

| Command | Output/Explanation |
| :--- | :--- |
| `$ pwd` | `/home/ubuntu` |
| `$ mkdir LinuxAssignment` | Creates the main directory. |
| `$ cd ./LinuxAssignment` | Changes to the new directory.|
| `$ mkdir docs data scripts` | Creates the three subdirectories. |
| `$ ls` | **Output:** `data docs scripts` (Confirms directory creation). |

### 2. File Creation and Content

| Command | Output/Explanation |
| :--- | :--- |
| `$ cd docs` | Changes the current directory to `docs/` . |
| `$ touch intro.txt commands.txt summary.txt` | Creates new, empty files. |
| `$ echo "Linux is an open-source operating system." > intro.txt` | Writes the string into `intro.txt` . |
| `$ echo "Common commands: ls, cd, pwd, mkdir, m" > commands.txt` | Writes the string into `commands.txt` . |
| `$ echo "This is a summary of Linux basics." > summary.txt` | Writes the string into `summary.txt` . |

### 3. Display Contents and Word Count

| Command | Output/Explanation |
| :--- | :--- |
| `$ cat intro.txt` | Displays the content . |
| `$ wc intro.txt commands.txt summary.txt` | Displays line count, word count, and byte count for the files. |

### 4. Copying and Renaming

| Command | Output/Explanation |
| :--- | :--- |
| `$ cp *.txt ../data/` | Copies all files ending in `.txt` to the `data/` subdirectory in the parent directory (`..`). |
| `$ cd ../data` | Changes the directory to `data/` . |
| `$ mv summary.txt overview.txt` | Renames `summary.txt` to `overview.txt` . |

### 5. Compression

| Command | Output/Explanation |
| :--- | :--- |
| `$ tar -czvf data_backup.tar.gz data/` | Compresses the `data/` folder into a gzipped tar archive (`.tar.gz`) . |

---

## Part B: System Navigation & Permissions

### 1. Current Directory and Home Path

| Command | Output/Explanation |
| :--- | :--- |
| `$ pwd` | Displays the current working directory. |
| `$ echo $HOME` | Displays the path to the home directory. |

### 2. File Permissions

| Command | Output/Explanation |
| :--- | :--- |
| `$ chmod 600 summary.txt` | Changes permissions so only the owner can read/write . |
| `$ ls -l summary.txt` | Lists file details to show the new permissions (`-rw-------`). |

### 3. User Management

| Command | Output/Explanation |
| :--- | :--- |
| `$ sudo adduser testuser` | Creates a new user account named `testuser` . |

### 4. Logged-in Users and Command History

| Command | Output/Explanation |
| :--- | :--- |
| `$ who` | Displays a list of users currently logged in . |
| `$ w` | Displays users logged in and what they are doing. |
| `$ history \| tail -n 10` | Displays the 10 most recent commands executed. |

---

## Part C: Process and System Monitoring

### 1. System Time and Uptime

| Command | Output/Explanation |
| :--- | :--- |
| `$ date` | Displays the current system date and time. |
| `$ uptime` | Displays how long the system has been running. |

### 2. Running Processes

| Command | Output/Explanation |
| :--- | :--- |
| `$ ps` | Displays a snapshot of the current processes . |
| `$ top` | Displays a dynamic, real-time view of running processes and system resources. |

### 3. Finding a Process ID (PID)

| Command | Output/Explanation |
| :--- | :--- |
| `$ pgrep bash` | Finds and prints the Process ID (PID) of the `bash` process. |

### 4. Killing a Process

| Command | Output/Explanation |
| :--- | :--- |
| `$ sleep 100 &` | Starts a `sleep` process in the background (dummy process). |
| `$ kill <PID>` | Terminates the process using its PID. |

### 5. System Resources

| Command | Output/Explanation |
| :--- | :--- |
| `$ free -h` | Displays used and free memory/swap in a human-readable format. |
| `$ top` | Used again for CPU and memory utilization. |

---

## Part D: Searching, Filtering & Redirection

### 1. Searching with `grep`

| Command | Output/Explanation |
| :--- | :--- |
| `$ grep 'Linux' intro.txt` | Searches for the word "Linux" in `intro.txt`. |

### 2. Locating Files with `find`

| Command | Output/Explanation |
| :--- | :--- |
| `$ find ~/LinuxAssignment -name '*.txt'` | Locates all files ending in `.txt` within the `LinuxAssignment` directory. |

### 3. Displaying File Head/Tail

| Command | Output/Explanation |
| :--- | :--- |
| `$ head -n 5 intro.txt` | Displays the first 5 lines of `intro.txt` . |
| `$ tail -n 3 intro.txt` | Displays the last 3 lines of `intro.txt` . |

### 4. Sorting

| Command | Output/Explanation |
| :--- | :--- |
| `$ sort names.txt` | Sorts the lines in ascending order. |
| `$ sort -r names.txt` | Sorts the lines in reverse (descending) order. |

### 5. Combining Files with Redirection

| Command | Output/Explanation |
| :--- | :--- |
| `$ cat file1.txt file2.txt > combined.txt` | Concatenates the contents of `file1.txt` and `file2.txt` and redirects the output to `combined.txt` . |

---

## Bonus Task: Simple Bash Script

**File:** `info.sh`

```bash
# Script Content:
echo "Current User: $(whoami)"
echo "Date & Time: $(date)"
echo "System Uptime: $(uptime)"
echo "Running Processes: $(ps | wc -l)"
