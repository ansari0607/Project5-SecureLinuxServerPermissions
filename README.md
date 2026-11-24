# Project 5: Secure Linux Server Permissions

## Description

This project demonstrates the implementation of user-based access control in a Linux environment. Two users (`alice` and `bob`) and two groups (`developers` and `admins`) were created. Each user was assigned to a specific group based on their role. Protected directories were then created and configured using Linux ownership and permission settings. Access testing confirmed that authorized users could access their designated resources, while unauthorized users received **Permission Denied** errors. 

---

## Commands Used and Purpose

| Command | Purpose |
|----------|----------|
| `groupadd admins` | Creates the **admins** group. |
| `groupadd developers` | Creates the **developers** group. |
| `useradd -m alice` | Creates user **alice** with a home directory. |
| `useradd -m bob` | Creates user **bob** with a home directory. |
| `passwd alice` | Sets password for user **alice**. |
| `passwd bob` | Sets password for user **bob**. |
| `usermod -aG developers alice` | Adds **alice** to the developers group. |
| `usermod -aG admins bob` | Adds **bob** to the admins group. |
| `groups alice` | Displays group membership of **alice**. |
| `groups bob` | Displays group membership of **bob**. |
| `mkdir /admin-data` | Creates a directory for admin resources. |
| `mkdir /dev-data` | Creates a directory for developer resources. |
| `chown root:admins /admin-data` | Assigns admins group ownership to the admin directory. |
| `chown root:developers /dev-data` | Assigns developers group ownership to the developer directory. |
| `chmod 770 /admin-data` | Grants full access to owner and group while denying access to others. |
| `chmod 770 /dev-data` | Grants full access to owner and group while denying access to others. |
| `touch filename` | Creates a test file inside a directory. |
| `echo "text" > file` | Writes sample content into a file. |
| `ls -ld /admin-data /dev-data` | Displays directory permissions and ownership details. |
| `su - alice` | Switches to user **alice** for access testing. |
| `su - bob` | Switches to user **bob** for access testing. |
| `cat filename` | Reads file content to verify allowed or denied access. |

---

## Result

- Created users and groups successfully.
- Assigned users to their respective groups.
- Configured secure directory ownership and permissions.
- Validated authorized access for permitted users.
- Verified access restrictions for unauthorized users.