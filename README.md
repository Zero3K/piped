# Named Pipe TCP Proxy

**The Problem**

To date of this writing there was no terminal client capable of connecting to named pipes on Windows (neither locally nor remotely). There may be various reasons for such type of access. In my case I was doing some kernel debugging on Linux/Solaris virtual machines that were running under supervision of VMware(or Virtual PC) software and I needed to access Guest OS serial consoles (virtual com ports emulated as named pipes) from the Host OS or remotely using TCP connection.

 

**Solution**

Named Pipe TCP Proxy - utility which provides access to named pipes on Windows (special files with names built using the following rule -\\<server_name>\pipe\<pipe_name>) via TCP/IP. Utility has intuitive GUI and allows to create "tcp port" <=> "named pipe" mappings. To access certain named pipe you need to create such a mapping and then connect to assigned tcp port using any terminal client program. For example one may access named pipe locally by issuing the following command:

 

 telnet 127.0.0.1 <TcpPort>

where TcpPort is the port assigned in the GUI for a given named pipe.

 

**Attention**

This software is provided as is. Use it at your own risk. Author does not take any responsibility for anything related to aforementioned utility.

 

If you want to redistribute this software you must provide the link to original developer's site. All of the associated and implied rights reserved.

 

**Feedback and Support**

However, in spite of paragraph above, I'll be glad to get feedback on the subject. Proposals, ideas and bug reports are highly appreciated. You may contact me at shvechkov@NOSPAMyahoo.com (remove NOSPAM) /Alexey Shvechkov/