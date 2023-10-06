# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:
## program:
Find out the ip address of the attackers system
## OUTPUT:
![244913964-1f538f40-f876-4459-8677-8dfbac405ba8](https://github.com/sanjeevraj0987/Metasploit-for-reconnaissance/assets/120698946/539fc41a-6e97-4cea-98b5-4433ef8a2449)
## Invoke msfconsole:

## OUTPUT:
![244913998-953379bc-27c4-4e87-9702-3316dfb7c3ef](https://github.com/sanjeevraj0987/Metasploit-for-reconnaissance/assets/120698946/467dc4fd-093f-4e1f-8731-2008f96440e5)
Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.



## OUTPUT:
Port Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000

## OUTPUT:
![244914060-c0cf7ce9-74cc-4c75-8e07-dd3785c52086](https://github.com/sanjeevraj0987/Metasploit-for-reconnaissance/assets/120698946/10f3263a-86a3-4845-91ac-d7d34b627a9f)
Step4: use the db-nmap command to scan and save the results into Metasploit's postgresql attached database. In that way, you can use those results in the exploitation stage later.
scan the targets with the command db_nmap as follows. msf > db_nmap 192.168.181.0/24

## OUTPUT:
Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l

## OUTPUT:
![244914146-99aca0dd-3fd0-4380-904c-773475effa74](https://github.com/sanjeevraj0987/Metasploit-for-reconnaissance/assets/120698946/4a0be091-e2c6-44b9-b88b-48b097057513)
Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit
![244914160-616d4518-88b6-4b8f-80eb-c0c6e16df08a](https://github.com/sanjeevraj0987/Metasploit-for-reconnaissance/assets/120698946/3423610a-b088-4c4f-a26e-fe05a39700db)
The info command provides information regarding a module or platform
## OUTPUT:
![244914190-09a5a034-e2b2-4100-a600-2994f2892c99](https://github.com/sanjeevraj0987/Metasploit-for-reconnaissance/assets/120698946/a65b5575-376f-4aa6-a697-2946ae5c6884)
Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows: systemctl start postgresql msfdb init ##MYSQL ENUMERATION Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>
![244914204-4357ed6f-62a5-4adb-ad5c-fee8dffdfd7b](https://github.com/sanjeevraj0987/Metasploit-for-reconnaissance/assets/120698946/d66508d9-ec51-4040-9c14-dfce8fcb019d)
Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql
![244914215-5dd2edca-fd00-45b3-956e-8dd5fe41465a](https://github.com/sanjeevraj0987/Metasploit-for-reconnaissance/assets/120698946/8e937214-69e3-4f99-8b20-4cad8e710cec)
use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version
![244914222-8f9525da-1a5b-4498-8f41-8ef701adb2d9](https://github.com/sanjeevraj0987/Metasploit-for-reconnaissance/assets/120698946/19b0ca87-95e8-4b63-b8b6-a538732a5100)
Use the set rhosts command to set the parameter and run the module, as follows:
![244914227-57882379-ea28-4349-a3dc-ecea7bb10dea](https://github.com/sanjeevraj0987/Metasploit-for-reconnaissance/assets/120698946/ef6b13d6-fb44-4bea-ab03-adfdcc6ec2ae)
After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.

![244914264-7234a9cb-8baf-485c-b743-f6c6250dded8](https://github.com/sanjeevraj0987/Metasploit-for-reconnaissance/assets/120698946/d80ed536-c400-4163-8f3d-4d16657c1a23)
set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true

![244914270-752e39b3-a594-4e46-b60e-1bb7a0ff9d5d](https://github.com/sanjeevraj0987/Metasploit-for-reconnaissance/assets/120698946/c793c641-49bd-42db-938d-181ad8ae3757)

## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
