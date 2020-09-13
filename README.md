# Go Chat Server 
A basic multi client, multiroom tcp chat server written in GO, can be accessed with telnet. Supports basic multi room and multiple simultaneous connections.  

## Build
go build server.go

##
go run server.go
	- server should start and will be listerning on the ip address:port that is defined in code

## Usage

* Starting the server:
```
/server --help
Usage of ./server:
  -ip string
    	IP address to listen on your localhost or  (default "127.0.0.1")
  -port string
    	Port to listen on (default "8181")

./server
```

##Connecting from Windows(10)

	- Please make sure the telenet is turned on
	- By default it is turned off in windows 10 hence please follow these steps:
	
		1.Click the start button, then start typing “Turn Windows features on or off”, and select this option, as shown below.
		2.The “Turn Windows Features on or off” window should open, scroll down and select “Telnet Client”.
		3.Click the OK button to proceed, this will display a screen while the changes apply.
		4.When complete it will display as below, you can now close the window
		5.Verifying that the telnet client is enabled-
			Simply open command prompt or powershell, type ‘telnet’ and press enter. If this was successful you should have a prompt similar to the below:
			
			Welcome to Microsoft Telnet Client

			Escape Character is 'CTRL+]'

			Microsoft Telnet>
	- Since the telnet is up on your command prompt, please open a connectetion using command "o 127.0.0.1 23"
	- Once connected, this would open a new windos promting for with a message Please Enter Name:
	- Please follow the insturctions from there onwards.

* Connecting to the server:

```
telnet 127.0.0.1 8181
Trying 127.0.0.1...
Connected to localhost.
Escape character is '^]'.
please enter name: dbnegative
---------------------------
* Welcome yourname *
---------------------------
HELP:
---------------------------
\listrooms list all online users
\create create a new room
\join join a room
\help prints all available commands
\quit quit
---------------------------
\create
please enter room name: testChatroom
---------------------------
* room testChatroom has been created *
---------------------------
hi
---------------------------
* current Timestamp * (yourname): "hi" *
---------------------------
```

## Liraries Used

	bufio - 	Package bufio implements buffered I/O. It wraps an io.Reader or io.Writer object, creating another object (Reader or Writer) that also implements the 				interface but provides buffering and some help for textual I/O.
	flag	- 	Package flag implements command-line flag parsing.
	log	-	Package log implements a simple logging package
	net	-	Package net provides a portable interface for network I/O, including TCP/IP, UDP, domain name resolution, and Unix domain sockets.   
	reflect - 	Package reflect implements run-time reflection, allowing a program to manipulate objects with arbitrary types.
	strconv - 	Package strconv implements conversions to and from string representations of basic data types.
	strings - 	Package strings implements simple functions to manipulate UTF-8 encoded strings. 
	time -    	Package time provides functionality for measuring and displaying time.
	
## Sofrwares required
	GoLang current version downladed from "https://golang.org/"
	Visual Studio Code latest downloaded from : "https://code.visualstudio.com/" 
	GIT for code check in etc.

## Notes
	Please make sure the go path & visual studio path variable are set properly if you are using Windows 10 or earlier versions depending upon the environment set up.
	
## References & To-Do's
	For libraries and other references, i referred to "https://github.com/avelino/awesome-go"
	Due to Time Constaint,i could not add much of the test cases, testing related information.
	A simple UI untility can be added in order to make the testing more user friendly as this is chat based app. 
	Vue.js or any lightweight java script library can be used to build simple UI.
	
