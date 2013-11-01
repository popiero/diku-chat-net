diku-chat-net
=============

A chat protocol under constant development. Create your client now!

Let's create our own chat network using our own protocol, servers and clients.

We can make new features and try to convince each other to support these.

Here is a first set of features that a chat network should at least support:

    Client sends to server:    Server responds...         ...to whom?
    NAME Simon                 NAME Simon                 All clients
    WHO                        NAMES Alice Bob John       Only sender
    BROADCAST Hello World!     FROM Simon Hello World!    All clients
    QUIT                       QUIT Simon                 All clients but sender

That is, it should be possible to connect to a server and call yourself
something (using the message `NAME <Name>`), ask who is currently on the server
(using the message `WHO`), send a message to everyone on the server (using the
message `BROADCAST <Message>`) and quit (using `QUIT`).

We should probably agree that all linebreaks are made with one set of `\r\n`
characters (called *carriage return* and *line feed*), that names cannot contain
spaces (for now), and that any one line is at most 1024 bytes long and contains
no `NUL`-bytes (bytes with ASCII value 0), in case anyone wants to write a
client in C.

Choose to write either a client or a server, or try one of the ones available in
this repository. If you have written a nice client or server in a language you
like, you can submit it here.

Let's also use the TCP port number `33333` for servers.

To test the server without a client, try `telnet some.server 33333`.
