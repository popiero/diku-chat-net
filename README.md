diku-chat-net
=============

A chat protocol under constant development. Create your client now!

Let's create our own chat network using our own protocol, servers and clients.

We can make new features and try to convince each other to support these.

Here is a first set of features that a chat network should at least support:

    NAME Simon
    WHO
    BROADCAST Hello World!
    QUIT

That is, it should be possible to connect to a server and call yourself
something (using the message `HELO <Name>`), ask who is currently on the server
(using the message `WHO`) and sending a message to everyone on the server (using
the message `BROADCAST <Message>`).

We should probably agree that linebreaks are made by one `\n` character, that
names cannot contain spaces (for now), and that any one line is at most 1024
bytes long, includes a `\n` and contains no NUL-bytes (bytes with ASCII value
0), in case anyone wants to write a client in C.

Choose to write either a client or a server, or try one of the ones available in
this repository. If you have written a nice client or server in a language you
like, you can submit it here.
