![!\[alt text\](image.png)](<screenshots/bypass password.png>)

step 1:analyze the file

i open in ghidra but it seems there's no lead so i try to analyze using DIE and the binary file is compiled in python program

step 2:extract 

```powershell
.\pyinstxtractor.py .\gatekeeper
pycdas chall.pyc
```

step 3:analyze the code

further analyze it seems that the password is C0DE_1S_AW3S0ME so i run the binary and input the password and got the flag

```bash
✦ ❯ ./gatekeeper
==============================
      GATEKEEPER v1.0
==============================
[?] Enter password to open the gate: C0DE_1S_AW3S0ME
[*] Verifying Stage 1...
[+] Stage 1 passed!
[*] Verifying Stage 2 (Anti-Debugging)...
[+] Anti-Debugging check passed.
[*] Verifying static password parts...
[+] All password checks passed!
[*] Verifying Stage 3 (Cryptography)...
[+] Decryption complete.

========================================
      THE GATE IS OPEN! FLAG ACQUIRED!
========================================

Your Flag is: n3xt{C0DE_1S_CHALLE^GE}
```
flag:n3xt{C0DE_1S_CHALLE^GE}
