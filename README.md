# Linux Foundation
I am talking about Liunx foundation and will add my learning summary in this repo. 

## Working with Shell:

### Shell Fundamental: 

#### Linux shell
- This command line interface (CLI) will enable you to effectively work on linux laptop/server/virtual machine.
- While the graphical version may see more appealing to the users but can be limited in case of functionality. These is where the Linux command line commonly known as **`Linux Shell`** comes to help.

#### What is a shell?

  - Linux shell is a program that allows text based interaction between the user and the operating system, this interaction is carried out by typing commands into the interface and receving the response in the same way.
  - The Linux shell is a powerful tool with which you can navigate between different locations within the system, however when you login to the shell the very first directory you were take into is your home directory.

#### Why do we need a home directoy?
  - The home directory allows users to store their personal data in the form of files and directories
  - Each user in the system gets their own unique home directory with complete access to it (to be able to save, retreive , delete data).
  - Think of it as a dedicated locker assign to you in which you can store or retreive items.
  - Other users can't access your files and folders with in your home directory **`(only you can)`.**

#### Command Prompt
- You can configure the command prompt to show whatever you want, such as the **`hostname`** , **`date`** or **`time`**. 
- It is currently configured to show the current working directory. The **`~` symbol**  here represents the home directory

![Command Prompt](Images/image.png)

#### Command and Arguments

- To interact with the linux system using the shell, a user has to type in commands
- When a command is run it executes a program to achieve a specific task.
  - **`For example`**: The **`echo`** command is used to print a line of text on the screen.
  ```
                          $ echo 
  ```
- An argument acts as an input to command
  - **`For example`**: To print a **`hello`** message type **`echo hello`** command.
  ```
                          $ echo hello
  ```
- There are several commands that can work without an argument too.
  - **`For example`**: Type in the command called **`uptime`**, this is used to print information about how long a system has been running for since the last reboot along with the other information (This command doesn't need an argument)
  ```
                          $ uptime 
  ```
- A command can also have options that modify its behaviour in some predetermine way. The option also sometime referred to as a switch or a flag 
  - **`For example`**: To print a same word `hello` but without a trailing line, use **`echo`** command with **`-n`** flag.
  ```
                          $ echo -n hello
  ```
  
![Command-and-Arguments](Images/image1.png)

#### Command Types

Command types in linux can be generally categorized in two types
 1. Internal or Built-in Commands 
    - Internal commands are part of the shell itself. It come bundled with it, there are in total about 30 such commands
    - **`For example`**: echo, cd, pwd, set e.t.c.
 2. External Commands
    - External commands on the other hand are binary programs or scripts which are usually located in distinct files in the system. They either come with pre-install with the distribution package manager or can be created or installed by the user
    - **`For Example`**: mv, date, uptime, cp e.t.c.
    
To determine a command is internal or external, use **`type`** command
 
![Command-Types](Images/image2.png)

### Basic Linux Commands

To print the present working directory. Run **`pwd`** command
```
$ pwd
```

To see the contents of the directory. Run **`ls`** command
```
$ ls 
````

To make (or) create a directory. Run **`mkdir`** command
```
$ mkdir Asia
```

To make (or) create multiple directories. Run **`mkdir`** command followed by **`<directory_name1> <directory_name2> .. <directory_nameN>`**
```
$ mkdir Europe Africa America
```

To change a directory from the current directory. Run **`cd <directory_name>`**
```
$ cd Asia
```

To recursively created directories. Run **`mkdir -p <directory_name1>/<sub_directory_of_name1>`**
```
$ mkdir -p India/Mumbai
```

To go back to one directory up. Run **`cd ..`**
```
$ cd ..
```

To go back directly to a home directory of the current user from any location in the system. Run **`cd`**
```
$ cd
```
#### Difference absolute path and relative path

- **Absolute Path** : An absolute path is defined as specifying the location of a file or directory from the root directory(/).
- **Relative Path** : Relative path is defined as the path related to the present working directly(pwd).

To change to a directory with absolute path. Run **`cd <directory_path>`**
```
$ cd /home/saurav
```

To Change to a directory with relative path. Run **`cd <directoryName>`**
```
$ cd Asia
```

To get the long list of files and directories. Run **`ls -l`** command
```
$ ls -l
```

To list all files including the hidden. Run **`ls -a`** command
```
$ ls -a
```

To list all the files in the order they were modified. Run **`ls -lt`** command
```
$ ls -lt
```

To list all the files form oldest to newest. Run **`ls -ltr`** command
```
$ ls -ltr
```
![Basic-Command](Images/image3.png)

