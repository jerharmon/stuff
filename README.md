# Creating and Editing Files with Vim

Vim is a powerful terminal-based text editor commonly used in Unix-like environments. It can be intimidating for beginners, but it's a valuable tool once you get the hang of it. This crash course will guide you through creating and editing a file using Vim.

## Creating a New File

1. **Open a Terminal**:
   Launch your terminal or command prompt.

2. **Create a New File**:
   To create a new file or open an existing one, type the following command, replacing `filename` with your desired file name:
   ```bash
   vim filename
   ```

## Entering Vim
After running the vim command, Vim will open with the new file. You'll see the empty document with a status line at the bottom.

## Editing a File in Vim
Vim operates in different modes: Normal, Insert, and Command-line. Here's how to navigate and edit text in each mode:

### Normal Mode (moving around document)

Use the arrow keys or H, J, K, L keys to navigate around the document.
- i: Enter Insert mode before the cursor.
- I: Enter Insert mode at the beginning of the line.
- a: Enter Insert mode after the cursor.
- A: Enter Insert mode at the end of the line.
- o: Open a new line below the current line and enter Insert mode.
- O: Open a new line above the current line and enter Insert mode.
- x: Delete the character under the cursor.
- dd: Delete the entire line.
- 2dd: Delete 2 lines.
- dG: Delete all lines from here until end of file.
- yy: Yank (copy) the current line.
- 2yy: copy 2 lines
- p: Paste the yanked or deleted text after the cursor.
- w: move to next word


### Insert Mode (Esc and then i goes into this mode -- used to add new text)

In Insert mode, you can type and edit text as you would in a regular text editor.
Press Esc to return to Normal mode.


### Command Mode (Esc and then : goes into this mode -- used to save, quit, etc)

- To save your changes and exit Vim, press Esc to ensure you're in Normal mode, and then type :w and press Enter.
- To quit Vim without saving changes, press Esc to ensure you're in Normal mode, and then type :q! and press Enter.
- To save changes and quit Vim, type :wq and press Enter.
- To search for text, press Esc to return to Normal mode, then type / followed by the search term and press Enter. Use n to go to the next match and N to go to the previous match.

Examples: 
- ESC and :w will save
- ESC and then :wq will save and quit Vim




# How to create shell script

## Open a Text Editor
Use a text editor like Vim or nano to create your script file. For this example, let's call it myscript.sh.

```vim myscript.sh```


## Shebang Line
The first line of your script should specify the shell interpreter. In most cases, you'll use #!/bin/bash to indicate that this is a Bash script.

#!/bin/bash


## Write Your Script
Add your Bash commands below the shebang line. Here's a simple example that prints "Hello, World!" to the terminal:

```#!/bin/bash
echo "Hello, World!"
```


Save the file (esc and then :wq in Vim)


## Make It Executable
You need to make your script executable. Use the chmod command to give it execute permissions:

chmod +x myscript.sh

## Run Your Script
To execute your script, simply type its name in the terminal:

./myscript.sh
Ensure that you are in the same directory as your script, or provide the full path if it's located elsewhere.

Note: you can also call the script without it being executable by calling the interpreter and then the script as an argument.  

sh ./myscript.sh


## Comments and Documentation
Good scripts have comments to explain what each part does. Use #  to add comments in your script

```#!/bin/bash
# This is a simple script that prints a greeting
echo "Hello, World!"
```



## Variables
You can use variables to store and manipulate data. Here's an example:

```#!/bin/bash
name="John"
echo "Hello, $name!"
```


## User Input
You can prompt the user for input using the read command:

```#!/bin/bash
echo "What's your name?"
read name
echo "Hello, $name!"
```


## Conditional Statements
Use if, elif, and else to create conditional statements:

```#!/bin/bash
age=18
if [ "$age" -ge 18 ]; then
    echo "You are an adult."
else
    echo "You are not yet an adult."
fi
```


## Loops
You can use loops like for and while for repetitive tasks:

```#!/bin/bash
for i in {1..5}; do
    echo "Iteration $i"
done
```


## Functions
You can define functions to organize your code:

```#!/bin/bash
greet() {
    echo "Hello, $1!"
}
greet "Alice"
greet "Bob"
```

## Error Handling
You can handle errors with exit codes and error messages:

```#!/bin/bash
if [ ! -f myfile.txt ]; then
    echo "Error: myfile.txt does not exist."
    exit 1
fi
```
