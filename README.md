# 👨‍💻​ Nano-Basics-SH.scripting
Welcome to the beginner's guide to writing scripts using Nano, the most accessible text editor in the Linux terminal. Whether you're automating your workflow or just getting comfortable with the command line, this repository covers the essentials.

### Opening or Creating a File
To start a new script (e.g., a Bash script), run:
```bash
nano myscript.sh
```

### Essential Shortcuts
In Nano, the ^ symbol represents the Ctrl key. Here are the "Big Four" commands you'll need:
```
Command	Action	Description
Ctrl + O	Write Out	Saves the current file.
Ctrl + X	Exit	Closes the editor (will ask to save if changes exist).
Ctrl + K	Cut Text	Deletes the current line (and saves it to the "buffer").
Ctrl + U	Uncut Text	Pastes the line you just cut.
Ctrl + S	Save your script.
```

### 📘​ Writing Your First Script
A basic script requires two things: a Shebang and Execute Permissions.
1. The Shebang
```bash
#!/bin/bash
```

### Simple "Hello World" Example
2. Your first script
```bash
#!/bin/bash
echo "Enter your name:"
read name
echo "Hello, $name! You are scripting in Nano."
```

### 💾​ Save and Exit
3. Save and exit nano with the shortcuts.
Press Ctrl + O then Enter to save.
Press Ctrl + X to exit.

### ⚡​ Running your script
4. Before you can run the script, you must tell Linux it's an executable file using chmod.
```bash
# Make the file executable
chmod +x myscript.sh

# Run it!
./myscript.sh
```

# 📜​ Create an Menu script
### 1. Create a header with the nessacary information such as name, version and autor.
```bash
#!/bin/bash
 2 #------------------------------------------------------------------------- 
 3 # Programm: Command Menu 
 4 # Beschreibung: Zeigt am meisten gebrauchte Commands in einem Menu
 5 # Aufruf: 
 6 # Optionen: 
 7 # Parameter: 
 8 # Autor: Luke
 9 # Version: 1.0
10 # Datum: 2026-02-10
11 # Aenderung: 
12 # Aenderungsdatum: 2026-02-10
13 #-------------------------------------------------------------------------
14 # LOADING STATION:
15 #
16 # ------------------------------------------
```

## 2. Create the Menu that the script should write out when you start the script
```bash
echo "Hauptmenü"
echo "-----------------------------"
echo "1. Aktueller Benutzername"
echo "2. Aktuelles Datum"
echo "3. Freie Festplattenkapazität"
echo "4. Meine IP-Adresse ausgeben"
echo "5. Letzte System Logs anzeigen"
echo "6. Programm beenden"
echo "7. Error messages suchen"
echo "8. System Update"
echo "-----------------------------"
```

## 3. Create the script to ask which Nummber you want to choose of the Menu
```bash
read -p "Bitte eine Zahl eingeben: " wahl
```

## 4. Create the options with "wahl"
```bash
case $wahl in
  1)
    echo "Benutzername: $USER"
    ;;
  2)
    echo "Datum: $(date)"
    ;;
  3)
    echo "Festplattenkapazität:"
    df -h
    ;;
  4)
    echo "4. Meine IP-Adresse:"
    hostname -I
    ;;
  5)
    echo "5. Letzte System Logs:"
    journalctl -n 5
    ;;
  6)
    echo "Tschüss"
    exit
    ;;
  7)
    read -p "Wie viele Zeilen willst du haben?" n
    ;;
  8)
    echo "System wird aktualisiert"
    sudo apt update
    sudo apt upgrade -y
    ;;
```

## 5. Add other numbers should send a statement and end the script
```bash
# create a sentence to say it need to be a number between 1 and 8.
  *)
    echo "Bitte eine Zahl zwischen 1 und 8 eingeben."
    ;;
# ends the script
esac
```



