# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.

# Program:
```
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```

# Calculation:
![WhatsApp Image 2025-10-03 at 20 38 39_6dea1687](https://github.com/user-attachments/assets/472977e7-1944-4a8c-a476-14043832cd4d)
![WhatsApp Image 2025-10-03 at 20 38 40_59c7fe8a](https://github.com/user-attachments/assets/928ae91e-54ca-46bb-b729-d9f3f4a98342)
![WhatsApp Image 2025-10-03 at 20 38 40_0857ea4e](https://github.com/user-attachments/assets/5d8e96b1-afce-4a12-8687-d9d18df0dab8)

# Output
<img width="324" height="144" alt="image" src="https://github.com/user-attachments/assets/073bee88-8cd4-423c-825e-335d0f174093" />

# Results:
Hence the average code word length, entropy, variance, redundancy, and efficiency are found for {0.55,0.15,0.15,0.1,0.05} usinf huffman
