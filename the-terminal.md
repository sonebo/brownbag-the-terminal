---
theme: ./dracula.json
author: ""
paging: Slide %d / %d
---

                ████████╗██╗  ██╗███████╗    ████████╗███████╗██████╗ ███╗   ███╗██╗███╗   ██╗ █████╗ ██╗
                ╚══██╔══╝██║  ██║██╔════╝    ╚══██╔══╝██╔════╝██╔══██╗████╗ ████║██║████╗  ██║██╔══██╗██║
                   ██║   ███████║█████╗         ██║   █████╗  ██████╔╝██╔████╔██║██║██╔██╗ ██║███████║██║
                   ██║   ██╔══██║██╔══╝         ██║   ██╔══╝  ██╔══██╗██║╚██╔╝██║██║██║╚██╗██║██╔══██║██║
                   ██║   ██║  ██║███████╗       ██║   ███████╗██║  ██║██║ ╚═╝ ██║██║██║ ╚████║██║  ██║███████╗
                   ╚═╝   ╚═╝  ╚═╝╚══════╝       ╚═╝   ╚══════╝╚═╝  ╚═╝╚═╝     ╚═╝╚═╝╚═╝  ╚═══╝╚═╝  ╚═╝╚══════╝


                (In unix, or unix-like systems)

---

# On the menu 🥗

- A bit of history
- keyboard tricks
- A sprinkle of man pages
- I/O Redirection - command pipelines

---

                 █████╗     ██████╗ ██╗████████╗     ██████╗ ███████╗
                ██╔══██╗    ██╔══██╗██║╚══██╔══╝    ██╔═══██╗██╔════╝
                ███████║    ██████╔╝██║   ██║       ██║   ██║█████╗
                ██╔══██║    ██╔══██╗██║   ██║       ██║   ██║██╔══╝
                ██║  ██║    ██████╔╝██║   ██║       ╚██████╔╝██║
                ╚═╝  ╚═╝    ╚═════╝ ╚═╝   ╚═╝        ╚═════╝ ╚═╝

                ██╗  ██╗██╗███████╗████████╗ ██████╗ ██████╗ ██╗   ██╗
                ██║  ██║██║██╔════╝╚══██╔══╝██╔═══██╗██╔══██╗╚██╗ ██╔╝
                ███████║██║███████╗   ██║   ██║   ██║██████╔╝ ╚████╔╝
                ██╔══██║██║╚════██║   ██║   ██║   ██║██╔══██╗  ╚██╔╝
                ██║  ██║██║███████║   ██║   ╚██████╔╝██║  ██║   ██║
                ╚═╝  ╚═╝╚═╝╚══════╝   ╚═╝    ╚═════╝ ╚═╝  ╚═╝   ╚═╝

---

            ██████╗ ███████╗██╗     ██╗         ██╗      █████╗ ██████╗ ███████╗
            ██╔══██╗██╔════╝██║     ██║         ██║     ██╔══██╗██╔══██╗██╔════╝
            ██████╔╝█████╗  ██║     ██║         ██║     ███████║██████╔╝███████╗
            ██╔══██╗██╔══╝  ██║     ██║         ██║     ██╔══██║██╔══██╗╚════██║
            ██████╔╝███████╗███████╗███████╗    ███████╗██║  ██║██████╔╝███████║
            ╚═════╝ ╚══════╝╚══════╝╚══════╝    ╚══════╝╚═╝  ╚═╝╚═════╝ ╚══════╝

---

# Bell Labs in the 70's

- Endless funds 💸
- Big brains work on things they find interesting 🧠

Ken Thompson and Dennis Ritchie invent _Unix_ ✨

---

# The Unix Philosophy

Make each program do one thing well. To do a new job, build afresh rather than complicate old programs by adding new "features".

Expect the output of every program to become the input to another, as yet unknown, program. Don't clutter output with extraneous information. Avoid stringently columnar or binary input formats. Don't insist on interactive input.

Design and build software, even operating systems, to be tried early, ideally within weeks. Don't hesitate to throw away the clumsy parts and rebuild them.

---

# Speaking of history...

$ history

Your command history 📖

---

# To summarize:

- CTRL + R - Reverse Incremental Search!

- History expansion: !! and !number

- CTRL + O - run a sequence of commands from your history

---

# Keyboard tricks ⌨️

# Beginning and end of line

- CTRL + A
- CTRL + E

# Jumping wordwise (bizarre default in iTerm? but possible to change your meta key to something else!)

- ESC + B
- ESC + F

# Transpose letters

- CTRL + T

# Transpose the words

- ESC + T

# Kill word by word

- ESC + BACKSPACE

# Kill text from the cursor location to the end or beginning of line

- CTRL + K
- CTRL + U

---

# Killing 🔪 ... and yanking? The kill-ring.

Yank stuff from the kill-ring with CTRL + Y 👻

---

# Manual pages, or man pages for short

Ken and Richie had a boss who told them to write docs

Try typing man man to see the man pages on the man pages!

---

# What are commands, really, tho?

1. Executable programs, like the files in /usr/bin
2. A shell builtin, like cd
3. A shell function - I've never done one, if you have, please share why and how? 🙏
4. An alias

To see the type of a command, you can write:
type command

---

# I/O Redirection

## Standard input, output and error

A theme in unix: everything is a file...?

- programs like _ls_ send their output to a file called standard output (**stdout**)
- and their errors to standard error (**stderr**)

They are linked to the screen and not saved to a disk file.

Additionally, many programs take input from standard input (**stdin**) which is connected to your keyboard by default.

---

# Example: **stdout**

ls -l /usr/bin _>_ ls-output.txt

less ls-output.txt

ls -l /bin/usr _>_ ls-output.txt

# Appending to existing files

ls -l /usr/bin _>>_ ls-output.txt

# Example: **stderr**

ls -l /bin/usr _2>_ ls-error.txt

---

# Example: building a really dumb word processor?

cat 🐱
Reads one or more files and copies them to standard output

---

# Disposing of Unwanted Output **/dev/null**

Where you redirect stuff you just want to throw away 🗑

ls -l /bin/usr 2> /dev/null

This file is a system device often referred to as a bit bucket, which accepts input and does nothing with it.

Apparently a part of Unix culture?

_"please send complaints to /dev/null"_

Kind regards,

Developer

---

# Pipelines

command1 | command2

Make a list of the executable files in /bin and usr/bin, sort them, show them!

ls /bin /usr/bin | sort | less

---

# grep - global regular expression print

- Origin: Finding word occurences in the 85 Federalist Papers

man grep

ls /bin /usr/bin | sort | uniq | grep zip

---

Some nice resources, where I found some of the examples I've illustrated here:

- The Linux Command Line by William Shotts - available in printed format, but also released under a creative commons license and available for download! You find it here: https://linuxcommand.org/tlcl.php

- The Unix Programming Environment by Kernighan and Pike

Where GREP came from (with Brian!)
https://www.youtube.com/watch?v=NTfOnGZUZDk

Unix Pipeline (with Brian!)
https://www.youtube.com/watch?v=bKzonnwoR2I

Brian Kernighan interviews Ken Thompson
https://www.youtube.com/watch?v=EY6q5dv_B-o

---
