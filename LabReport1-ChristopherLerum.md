<h2>cd Without Arguments</h2>

    [user@sahara ~]$ cd
    [user@sahara ~]$ pwd
    /home
    
For using the cd command without any arguments, nothing is printed and nothing changes in the terminal. That is because the cd command is meant to change the directory and no directory is listed.


<h2>cd With Directory Arguments</h2>

    [user@sahara ~]$ cd lecture1
    [user@sahara ~/lecture1]$ pwd
    /home/lecture1
    
For using the cd command with a directory path argument like lecture1, the terminal now shows that you are working in that directory. That is because the cd command is meant to change the directory to whatever you list as an argument


<h2>cd With File Arguments</h2>

    [user@sahara ~/lecture1]$ cd hello.java
    bash: cd: hello.java: not a directory 
    [user@sahara ~/lecture1]$ pwd
    /home/lecture1
    
For using the cd command with a file argument like hello.java, the terminal prints "bash: cd: hello.java: not a directory ". That is because the cd command is meant to change the directory you are working in and a file is not a directory.


<h2>ls Without Arguments</h2>

    [user@sahara ~/lecture1]$ ls
    Hello.class Hello.java messages README
    [user@sahara ~/lecture1]$ pwd
    /home/lecture1
    
For using the ls command without any arguments, a list of files within the current directory is printed. That is because the ls command is meant to print all files in the listed directory and if none is listed as an argument it prints the files in the current directory.


<h2>ls With Directory Arguments</h2>

    [user@sahara ~/lecture1]$ ls messages
    en-us.txt es-mx.txt ja.txt zh-cn.txt
    [user@sahara ~/lecture1]$ pwd
    /home/lecture1
    
For using the ls command with a directory path argument like messages, a list of files within the listed directory is printed. That is because the ls command is meant to print all files in the listed directory.


<h2>ls With File Arguments</h2>

    [user@sahara ~/lecture1]$ ls Hello.java
    Hello.java
    [user@sahara ~/lecture1]$ pwd
    /home/lecture1
    
For using the ls command with a file argument like hello.java, the name of the file is printed. That is because the ls command is meant to print all accessible files in the listed directory and when a file is listed the only accessible file is the file listed.


<h2>cat Without Arguments</h2>

    [user@sahara ~/lecture1]$ cat 
    this is a test
    this is a test
    lorem ipsum
    lorem ipsum
    [user@sahara ~/lecture1]$ pwd
    /home/lecture1
    
For using the cat command without any arguments, nothing is printed and the terminal waits for more keyboard inputs and prints out anything that is typed until ctrl+D is input. That is because the cat command is used to print the contents of what is input and keyboard inputs count.


<h2>cat With Directory Arguments</h2>

    [user@sahara ~/lecture1]$ cat messages
    cat: messages: Is a directory
    [user@sahara ~/lecture1]$ pwd
    /home/lecture1
    
For using the cat command with a directory path argument like messages, a message saying "cat: messages: Is a directory" is printed. That is because the cat command is used to print the contents of what is input mainly files and in this case, since a directory is used as an argument it just prints the fact that it is a directory.


<h2>cat With File Arguments</h2>

    [user@sahara ~/lecture1]$ cat README
    To use this program:

    javac Hello.java
    java Hello messages/en-us.txt
    [user@sahara ~/lecture1]$ pwd
    /home/lecture1
    
For using the cat command with a file argument like README, it prints the contents of what is in the file. That is because the cat command is used to print the contents of what is input.
