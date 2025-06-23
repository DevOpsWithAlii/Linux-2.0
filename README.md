# Linux-2.0


**Title: Part 1, All Types of Linux Commands Explained – Full Beginner’s Guide to Mastering the Linux CLI**

---

**🎧 Introduction**


Today, we’re diving into the world of **Linux commands**. If you’ve ever felt intimidated by the Linux terminal, don’t worry—you’re not alone. In this notes, we’ll break down **all the essential types of Linux commands** in a way that’s simple, clear, and perfect for beginners.

Whether you're preparing for your first IT job, a DevOps role, or just trying to improve your Linux skills, this guide will walk you through the **most important commands** step by step.

So grab a notebook, and let’s get started!

---

## 🧱 SECTION 1: What Is the Linux Command Line?

Before we start typing commands, let’s understand what the command line actually is.

The Linux terminal—also known as the **command line interface** or CLI—is like a conversation window where you type instructions to talk directly to your computer’s operating system.

Unlike Windows or Mac with icons and menus, Linux lets you **type everything**—and that gives you **more power, speed, and flexibility**.

> **Analogy:** Think of it like driving a manual car. It takes a bit to learn, but once you do, you have full control.

---

## 🛠️ SECTION 2: File and Directory Commands

Let’s start with the most basic and commonly used commands.

### 1. `pwd` – Print Working Directory

This tells you **where you are** in the system.

```bash
$ pwd
/home/user
```

### 2. `ls` – List Files

Lists all files and folders in the current directory.

```bash
$ ls
Documents  Downloads  Pictures
```

**Pro Tip:** Use `ls -l` to see file details, or `ls -a` to show hidden files.

### 3. `cd` – Change Directory

Moves you from one folder to another.

```bash
$ cd Documents
```

Use `cd ..` to go **one level up**.

### 4. `mkdir` – Make Directory

Creates a new folder.

```bash
$ mkdir projects
```

### 5. `touch` – Create a New File

Creates a blank file.

```bash
$ touch notes.txt
```

### 6. `rm` – Remove File or Directory

Deletes a file or folder.

```bash
$ rm oldfile.txt
```

Use `rm -r foldername` to remove a directory.

**⚠️ Warning:** No recycle bin. Once deleted, it’s gone.

### 7. `cp` – Copy Files

Copies a file or directory.

```bash
$ cp file.txt backup.txt
```

### 8. `mv` – Move or Rename Files

```bash
$ mv file.txt Documents/
$ mv oldname.txt newname.txt
```

---

## 🔍 SECTION 3: Viewing and Editing File Content

### 1. `cat` – View File Content

```bash
$ cat notes.txt
```

### 2. `more` and `less` – Paginate File Output

For long files:

```bash
$ less bigfile.txt
```

### 3. `head` and `tail` – Show Top or Bottom of File

```bash
$ head -n 10 logfile.txt
$ tail -n 10 logfile.txt
```

### 4. `nano`, `vim`, `vi` – Edit Text Files

Use `nano` for beginners:

```bash
$ nano notes.txt
```

---

## 👁️‍🗨️ SECTION 4: User and Permissions Commands

### 1. `whoami` – Shows your username

### 2. `id` – Shows user ID and group ID

### 3. `chmod` – Change file permissions

```bash
$ chmod 755 script.sh
```

### 4. `chown` – Change file ownership

```bash
$ chown user:group file.txt
```

---

## 📦 SECTION 5: Package Management Commands

### Debian-based (Ubuntu):

```bash
$ sudo apt update
$ sudo apt install nginx
$ sudo apt remove nginx
```

### RedHat-based (CentOS):

```bash
$ sudo yum install nginx
$ sudo yum remove nginx
```

---

## ⚙️ SECTION 6: Process and System Monitoring

### 1. `top` – Live view of system usage

### 2. `htop` – Advanced version of top

### 3. `ps` – List running processes

```bash
$ ps aux
```

### 4. `kill` – Kill a process

```bash
$ kill 1234
```

---

## 🌐 SECTION 7: Network Commands

### 1. `ping` – Test connectivity

```bash
$ ping google.com
```

### 2. `ifconfig` or `ip a` – View IP address

### 3. `netstat` – View network connections

### 4. `curl` – Transfer data from URLs

```bash
$ curl https://example.com
```

---

## 📁 SECTION 8: Disk and File System Commands

### 1. `df -h` – Disk usage

### 2. `du -sh foldername` – Folder size

### 3. `mount` / `umount` – Mount or unmount drives

---

## 🧹 SECTION 9: Log Files and System Info

### 1. `dmesg`, `journalctl`, `syslog` – System logs

### 2. `uname -a` – System info

### 3. `uptime` – How long the system has been running

---

## 💡 SECTION 10: Tips for Beginners

* Use `tab` to auto-complete commands
* Use `history` to see previous commands
* Use `!!` to repeat the last command
* Use `man command` to read the manual

Example:

```bash
$ man ls
```

---

## 🧠 Summary and Takeaways

Linux commands can feel overwhelming, but with practice, they become second nature.

> **Quote:** “The more you use it, the more it becomes muscle memory.”

Here’s a quick recap:

* Start with basic file and directory commands
* Learn to view and edit files
* Understand permissions and users
* Manage software with apt/yum
* Monitor processes and networks

