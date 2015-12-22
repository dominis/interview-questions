# Interview Questisons

I mostly apply to devops / sysops / sys engineer / release engineer / automatization engineer jobs.


Here you can find my up to date [cv](https://docs.google.com/document/d/1L2Rh_oduCPS4CwVzUFeNnti9MCHpnKUa1OatkLU9Ni4/edit)


## List of questions:


- Difference between apache and nginx?

  https://www.digitalocean.com/community/tutorials/apache-vs-nginx-practical-considerations

- If you wanted to find the procedures that a Linux program executes, what tool could you use?

  http://linux.die.net/man/1/strace

- From the shell, what built-in function would you use to replace the current process with its argument(s)?

  http://linux.die.net/man/1/xargs

- What file would you edit if you wanted to change the ordering of which name systems are consulted?

  http://linux.die.net/man/5/resolv.conf

- What are the three types of messages issued while establishing a TCP connection?

  http://www.tcpipguide.com/free/t_TCPConnectionEstablishmentProcessTheThreeWayHandsh-3.htm

- In a reverse HTTP proxy, to which header is customary to add the remote IP address in the new request?

  https://en.wikipedia.org/wiki/X-Forwarded-For

- Which Elasticsearch API would you call to get the JVM versions of all running nodes?

  https://www.elastic.co/guide/en/elasticsearch/reference/current/cluster-nodes-info.html

- Describe how PXE works

  https://en.wikipedia.org/wiki/Preboot_Execution_Environment

- Talk aobut TFTP

  https://en.wikipedia.org/wiki/Trivial_File_Transfer_Protocol

- How would you change the `resolv.conf` on 20 machines in the same time?

  `for HOST in $(cat servers.txt ) ; do ssh $HOST "echo nameserver 1.1.1.1 > /etc/resolv.conf" ; done`

- How would you do this on thousands faster?

  `for HOST in $(cat servers.txt ) ; do ssh $HOST "echo nameserver 1.1.1.1 > /etc/resolv.conf" & ; done`
  http://unix.stackexchange.com/a/103734

- What tool would you use to change the existing line in `resolv.conf`?

  http://linux.die.net/man/1/sed

- You have 10 webservers how would you tell the top10 ip addresses from their access log

  For ten servers you can use the `for` loop above with this command: `awk '{ print $1 }' access.log | sort | uniq -c | sort -nr | head -10`

- How would you do that on thousands of servers

  Here you can talk about centralized log collection or event based logging
  http://www.rsyslog.com/
  https://www.elastic.co/webinars/introduction-elk-stack

- Talk about the major RAID types

  http://www.tonypickett.com/wp-content/uploads/2013/12/allraid.png

- What is a zombie process?

  https://en.wikipedia.org/wiki/Zombie_process

- What is an ephemeral port?

  https://en.wikipedia.org/wiki/Ephemeral_port

- What limits the maximum number of connections on a linux server?

  http://stackoverflow.com/a/2332756

- How netstat works?

  http://linuxcommand.org/man_pages/netstat8.html

- How traceroute works?

  https://ccieblog.co.uk/basic-troubleshooting-commands/how-does-traceroute-work

- What process has PID 0 and PID 1?

  http://unix.stackexchange.com/a/145581

- What is `/proc`?

  http://linux.die.net/man/5/proc

- What is the difference between ext2 ext3 and ext4 filesystems?

  http://www.thegeekstuff.com/2011/05/ext2-ext3-ext4/

- Why is a battery on a RAID controller?

  http://serverfault.com/a/203361

- How would you fix `chmod a-x -Rf /bin`?

  http://unix.stackexchange.com/questions/83862/how-to-chmod-without-usr-bin-chmod
