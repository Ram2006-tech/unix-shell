# Unix Shell

A Unix-like command-line shell implemented in **C** using **POSIX system calls**. The shell replicates core Linux shell functionality by supporting command execution, process creation, piping, input/output redirection, background execution, and custom built-in commands while providing hands-on experience with Linux system programming.

---

## Features

- Interactive command-line shell
- Execute external Linux commands
- Built-in shell commands
- Input (`<`) and output (`>`, `>>`) redirection
- Command pipelines using (`|`)
- Background process execution (`&`)
- Process management
- Signal handling
- Command history and logging
- Modular project architecture

---

## Built-in Commands

The shell includes several custom built-in commands in addition to executing standard Linux commands.

Implemented modules include:

- `hop` – Directory navigation
- `reveal` – File and directory listing
- `log` – Command history management
- `activities` – Process monitoring
- `execute` – Command execution engine
- `commands` – Command parsing and dispatch

---

## Project Structure

```
shell
├── include
│   ├── activities.h
│   ├── commands.h
│   ├── execute.h
│   ├── hop.h
│   ├── log.h
│   └── reveal.h
│
├── src
│   ├── activities.c
│   ├── commands.c
│   ├── execute.c
│   ├── hop.c
│   ├── log.c
│   ├── main.c
│   └── reveal.c
│
├── Makefile
└── README.md
```

---

## Technologies Used

- C
- POSIX System Calls
- Linux
- GCC
- Make

---

## Build

Compile the project using:

```bash
make
```

---

## Run

```bash
./shell.out
```

---

## Supported Functionality

The shell supports:

- Executing Linux commands
- Running commands in the background
- Command pipelines
- Input and output redirection
- Built-in shell commands
- Process management
- Signal handling
- Interactive command execution

---

## Operating System Concepts Demonstrated

This project provides practical implementation of several core operating system concepts including:

- Process creation using `fork()`
- Program execution using `exec()`
- Process synchronization using `wait()`
- File descriptor manipulation
- Inter-process communication using pipes
- Input and output redirection
- Signal handling
- Linux filesystem operations

---

## Example Usage

```bash
$ pwd

$ ls -la

$ hop ..

$ reveal

$ cat file.txt

$ cat file.txt | grep hello

$ sort < input.txt > output.txt

$ sleep 20 &
```

---

## Learning Outcomes

This project helped strengthen understanding of:

- Linux system programming
- POSIX APIs
- Shell architecture
- Process management
- Command parsing
- Inter-process communication
- File descriptor management
- Operating system fundamentals

---

## Future Improvements

Potential enhancements include:

- Job control (`jobs`, `fg`, `bg`)
- Auto-completion
- Environment variable expansion
- Alias support
- Shell scripting
- Improved history search

---

## License

Developed for educational purposes as part of an Operating Systems / Systems Programming course.