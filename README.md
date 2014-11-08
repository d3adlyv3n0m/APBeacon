APBeacon
========
This script is a wrapper for the mdk3 tool which allows the sending of wireless access point beacon frames using one or multiple MAC Addresses and SSID names.

The script is prompt oriented, so just make sure the mdk3 tool is installed and have a wireless adapter that allows injection (see how to test below) and just run it.

As an example of the usage, for Halloween I setup what appeared to be a normal access point aptly named HAPPY_HALLOWEEN.

TEST IF ADAPTER IS INJECTION CAPABLE
If aircrack-ng is not installed, then install it, then run the below commands to perform the test:

Put the adapter in monitor mode:

airmon-ng start wlanX

Change the channel for both the base adapter and the monitor interface:

iwconfig wlanX channel 1
iwconfig monX channel 1

Use the aireplay-ng command to begin the test. It'll display if injection is possible and grab information on nearby access points:

aireplay-ng --test monX

Have fun!
