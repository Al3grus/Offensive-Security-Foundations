# Offensive Security Foundations

An open-source, self-study curriculum that builds the computer-science and security foundation behind offensive security, using only free and public materials.

Every course follows the same shape: **🎥 teaching → 📖 reference → 🧪 practice**.

<details>
<summary><strong>Legend</strong> (click to expand)</summary>

| | |
|---|---|
| ⬜ 🟨 ✅ | Course status: not started, in progress, done (edit the emoji in the title) |
| 🎥 | Lectures to watch (the teaching) |
| 📖 | Book or notes (the reference, read alongside the lectures) |
| 🧪 | Labs and challenges (the practice) |
| ⏱️ | Estimated time |
| 📝 | Link to your own notes or write-up: your evidence the course is done |

</details>

**Order:** courses are numbered in the order to take them: easiest first, each one building on the last, and the most relevant to red teaming as early as prerequisites allow. If you stop part-way, what's done is what matters most.

> **Rule:** never publish solutions to course labs, PEN-200, or active HTB machines. Write about concepts, not answers.

---

### ⬜ 0. Programming in Python

> Most security tooling and scripting is Python. Skip this if you already program.

- 🎥 [CS50P](https://cs50.harvard.edu/python/) (Harvard, free)
- 🧪 CS50P problem sets (auto-checked with check50)
- ⏱️ ~50 hours
- 📝 Notes: _add link_

---

### ⬜ 1. The Missing Semester of Your CS Education (MIT)

> Everything you do on an engagement happens in a terminal: moving around systems, scripting, reading logs, using git. This gives you that fluency first so it never slows the later courses down.

- 🎥 [Lecture videos](https://missing.csail.mit.edu/) (shell, scripting, vim, git, debugging; each lecture has exercises)
- ⏱️ ~25 hours
- 📝 Notes: _add link_

---

### ⬜ 2. Programming in C

> Exploits, kernels, malware and most of the tools you will read are written in C. You need to read it comfortably before you can understand how memory bugs work.

- 🎥 [CS50x weeks 1 to 5](https://cs50.harvard.edu/x/) (C, arrays, algorithms, memory, data structures)
- 📖 Kernighan & Ritchie, *The C Programming Language*, 2nd ed. (paid)
- 🧪 CS50x problem sets for weeks 1 to 5 (auto-checked with check50)
- ⏱️ ~60 hours
- 📝 Notes: _add link_

---

### ⬜ 3. Computer Networks

> Recon, pivoting and tunnelling are all networking. You also need to know what your traffic looks like on the wire, because that is what defenders see.

- 🎥 [Kurose & Ross lectures](https://gaia.cs.umass.edu/kurose_ross/online_lectures.htm) (one video per textbook section)
- 📖 Peterson & Davie, [*Computer Networks: A Systems Approach*](https://book.systemsapproach.org/) (free)
- 📖 [Beej's Guide to Network Programming](https://beej.us/guide/bgnet/) (free, for the project)
- 🧪 Practice
  - [ ] [Wireshark Labs](https://gaia.cs.umass.edu/kurose_ross/wireshark.php)
  - [ ] Project: write an HTTP/1.1 server in C
- ⏱️ ~120 hours
- 📝 Notes: _add link_

---

> **Checkpoint 1: switch to OSCP.** After course 3, OSCP prep becomes the main work: HTB Academy (Windows and AD), the TJ Null / Lainkusanagi list, Proving Grounds, then PEN-200.

---

### ⬜ 4. Computer Systems (CMU 15-213)

> How programs really run: memory, the stack, assembly, how the CPU executes code. The Bomb Lab is reverse engineering and the Attack Lab is writing buffer-overflow and ROP exploits. This is the course that turns you from someone who runs exploits into someone who understands them.

- 🎥 [UW CSE 351 lecture videos, Summer 2023](https://courses.cs.washington.edu/courses/cse351/23su/videos) (61 public videos teaching the CS:APP material; CMU's own recordings are not public)
- 📖 Bryant & O'Hallaron, *Computer Systems: A Programmer's Perspective*, 3rd ed. (paid, worth buying)
- 🧪 [CS:APP labs](https://csapp.cs.cmu.edu/3e/labs.html)
  - [ ] Data Lab
  - [ ] Bomb Lab
  - [ ] Attack Lab
  - [ ] Cache Lab
  - [ ] Malloc Lab
  - [ ] Shell Lab
  - [ ] Proxy Lab
- ⚠️ Attack Lab targets need the `-q` flag. There's no autograder, so write your own tests.
- ⏱️ ~175 hours
- 📝 Notes: _add link_

---

### ⬜ 5. Computer Security (Berkeley CS161)

> The attacker mindset applied to real targets: memory corruption, web attacks, authentication flaws. OSCP teaches you to use these attacks; this course teaches why they work, so you can adapt them when the known tool fails. It builds on the Attack Lab from course 4, and its practice overlaps with OSCP prep, so it fits alongside or just after it.

- 🎥 [CS161 lectures](https://fa26.cs161.org/) (YouTube, linked from the schedule)
- 🎥 [KU Leuven Web Security Fundamentals](https://www.edx.org/learn/computer-security/ku-leuven-web-security-fundamentals) (edX, free to audit)
- 📖 [CS161 textbook](https://textbook.cs161.org) (free)
- 🧪 Practice
  - [ ] [pwn.college Program Security](https://pwn.college/program-security/) (videos plus challenges: memory errors, reverse engineering, ROP, heap)
  - [ ] [Georgia Tech CS6265 tutorials](https://tc.gts3.org/cs6265/tut/index.html) Tut01 to Tut06
  - [ ] [PortSwigger Web Security Academy](https://portswigger.net/web-security) (XSS, CSRF, SQLi, SSRF paths)
- ⏱️ ~200 hours
- 📝 Notes: _add link_

---

> **Checkpoint 2: OSCP done.** Courses 1 to 5 are the full pentester foundation. 6 to 9 are red-team depth: reverse engineering, crypto, vulnerability research, kernel. Do them after OSCP, in parallel with CRTO.

---

### ⬜ 6. Reverse Engineering and Malware Analysis (OpenSecurityTraining2)

> Red teams must understand what the binaries they drop look like to defenders and EDR. Reverse engineering and malware analysis are the base for evasion work later.

- 🎥🧪 [OST2 Reverse Engineering & Malware Analysis path](https://ost2.fyi/) (free, video classes with built-in exercises)
- 📖 [CyLab Academy Reversing guide](https://cylabacademy.org/learning_guides/Book-6-Reversing.pdf) (free)
- ⏱️ ~150 hours
- 📝 Notes: _add link_

---

### ⬜ 7. Cryptography (Stanford Cryptography I)

> Red teams break weak crypto: forged tokens, bad TLS, Kerberos tickets.

- 🎥 [Cryptography I, Dan Boneh](https://www.coursera.org/learn/crypto) (Coursera, free to audit; teaches the number theory it needs in Module 5)
- 📖 Boneh & Shoup, [*A Graduate Course in Applied Cryptography*](https://toc.cryptobook.us/) (free)
- 📖 Mike Rosulek, [*The Joy of Cryptography*](https://joyofcryptography.com) (free)
- 🧪 Practice
  - [ ] Coursera weekly problem sets
  - [ ] [cryptopals](https://cryptopals.com) sets 1 to 6
- ⏱️ ~100 hours
- 📝 Notes: _add link_

---

### ⬜ 8. Secure Software Systems (MIT 6.858)

> Fuzzing, symbolic execution and sandbox escapes are how you find new vulnerabilities instead of only using known ones. This is the step towards vulnerability research and custom tooling.

- 🎥 [MIT 6.858 lectures, Fall 2014](https://ocw.mit.edu/courses/6-858-computer-systems-security-fall-2014/) (OCW)
- 📖 [MIT 6.858 2026 lecture notes](https://css.csail.mit.edu/6.858/2026/schedule.html) (free)
- 🧪 Practice
  - [ ] [MIT 6.858 2026 labs](https://css.csail.mit.edu/6.858/2026/schedule.html): buffer overflows, privilege separation, symbolic execution, browser security, HTTPS
  - [ ] [Georgia Tech CS6265](https://tc.gts3.org/cs6265/tut/index.html) Tut09 to Tut10 (heap, fuzzing, symbolic execution)
- ⏱️ ~200 hours
- 📝 Notes: _add link_

---

### ⬜ 9. Operating Systems (MIT 6.1810)

> Rootkits, EDR evasion and privilege escalation all live in the kernel. Building a small OS is the clearest way to understand processes, memory and system calls from the inside.

- 🎥 [MIT 6.S081 lectures, 2021 schedule](https://pdos.csail.mit.edu/6.S081/2021/schedule.html) (YouTube videos linked per lecture)
- 📖 [xv6 book](https://pdos.csail.mit.edu/6.1810/xv6) (free)
- 📖 [*Operating Systems: Three Easy Pieces*](https://pages.cs.wisc.edu/~remzi/OSTEP/) (free)
- 🧪 [MIT 6.1810 labs](https://pdos.csail.mit.edu/6.1810/2025/schedule.html) (each lab has a `make grade` test suite)
  - [ ] util
  - [ ] syscall
  - [ ] pgtbl
  - [ ] traps
  - [ ] cow
  - [ ] net
  - [ ] lock
  - [ ] fs
  - [ ] mmap
- ⏱️ ~150 hours
- 📝 Notes: _add link_

---

## Throughout

- [ ] 🧪 [picoCTF / CyLab Security Academy](https://cylabacademy.org/): CTF challenges alongside each matching course

---

## Career Track (parallel)

| Done | Cert / Training | When | Cost (Oct 2026) |
|---|---|---|---|
| ⬜ | eJPT | Optional warm-up | $299 |
| ⬜ | HTB Academy Windows & AD, TJ Null / Lainkusanagi list, Proving Grounds | After course 3 | Subscriptions |
| ⬜ | OSCP (PEN-200) | After course 4 | $1,749 bundle |
| ⬜ | 🎥 [MITRE ATT&CK trainings](https://attack.mitre.org/resources/learn-more-about-attack/training/): Fundamentals + [Adversary Emulation](https://attack.mitre.org/resources/learn-more-about-attack/training/adversary-emulation/) | Before CRTO | Free |
| ⬜ | CRTO (Zero-Point Security) | After course 5 | £399 |

---

## Credits

Course structure based on the security path through [Carnegie Mellon University's B.S. in Computer Science](https://coursecatalog.web.cmu.edu/schools-colleges/schoolofcomputerscience/undergraduatecomputerscience/computer-science-bs/index.html) and its [Security and Privacy concentration](https://s3d.cmu.edu/education/undergrad-programs/secpriv). Materials from CMU, MIT, Harvard, Stanford, UC Berkeley, Georgia Tech, Arizona State, KU Leuven, OpenSecurityTraining2 and the other linked authors. Not affiliated with any of them.

*Last updated: October 2026.*
