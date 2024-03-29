# Cisco C coding challenge

## Goal

The goal of the programming challenge will be to forward a stream of packets to their respective files. From there, you will copy the data from the packet to the file.

You will be given a table which has the information on which ip addresses and subnet masks corrolate with certain files. This is table is called MAPPING_TABLE which is an array of Mapping stucts. The attributes of a Mapping stuct are defined in the beginning of the file.

## Given to you

You will be given the following:
-sample file which contains a stream of packets (containing source and destination IPv4s, as well as data) named "packets.data".
-a table that will forward matching packets to the next hop which points to a file
-library code you can use located above the area where you will impliment your code

### Packet Data Format

The input stream will have the following format:
```
                    Packet 1
+----------------------------------------------+
|    src ip (32 bits)   |    dst ip (32 bits)  |
|----------------------------------------------|
|            Data (length unknown)             |
|                (stopped by '.')              |
+----------------------------------------------+
                    Packet 2
+----------------------------------------------+
|   src ip (32 bits)   |   dst ip (32 bits)    |
|----------------------------------------------|
|            Data (length unknown)             |
|               (stopped by '.')               |
+----------------------------------------------+
                      ...
+----------------------------------------------+
|   src ip (32 bits)   |   dst ip (32 bits)    |
|----------------------------------------------|
|            Data (length unknown)             |
|               (stopped by '.')               |
+----------------------------------------------+
                   Packet 'n'
+----------------------------------------------+
|   src ip (32 bits)   |   dst ip (32 bits)    |
|----------------------------------------------|
|            Data (length unknown)             |
|               (stopped by '.')               |
+----------------------------------------------+
```

For example, the following is a possible packet originating with the IP address 1.2.3.4 with a destination address of 5.6.7.8 with the data "Hello World!" (I added spaces to seperate sections to give you a better understanding, however, the data in the file will not have spaces):

00000001000000100000001100000100 00000101000001100000011100001000 010010000110010101101100011011000110111100100000010101110110111101110010011011000110010000100001.



### Prerequisites

You will need a basic understanding of subnet masks and IP address as well as experience in programming in C.