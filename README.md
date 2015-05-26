NetSec
======

Network and Computer Forensic Tools

LiMDE ==> (Li)nux (M)emory and (D)rive (E)xtractor
* A BASH Script that:
* Compiles LiME (https://github.com/504ensicsLabs/LiME)
* Creates Linux profile for volatility (https://github.com/volatilityfoundation/volatility)
* Displays commandline to install LiME to capture memory locally or over network,
* Displays commandline to dd file locally or over network.
 
LiDE ==> (Li)nux (D)rive (E)xtractor
* A "C" project That:
* As of version 0.0.3.0 it has the same functionality as running a string of commands:
* "dd" to capture a file (more like cat though)
* pv "pipe viewer" to view the progress of the file transfer
* "netcat" to send the file over the network
* "md5sum" to report the unique file hash, in order to confirm a 100% good file transfer
* "ifconfig" to report the local IP address (currently hardcoded for eth0)
* All packaged into a small executable less than 19Kb in size.
** The following command could accomplish the same results:
* ifconfig | grep -A1 eth0 | grep inet | cut -f2 -d ":" | cut -f1 -d " " && md5sum File_to_Transfer && cat File_to_Transfer | pv | nc -l -p 31337