**Keep practicing. Break things. Fix them. That’s how real learning happens.**

---


**Title: Linux Commands Part 2 & 3 – Advanced Commands, Scripting, Interview Questions & Labs**

---

**🎧 INTRODUCTION**

Hey everyone, welcome back to our Linux Command Mastery series!

In this special double episode, we’re diving deep into **Part 2 and Part 3** — that means you’re getting a full tour of **advanced Linux commands, bash scripting**, and a bonus pack of **real-world labs and interview questions**.

Whether you're aiming for a DevOps job, preparing for an exam, or just leveling up your command-line confidence — this video is for you.

Let’s jump right in.

---

## 🔧 PART 2: Advanced Linux Commands & Bash Scripting

---

### 🔍 1. Search & Filter Tools

#### a. `grep` – Global Regular Expression Print

Searches through file contents.

```bash
$ grep "error" logfile.txt
```

#### b. `awk` – Pattern scanning and processing

Extracts and processes text.

```bash
$ awk '{print $1}' file.txt
```

#### c. `sed` – Stream editor

Used to find and replace text.

```bash
$ sed 's/old/new/g' file.txt
```

#### d. `cut` – Cuts sections of each line

```bash
$ cut -d ':' -f1 /etc/passwd
```

#### e. `find` – Find files by name, type, size, etc.

```bash
$ find /home -name "*.txt"
```

#### f. `locate` – Searches faster using a pre-built index

```bash
$ locate notes.txt
```

---

### 🔗 2. Pipes, Redirection, and Chaining

#### a. Redirect output to a file

```bash
$ echo "Hello" > hello.txt
```

#### b. Append output

```bash
$ echo "World" >> hello.txt
```

#### c. Chain commands

```bash
$ mkdir test && cd test
```

#### d. Use pipe `|` to link commands

```bash
$ cat file.txt | grep "error"
```

#### e. `tee` – Show output AND write to file

```bash
$ ls -l | tee list.txt
```

---

### 📜 3. Bash Scripting Basics

#### a. Your first script

```bash
#!/bin/bash
echo "Hello, world!"
```

Save as `hello.sh`, then run:

```bash
$ chmod +x hello.sh
$ ./hello.sh
```

#### b. Variables

```bash
name="Ali"
echo "Hello $name"
```

#### c. Conditions

```bash
if [ -f "file.txt" ]; then
  echo "File exists"
fi
```

#### d. Loops

```bash
for i in 1 2 3; do
  echo "Number $i"
done
```

#### e. Arguments

```bash
#!/bin/bash
echo "First arg: $1"
```

---

### 🔄 4. Useful Script Examples

#### a. Backup script

```bash
#!/bin/bash
tar -czvf backup_$(date +%F).tar.gz /home/user
```

#### b. User check script

```bash
#!/bin/bash
if id "$1" &>/dev/null; then
  echo "User exists."
else
  echo "User not found."
fi
```

#### c. Service monitor script

```bash
#!/bin/bash
if systemctl is-active apache2; then
  echo "Apache is running."
else
  echo "Restarting Apache..."
  systemctl restart apache2
fi
```

---

## 🧪 PART 4: Interview Questions, Labs & Projects

---

### ❓ 1. Linux Interview Questions (with examples)

#### Q1. How do you find large files in a directory?

```bash
$ find / -type f -size +100M
```

#### Q2. How do you schedule a job?

```bash
$ crontab -e
```

Add:

```bash
0 5 * * * /home/user/backup.sh
```

#### Q3. Difference between `hard link` and `soft link`?

* Hard Link: Points directly to the file inode.
* Soft Link: A shortcut (like in Windows).

#### Q4. How do you check disk usage?

```bash
$ df -h
$ du -sh *
```

#### Q5. How do you monitor memory?

```bash
$ free -m
```

---

### 🔬 2. Real-Life Practice Labs

#### Lab 1: Create a user and give them sudo access

```bash
$ adduser devuser
$ usermod -aG sudo devuser
```

#### Lab 2: Write a script to archive logs

```bash
#!/bin/bash
tar -czf logs_$(date +%F).tar.gz /var/log/*.log
```

#### Lab 3: Setup a cron job to clear temp folder daily

```bash
$ crontab -e
```

```bash
0 2 * * * rm -rf /tmp/*
```

---

### 🧩 3. Mini Projects

#### Project 1: Disk Usage Alert Script

Sends alert email if disk > 80%

#### Project 2: Health Check Script

* Checks CPU, memory, disk
* Logs report to a file
* Sends warning if thresholds exceed

#### Project 3: Automated Backup System

* Compresses files
* Stores by date
* Runs daily with cron

---

### 🧠 Final Takeaways

* Practice by building things
* Break things. Fix them.
* Read logs. Explore man pages.
* Interview prep = daily command use + scripting

> **Quote:** "Linux is not just an OS. It's a toolset. Learn to wield it."

---

Until next time, keep practicing and keep mastering the terminal.

**🙏 Closing Message**

Thanks so much for watching!

If this notes helped you, leave a like, drop a comment, and don’t forget to subscribe for more tutorials on Linux, DevOps, AWS, and cloud computing.

Until next time, keep learning and keep building.

