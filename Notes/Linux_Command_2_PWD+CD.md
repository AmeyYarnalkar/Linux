Here are the Markdown notes for the `pwd` (Print Working Directory) and `cd` (Change Directory) commands:

# `pwd` (Print Working Directory)

## 1. What is `pwd`?

The `pwd` command stands for **Print Working Directory**. It is used to display the current directory (folder) you are in, within the filesystem. It shows the absolute path from the root directory to your current location.

### Syntax:
```bash
pwd
```

### Example:
```bash
$ pwd
/home/user/Documents
```
In this example, the current directory is `/home/user/Documents`.

### Use Cases:
- **Check Current Location:** Helps you identify your location in the directory structure.
- **Understand Script Context:** Often used in scripts to print the current working directory.

### Options:
- **`-L`** (Logical): Prints the logical path, accounting for symbolic links.
- **`-P`** (Physical): Prints the actual physical path, ignoring symbolic links.

### Example with Options:
```bash
$ pwd -L
/home/user/Documents
```

```bash
$ pwd -P
/home/user/Documents
```
Both options usually display the same result unless symbolic links are involved.

---

# `cd` (Change Directory)

## 1. What is `cd`?

The `cd` command stands for **Change Directory**. It allows you to navigate between directories in the filesystem. Using `cd`, you can move to any directory in the filesystem based on its path.

### Syntax:
```bash
cd [directory]
```
- **[directory]** is the directory you want to navigate to. It can be an absolute or relative path.

### Examples:

#### 1. **Change to an Absolute Path:**
```bash
$ cd /home/user/Documents
```
This will move you directly to the `/home/user/Documents` directory.

#### 2. **Change to a Relative Path:**
```bash
$ cd Documents
```
This will move you to the `Documents` directory from your current location.

#### 3. **Move Up One Directory:**
```bash
$ cd ..
```
This will move you up one level in the directory structure (to the parent directory).

#### 4. **Move to the Home Directory:**
```bash
$ cd ~
```
This will take you to the home directory of the current user.

#### 5. **Move to the Previous Directory:**
```bash
$ cd -
```

#### 6. **Move to the root Directory:**
```bash
$ cd /
```
This will switch to the previous directory you were in.

---

## 2. Practical Examples

### 1. **Navigating Multiple Levels:**
To move to a directory two levels up:
```bash
$ cd ../..
```

### 2. **Using `cd` in Scripts:**
In shell scripts, `cd` is often used to change to a specific directory before performing file operations.

Example:
```bash
#!/bin/bash
cd /var/log
ls -l
```
This script changes the directory to `/var/log` and lists its contents.

---

## 3. Troubleshooting `cd`

- **Directory Does Not Exist:**
  If the directory does not exist, `cd` will return an error:
  ```bash
  $ cd non_existent_directory
  bash: cd: non_existent_directory: No such file or directory
  ```
- **Permission Denied:**
  If you don’t have permission to access a directory, you will get:
  ```bash
  $ cd /root
  bash: cd: /root: Permission denied
  ```

---

# Conclusion

- **`pwd`** helps you check your current location within the filesystem.
- **`cd`** allows you to navigate to different directories, either by absolute or relative paths, or by using shortcuts like `..`, `~`, or `-`.
These commands are essential for navigating the file system in a shell environment and are often used together to manage your file structure effectively.
```

These notes explain both the `pwd` and `cd` commands, providing examples and practical use cases, ready for GitHub or any markdown-supported platform. Let me know if you need any further modifications!
