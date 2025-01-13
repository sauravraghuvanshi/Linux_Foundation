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

### Using command line to get help

First command is **`whatis`** , this command will displays a one line description of a command does. 

**`Syntax: whatis <command>`**

```
$ whatis date
```

Most of the commands internal or external come bundled with **`man pages`** which provides information about the command in detail (with examples, usecases and with command options)

**`Syntax: man <command>`**

```
$ man date
```

Several commands will provide **`-h`** or **`--help`** to provide users with the options and usecases available in a command

```
$ date -h
$ date --help
```

To search through the man page names and descriptions for instances of the keyword use **`apropos`**. This is useful if you want to look for all commands within the system that contains the specifc keyword.

**`Syntax: apropos <keyword>`**
```
$ apropos modpr
```
![Using command line to get help](Images/image4.png)

### Bash Shell

#### Different types of Shells

- There are different types of shells in linux, some of the popular ones are below
  - Bourne Shell (sh)
  - C Shell (csh or tsh)
  - Korn Shell (ksh)
  - Z Shell (zsh)
  - Bourne again shell (Bash)

To check the shell being used. Use the command **`echo $SHELL`**
```
$ echo $SHELL
```

To change the default shell. Use the command chsh, you will be prompted for the password and following that input the name of the new shell. You have to login into new terminal session to see this change though.
```
$ chsh
```

#### Bash Shell Features

1. Bash supports command auto-completion. What this means is bash means to auto-complete commands for you if you type part of it and press the **`tab`** key.
2. In Bash we can set custom aliases for the actual commands
   ```
   $ date
   $ alias dt=date
   $ dt
   ```
3. Use the **`history`** command to list the previous run commands that you ran earlier
   ```
   $ history
   ```

#### Bash environment variables
 
 To print **`SHELL`** environment variable
 ```
 $ echo $SHELL
 ```
 
 To see a list of all environment variables. Run **`env`** from the terminal
 ```
 $ env
 ```
 
 To set an environment variable with in the shell. The value is not carry forward to any other process.
 ```
 $ OFFICE=Bangalore
 ```
 
 To set an environment variable we can use the **`export`** command. To make the value carry forward to any other process. 
 ```
 $ export OFFICE=Bangalore
 ```
 
 To persistently set an environment variable over subsequent login or a reboot add them to the **`~/.profile`** or **`~/.pam_environment`** in the users home directory.
 
 ```
 $ echo "export OFFICE=Bangalore" >> ~/.profile (or)
 $ echo "export OFFICE=Bangalore" >> ~/.pam_environment
 ```
 
 To check the value of a environment variable called **`LOGNAME`**
 ```
 $ echo $LOGNAME
 ```

#### Path Variable

##### Speaking about the environment variables, when a user issues an external command into the shell, the shell uses path variable to search for these external commands
 
To see the directories defined in path variable. Use the command **`echo $PATH`**.
```
$ echo $PATH
```

To check if the location of the command can be identified. Use the **`which`** command

**`Syntax: which <command>`**

```
$ which obs-studio
```

To define a command in the **`PATH`** variable. To add we can use the **`export`** command.
```
$ export PATH=$PATH:/opt/obs/bin
$ which obs-studio
```

#### customize Bash Prompt

To see the value assign to **`PS1`**, type **`echo $PS1`**
```
$ echo $PS1
```

To change the PS1 to only display the word **`ubuntu-server`**.
```
$ PS1="ubuntu-server"
$ echo $PS1
```

#### To customize further, have a look at the below special character.

To change the bash prompt to display **`date`**, **`time`**, **`username of the current 
user`**, the **`hostname`** and the **`current working directory`**

```
$ PS1="[\d \t \u@\h:\w ] $ "
```

![Bash_Shell](Images/image5.png)


## Linux Core Concept

### Linux Kernel

#### If you have worked with any operating system, you have run into the term kernel. 

- The Linux kernel is monolithic, this means that the kernel carrries out CPU scheduling, memory management and several operations by itselfs. 
- The Linux Kernel is also modular, which means it can extends its capabilities through the use of dynamically loaded kernel modules

#### To understand a kernel in simple terms, let us use an analogy of a **`College Library`**. Here the librarian is equal to Linux Kernel.

#### The Kernel is responsible for 4 major tasks

1. Memory Management
1. Process Management
1. Device Drivers
1. System calls and Security

#### Linux Kernel Versions

##### let us know identify the ways to identify linux kernel versions

Use **`uname`** command to get the information about the kernel (by itself it doesn't provide much information except that the system uses the **`Linux`** Kernel.
```
$ uname
```

Use the **`uname -r`** or **`uname`** comamnd and option to print the kernel version
```
$ uname -r
$ uname -a
```

![Linux Kernel Versions](Images/image6.png)

#### Kernel and User Space

##### One of the important functions of the linux kernel is the **`Memory Management`** . We will now see how memory is seperated within the linux kernel

Memory is divded into two areas.
1. Kernel Space
   1. Kernel Code
   1. kernel Extensions
   1. Device Drivers
1. User Space
   1. C
   1. Java
   1. Python
   1. Ruby e.t.c
   1. Docker Containers

#### Let us know see how programs running in the `User Space` work

All user programs function by manipulating data that is stored in memory and on disk. User programs get access to data by making special request to the kernel called **`System Calls`**
- Examples include, allocating memory by using variables or opening a file.