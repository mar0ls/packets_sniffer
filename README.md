<div id="header" align="center">
    <img src="https://media1.giphy.com/media/3oKIP83aTWXTZZBgmA/200w.webp?cid=ecf05e47kc9m1dgov0kf1c38hmjvub2mgs1hlq7zr0qyp1lx&rid=200w.webp&ct=g" width="100"/>
</div>

# Packets sniffer
Written as part of self-study. The python [library socket](https://docs.python.org/3/library/socket.html) was used . Below I will present what was helpful to create the above application.

# What`s i need to know ?

* Exterior Gateway Protocol in Hex format from [list of IP protocol numbers](https://en.wikipedia.org/wiki/List_of_IP_protocol_numbers) 
  and you should know something about  [packet reading](https://www.cs.ryerson.ca/~zereneh/linux/PacketReading.pdf)


# IP Header Struckture
#![image](https://user-images.githubusercontent.com/120790937/220673077-c1c9f205-037f-472d-83d3-5e3f203b086d.png)


# TCP Header Structure
![image](https://user-images.githubusercontent.com/120790937/220673298-210254c4-f229-4231-8c61-0fb9295a740c.png)


# UDP Header Structure
![image](https://user-images.githubusercontent.com/120790937/220673476-dae63136-234b-4db3-a912-1bda6b14767c.png)

# This program works on linux.

* If you run this program on Windows, you show this:
```bash
Traceback (most recent call last):
  File "C:\packets_sniffer.py", line 165, in <module>
    main()
  File "C:\packets_sniffer.py", line 141, in main
    sniffer_socket = socket.socket(socket.PF_PACKET, socket.SOCK_RAW, socket.htons(0x0003))
                                   ^^^^^^^^^^^^^^^^
AttributeError: module 'socket' has no attribute 'PF_PACKET'
```
If you want to run it on Windows, you should PF_PACKET change to AF_INET in socket.




