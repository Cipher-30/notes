# SOME BASH COMMANDS

## touch 
- touch a.txt - for creating a new file

## cat (concatenate)
- cat a.txt - for viewing the file
- cat > a.txt - make and open the file
- cat >> a.txt - modify the existing a.txt file

## mkdir (make directory)
- mkdir newFolder - create newFolder directory
- mkdir newFolder && ls newFolder - combined two commands
- mkdir -p newFolder/file2 - creating folder recursivly inside newFolder

## mv (move and rename) 
- mv a.txt a1.txt - rename the a.txt to a1.txt
- mv a.txt newFolder/file2 - moving a.txt to file2 directory
- mv a.txt newFolder/file2/a1.txt - moving a.txt and renaming at the same time

## cp (coping)
- cp a.txt newFolder/file1 - coping a.txt to file1 directory
- cp -r folder1 newFolder/file1 - copy folder recursivly to another folder 

## rm (remove)
- rm a.txt - remove/delete file a.txt
- rm -r newFolder - remove recursivly newFolder

## chmode (change file permissions)
   ***chmode -R ugo-rwx ***
    - you can change permissions for u(user), g(group), o(others)
    -  (+) -> adding permissions(read, write, execute)
    -  (-) -> removing permissions(read, write, execute)
    -  -R ->  recursive for Folders
- chmode u-r file1 - removing user from read the file1

## echo
- echo "hello there" -> to print on the cli
- echo $PATH -> prints full path of current working directory

## head/tail
- head file.txt -> prints first 10 line of the file
- tail file.txt -> prints last 10 lines of the file
- head -20 file.txt -> prints first 20 line of the file

## | (pipe operator)
   ***command 1 | command 2 ***
    - command 1 serves as a input for the command 2
- tail -n -25 file.txt | head -5 -> cmd1 (last 25 lines) then give first 5 line.

## wc (counts line,words,char)
 - wc file.txt

## grep (find words)
- grep "one" file.txt -> prints all occurance of one in file1.txt
- grep "one"  file.txt | wc -l -> prints how many times "one" occurs
- grep -c "one" file.txt -> no of lines it was present in file
- grep -h "one" file.txt -> gives lines it was present in file
- grep -hi "one" file.txt -> not case In-sensitive and gives even present with other word
- grep -hin "one" file.txt -> prints with line No
- grep -hinw "one" file.txt -> prints only if whole word is matched
- grep -hir "one" newFolder -> one present in folder

-grep -o "one" file.txt -> only matched parts
-grep -w "one" file.txt ->  matched parts

## bash Script
  **to automate task**
  - `!/bin/bash`
  - `echo "hello there"`
  - `mkdir newFolder1`
  -  `cd newFolder && touch a.txt`
  -  `rm a.txt`

- `bash myScript.sh` -> to execute the bash file

## vi (Vim editor)
- vi a.txt -> opens a.txt in vim
  - PRESS "I" -> to go in INSERT mode
  - PRESS "ESC" -> to get out from INSERT mode
  - :q! -> enter this phrase to exit file without saving
  - :wq! -> save and exit the file