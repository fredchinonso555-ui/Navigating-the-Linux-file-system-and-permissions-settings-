Linux Filesystem and Permissions — Command Reference

1. Filesystem Exploration

lsblk
mount
mount | grep sda1
cd /
ls -l

2. Directory Navigation

cd ~
pwd
ls -la
mkdir second_drive
ls -l second_drive/

3. Mounting and Unmounting

sudo mount /dev/sdb1 ~/second_drive/
mount | grep /dev/sd
ls -l second_drive/
sudo umount /dev/sdb1

4. File Permissions

ls -l
ls -ld /mnt
touch /mnt/myNewFile.txt
sudo chmod 665 myFile.txt
sudo chmod 777 myFile.txt

5. File Ownership

sudo chown analyst myFile.txt
sudo chown analyst:analyst myFile.txt

6. File Operations

echo test >> myFile.txt
cat myFile.txt

7. Symbolic Links and Hard Links

echo "symbolic" > file1.txt
echo "hard" > file2.txt

ln -s file1.txt file1symbolic
ln file2.txt file2hard

ls -l

mv file1.txt file1new.txt
mv file2.txt file2new.txt

cat file1symbolic
cat file2hard

8. Additional Useful Commands

Command| Purpose
"df -h"| Displays disk space usage
"findmnt"| Displays mounted filesystems
"readlink"| Displays symbolic link targets
"stat"| Displays file information
"file"| Identifies file types
"id"| Displays user and group information

Security Note

The "chmod 777" command grants everyone full permissions. It is included because the lab asks about it, but should not be used carelessly on real systems.
