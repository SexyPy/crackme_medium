
# CrackMe Medium

## 🛠️ Tools

    • Ghidra 10.1.1

    • Python 3.9.0


## 🚀 Let's get started
Let's get a CrackMe... [Dojas's MEDIUM](https://crackmes.one/crackme/6167747a33c5d4329c345148) will be perfect...

**Platform:**
Windows

**Difficulty:**
1.9

**Quality:**
4.0

**Arch:**
x86-64


## 1) Find the main function
![main func](https://imgur.com/U0uvOxr.png)

## 2) What does the software do when you use it
![bad](https://imgur.com/SttvZyl.png)

Okay, so we can see here that when we enter wrong information we have in return 'BAD >:('

Let's see if we can find this famous 'BAD >:(' in the decompiled code

## 3) Function Graph
![graph](https://imgur.com/nkPAael.png)

As we can see we have here an if/else condition which when reached returns 'GOOD!' or 'BAD >:('.

## 4) Patch Function

![](https://imgur.com/UVLbcIc.png)

JNE/JNZ : jump if Z=0

So we will change it into:

JE/JZ : jump if Z=1 (if equality after CMP or subtraction)

![](https://imgur.com/4SJma2c.png)

## 5) ReCompile

![](https://imgur.com/nmLgJGp.png)

## 6) Test

![](https://imgur.com/3JfNnmc.png)
