# Operating Systems & Terminal Fundamentals

## 1. Operating System Concepts

### What is an Operating System?
An Operating System (OS) manages hardware resources and provides services to applications. It acts as an intermediary between users/programs and computer hardware.

### Core Responsibilities
- **Process Management**: Creates, schedules, and terminates processes
- **Memory Management**: Allocates RAM efficiently across applications
- **File Management**: Organizes and manages files on storage devices
- **Device Management**: Controls peripheral devices (printers, monitors, storage)
- **User Interface**: Provides shell (CLI) or graphical interface (GUI) for interaction

### Common Operating Systems
- **Windows**: GUI-centric, widely used for desktop/enterprise environments
- **Linux**: Open-source, server-focused, highly customizable
- **macOS**: Unix-based, used in development environments

---

## 2. File System Fundamentals

### What is a File System?
A File System (FS) is a structured method of organizing, storing, and retrieving files on a storage device.

### Key Concepts

**File Structure**
- A file is a named collection of data stored on disk
- Files have names, extensions (e.g., `.java`, `.txt`), and attributes (size, permissions, timestamp)

**Directory Structure**
- Directories (folders) are containers for files and other directories
- Create a hierarchical tree structure for organization

**Root Directory**
- **Windows**: `C:\` (represents the primary hard drive)
- **Linux/macOS**: `/` (top of the entire file system)

### File System Organization Example
```
C:\ (Windows)                    / (Linux)
├── Users/                       ├── home/
├── Program Files/               ├── usr/
├── Windows/                     ├── var/
└── Documents/                   └── etc/
```

---

## 3. Absolute vs. Relative Paths

### Absolute Paths
An **absolute path** specifies the complete location of a file from the root directory.

**Characteristics:**
- Starts from the root (`C:\` on Windows, `/` on Linux)
- Same regardless of current location
- Unambiguous and explicit

**Examples:**

| OS | Example |
|---|---|
| **Windows** | `C:\Users\komshor\Documents\project\Main.java` |
| **Linux** | `/home/komshor/documents/project/Main.java` |

### Relative Paths
A **relative path** specifies the location of a file relative to the current working directory.

**Characteristics:**
- Does not start from root
- Changes meaning based on current directory
- More concise for nearby files
- Uses special symbols: `.` (current dir), `..` (parent dir)

**Examples:**

| Scenario | Path | Meaning |
|---|---|---|
| Current file in same directory | `Main.java` | Current directory |
| File in subdirectory | `src/Main.java` | Subdirectory of current location |
| Parent directory | `../config.xml` | One level up |
| Sibling directory | `../resources/data.txt` | Sibling folder's file |

**When to Use:**
- **Absolute**: Cross-directory navigation, scripts, configuration
- **Relative**: Within projects, portable file references

---

## 4. Windows Command Prompt (CMD)

### Accessing CMD
1. Press `Windows Key + R`
2. Type `cmd` and press Enter
3. Or search "Command Prompt" in Start menu

### Essential CMD Commands

| Command | Syntax | Purpose |
|---|---|---|
| **cd** | `cd [path]` | Change directory |
| **cd ..** | `cd ..` | Go to parent directory |
| **cd \\** | `cd \\` | Go to root directory |
| **dir** | `dir [path]` | List files and directories |
| **mkdir** | `mkdir [folder_name]` | Create a new directory |
| **rmdir** | `rmdir [folder_name]` | Delete an empty directory |
| **del** | `del [file_name]` | Delete a file |
| **copy** | `copy [source] [destination]` | Copy files |
| **move** | `move [source] [destination]` | Move/rename files |
| **type** | `type [file_name]` | Display file contents |
| **cls** | `cls` | Clear screen |
| **echo** | `echo [text]` | Print text to console |
| **where** | `where [program_name]` | Locate a program or file |
| **cd** (no args) | `cd` | Display current directory |

### CMD Usage Examples
```cmd
C:\Users\komshor> cd Documents
C:\Users\komshor\Documents> mkdir JavaProject
C:\Users\komshor\Documents> cd JavaProject
C:\Users\komshor\Documents\JavaProject> dir
C:\Users\komshor\Documents\JavaProject> echo Hello > notes.txt
C:\Users\komshor\Documents\JavaProject> type notes.txt
```

---

## 5. Linux Shell (Bash)

### Accessing the Shell
- Open Terminal application
- Or press `Ctrl + Alt + T` on many Linux distributions

### Essential Bash Commands

| Command | Syntax | Purpose |
|---|---|---|
| **pwd** | `pwd` | Print working directory (show current location) |
| **cd** | `cd [path]` | Change directory |
| **cd ..** | `cd ..` | Go to parent directory |
| **cd ~** | `cd ~` | Go to home directory |
| **cd /** | `cd /` | Go to root directory |
| **ls** | `ls [path]` | List files and directories |
| **ls -l** | `ls -l` | List with detailed information |
| **ls -a** | `ls -a` | List including hidden files |
| **mkdir** | `mkdir [folder_name]` | Create a new directory |
| **rmdir** | `rmdir [folder_name]` | Delete an empty directory |
| **rm** | `rm [file_name]` | Delete a file |
| **cp** | `cp [source] [destination]` | Copy files |
| **mv** | `mv [source] [destination]` | Move/rename files |
| **cat** | `cat [file_name]` | Display file contents |
| **touch** | `touch [file_name]` | Create empty file or update timestamp |
| **echo** | `echo [text]` | Print text to console |
| **which** | `which [command]` | Locate a command |
| **clear** | `clear` | Clear screen |

### Bash Usage Examples
```bash
komshor@ubuntu:~$ pwd
/home/komshor

komshor@ubuntu:~$ cd Documents
komshor@ubuntu:~/Documents$ mkdir JavaProject
komshor@ubuntu:~/Documents$ cd JavaProject
komshor@ubuntu:~/Documents/JavaProject$ ls -la
komshor@ubuntu:~/Documents/JavaProject$ touch Main.java
komshor@ubuntu:~/Documents/JavaProject$ echo "Hello Java" > notes.txt
komshor@ubuntu:~/Documents/JavaProject$ cat notes.txt
```

---

## 6. Quick Reference: Path Navigation

### Directory Navigation Cheat Sheet

| Task | Windows CMD | Linux Bash |
|---|---|---|
| View current location | `cd` | `pwd` |
| Move to folder | `cd Documents` | `cd Documents` |
| Go up one level | `cd ..` | `cd ..` |
| Go to root | `cd \\` | `cd /` |
| Go to home | `cd %USERPROFILE%` | `cd ~` |
| List contents | `dir` | `ls` |
| Create folder | `mkdir NewFolder` | `mkdir NewFolder` |

---

## 7. Key Takeaways

✓ The OS manages hardware and provides services to applications  
✓ File systems organize data hierarchically using directories  
✓ **Absolute paths** start from root; **relative paths** depend on current location  
✓ Windows CMD and Linux Bash provide similar core functionality with syntax differences  
✓ Master `cd`, `ls`/`dir`, and `mkdir` first—these are foundational  
✓ Combine commands and paths to navigate efficiently in both environments  