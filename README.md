# rpiC12R
A Raspberry Pi implementation of the Cacophonometer (C12R) birdsong recorder from The Cacophony Project

[The Cacophonometer](https://cacophony.org.nz/technology) is an open-source [Android application](https://github.com/TheCacophonyProject/cacophonometer) which wakes up at regular intervals, records audio and then uploads it to the Cacophony Project API server for analysis. Among other things, the recordings can be used to make estimates of bird population health.

Using a Android Smartphone is a great way of leveraging an off-the-shelf hardware/software stack to quickly develop a MVP however this brings with it a few challenges in a off-grid situation:
* How to power the device for extended periods of time
* How to protect the device from wind/rain etc while maintaining audio-recording quality from the built-in microphone
* Overhead of the Android OS/Software stack

### Approach
* The RTC on the rPi UPS board can be programmed to power-on the pi at a specified time in the future.
* Each time the pi boots it will:
  * Record Audio for a specified duration
  * Calculate *StartTime* for the next recording window (based on Dawn/Dusk time at the unit's location) and load that *StartTime* into the RTC on the UPS board
  * Perform a orderly shutdown on the pi
  * rinse and repeat



### Example Parts List
| Item        | Description           | Cost (NZ$)  |
| ------------- |:-------------| -----:|
|Raspberry Pi A+|Cut-down rPi with lower power requirements|$ 45|
|microSDHC Card|8GB SD card with Raspian OS|$ 15|
|PS3 Move Camera|USB Webcam (640x480) with 4-channel spatial microphone array. Second hand units readily available on TradeMe|$ 20|
|rPi UPS board| power extension board with RTC and serial interface - AliExpress|$ 35|
|Batteries|2 x 18650 ~3000mah Li-Ion batteries for the UPS/RTC board|$ 40|
|Case|Sealed ABS Enclosure - 171 x 121 x 80mm|$ 27|
|Total||$ 182|


