# SocketGames
Sometimes one simply wants to play text games across a TCP socket.  For those times, this project.  

Game classes written for this project should:
* provide a default constructor,  
* extend AbstractGame, to facilitate tracking high scores,
* implement the Servable interface, and  
* carry the @GameInfo class annotation.  

Game class files so outfitted should be placed into the server working directory where they will be detected automatically and made available for play.  

The threaded server must be compiled before it can be run, as -- for example -- <b> javac GameServer.java </b>.

The server may be launched as follows: <b> java GameServer <i>tcp_port</i> <i>num_threaded_connections</i> </b>
* java GameServer 9090 5 // launches the service on port 9090 and accepts up to 5 simultaneous connections

Access a running server from a remote shell or terminal by, for example: 
* <b>telnet <i>server_ip_address tcp_port</i></b>, or  
* <b>nc <i>server_ip_address tcp_port</i></b> // macOS 10.13 removed telnet, so use netcat/nc instead

Several games are available as examples.  These games are provided as source code and must be compiled locally in order to be discovered by the server.
* <b> javac SecretWord.java </b>
* <b> javac OneInAMillion.java </b>
