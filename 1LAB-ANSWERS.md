Lab Questions and Answers

PART 1: Exploring Filesystems

Question 1

What is the meaning of the output of "ls -l" in the root directory? Where are the listed files physically stored?

Answer:

The command displays files and directories located in the root filesystem. In the supplied lab example, the root filesystem is stored on the "/dev/sda1" partition.

Question 2

Why is "/dev/sdb1" not shown?

Answer:

The partition has been detected by Linux but has not yet been mounted. A filesystem must be mounted before it becomes accessible through a mount point.

Question 3

Why is the second_drive directory no longer empty after mounting?

Answer:

Mounting "/dev/sdb1" makes its filesystem accessible through the second_drive directory. The files displayed are physically stored on the "/dev/sdb1" partition.

---

PART 2: File Permissions

Question 4

Who owns cyops.mn? What is its group?

Answer:

The owner is "analyst", and the group is also "analyst".

Question 5

What does "-rw-r--r--" mean?

Answer:

The first dash indicates a regular file.

- Owner: Read and write.
- Group: Read only.
- Others: Read only.

Question 6

Why was the file not created inside /mnt?

Answer:

The "/mnt" directory belongs to root and does not grant ordinary users write permission. Therefore, the analyst user cannot create a file there without administrator privileges.

Question 7

What can make the touch command successful?

Answer:

Using "sudo touch /mnt/myNewFile.txt" allows the command to execute with administrator privileges.

Question 8

What are the original permissions of myFile.txt?

Answer:

"-rw-r--r--" (644).

Question 9

Did the permissions change after chmod 665?

Answer:

Yes. The permissions changed to "-rw-rw-r-x".

- Owner: Read and write.
- Group: Read and write.
- Others: Read and execute.

Question 10

What command grants everyone full access?

Answer:

sudo chmod 777 myFile.txt

Question 11

Was appending the word test successful?

Answer:

Yes. The file owner was changed to analyst, and the owner had write permission. Therefore, the analyst user could append text to the file.

Question 12

What is the difference between malware and mininet_services?

Answer:

The malware entry begins with "d", meaning it is a directory. The mininet_services entry begins with "-", meaning it is a regular file.

---

PART 3: Symbolic Links and Special File Types

Question 13

What happens to file2hard if file2new.txt is edited?

Answer:

The changes will also appear when opening file2hard because both filenames refer to the same inode and underlying file data.

---

REFLECTION

Linux filesystem permissions and ownership are important because they determine who can access, modify or execute files and directories.

Understanding mounting, file permissions, ownership and links helps administrators manage storage, troubleshoot access problems and protect systems against unauthorized access.

This lab improved my understanding of Linux filesystem management and strengthened my practical Linux administration skills.
