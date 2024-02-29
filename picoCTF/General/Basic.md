
---
1. Obedient cat : Just opened the file to see the flag staring at me!
  
1. Wave a flag : ran an ELF64 executable
   ```
   ./warm -h
   ```
1. What's a netcat?: simple enough, just convert ascii back to text
```
import subprocess

cmd = ["nc", "mercury.picoctf.net","7449"]

process = subprocess.Popen(cmd, stdout=subprocess.PIPE, stderr=subprocess.PIPE, text=True)

lines = []

while True:
    line = process.stdout.readline().strip()
    lines.append(line)
    print(lines)
```
```
ans = ''
 

lol = ['112', '105', '99', '111', '67', '84', '70', '123', '103', '48', '48', '100', '95', '107', '49', '116', '116', '121', '33', '95', '110', '49', '99', '51', '95', '107', '49', '116', '116', '121', '33', '95', '102', '50', '100', '55', '99', '97', '102', '97', '125', '10']

for i in lol:
    ans += chr(int(i))

print(ans)
```
