## What is 316CTF?

316CTF is an educational “capture‑the‑flag” (CTF) platform created by Anderson University.  It presents a series of short, self‑contained cybersecurity puzzles that you solve to capture a “flag” (a string enclosed in curly braces, e.g., `{FLAG}`).  You’ll earn points for each flag and can see how your progress compares on a scoreboard.  Our class will use this platform in and out of class; you’ll have opportunities to work individually or in teams, and we’ll review interesting solutions together.

Site Link: https://play.316ctf.com/

You'll need to register for an account. Your chosen username WILL BE PUBLIC. Check out [Creating Your Hacker Name](Creating_Your_Hacker_Name.md) to help guide you in creating a safe and fun username.

## Challenge categories

### 1. Password Cracking

These puzzles teach you about digital hash functions and the basics of password cracking.  Some challenges give you a hashed password and ask you to recover the original.  For example, the “Maryland” series uses MD5 hashes, while the “SHArkba1t! Ooh ha ha!” series introduces the SHA‑1 algorithm and explains how it differs from MD5.  You will learn how to use dictionaries, brute‑force attacks and online resources to crack simple hashes, and you’ll gain appreciation for why good password hygiene and strong hashing are so important.

### 2. Crypto

The Crypto category focuses on classic ciphers, encoding schemes and other “by‑hand” cryptography.  Early challenges ask you to reverse text or apply simple Caesar ciphers, e.g., one puzzle presents the reversed string “sllihtoof si galf ehT” and asks for the original flag.  Others use ROT‑1 or ROT‑n substitutions (“Uif gmbh jt Cfbujuveft”), binary‑to‑decimal conversions (“Convert 10 from binary to decimal”) or more complex systems like the Vigenère cipher.  Working through these problems builds your ability to recognise and decode different types of encodings and lays a foundation for modern cryptography topics.

### 3. Find Stacy

In this unique category you are given a photograph taken by “Stacy” and must identify where the photo was taken.  The first challenge introduces the theme and asks: “What zip code is Stacy at in this photo?”.  You’ll practice reverse‑image searching, analysing landmarks, reading subtle visual clues and using online maps to geolocate the picture.  It’s a fun way to learn about digital geolocation and shows how much information is hidden in ordinary photographs.

### 4. OSINT (Open‑Source Intelligence)

OSINT challenges test your ability to research and piece together information from publicly available sources.  Some puzzles resemble “security questions”: one asks for the middle name of Brandon Grech, the CTF organiser.  Others give you a picture of a landmark and ask who it’s named after.  You may need to search social media, public records, maps or websites to answer questions.  This category teaches critical research skills, awareness of digital footprints and the importance of verifying information.

### 5. Web

Web challenges introduce basic web reconnaissance and data retrieval.  In the first “Book” challenge, the author explains that he has hidden four flags on his `100linuxcommands.com` website and tells you to scan or scrape the site—but **not** to log in or launch denial‑of‑service attacks.  You’ll learn to view page source, crawl directories, understand HTTP requests and avoid breaking rules.  These skills form the basis of ethical web reconnaissance and vulnerability assessment.

### 6. Network Analysis

These problems teach you to examine network traffic and metadata.  For example, the “Starter PCAP” series provides packet‑capture (PCAP) files and asks simple questions like “How many packets are in this pcap file?”, pushing you to open the file with Wireshark and explore the packet list.  Other tasks have you determine the hosting provider for the CTF website or differentiate between URLs and IP addresses.  Through these exercises you’ll gain familiarity with network protocols, packet inspection, and how to extract useful information from network captures.

---

### Tips

* **Work methodically.** Read the challenge description carefully and start with the easiest puzzles in each category.
* **Document your steps.** Especially for OSINT and Find Stacy tasks, keep notes; some later challenges build on earlier findings.
* **Use online tools wisely.** For cryptography, websites like [CyberChef](https://gchq.github.io/CyberChef/) can help decode text; for geolocation, try reverse‑image search and map services; for PCAPs, use [Wireshark](https://www.wireshark.org/).
* **Stay ethical.** Never attempt to compromise any real system without permission.  316CTF challenges are designed to be solved legally.

By exploring these categories, you’ll build a strong foundation in several areas of cybersecurity and gain problem‑solving skills that will serve you well in future competitions. Enjoy the hunt!
