# DevOps with AWS Challenge 2

## CHEATSHEET
**Linux Terminal Cheatsheet for Beginners**

### 1. Basics of the Terminal
- **What is a Terminal?** The terminal is a text-based interface to interact with the computer. It allows users to execute commands directly and is an essential tool in DevOps for automating tasks.
- **Basic Commands**:
  - `pwd`: Print current working directory.
  - `ls`: List files and directories in the current directory.
  - `cd <directory>`: Change to a specific directory.
  - `man <command>`: Show the manual page for a command (e.g., `man ls`).

### 2. Directory Structure
- **/ (Root Directory)**: The base of the Linux filesystem.
  - **/bin**: Essential command binaries (e.g., `ls`, `cp`).
  - **/etc**: Configuration files for the system.
  - **/home**: User home directories.
  - **/var**: Variable files like logs.
  - **/tmp**: Temporary files.
  - **/usr**: User binaries and applications.

### 3. Reading Text from a File
- **View the content** of a file:
  - `cat filename`: Print all content.
  - `less filename`: View content one page at a time.
  - `tail -n 10 filename`: Show the last 10 lines.

### 4. Reading Specific Lines from a File
- **Read a specific line** (e.g., line 5):
  - `sed -n '5p' filename`
- **Read a range of lines** (e.g., lines 5 to 10):
  - `sed -n '5,10p' filename`

### 5. Piping Commands
- **Piping**: Send the output of one command to another.
  - Example: `cat filename | grep "keyword"`
  - **Explanation**: `|` takes the output of `cat` and passes it to `grep` to search for "keyword".

### 6. Writing Text to a File
- **Overwrite a file**:
  - `echo "Hello, World!" > filename`
- **Append to a file**:
  - `echo "Another line" >> filename`

### 7. Editing Text in a File
- **Using `nano` (simple text editor)**:
  - `nano filename`: Opens the file in the Nano editor.
  - Save changes with `Ctrl + O`, exit with `Ctrl + X`.

### 8. Deleting Files
- **Delete a file**:
  - `rm filename`
- **Delete a directory and its content**:
  - `rm -r directoryname`

### 9. Changing Permissions on Files
- **Change file permissions**:
  - `chmod 755 filename`: Set read, write, execute for owner; read, execute for others.
  - **Explanation**: The `755` sets permissions in three groups (owner/group/others).

### 10. Application and Process Management
- **`which`**: Get the full path to a command's executable file.
  - Example: `which ls`
- **`yum`**: Search for, install, remove, and update packages and dependencies (Fedora, CentOS, RHEL).
  - Example: `yum install httpd`

### 11. Console and Output Management
- **`cat`**: Display file contents on the terminal.
  - Example: `cat filename`
- **`clear`**: Clear the terminal display.
  - Example: `clear`
- **`echo`**: Print text or variables in the terminal.
  - Example: `echo "Hello, World!"`
- **`top`**: Get information about running processes.
  - Example: `top`

### 12. Creating and Exporting Environment Variables
- **`env`**: Display all environment variables running on the system.
  - Example: `env`
- **`export`**: Export environment variables.
  - Example: `export MY_VAR=value`
- **`printenv`**: Print a particular environment variable to the console.
  - Example: `printenv PATH`
- **`source`**: Execute commands stored in a file from within the current shell, or refresh environment variables.
  - Example: `source ~/.bashrc`

### 13. Working with Files and Directories
- **`cd`**: Change to another directory.
  - Example: `cd /etc`
- **`cp`**: Copy the contents of the source directory or file to a target directory or file.
  - Example: `cp source.txt target.txt`
- **`find`**: Locate a file or directory by name.
  - Example: `find / -name filename`
- **`grep`**: Search for a string within an output.
  - Example: `grep "text" filename`
- **`ls`**: List the contents of a directory.
  - Example: `ls -l`
- **`mkdir`**: Create directories.
  - Example: `mkdir new_folder`
- **`more`**: View and traverse the content of a file or stdout.
  - Example: `more filename`
- **`mv`**: Move or rename files.
  - Example: `mv oldname.txt newname.txt`
- **`pwd`**: Get the name of the present working directory.
  - Example: `pwd`
- **`rm`**: Delete files or directories.
  - Example: `rm unwanted_file.txt`
- **`tar`**: Extract and compress files.
  - Example: `tar -cvf archive.tar directory`

### 14. Accessing Command-Line Help Documentation
- **`man`**: Access manual pages for all Linux commands.
  - Example: `man ls`

### 15. Working with Networks on and from a Linux Computer
- **`curl`**: Get or post a file to or from the Internet according to a URL.
  - Example: `curl http://example.com`
- **`ip`**: Gets the IP information for the physical or virtual machine.
  - Example: `ip a`
- **`netstat`**: Get information about network connections and more.
  - Example: `netstat -tuln`
- **`ssh`**: Establish a secure encrypted connection between two hosts over an insecure network.
  - Example: `ssh user@hostname`
- **`wget`**: Direct download files from the Internet.
  - Example: `wget http://example.com/file.txt`

### 16. Process Management
- **`&&`**: Execute commands in a sequence.
  - Example: `command1 && command2`
- **`kill`**: Removes a running process from memory.
  - Example: `kill 1234` (where `1234` is the process ID)
- **`ps`**: Display active processes.
  - Example: `ps aux`

### 17. System Control
- **`poweroff`**: Shut down a computer.
  - Example: `poweroff`
- **`restart`**: Restart a computer.
  - Example: `restart`

### 18. User Management
- **`whoami`**: Display the user ID.
  - Example: `whoami`

### 19. Package Management
- **Package Managers**: Tools that help you install, update, and remove software packages on Linux.
  - **`apt` (Debian/Ubuntu-based systems)**:
    - **Install a package**: `apt install package_name`
      - Example: `apt install nginx`
    - **Update package lists**: `apt update`
    - **Upgrade installed packages**: `apt upgrade`
  - **`yum` (Fedora, CentOS, RHEL)**:
    - **Install a package**: `yum install package_name`
      - Example: `yum install httpd`
    - **Remove a package**: `yum remove package_name`
    - **Update all packages**: `yum update`

### 20. How This Fits Into DevOps
- **Automation**: Terminal commands are used to write scripts for automation, reducing manual tasks.
- **Configuration Management**: Tools like `chmod` and `nano` help manage system settings and permissions, which is crucial for setting up environments.
- **Collaboration**: Understanding Linux terminal commands is key to working in cloud environments, often used in DevOps for CI/CD pipelines, server management, and troubleshooting.

### Tips for Windows Users
- **Linux vs. Windows**: The terminal is like Command Prompt or PowerShell but much more powerful for scripting and automation.
- **Practice**: Start by using a Linux terminal emulator, like WSL (Windows Subsystem for Linux), which allows you to run Linux commands on Windows.

