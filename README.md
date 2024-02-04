# PORT_SCANNER

# DISCLAIMER 
 we are not responsible for any illegal action performed by any reader. If you planned to use the content for illegal purpose, please leave this NOW...!!!!

This is a basic python code essentially performs port scanning on the specified IP address using threading for concurrency. It attempts to connect to each port, and if successful, it prints the port number, associated service, and marks it as OPEN. The output is color-coded for better visibility.
# AN OUTPUT EXAMPLE IS SHOWN AS FOLLWING : 
![Untitled](https://github.com/shankar219/PORT_SCANNER/assets/80420170/0f9d862f-8c97-4460-b74b-a3a38619f1b2)


# INSTALLATION (IN LINUX)

$ sudo apt update

$ sudo apt upgrade

$ sudo apt install python3

$ sudo apt install git 

$ git clone https://github.com/shankar219/PORT_SCANNER.git 

$ cd PORT_SCANNER

$ python3 port_scanner.py

![Untitled1](https://github.com/shankar219/PORT_SCANNER/assets/80420170/563c97a5-2ca7-481b-a7a3-9f4d622a62f3)



# EXPLANATION OF THE CODE : 

IMPORTS:

socket: This module provides a low-level interface to networking operations.

termcolor: This module is used for colored output in the console.

threading: This module provides a way to create and manage threads.

ASCII Art:

An ASCII art is displayed at the beginning, which is a visual representation of a network-related theme.

FUNCTION DEFINITIONS:

scan(target, ports): This function is responsible for creating and starting threads for scanning ports on the target.
scan_port(ipaddress, ports): This function is used by the threads to attempt a connection to a specific port on the target IP address and print the result.

USER INPUT:

The user is prompted to enter the target IP address and the total number of ports to be scanned (limited to a maximum of 65535 ports).

IP ADDRESS VALIDATION:

The entered IP address is validated using the ipaddress module.

PORT SCANNING:

If the IP address is valid, the program proceeds to scan for open ports on the target.
The scan function is called, which creates a thread for each port and starts the scanning process concurrently.

OUTPUT DISPLAY:

The program prints a table with information about each scanned port, including the port number, service name, and its status (OPEN or not).

EXCEPTION HANDLING:

If there is any ValueError (e.g., invalid IP address) or KeyboardInterrupt (user interrupts the program), appropriate messages are displayed.

Closing Message:

The program prints a closing message if it is interrupted by the user.

