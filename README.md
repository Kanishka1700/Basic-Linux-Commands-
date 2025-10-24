# Assignment on Basic Linux Commands

**Student:** Kanishka Anand
**Roll Number:** 24122016

## Objective
[cite_start]To gain practical understanding of essential Linux commands for file management, system navigation, user and process handling, and system information retrieval[cite: 3, 4].

---

## Part A: File and Directory Management

### 1. Directory Structure Creation

| Command | Output/Explanation |
| :--- | :--- |
| `$ pwd` | `/home/ubuntu` |
| `$ mkdir LinuxAssignment` | Creates the main directory. |
| `$ cd ./LinuxAssignment` | [cite_start]Changes to the new directory. [cite: 6, 9] |
| `$ mkdir docs data scripts` | [cite_start]Creates the three subdirectories[cite: 6]. |
| `$ ls` | [cite_start]**Output:** `data docs scripts` (Confirms directory creation) [cite: 6] |

### 2. File Creation and Content

| Command | Output/Explanation |
| :--- | :--- |
| `$ cd docs` | [cite_start]Changes the current directory to `docs/`[cite: 13]. |
| `$ touch intro.txt commands.txt summary.txt` | [cite_start]Creates new, empty files[cite: 11, 14]. |
| `$ echo "Linux is an open-source operating system." > intro.txt` | [cite_start]Writes the string into `intro.txt`[cite: 16, 18]. |
| `$ echo "Common commands: ls, cd, pwd, mkdir, m" > commands.txt` | [cite_start]Writes the string into `commands.txt`[cite: 16, 19]. |
| `$ echo "This is a summary of Linux basics." > summary.txt` | [cite_start]Writes the string into `summary.txt`[cite: 16, 20]. |

### 3. Display Contents and Word Count

| Command | Output/Explanation |
| :--- | :--- |
| `$ cat intro.txt` | [cite_start]Displays the content[cite: 21, 23]. |
| `$ wc intro.txt commands.txt summary.txt` | [cite_start]Displays line count, word count, and byte count for the files[cite: 21, 26]. |

### 4. Copying and Renaming

| Command | Output/Explanation |
| :--- | :--- |
| `$ cp *.txt ../data/` | [cite_start]Copies all files ending in `.txt` to the `data/` subdirectory in the parent directory (`..`)[cite: 27, 29]. |
| `$ cd ../data` | [cite_start]Changes the directory to `data/`[cite: 30]. |
| `$ mv summary.txt overview.txt` | [cite_start]Renames `summary.txt` to `overview.txt`[cite: 27, 31]. |

### 5. Compression

| Command | Output/Explanation |
| :--- | :--- |
| `$ tar -czvf data_backup.tar.gz data/` | [cite_start]Compresses the `data/` folder into a gzipped tar archive (`.tar.gz`)[cite: 32, 34]. |

---

## Part B: System Navigation & Permissions

### 1. Current Directory and Home Path

| Command | Output/Explanation |
| :--- | :--- |
| `$ pwd` | [cite_start]Displays the current working directory[cite: 36, 38]. |
| `$ echo $HOME` | [cite_start]Displays the path to the home directory[cite: 36, 39]. |

### 2. File Permissions

| Command | Output/Explanation |
| :--- | :--- |
| `$ chmod 600 summary.txt` | [cite_start]Changes permissions so only the owner can read/write[cite: 40, 42]. |
| `$ ls -l summary.txt` | [cite_start]Lists file details to show the new permissions (`-rw-------`)[cite: 43]. |

### 3. User Management

| Command | Output/Explanation |
| :--- | :--- |
| `$ sudo adduser testuser` | [cite_start]Creates a new user account named `testuser`[cite: 44, 46]. |

### 4. Logged-in Users and Command History

| Command | Output/Explanation |
| :--- | :--- |
| `$ who` | [cite_start]Displays a list of users currently logged in[cite: 47, 49]. |
| `$ w` | [cite_start]Displays users logged in and what they are doing[cite: 47, 50]. |
| `$ history \| tail -n 10` | [cite_start]Displays the 10 most recent commands executed[cite: 51, 53]. |

---

## Part C: Process and System Monitoring

### 1. System Time and Uptime

| Command | Output/Explanation |
| :--- | :--- |
| `$ date` | [cite_start]Displays the current system date and time[cite: 55, 57]. |
| `$ uptime` | [cite_start]Displays how long the system has been running[cite: 55, 58]. |

### 2. Running Processes

| Command | Output/Explanation |
| :--- | :--- |
| `$ ps` | [cite_start]Displays a snapshot of the current processes[cite: 59, 61]. |
| `$ top` | [cite_start]Displays a dynamic, real-time view of running processes and system resources[cite: 59, 62]. |

### 3. Finding a Process ID (PID)

| Command | Output/Explanation |
| :--- | :--- |
| `$ pgrep bash` | [cite_start]Finds and prints the Process ID (PID) of the `bash` process[cite: 64, 66]. |

### 4. Killing a Process

| Command | Output/Explanation |
| :--- | :--- |
| `$ sleep 100 &` | [cite_start]Starts a `sleep` process in the background (dummy process)[cite: 69]. |
| `$ kill <PID>` | [cite_start]Terminates the process using its PID[cite: 67]. |

### 5. System Resources

| Command | Output/Explanation |
| :--- | :--- |
| `$ free -h` | [cite_start]Displays used and free memory/swap in a human-readable format[cite: 71, 73]. |
| `$ top` | [cite_start]Used again for CPU and memory utilization[cite: 74]. |

---

## Part D: Searching, Filtering & Redirection

### 1. Searching with `grep`

| Command | Output/Explanation |
| :--- | :--- |
| `$ grep 'Linux' intro.txt` | [cite_start]Searches for the word "Linux" in `intro.txt`[cite: 76, 78]. |

### 2. Locating Files with `find`

| Command | Output/Explanation |
| :--- | :--- |
| `$ find ~/LinuxAssignment -name '*.txt'` | [cite_start]Locates all files ending in `.txt` within the `LinuxAssignment` directory[cite: 79, 81]. |

### 3. Displaying File Head/Tail

| Command | Output/Explanation |
| :--- | :--- |
| `$ head -n 5 intro.txt` | [cite_start]Displays the first 5 lines of `intro.txt`[cite: 82, 84]. |
| `$ tail -n 3 intro.txt` | [cite_start]Displays the last 3 lines of `intro.txt`[cite: 82, 85]. |

### 4. Sorting

| Command | Output/Explanation |
| :--- | :--- |
| `$ sort names.txt` | [cite_start]Sorts the lines in ascending order[cite: 86, 88]. |
| `$ sort -r names.txt` | [cite_start]Sorts the lines in reverse (descending) order[cite: 86, 89]. |

### 5. Combining Files with Redirection

| Command | Output/Explanation |
| :--- | :--- |
| `$ cat file1.txt file2.txt > combined.txt` | [cite_start]Concatenates the contents of `file1.txt` and `file2.txt` and redirects the output to `combined.txt`[cite: 90, 92]. |

---

## Bonus Task: Simple Bash Script

**File:** `info.sh`

```bash
# Script Content:
echo "Current User: $(whoami)"
echo "Date & Time: $(date)"
echo "System Uptime: $(uptime)"
echo "Running Processes: $(ps | wc -l)"
