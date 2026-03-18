*This project has been created as part of the 42 curriculum by dvidal.*

# NetPractice

## Description 

NetPractice is a general practical exercise about networking. It is a exercise where you must configure small scale networks, it serves as an introduction to IP addressing and subnet masks.
The networks you work with are not "real". They are available via a training interface opened in your web browser. 

- - - - - - -

## Concepts

### TCP/IP and IP Addressing
TCP/IP stands for Transmission Control Protocol/Internet Protocol — a set of rules that guide and allow computers to communicate on a network such as the internet. 

An IPv4 address is a 32 bit number divided into four octets (8-bit blocks), each ranging from 0 to 255. Every IP address can be split into two parts: the **Network Address** and the **Host Address**. In order to communicate with each other, nodes must be on the same network. 

### Subnet Mask :

The subnet mask defines which bits of an IP address belongs to the network and which belongs to the host. For example:
- `/24` → `255.255.255.0` — first 3 octets are the network
- `/18` → `255.255.0.0` — there are more bits available for hosts

To limit the hosts we will allways start "locking" from left to right.

We have 2 ways on how to represent masks, one is by how many blocks are active from each octet. For example:
- `/24` or `/26`

This can vary between /0 to /32.

The other way of representing masks is:
- `/24` → `255.255.255.0`

- `/26` → `255.255.255.192`


The way we cant convert the masks is very simple. For each octet we have a range between 0 to 255. For example:
- `128 64 32 16 8 4 2 1` →  All these 8 numbers added together are 255.

So if i want to know what /20 is, we already know that 8 plus 8 is 16 so we dont need to worry about that, now 16 plus 8 is 24 that means we already passed the goal of 20, so what do we do:
`255.255.0.0` is 16 so we have to change the 3rd octet, 16 to 20 goes four so we count.

    1  2  3  4
- `128 64 32 16 8 4 2 1`

That gives us `255.255.240.0`.

- - - - - - -

## Instructions

Download the file attached to the project page, extract the files to any folder, then execute the `run.sh` file on the terminal. The training interface will open in your web browser and u are ready to go. 

- - - - - - -

## Resources

For this project i asked my peers about networking and how i should start learning it, so they passed me a tutorial playlist.

- [Link to the play list](https://www.youtube.com/playlist?list=PLIhvC56v63IJVXv0GJcl9vO5Z6znCVb1P)

### AI usage

I used AI in this project as a helpfull tool to clarify some doubts that i had along the way.
