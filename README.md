# censys_anonftp-scan

# FTP Anonymous Recon – OSINT Using Censys

This repository show cases how i explored the  **Censys** to identify **FTP servers that allow anonymous login**. This misconfiguration is commonly seen and can be dangerous if left unnoticed. This hands-on practice helped me understand real-world enumeration and open-source intelligence (OSINT) techniques.

---

## What is Censys?

[Censys](https://search.censys.io) is an internet-wide scanning engine that collects and indexes data from internet-connected systems, such as banners, SSL certificates, and service metadata. It allows researchers, red teamers, and defenders to perform OSINT (Open Source Intelligence) by searching for exposed services or misconfigured devices.

---

##  Objective

The goal of this project is to:
- Use **Censys search queries** to find FTP servers with anonymous login enabled.
- Connect to one or more of these servers using the `ftp` command.
- Verify access by listing files and downloading one if allowed.
- Demonstrate how small misconfigurations can become major security issues.

---

## Censys Search Query Used

To find servers that expose FTP banners allowing anonymous access, I used this search query:

```
services.service_name: "ftp" AND services.ftp.banner: "anonymous"
```
## Steps
1. Identified Target:
   - From the results, I selected an IP address that responded with a 220 FTP banner indicating anonymous access.

2. Connected via FTP:
   - In my terminal:
     ftp <target_ip>
   - When prompted:
     Username: anonymous
     Password: [press Enter]

3. Listed Directory Contents:
   - ls

4. Downloaded a File (if allowed):
   - get example.txt

##  Reference Notes

You can view my full notes and step-by-step demonstration in the following PDF:

[📄 Censys.pdf](https://github.com/khajaazhar/censys_anonftp-scan/blob/main/Censys.pdf)

## About Me
 Khaja Azhar Uddin 
 [LinkedIn – Khaja Azhar](https://www.linkedin.com/in/khajaazhar)
