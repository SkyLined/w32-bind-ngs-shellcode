A small, null-free [port binding](http://skypher.com/wiki/index.php/Bindshell) [shellcode](http://skypher.com/wiki/index.php/Shellcode) for 32-bit versions of Windows. Windows 5.0-7.0 all service packs are supported. The code binds a socket to a port to accept incomming connections. This code is based largely on [code and ideas](http://www.ngssoftware.com/papers/WritingSmallShellcode.pdf) (C) 2005 by Dafydd Stuttard, NGS Software. Thanks to Pete Beck.

Features both in this and the original code:
  * NULL Free
  * Windows version and service pack independant.
Improvements of this code over the original:
  * No assumptions are made about the values of registers.
  * "/3GB" compatible: pointers are not assume to be smaller than 0x80000000.
  * [DEP](http://skypher.com/wiki/index.php/DEP)/[ASLR](http://skypher.com/wiki/index.php/ASLR) compatible: data is not executed, code is not modified.
  * Windows 7 compatible: [kernel32](http://skypher.com/wiki/index.php/kernel32) is found based on the length of its name.
  * Stealth: does not display a console windows on the target machine when cmd.exe is executed.
  * Allows an unlimited number of consecutive connections.
  * Can except connections on almost any port. The range of acceptable port numbers is only limited by the fact that the negative value of the port number must not contain nulls.

For more information, have a look at [this wiki page](http://skypher.com/wiki/index.php/Hacking/Shellcode/Bind/NGS).