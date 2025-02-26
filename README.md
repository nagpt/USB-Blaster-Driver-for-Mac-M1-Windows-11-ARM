# USB-Blaster-Driver-for-Mac-M1-Windows-11-ARM



Instructions for installing USB Blaster Driver in Mac M1 with Windows 11 ARM running in a Virtual Machine (Useful for Max10 aka DE10-lite)

Install the driver files at this location: https://github.com/jonpalmisc/usb_blaster_arm64/releases/tag/v2.12.28%2C2.12.36.4
A cleaned up version is also present in the repo.
Followed by that adding certificates is recommended.

https://community.intel.com/t5/Programmable-Devices/Solution-USB-Blaster-Driver-for-Windows-11-ARM/m-p/1543852#M93480

Summary: To install a driver without disabling signature enforcement, first add the security certificate to (Local Machine) Trusted Root Certification Authorities as well as (Local Machine) Trusted Publishers.


(Useful for CycloneV aka DE10-nano)
For USB Blaster ii seen to work with advanced restart with disabling the security but certificate is a more permanent method. This highlighted answer helps:

https://community.intel.com/t5/Programmable-Devices/Solution-USB-Blaster-Driver-for-Windows-11-ARM/m-p/1543852#M93480:~:text=I%20also%20have%20an%20update%20for%20those%20with%20an%20USB%20Blaster%20II%20(such%20as%20the%20one%20integrated%20into%20the%20de10%2Dnano)

Bascially idea is to make two changes in the .inf file inside blaster-ii folder. First change properties to give full control over file edit. Then, comment the catalog line and replaced amd64 with arm64.
After that either follow the restart process in tne link. I think the security ceritficate adding could also work as a more permanent solution.

Install the software as it is. When the FPGA is connected, the Device Manager simply lists it as an unknown device. Follow the instructions below to install the .inf file and help the system recognize the device. Summary: 
