Linux Commands – Documentation

1. Finding Files and Paths
whereis python3
which python3
View the current PATH:

echo $PATH

2. File and Directory Operations
pwd                # Print working directory
ls -a              # List all files including hidden
ls -l              # Long listing (permissions, size)
ls -al             # All files with detailed view
ls -R              # Recursive directory listing
cd                 # Change directory
mkdir directory    # Create a directory
open .             # Open current directory (macOS)

3. Viewing and Transforming Files
cat file.txt                   # View file content
cat file.txt | tr a-z A-Z > upper.txt   # Convert content to uppercase

4. Environment Variables

Set an environment variable temporarily:

export MY_PATH="Asvith"
echo $MY_PATH

5. File Permissions and Ownership
Permission Values

Read (r) = 4

Write (w) = 2

Execute (x) = 1

User Categories

u — user

g — group

o — others

Viewing Permissions
ls -l file.txt

Changing Permissions
chmod u=rwx,g=rx,o=r file.txt
chmod 764 file.txt

Changing Ownership
sudo chown root file.txt

Finding Files with Specific Permissions
find . -perm 777

Executing Commands on Found Files
find . -type f -name "*.txt" -exec rm -rf {} +

6. Searching Files (grep)

Basic usage:

grep "text" file.txt
grep -i "text" file.txt        # Case insensitive
grep -w "John Doe" file.txt    # Whole word
grep -n "text" file.txt        # Line numbers
grep -c "pattern" file.txt     # Count matches


Search multiple files:

grep -win "pattern" ./*.txt
grep -rwin "pattern" .

7. Disk and File System Usage
df        # Disk usage in KB
df -m     # Disk usage in MB
df -h     # Human readable
df -hg    # Human readable (GB)
du        # Disk usage statistics

8. System Monitoring
top            # Running processes
ps aux         # Process listing
kill <pid>     # Kill a process
htop           # Interactive process viewer
free           # Memory usage
free -h        # Human readable memory usage
vmstat         # Virtual memory statistics
lscpu          # CPU information

9. Networking
hostname
hostname -i        # Device IP address
nslookup google.com
netstat            # View open/listening ports
ifconfig
ping google.com &
ping vercel.com &

10. User and Group Management
useradd User
passwd User        # Set user password
userdel User
id                 # User identity information
id -g              # Primary group ID
id -G              # All group IDs
id -r              # Real IDs
getent group User
getent passwd User

11. Command History
history | grep "ls"

12. Operators
cmd1 && cmd2    # Run cmd2 only if cmd1 succeeds
cmd1 || cmd2    # Run cmd2 only if cmd1 fails
cmd &           # Run in background


Example:

echo "first" && echo "second"
