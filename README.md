# Nano-Basics-scripting
Welcome to the beginner's guide to writing scripts using Nano, the most accessible text editor in the Linux terminal. Whether you're automating your workflow or just getting comfortable with the command line, this repository covers the essentials.

## Opening or Creating a File
To start a new script (e.g., a Bash script), run:
```bash
nano myscript.sh
```

## Essential Shortcuts
In Nano, the ^ symbol represents the Ctrl key. Here are the "Big Four" commands you'll need:
```
Command	Action	Description
Ctrl + O	Write Out	Saves the current file.
Ctrl + X	Exit	Closes the editor (will ask to save if changes exist).
Ctrl + K	Cut Text	Deletes the current line (and saves it to the "buffer").
Ctrl + U	Uncut Text	Pastes the line you just cut.
```

## Writing Your First Script
A basic script requires two things: a Shebang and Execute Permissions.
1. The Shebang
```bash
#!/bin/bash
```

## Simple "Hello World" Example
2. Your first script
```bash
#!/bin/bash
echo "Enter your name:"
read name
echo "Hello, $name! You are scripting in Nano."
```

## Save and Exit
3. Save and exit nano with the shortcuts.
Press Ctrl + O then Enter to save.
Press Ctrl + X to exit.

## Running your script
4. Before you can run the script, you must tell Linux it's an executable file using chmod.
```bash
# Make the file executable
chmod +x myscript.sh

# Run it!
./myscript.shbash
```




