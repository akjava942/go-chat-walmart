# Go Chat Server 
A basic multi client, multiroom tcp chat server written in GO, can be accessed with telnet. Supports basic multi room and multiple simultaneous connections.  

## Build

```
go build server.go
```

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

	bufio - 	Package bufio implements buffered I/O. It wraps an io.Reader or io.Writer object, creating another object (Reader or Writer) that also implements the interface but               provides buffering and some help for textual I/O.
	flag - 	  Package flag implements command-line flag parsing.
	log	 -    Package log implements a simple logging package.	
  net	-     Package net provides a portable interface for network I/O, including TCP/IP, UDP, domain name resolution, and Unix domain sockets.
	reflect - Package reflect implements run-time reflection, allowing a program to manipulate objects with arbitrary types.
	strconv - Package strconv implements conversions to and from string representations of basic data types.
	strings - Package strings implements simple functions to manipulate UTF-8 encoded strings. 
	time -    Package time provides functionality for measuring and displaying time.
