### COMMAND TRAINING

- Search in history
```bash
Ctrl + r
```

- Jump to beginning of the line
```bash
Ctrl + a
```

- Jump to the end of the line
```bash
Ctrl + e
```

- Clear terminal
```bash
Ctrl + l
```

- Get information about program
```bash
man bash
man git
```

- Creating a new file
```bash
touch example.txt
```

- Writing something into a file
```bash
echo "hello text file" > file.txt
```

- Creating directory
```bash
mkdir mydirectory
```

- Creating nested directories
```bash
mkdir -p mydirectory/hello/node
```

- Listing all files
```bash
ls
```

- Listing all files with formats and permissions and extension
```bash
ls -lah
```

- Navigating into directories
```bash
cd directory/init
cd ..
```

- Finding files

```bash
find / -name catpic
find . -name catpic
```

- Fuzzy Search
```bash
ack
```

- removing files
```bash
rm mydirectory
```

- append content to a file
```bash
echo "more content" >> file.txt
```

- Moving and changing names of the files
```bash
mv myfile.txt to mynewfile.txt
```

- Copy files
```bash
cp myfile.txt file3.txt
```

- Connect to a server
```bash
ssh root@1.2.3.4
tmux
vim
tmux attach
tmux ls
```

- Process Management
```bash
pidof program
kill 9378
pkill program
top
htop
```

- Printing the file into the screen
```bash
cat file.txt
```

- To understand where you are in directory
```bash
pwd
```

- List of all files in a directory
```bash
ls /home/doc/mydirectory
```

- Showing everything
```bash
ls -a
ls -l
ls -lah
```

- Returning to home directory
```bash
cd ~
cd
```

- Jumping to another directory and return
```bash
pushd /etc
popd
```

- getting the format of files and more information
```bash
file mydirectory
file example.txt
```

- Finding the location of a file
```bash
locate example.txt
locate fstab
```

- Updating location files
```bash
sudo updatedb
```

- When you wanna know a command exist or installed or not
```bash
which cal
which nano
```

- History of commands
```bash
history
```

- To get information about a command
```bash
whatis cal
```

- To get all different commands about something
```bash
apropos time
```

- to see all information about a command
```bash
man cal
```

- remove directory
```bash
rm -r
```

- remove empty directories
```bash
rmdir junk
```

- adding text to a file
```bash
cat >> file2
here is the text
```

- Reading a file in terminal with pager, both of them do the same thing in different ways
```bash
more file1
less file1
```

- Piping two commands
```bash
history | less
```
 
