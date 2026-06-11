---
title: "Why Terminal-Based Development Is Best For Me"
date: 2026-06-11T16:58:29-04:00
draft: false
desctiption: ""
tags: ["linux", "productivity", "discuss", "python"]
showToc: true
TocOpen: false
comments: true
---

One day, I was working on a Python project. I had my 'reliable and speedy' Windows and my 'fast and optimized' VS Code. But, the only issue with this, is that those adjectives, are false. To have three browser tabs and one VS Code window open at the same time was like a death wish to my 16GB of RAM. And, as you may have guessed, this wasn't just 'one day', but rather, every single time I wanted to do any sort of development in the Microsoft ecosystem (minus the browser, I viewed Microsoft Edge as terrible and Chrome as just the only replacement, despite its lag).

At that rate, imagine how slow it was for me to code. I was running the newest Windows, the newest VS Code, didn't have any unnecessary background apps, and followed every single 'secret' step to 'optimize' and 'speed up' Windows and its associated applications. I was doing everything right, but it still was too slow. Oftentimes, a large portion of my 16GB of RAM, was used simply by thousands of background services that added up to use a large amount of memory.

So, approximately three months ago, on March 10th, 2026, I decided to experiment with dual-booting a Linux distribution on my main computer. I shrunk my Windows partition with the Disk Management application and proceeded to allocate around 300GB of space on my 1TB SSD (solid-state drive) for Debian 13.3, (Trixie), a Linux distribution notable for its stability, large software repository, extensive architecture support, strict free and open source software (FOSS) philosophy, and upgrade reliability. And, so far, I have only used 62GB of space on the 300GB partition, meaning that I could have been very comfortable with 100GB. This data usage is including large media files.

I originally thought I would only use Linux as a side project or hobby, and that I would often boot to Windows, too. But, two facts made me never boot Windows again with the intent to use it for purposes other than data collection. Those facts are:

1. I have never experienced lagginess on Linux that I deemed to not have a reasonable cause.
2. It was not as hard to use as I thought it would be.

To elaborate more on fact two, at least to me, the complexity of Linux is decided by your Desktop Environment (DE). On Windows, you are locked down to one Desktop Environment (DE) that can be very laggy, but is extremely simple to use for basic tasks. On the other hand, Linux generally allows users to choose their own Desktop Environment (DE), with the exception being certain immutable distributions and Operating Systems like Android OS and Chrome OS (yes, they rely on Linux). On Linux, users can choose themselves the correct balance between accessibility, usability, and speed for their specific circumstances by making an educated choice on which Desktop Environment (DE) to utilize.

I originally tried my best to find the 'perfect', light-weight IDE for Linux. I tried [Sublime Text](https://www.sublimetext.com/), and I was fine with it for a while. But, I eventually decided to strip out the IDE, and instead, simply code in the terminal.

When using the terminal to code via a code or text editor (like micro or nano), the tools you write code with generally do not significantly contribute to the resource usage of your computer, with the exception of certain advanced code analysis tools to prevent security, speed, and other issues or errors, along with certain other applications. For example, if you can have 5 browser tabs open without any lag, adding on something like micro will not make your experience any more laggy.

With my new development workflow, I am able to code—minus the lag. I can have 10 different terminal tabs open, and it's not even as hard on my laptop as resting a feather on its lid, (figuratively). It's 2 cents compared to the resource utilization on the rest of the computer.

And, my choice of using Linux also greatly contributed to reduced lag when using my computer, both in general and in development workflows, —in addition to utilizing terminal based code editing. Because of Linux's open-source nature, every single line of code is scrutinized by the public, and every issue is eventually caught and handled (if you are going to comment about copy fail and similar issues, it was in fact, eventually fixed). On the contrary, Windows' proprietary nature allows for extreme telemetry and non-optimization, despite their claims of speed. Windows is even thinking about utilizing more system resources—instead of actually optimizing—to make the Windows experience faster.

## My General Workflow for Making Python Projects on Linux While Utilizing the Terminal

- I generally use the micro code editor or the nano text editor, both terminal-based applications.
- I may have the Firefox FOSS (free and open-source) web browser open to a documentation page or a forum of some sorts. Web browsers like [Google Chrome](https://www.google.com/chrome/), [Apple Safari](https://www.apple.com/safari/), and [Microsoft Edge](https://www.microsoft.com/en-us/edge/?ep=0&form=MA1403&es=325&cs=1301686474) are not FOSS (free and open-source).
- Now that I have started my Python project [devto-followers2md](https://github.com/tyleruploads/devto-followers2md/tree/main), I have recently started checking my code with [Ruff](https://docs.astral.sh/ruff/), a fast Rust-based Python linter and code formatter. I also started using [pyright](https://github.com/microsoft/pyright), (yes, I know it is very ironic, it is made by Microsoft), and will be working on making sure the project aligns with its standards too.

## The Final Anecdote (for now)
Due to Windows' confusing file storage locations (including Microsoft OneDrive), I was forced to boot Windows in order to recover my coding folder that was not visible when I decrypted my Windows partition with my [BitLocker](https://support.microsoft.com/en-us/windows/bitlocker-drive-encryption-76b92ac9-1040-48d6-9f5f-d14b3c5fa178) recovery key. I tried to copy it to my Google Drive account, but it was transferring at a rate close to **ZERO** megabits per second, so that was a no go. I tried to transfer to a flash drive that generally works just fine, and it said my 16GB or so of data would take 16 hours, then 20 hours, then just weeks to copy. That, also, was not going to work. It turns out that the Antivirus system, [BitDefender](https://www.bitdefender.com/en-us/), completely crashed, on every level. Because Windows does not allow the administrator to force kill the antivirus process or its associated programs, the antivirus GUI dashboard and control center hung and never closed due to the crash of its antivirus process. Possibly, the antivirus software was attempting to scan files when it was not able to, causing this issue. I eventually was able to transfer it (very slowly), with the terminal!

## Conclusion
While I switched from Windows to Linux and greatly benefited from it, I acknowledge that it is not the right move for everyone. People may be locked into it because of their jobs, or they may have a certain circumstance making Linux not the best for their specific workflow. And, of course, I acknowledge macOS, too. Since macOS is built on a UNIX foundation (like Linux), it is much closer to Linux than Windows is.

Windows users who want to experience Linux can utilize [WSL](https://learn.microsoft.com/en-us/windows/wsl/install), which lets Windows users utilize a Linux environment on their Windows computer. (It is made by Microsoft, so if you are wondering, no, it is not unofficial or dangerous). WSL is free to use, but is not completely FOSS (free and open-source).

**What is your favorite coding workflow, and, what OS do you use? Do you agree with what I said?**

I'll share my OS:

> OS: Debian GNU/Linux 13 (trixie) x86_64  
> Kernel: Linux 6.12.90+deb13.1-amd64  
> DE: KDE Plasma 6.3.6  
> WM: KWin (Wayland)  
> Shell: bash 5.2.37  
> Display: 1920x1080 @ 60 Hz  
> CPU: 12th Gen Intel(R) Core(TM) i7-1255U (12)  
GPU: Intel Iris Xe Graphics [Integrated]
Memory: 16GB
