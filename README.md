# Zen Lake Architecture

Using a 10-year-old PC (HP ProDesk 600 G2 SF), we successfully computed 50 billion digits of π in 22 hours using y-cruncher.  
This is a practical guide to achieving stable, reproducible π computations up to 100 billion digits on low-cost hardware.  
(*Note: Calculations beyond 100 billion digits may require additional SSDs and, in some cases, RAM upgrades.)

High-precision computation is no longer exclusive to supercomputers or corporations.  
It is now within reach for individuals.  
This architecture was designed and refined through collaboration between a human and AI Copilot.

---

## ⚠️ Important Notice Before Use

This project places extremely high stress on SSD, RAM, and CPU.  
We take no responsibility for hardware damage. Use entirely at your own risk.

- Heavy use of virtual memory (Swap)  
- Potential impact on SSD lifespan  
- Increased heat and power consumption during long computations  

---

## 🧰 Example Hardware Configuration

- PC: HP ProDesk 600 G2 SF (Small Form Factor)  
- CPU: Intel Core i3-6100 (2 cores, 4 threads)  
- RAM: 16GB DDR4  
- USB SSD: 500GB (up to 500MB/sec)  
- Internal SSD: 125GB (SATA)  
- OS: Windows 10 (64-bit)  

---

## 💾 Storage Layout & Virtual Memory Settings

**G: USB SSD 500GB**  
- NTFS format (cluster size: 64KB)  
- Virtual memory (Swap): 24GB  
- y-cruncher executable placed here  

**C: Internal SSD 125GB**  
- OS (Windows 10)  
- Virtual memory (Swap): 24GB  

---

## 🧠 Execution Flow (Swap Mode)

1. Set virtual memory to 24GB on both G: and C:  
2. Launch y-cruncher from G: via “Right-click → Run as administrator”  
3. During execution, RAM and Swap are used together, placing high load on SSD  
4. Upon completion, results are saved  

---

## 🪷 Philosophy & Poetic Structure

> “The lake where π swims is made of 64KB grains.  
> When the grains align, the waves calm, and computation flows beautifully.  
> Two lakes—one supports the OS, the other receives π.  
> Their harmony sustains the 22-hour dance.”

---

## 📘 For Education & Reproducibility

- This setup is designed to be reproducible by students and researchers worldwide  
- You can experiment by varying SSD types, RAM capacity, and Swap settings  
- Cluster size and virtual memory configuration are key to stability and reproducibility  

---

## 🔗 About y-cruncher

This project uses y-cruncher, a high-precision constant calculator developed by Alex Yee.  
It is used here for non-commercial, educational purposes within the bounds of its official license.  
For more information and downloads, visit the official site:  
https://www.numberworld.org/y-cruncher/
