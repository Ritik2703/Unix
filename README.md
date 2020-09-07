# Unix
# Hare krishna
# Radhe Radhe


# Unix commands - https://unixguide.readthedocs.io/en/latest/unixcheatsheet/index.html
# Shell Scripting - https://unixguide.readthedocs.io/en/latest/script/index.html

Various useful unix-commands are listed in this chapter. Also, some of the examples of these commands are shown in the last section. Further, in next chapter, shell-scripting is discussed.

## Unix commands cheatsheet
Following are the list of various useful unix-commands,

### Basic file commands

        Commands	                           Details
     Basic opeations	 
 
      ls	                  directory listing
      ls -a	                  show hidden file
      ls -l	                  show details for file
    ln file1 file2	          create file2 (linked with file1). Changes will appear in both file
    ln -s file1 file2	          create shortcut of file1 as file2 (soft link)
    mkdir dirname	          create directory dirname
    cd dirname	                  go to dirname
    cd	                          go to home directory
    pwd	                          present working directory
    rm filename	                  remove (delete) filename
    rm -r dirname	          remove directory dirname
    rm -f filename	          Force remove file filename
    rm -rf dirname	          Force remove directory dirname
    cp file1 file2	          copy file1 to file2
    cp -r dir1 dir2	          copy dir1 to dir2
    mv file1 file2	          rename file1 to file2
    touch filename	          create filename (if not exist)
    cat > filename	          add content to file (ctrl-c to exit)
    cat >> filename	          add content at the end of the filename
    cat filename	          show content of filename (all at once)
    more filename	         show content of filename (fit to screen with more option)
    head filename	         show first 10 lines of filename
    tail filename	         show last 10 lines of filename
    tail -f filename	         last 10 lines of the filename (useful for log files)
    command > filename	         write output of command in the filename (overwrite the fie
    command >> filname	         append the output at the end of file name
    wc filename (wc -l, -w, -c)	 returns number of lines, word, character and filename.
    chmod 777 filename	         read(4), write(2) and execute(1) permission to all [4+2+1=7]
                                 chmod [owner, group, others] filename

### Sort
### Cut
### Paste
### Grep
### Sed

## Multiple commands

### Pipes
Pipes are used for sending output of one command to next command.

### Run individual commands (;)
Commands can be run separately from one line by separating them using semicolon,

## Sort example
# create a file
$ cat > test
Tiger
Lion
Cat
Eagle
^C

# see the content
$ cat test
Tiger
Lion
Cat
Eagle

# sort the content
$ sort test
Cat
Eagle
Lion
Tiger
dhriti@meher ~/Desktop $
1.3.3. Cut command
$ cat > test
first last age id
Meher Patel 20 101
Krishna patel 30 102
Tom Jerry 43 103
^C

$ cut -d" " -f 1,3,4 test
first age id
Meher 20 101
Krishna 30 102
Tom 43 103
