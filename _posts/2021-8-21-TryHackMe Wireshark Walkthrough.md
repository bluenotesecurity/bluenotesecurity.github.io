Today’s post will be a walkthrough of TryHackMe’s Wireshark room. This is an excellent room to do early on in your networking/cybersecurity journey because Wireshark, and packet capture in general, is an essential skill in these fields. Not only can Wireshark capture packets directly from a network, it can also be used to open and visualize packet capture files (known as .pcap files) collected from other sources such as the command line utility tcpdump for further analysis.

Wireshark can seem intimidating at first because of the sheer amount of information it provides. Even on a small home network, just a few minutes of capturing can give you thousands of packets. Fortunately, it also provides a very powerful, flexible, and user-friendly set of tools for filtering and searching through these packets to make it easier to find what you’re looking for. 

The THM room here does a good job of explaining the basics of the application, and the first 6 tasks have no questions to answer—you’ll want to spend some time exploring the application and tools. Once you’ve done so you should be ready for task 7, which is where we’ll begin here with the walkthrough.



What is the Opcode for Packet 6?

![alt text](https://i.imgur.com/TFfWORb.png)
Request (1)

What is the source MAC Address of Packet 19?

![alt text](https://i.imgur.com/OZMV4OO.png)
80:fb:06:f0:45:d7

What 4 packets are Reply packets?

These are easy to spot if you've filtered to only search for ARP packets.
76,400,459,520

What IP Address is at 80:fb:06:f0:45:d7?

![alt text](https://i.imgur.com/oF97QCA.png)
10.251.23.1



What is the type for packet 4?

![alt text](https://i.imgur.com/Fa1TxAu.png)
8

What is the type for packet 5?

![alt text](https://i.imgur.com/z6Wu4bQ.png)
0

What is the timestamp for packet 12, only including month day and year?
note: Wireshark bases it’s time off of your devices time zone, if your answer is wrong try one day more or less. 

![alt text](https://i.imgur.com/Ak7W0mJ.png)
May 30, 2013

What is the full data string for packet 18?

![alt text](https://i.imgur.com/LnPu14F.png)

The easiest way to grab this information is to right-click, then click select "Copy" -> "Value"

![alt text](https://i.imgur.com/lpIk4ud.png)
08090a0b0c0d0e0f101112131415161718191a1b1c1d1e1f202122232425262728292a2b2c2d2e2f3031323334353637



What is being queried in packet 1?

![alt text](https://i.imgur.com/3Vk7U2i.png)
8.8.8.8.in-addr.arpa

What site is being queried in packet 26?

![alt text](https://i.imgur.com/HBjIn24.png)
www.wireshark.org

What is the Transaction ID for packet 26?

You can find this at the top of the DNS data in the same screenshot above:

0x2c58



What percent of packets originate from Domain Name System?

Filter for DNS packets, and Wireshark will show you the precentage at the bottom of the application:
![alt text](https://i.imgur.com/6sNu7YU.png)
4.7

What endpoint ends in .237?

![alt text](https://i.imgur.com/XqGAmmF.png)
145.254.160.237

What is the user-agent listed in packet 4?

![alt text](https://i.imgur.com/zH7tXJC.png)
Mozilla/5.0 (Windows; U; Windows NT 5.1; en-US; rv:1.6) Gecko/20040113\r\n

Looking at the data stream what is the full request URI from packet 18?

![alt text](https://i.imgur.com/uWCJ35z.png)
https://pagead2.googlesyndication.com/pagead/ads?client=ca-pub-2309191948673629&random=1084443430285&lmt=1082467020&format=468x60_as&output=html&url=http%3A%2F%2Fwww.ethereal.com%2Fdownload.html&color_bg=FFFFFF&color_text=333333&color_link=000000&color_url=666633&color_border=666633

What domain name was requested from packet 38?

![alt text](https://i.imgur.com/Gj3ktxN.png)
www.ethereal.com

Looking at the data stream what is the full request URI from packet 38?


http://www.ethereal.com/download.html



Looking at the data stream what is the full request URI for packet 31?

![alt text](https://i.imgur.com/W6xqHlJ.png)
https://localhost/icons/apache_pb.png

Looking at the data stream what is the full request URI for packet 50?

![alt text](https://i.imgur.com/2jD4qDq.png)
https://localhost/icons/back.gif

What is the User-Agent listed in packet 50?

![alt text](https://i.imgur.com/GQATsuF.png)
Mozilla/5.0 (X11; U; Linux i686; fr; rv:1.8.0.2) Gecko/20060308 Firefox/1.5.0.2\r\n


At this point, we’ve finished all the questions. The next section will guide you through an example of what the Zerologon attack looks like when viewed from a set of captured packets; take the time to go through it so you can get an idea of how this would look—being able to see attacks in packet captures is a powerful skill for incidence response and threat hunting.

Wireshark is an extremely deep subject, and while THM provides an excellent introduction, there’s plenty more to learn. I highly recommend David Bombal’s Wireshark course, which can be found on his website at: https://courses.davidbombal.com/p/wireshark-packet-analysis-and-ethical-hacking-core-skills/?product_id=1372317
