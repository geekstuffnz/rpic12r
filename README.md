# rpiC12R
A Raspberry Pi implementation of the Cacophonometer (C12R) birdsong recorder from The Cacophony Project

[The Cacophonometer](https://cacophony.org.nz/technology) is an open-source [Android application](https://github.com/TheCacophonyProject/cacophonometer) which wakes up at regular intervals, records audio and then uploads it to the Cacophony Project API server for analysis. Among other things, the recordings can be used to make estimates of bird population health.

Using a Android Smartphone is a great way of leveraging an off-the-shelf hardware/software stack to quickly develop a MVP however this brings with it a few challenges in a **off-grid** situation:
* Powering the unattended device for extended periods of time
* Always-On device power consumption
* Protecting the device from wind/rain etc while maintaining audio-recording quality from the built-in microphone
* Overhead of the Android OS/Software stack


