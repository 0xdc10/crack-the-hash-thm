# Crack the hash

## Resources
- hashid
- hash-identifier
- [https://www.tunnelsup.com/hash-analyzer/](https://www.tunnelsup.com/hash-analyzer/)
- [https://dcode.fr](https://dcode.fr)
- [https://hashcat.net/wiki/doku.php?id=example_hashes](https://hashcat.net/wiki/doku.php?id=example_hashes)


## Level 1

### 48bb6e862e54f2a795ffc4e541caed4d
- md5
- hashcat -m 0 -a 0
- rockyou
- Answer: easy

### CBFDAC6008F9CAB4083784CBD1874F76618D2A97 
- sha1
- hashcat -m 100 -a 0
- rockyou
- Answer: password123

### 1C8BFE8F801D79745C4631D09FFF36C82AA37FC4CCE4FC946683D7B336B63032
- sha256
- hashcat -m 1400 -a 0
- rockyou
- Answer: letmein

### $2y$12$Dwt1BZj6pcyc3Dy1FWZ5ieeUznr71EeNkJkUlypTsgbX1H68wsRom
- bcrypt
- hashcat throws memory insufficient
- HINT: `filter rockyou for 4 letter words
- filtered using grep: `grep -P '^.{4}$' rockyou.txt > rockyou-len4.txt`
- cracked in 1min 43sec: `bleh`

### 279412f945939ba78ce0758d3fd83daa
- MD4
- hashcat -m 900 didn't work on CPU
- decoded using [https://dcode.fr](https://dcode.fr)
- Ans: `Eternity22`

## Level 2

### F09EDCB1FCEFC6DFB23DC3505A882655FF77375ED8AA2D1C13F640FCCC2D0C85
- SHA256
- hashcat -m 1400
- `paule`

### 1DFECA0C002AE40B8619ECF94819CC1B
- NTLM
- hashcat -m 1000
- `n63umy8lkf4i`

### $6$aReallyHardSalt$6WKUTqzq.UQQmrm0p/T7MPpMbGNnzXPMAXi4bJMl9be.cfi3/qxIf.hsGpS41BqMhSrHVXgMpdjS6xeKZAs02.
- sha512crypt : $6$
- hashcat -m 1800
- `waka99`

### e5d8870e5bdd26602cab8dbe07a942c8669e56d6
- salt: tryhackme
- hmac-sha1
- hashcat -m 110
- `481616481616`
 

