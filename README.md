# DevOps with AWS Challenge 2

**Linux Terminal Challenge for Students**

### Overview
This challenge is designed to help you become comfortable with fundamental Linux terminal commands. The activity is split into a walkthrough phase where we go through several commands step-by-step, and a challenge phase where you need to apply your new knowledge to solve real tasks.

All of these commands should be run from a container:
```
docker container run -it ubuntu:latest /bin/bash
```

**Total Time**: 50-60 minutes

- **Walkthrough Phase**: 30-40 minutes
- **Challenge Phase**: 10-15 minutes

### Walkthrough Phase (30-40 minutes)
We will cover the following commands step-by-step, focusing on understanding what each command does and practicing using them in simple scenarios.

1. **Navigating the Filesystem**
   - **Commands**: `pwd`, `cd`, `ls`
   - **Exercise**: Start in the home directory. Use `pwd` to see where you are, `ls` to list its contents, and `cd` to explore different directories (e.g., `cd /etc` and then back to home using `cd ~`).

2. **Working with Files and Directories**
   - **Commands**: `mkdir`, `touch`, `cp`, `mv`, `rm`
   - **Exercise**: Create a directory called `test_folder` with `mkdir`, then use `touch` to create an empty file named `example.txt` inside it. Copy `example.txt` to a new file called `example_copy.txt` with `cp`, rename `example_copy.txt` to `renamed_example.txt` with `mv`, and finally delete the file using `rm`.

3. **Viewing File Content**
   - **Commands**: `cat`, `less`, `more`
   - **Exercise**: Use `cat` to display the content of `/etc/hostname` or another small text file. Use `less` or `more` to explore larger files (e.g., `/var/log/syslog`, `/var/log/dmesg`, or `/var/log/bootstrap.log`).

4. **Finding and Searching**
   - **Commands**: `find`, `grep`
   - **Exercise**: Use `find` to locate a file by name (e.g., `find / -name example.txt`). Use `grep` to search for a specific string within a file (e.g., `grep "root" /etc/passwd`).
   - **TRICK**: Sometimes `find` is very noisy and will return ***a lot*** of entries of the things it checks, especially when you're not root. To avoid displaying all the locations that `example.txt` doesn't exist or that you don't have permission to access you can add `2>/dev/null` to the end of the command to only display the matches instead of errors.

5. **Editing Files**
   - **Commands**: `nano`
   - **Exercise**: Open `example.txt` with `nano`, add some text, save the changes, and exit (`Ctrl + O` to save, `Ctrl + X` to exit).

6. **Process Management and System Control**
   - **Commands**: `top`, `ps`, `kill`, `poweroff`
   - **Exercise**: Use `top` to monitor system processes. Use `ps aux` to list all running processes, identify a process, and use `kill` to stop it (use `kill <process_id>`).

7. **Package Management**
   - **Commands**: `apt`, `yum`
   - **Exercise**: Use `apt update` or `yum update` to update package lists (depending on the system type) and to install the `net-tools` package.
   - **BONUS**: Use `apt` with the `&&` to combine updating the packages and installing the `net-tools` package all in one command, i.e. only hit enter once.

8. **Permissions**
   - **Commands**: `chmod`
   - **Exercise**: Create a file called `secret.txt` and change its permissions to be read-only for everyone (`chmod 444 secret.txt`).

9. **Accessing Manual Pages**
   - **Commands**: `man`
   - **Exercise**: Use `man` to access the manual page for any command you are unfamiliar with (e.g., `man ls`). Practice finding out what different options do for commands like `ls` and `grep`.


### Challenge Phase (10-15 minutes)
Now that we've gone through these commands, it's your turn to complete a small challenge using what you've learned.

**Challenge Task**:
1. **Create a Directory and a File**
   - Create a directory called `project` inside your home directory.
   - Inside `project`, create a file called `notes.txt`.

2. **Edit and Move Files**
   - Open `notes.txt` with `nano` and add the line: "This is my first Linux project!"
   - Save and exit the editor.
   - Move `notes.txt` to the `/tmp` directory.

3. **Find and Copy the File**
   - Use `find` to locate `notes.txt` in `/tmp`.
   - Copy `notes.txt` back to your `project` directory.

4. **Change File Permissions**
   - Change the permissions of `notes.txt` so that only the owner can read and write, but not execute (`chmod 600 notes.txt`).

5. **Bonus Challenge (Optional)**
   - **Process Hunting**: Start a process in the background by running `sleep 300 &`. List all currently running processes using `ps` and try to identify the process ID of the `sleep` command. Once found, use `kill` to terminate the `sleep` process.
   - **Network Configuration**: Use `ifconfig` or `ip a` to find the network interface information. Identify the IP address assigned to your system and make a note of it.
   - Use `echo` to append "Completed the Linux challenge!" to `notes.txt`.

**Expected Outcome**: By the end of this challenge, you should have a directory called `project` with a file `notes.txt` that contains your notes and has restricted permissions. You should also feel more comfortable using basic Linux terminal commands.

### Wrap-Up (5 minutes)
After completing the challenge, please mark down the answers to the following in your notes for later review, and optionally if you're comfortable with it then please share the following in class:
- **What did you find easy?**
- **What was challenging?**
- **How do you think you can use these commands in real-world scenarios?**

These skills are the building blocks for using Linux in a DevOps environment—whether for automating tasks, managing servers, or configuring software environments.

