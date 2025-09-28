# Shell Whisperer (SWR): Even the Layman Can Use the Command Line

## Vision

Shell Whisperer (SWR) is designed to revolutionize the way users interact with the command line, making it accessible even to those with little to no experience. The command line can be daunting with its vast array of commands and syntax, but SWR simplifies this by allowing users to describe their tasks in natural language. SWR then translates these descriptions into the appropriate shell commands, making the command line intuitive and user-friendly. Whether you're using Bash, Zsh, or any other shell, SWR can be easily configured to fit your environment. Each time SWR suggests a command, it provides a clear description, giving users the option to edit, execute, deny, or save the command. This interactive process continues until the user decides to exit, ensuring that every interaction with the command line is both educational and productive. SWR is not just a tool; it's a companion that helps users master the command line with ease and confidence.

## Features

- **Natural Language Processing:** Converts user descriptions into shell commands.
- **Customizable Shell Support:** Works with Bash, Zsh, and other shells.
- **Interactive Feedback:** Users can edit, execute, deny, or save suggested commands.
- **Educational Experience:** Provides clear descriptions of suggested commands.
- **Continuous Learning:** Users can train SWR to better understand their specific command line usage patterns.

## Getting Started

To get started with Shell_whisperer, follow these steps:

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/shell_whisperer.git
   ```
2. Navigate to the project directory:
   ```sh
   cd shell_whisperer
   ```
3. Build the binary (ensure you have Go installed):
   ```sh
   go build -o swr
   ```
4. Run the program:
   ```sh
   ./swr
   ```

## Example Run

### Interactive Mode

Here's a compact and easy-to-use example of how SWR can be used in interactive mode:

```sh
$ ./swr --interactive
> Describe what you want to do:
I want to list all files in the current directory and sort them by modification time.
Suggested Command:
ls \-lt
Description:
Lists all files in the current directory, sorted by modification time.
[1] Edit  [2] Execute  [3] Deny  [4] Save
Choose: 2
Executing:
ls \-lt
total 40
drwxr-xr-x  2 user group 4096 Sep 25 12:34 directory
-rw-r--r--  1 user group  123 Sep 25 12:30 file1.txt
-rw-r--r--  1 user group  456 Sep 25 12:25 file2.txt

> Describe what you want to do:
...
```

### Non-Interactive Mode

Alternatively, you can provide the description directly in the command line and respond with "yes" or "no":

```sh
$ ./swr "I want to list all files in this folder and sort them by modification time."
Suggested Command:
ls \-lt
Description:
Lists all files in the current directory, sorted by modification time.
Execute? (yes/no): yes
Executing:
ls \-lt
total 40
drwxr-xr-x  2 user group 4096 Sep 25 12:34 directory
-rw-r--r--  1 user group  123 Sep 25 12:30 file1.txt
-rw-r--r--  1 user group  456 Sep 25 12:25 file2.txt
```

This interface is designed to be straightforward and efficient, allowing users to quickly interact with the command line through natural language descriptions, whether in interactive or non-interactive mode.

---

Shell Whisperer is more than just a tool; it's a companion that helps users master the command line with ease and confidence, bridging the gap between natural language and Unix operations.
