CShell

cshell is an implementation of the original UNIX shell in C. It uses the POSIX API to implement a lot of the same functionality of Ken Thompson's first shell.
The API calls predominantly used are read, write, fork, exec, and wait to name a few.

Task

The project involved handling multiple commands in the same input (dealing with logical seperators). The challenge was solved through building a command queue that could be built based on each input. Scanning for seperators that would split the command. This way we could handle flags and more for our commands at the same time.

Using a queue also allowed us to easily check commands for success and failure, a doubly linked list queue could have been a possible improvement allowing for traversal in both directions. However, we ended up just setting flags as we dequeued the elements.

Some of the code could certainly be refactored to be more generic, for instance both history queues and command queues have entirely seperate data structures and functions, this could certainly be improved upon. As well as some of the ways traversal of the queues was handled.

I am still overall very happy with the net result of this project as I learned tons about memory management, string parsing, and process forking.
