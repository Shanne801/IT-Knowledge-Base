# Linux CLI Fundamentals Cheat Sheet

## Directory & File Operations
* `pwd` - Print absolute working directory path.
* `ls -la` - List all files and directories (including hidden) with detailed attributes.
* `cd [path]` - Change directory.
* `mkdir [dir_name]` - Create a new directory.
* `rmdir [dir_name]` - Remove an empty directory.
* `touch [filename]` - Create an empty file or update file timestamps.
* `cp [source] [destination]` - Copy files or directories.
* `mv [source] [destination]` - Move or rename files.
* `rm [filename]` - Remove/delete a file.

## File Viewing & Text Editing
* `cat [filename]` - Display full contents of a file.
* `less [filename]` - View file content page by page.
* `head -n 10 [filename]` - Output the first 10 lines of a file.
* `tail -f /var/log/syslog` - Output appended data in real-time (essential for log monitoring).
* `nano [filename]` - Terminal-based text editor for quick file creation and modifications.

## System & Memory Monitoring
* `uname -a` - Display system and kernel information.
* `free -h` - Display total, used, and available memory (RAM and Swap) in human-readable format.
* `free -m` - Display memory usage in Megabytes.
* `free -h -t` - Display memory usage with a total line including buffer/cache.
* `top` - Display real-time dynamic view of running processes, CPU, and RAM usage (Press `q` to quit).
* `top -b -n 1 > system_snapshot.txt` - Run `top` in batch mode for a single iteration and redirect output to a file.

> **Key Memory Concepts:**
> * **Swap:** Secondary storage partition used by the OS as an extension of physical RAM.
> * **available:** Estimated memory available for launching new applications without swapping.

## Process Management & Networking
* `ps aux` - List all running processes with user and PID details.
* `ip a` / `ifconfig` - Display network interfaces and IP addresses.
* `ping -c 4 [host]` - Send 4 ICMP ECHO_REQUEST packets to test reachability.
* `systemctl status [service]` - Check status of a system service (e.g., ssh, nginx).

## File Permissions & Ownership
* `chmod 755 [filename]` - Change file permissions (Read/Write/Execute).
* `chown [user]:[group] [filename]` - Change file owner and group.
