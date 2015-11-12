# Sleipnir
Open source APRS display unit with navigation ideas.
Some ideas i have for a carputer that has built in navigation and
support for APRS,and connection to a vhf/uhf radio.

Hardware:
Touchscreen with mount that fits in a cars 2x DIN (180x100mm) hole.
A viable unit is the Icarus 2DIN housing, it has a touch screen and a
rotary encoder,on/off switch and a 4 port active usb hub with connectors
in the front. It also has a metal box. 
It does not have the possibillities for detachment so it is not so attractive for car burglars.
USB hub with 6 ports for under the dashboard modules.
A 12V to 5 V converter is also needed,this can be on board if a PCB is made.
"motherboard" for now:
Rasberry Pi B+ or better.
USB sound card for voice directions from navigation software.
TNC-Pi 2 for those radios that does not have a built in TNC.
( www.tnc-x.com)
USB or on board RS-232 converter for interfacing to radios Terminal Data
port. Some never radios uses (ex Yaesu FTM-400DR) a usb cable with a
something that i am sure is a built in converter.
USB port with optional rs-232 converter for CAT communication with the
radio.
GPS receiver with external or internal antenna
UBLOX NEO-M8N,Supports:
GPS,BeiDou WAAS, EGNOS, MSAS and is Galileo-ready
https://www.u-blox.com/en/product/neo-m8-series
Good RFI/tvi shielding.

Optional hardware:
RTL2832U based usb recevier, this one supports DVB-T and FM and DAB+ (Glass mount antenna?)
Good quality 4x50W audio amplifier with interface plugs to typical car speaker plugs.

automatic brightness regulation with  light-dependent resistor(useful
for night operation)

Basic Software features and options:
Navigation and routing to addresses and gps coordinates,other APRS stations(when they are stationary for the moment).
display distance and bearing to the nearest APRS station
with adjustable range filter(display only units that is inside xx
kilometers,also displays beaconed message,this depends on the hardware).
display altitude and GPS status.
GPS track logging.
display speed/bearing of travel.
Stations that are inside the filtered range but outside the current zoom
level is displayed in the right side bar on the units navigation/map
display. If the station transmits a message with a frequency, double
tapping on the message transmitted causes a CAT commando to be sent to
the radio, so it tunes VFO2 to that frequency.
Tapping it again returns it to your "home frequency",that is stored in
the options/settings dialogue.
Hamlib can be used for software interfacing of many radios.
API documentation:
http://hamlib.sourceforge.net/manuals/1.2.15/index.html

About APRS:
https://en.wikipedia.org/wiki/Automatic_Packet_Reporting_System
The symbols and misc info about them is on this page:
http://www.aprs.org/symbols.html
Information on the APRS protocol can be found here:
http://www.aprs.org/doc/APRS101.PDF

Compatible with https://www.repeaterbook.com (import of database from
file or via wlan connection?) Database stored on SD card.
Automatic swithing to navigation map if the vechile starts moving, or no input from the toucshreen is detected. I suggest a timer of 5 seconds.

compatibility with maps from openstreetmap:
Suggested routing software(unsure about licensing for commercial usage etc):
http://sourceforge.net/projects/gosmore/
http://code.google.com/p/monav/
I don't know if anyone of these can display APRS symbols.
The software can possibly be customized to do so, or a "digital layer" that is displayed over the navigation map created.


Optional software functions:
DAB/FM tuner
Media player (MP3 and common formats from USB key)
Audio level control
