ninja-orvibo
============

A driver for the Ninja Blocks that controls Orvibo Wi-Fi Smart Sockets

Please note: This code mostly works, but saving options is not yet implemented. You'll need to add your MAC address manually to ../../config/ninja-orvibo/config.json for it to work. Fix coming soon!

At this time, you can only control one socket, but you can control it via the dashboard or the rules page. 

Getting started
===============

To install this driver, SSH into your block, go to the location of your Ninja Block drivers (on Raspbian, this will be /opt/ninjablocks/block-client/drivers/) and run:

`git clone http://github.com/Grayda/ninja-orvibo && cd ninja-orvibo && npm install && restartninja`

Feedback
========

This is a beta driver. It has been built and tested against the smart socket by Bauhn (which is the Orvibo S10 smart socket, I believe). I'm looking for people who have different types of Orvibo Wi-Fi smart sockets to test this and report back. Packet captures (via TCPdump or Wireshark) definitely most welcome

To-Do:
======

* ~~Actually get this to run~~
* Make it more robust so it doesn't accidentally detect the SmartPoint app as a socket (a bug in the SP app, perhaps?)
* Fix up the options so you can modify the settings instead of it recreating them each time
* Maybe: Make this a truly automatic setup. Set it up in the SP app, then the Ninja driver will detect the MAC address and stuff
* Rewrite parts (most?) of this code so you can control more than one socket. Pull requests DEFINITELY welcome on this part!
* Add the ability to read the state of the device without turning it on or off
* Modify sockettest.js to provide more details about the socket and where stuff is failing

Thanks to:
==========

* Nozza87 on the Ninja Blocks forum for taking my basic code and making it run, and for doing the hard work in reverse-engineering the protocol, and to mlava for initial research on the manufacturer, plus data sheets of the socket 
