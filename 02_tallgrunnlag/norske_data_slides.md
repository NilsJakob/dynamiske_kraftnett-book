---
title: Tallgrunnlag i det norske kraftsystemet
---

# Tallgrunnlag (Norge)

Vi ser på:
- Lastnivå
- Produksjon
- Variasjon over tid

---

# Nøkkeltall (Norge)

- Installert effekt: ~40–45 GW  
- Toppforbruk: ~25 GW  
- Normal last: 10–20 GW  
- Frekvens: 50 Hz  

---

# Typisk døgnprofil (Norge)

```{code-cell} python
import numpy as np
import matplotlib.pyplot as plt

# Tid (timer i ett døgn)
t = np.linspace(0, 24, 200)

# Typisk norsk lastprofil (syntetisk, realistisk form)
load = 15 + 5*np.sin(2*np.pi*(t-7)/24) + 3*np.sin(2*np.pi*(t-17)/24)

plt.figure()
plt.plot(t, load)
plt.xlabel("Tid [timer]")
plt.ylabel("Last [GW]")
plt.title("Typisk lastprofil i Norge (døgn)")
plt.grid()
plt.show()