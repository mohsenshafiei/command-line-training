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

 - Exiting from super user
 ```bash
 exit
 ```

- To understand who logged into the system
```bash
users
```

- To get id of information
```bash
id
```

- To make executable
```bash
chmod +x file
```

- To change the file permission personal
```bash
chmod 700 exampleFile
chmod 644 exampleFile
```

- make the terminal font larger and smaller
```bash
ctrl + shift + +
ctrl + shift + -
```

- search on a file
```bash
grep "sample text or regex" file.txt
grep -w "sample text or regex" file.txt
grep -wi "sample text or regex" file.txt
grep -win "sample text or regex" file.txt
grep -win -B 4 "sample text or regex" file.txt
grep -win -A 4 "sample text or regex" file.txt
grep -win -C 2 "sample text or regex" file.txt
```

- Searching on all files in a directory
```bash
grep -win "simple text or regex" ./*
grep -win "simple text or regex" ./*.txt
grep -winr "simple text or regex" ./ => search recursively a directory
grep -wirl "simple text or regex" ./ => files of matches
grep -wirc "simple text or regex" ./ => number of matches
history | grep "git commit" | grep "dotfile"
```

- install new version of grep
```bash
brew install grep --with-default-names
```

- Select the data and present in columns and rows
```bash
awk '{print $3 $4}' file.txt
``

- Filtering lines in terminal using sed
```bash
cat file.txt | sed -r '2,4d'
cat file.txt | sed -n -r '2,4p'
cat file.txt | sed -n -r '/regex/d'
cat file.txt | sed -r 's/Frank/Mohsen/' => replace the text
cat file.txt | sed -r 's//Mohsen/' => remove the text
```

- Which files are open
```bash
lsof | head
```

- Which processes have this file open?
```bash
lsof /var/log/nginx-error.log
```

- Which files does process X have open?
```bash
lsof -p 1
lsof -p `pgrep ABC`
```

- Where is the binary for this process?
```bash
lsof -p ABC | grep bin
```

- Which shared libraries is this program using? (manually upgrading software, i.e. openssl)
```bash
lsof -p PID | grep .so
```
- Where is this thing logging to?
```bash
lsof -p ABC | grep log
```

- Which processes still have this old library open?
```bash
lsof grep libname.so
```

- Which files does user XYZ have open?
```bash
lsof -u XYZ
lsof -u XYZ -i
```

- Which process is listening on Port X (or using Protocol Y)?
```bash
lsof -i :80
lsof -i tcp
```

- Getting data from server with curl

```bash
curl https://localhost:5000/products
curl -i https://localhost:5000/products => more information
curl -d "first=mohsen&last=shafiei" https://localhost:5000/person
curl -d X PUT "first=mohsen&last=shafiei" https://localhost:5000/person
curl -d X DELETE "first=mohsen&last=shafiei" https://localhost:5000/person
curl -u username:password https://localhost:5000/person
curl -o  https://localhost:5000/person/image.jpeg
curl -o file.txt https://localhost:5000/person/file.txt
```
note: you can use curl for many other things like test speed and etc.

- The find command allows us to scan through our file system in order to find files and directories that meet a certain criteria

```bash
find .
find my-directory
find my-directory -type -f => returns all files not directories
find my-directory -type -f -name "test" => returns all files not directories
find my-directory -type -f -name "test*" => returns all files with name test
find my-directory -type -f -iname "test*" => returns all files with name test and case sensitive
find . -type f -mmin -10 => files that modified less than ten minutes ago
find . -type f -mmin -1 -min +10 => files that modified less than one minute ago or more than 10 minutes ago
find . -type f -mtime -1 => files that modified less than one day ago
find . -type f -mtime +1 => files that modified more than one day ago
find . -size +5M => files that modified more than one day ago
find . -perm 777 => search based on file permissions
find ./sample-directory exec chown mohsenshafiei:www-data {} +
find . -type f -name "*.pyc" -maxdepth 1 -exec rm {} +
```

- The rsync command will allow you to sync file and directories on your local machine or even over a network between servers.

```bash
rsync ./original ./backup
rsync -r ./original ./backup
rsync -a --dry-run ./original ./backup
rsync -av --dry-run ./original ./backup
rsync -zaP ~/web-files username@192.168.1.1:password~/public/ => syncing files between local and remote
rsync -zaP username@192.168.1.1:password~/public/ ~/backup-directory  => syncing files between local and remote
```

- cron will allow you to run commands on a repetitive schedule

```bash
crontab -l => list of all cron jobs
* * * * * rm -rf ~/backup
```

- download files from WWW
```bash
wget link-address
wget -O your-name.txt link-address
wget link-address-1 link-address-2
wget --help
```
