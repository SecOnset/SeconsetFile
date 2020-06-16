---
title: 'CTFLearn-The adventures of Boris Ivanov. Part 1.'
date: '2020-01-07'
author: 'Pratyaksh Singh'
background: 'https://raw.githubusercontent.com/SecOnset/SeconsetFile/master/writeups_pratyaksh/CTFLearn/CTFLearn%20SS/The%20adventures%20of%20Boris%20Ivanov.%20Part%201./wall.jpg'
description:
  'CTFlearn is an ethical hacking platform that enables tens of thousands to learn, practice, and compete. Here in this challenge we are going to have a look on a forensics based problem.'
SEO: 'Cybersecurity,Forensics, forensics investigation, hacking, cyber, binwalk,stego,steganography,stegsolve,foremost ,CTFlearn, CTF, Capture the flag'
---

Today we are going to solve yet another challenge of CTFLearn. Let us go ahead and straight away dive into it.

First we go through the statement.

![Cybersecurity,Forensics, forensics investigation, hacking, cyber, binwalk,stego,steganography,stegsolve,foremost ,CTFlearn, CTF, Capture the flag](https://raw.githubusercontent.com/SecOnset/SeconsetFile/master/writeups_pratyaksh/CTFLearn/CTFLearn%20SS/The%20adventures%20of%20Boris%20Ivanov.%20Part%201./Ques.png)


[Link to the Question](https://ctflearn.com/challenge/373) 

[Link to the mega resource](https://mega.nz/#!HfAHmKQb!zg6EPqfwes1bBDCjx7-ZFR_0O0-GtGg2Mrn56l5LCkE)

![Cybersecurity,Forensics, forensics investigation, hacking, cyber, binwalk,stego,steganography,stegsolve,foremost ,CTFlearn, CTF, Capture the flag](https://raw.githubusercontent.com/SecOnset/SeconsetFile/master/writeups_pratyaksh/CTFLearn/CTFLearn%20SS/The%20adventures%20of%20Boris%20Ivanov.%20Part%201./Boris_Ivanov_1.jpg)

Let us see what we can find in the meta-data of the image file, we just downloaded.


![Cybersecurity,Forensics, forensics investigation, hacking, cyber, binwalk,stego,steganography,stegsolve,foremost ,CTFlearn, CTF, Capture the flag](https://raw.githubusercontent.com/SecOnset/SeconsetFile/master/writeups_pratyaksh/CTFLearn/CTFLearn%20SS/The%20adventures%20of%20Boris%20Ivanov.%20Part%201./Exiftdata.png)


Looking at the image we can see a very distorted strip on the bottom of the image. I'll use a tool called [stegsolve](https://github.com/zardus/ctf-tools/tree/master/stegsolve) to check whether we find anything into the file.

Anayzing the image with the "Stereogram Solver" option and moving the image to "offset 102" we can find the flag, on the bottom strip of the image.

![Cybersecurity,Forensics, forensics investigation, hacking, cyber, binwalk,stego,steganography,stegsolve,foremost ,CTFlearn, CTF, Capture the flag](https://raw.githubusercontent.com/SecOnset/SeconsetFile/master/writeups_pratyaksh/CTFLearn/CTFLearn%20SS/The%20adventures%20of%20Boris%20Ivanov.%20Part%201./Soln.png)

Flag: **flag{d0nt_mes5_wit3_th3_KGB}**




