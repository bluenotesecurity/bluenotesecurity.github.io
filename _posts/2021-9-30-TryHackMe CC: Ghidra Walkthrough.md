

For today’s post we’ll be doing a quick walkthrough of the short Ghidra crash course at TryHackMe. Ghidra, a free and open-source tool developed and released by the US National Security Administration, is used for decompiling and static analysis of code. It is excellent for malware analysis, as it can take the code of a malicious executable and reverse it back into human-readable code, allowing the analyst to safely investigate the functions and properties of the malware.

The first few tasks will take you through a basic overview of Ghidra and how to install it on your system. We’ll begin with the questions in Task 4. Task 5 is a quick overview of miscellaneous functions in Ghidra; in task 6, there is a final task binary to analyze.



4.1: *How many user created functions (including main) are there?*

2

4.2: *What is the first variable set to in the main function?*

![alt text](https://i.imgur.com/mhyvirb.png)
10

4.3: *What is the first variable set to, in the function “fn1”?*

![alt text](https://i.imgur.com/bwQl2SM.png)
hello

4.4: *If you provide the input "1", when you run the binary, what would the output be.(Note you can just run the binary to find this out, but that would defeat the whole purpose!).*

![alt text](https://i.imgur.com/xPadmq7.png)
nice!

6.1: *What outputs the good job message?*    

![alt text](https://i.imgur.com/fmuhBd9.png)
goodjob
