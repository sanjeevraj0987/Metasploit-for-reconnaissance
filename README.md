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



https://user-images.githubusercontent.com/121148715/244914190-09a5a034-e2b2-4100-a600-2994f2892c99.png











## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
