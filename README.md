# Sleipnir
Open source APRS display unit with navigation ideas.
Some ideas i have for a carputer that has built in navigation and
support for APRS,and connection to a vhf/uhf radio.
This is a template for the idea,its hardware and software functions.

Hardware:
Touchscreen with mount that fits in a cars 2x DIN (180x100mm) hole.
A viable unit is the Icarus 2DIN system from:
https://i-carus.com/
, it has a touch screen and a
rotary encoder,on/off switch and a 4 port active usb hub with connectors
in the front. It also has a metal box. 
microphone for hands free phone calls.


USB or on board RS-232 converter for interfacing to radios Terminal Data
port. Some never radios uses (ex Yaesu FTM-400DR) a usb cable with a
something that i am sure is a built in converter.
USB port with optional rs-232 converter for CAT communication with the
radio.

GPS receiver with external or internal antenna.
UBLOX NEO-M8N,Supports:
GPS,BeiDou WAAS, EGNOS, MSAS and is Galileo-ready
https://www.u-blox.com/en/product/neo-m8-series
Good RFI/tvi shielding.

DAB radio receiver with Traffic Message Channel,
automatically recompute best route if there are any traffical delays.

4 sound output channels.
+One sound input channel ( microphone ).

RTL2832U based usb recevier, this one supports DVB-T and FM and DAB+ (Glass mount antenna?)
Good quality 4x50W audio amplifier with interface plugs to typical car speaker plugs.
Bluetooth, pairing with phone,

automatic brightness regulation with  light-dependent resistor(useful
for night operation)

Basic Software features and options:
Navigation and routing to addresses and gps coordinates,other APRS stations(when they are stationary for the moment).
display distance and bearing to the nearest APRS station
with adjustable range filter(display only units that is inside xx
kilometers,also displays beaconed message.
Display altitude and GPS status.
GPS track logging.
Display speed/bearing of travel.
Stations that are inside the filtered range but outside the current zoom
level is displayed in the right side bar on the units navigation/map
display. 
Display of caller ID and name/information from phones number book.
Map update over wlan.


About APRS:
https://en.wikipedia.org/wiki/Automatic_Packet_Reporting_System
The symbols and misc info about them is on this page:
http://www.aprs.org/symbols.html
Information on the APRS protocol can be found here:
http://www.aprs.org/doc/APRS101.PDF

Compatibility with https://www.repeaterbook.com (import of database from
file or via wlan connection?) Database stored on SD card.
Automatic swithing to navigation map if the vechile starts moving, or no input from the toucshreen is detected. I suggest a timer of 5 seconds.

compatibility with maps from openstreetmap:
Suggested routing software:
http://www.navit-project.org/
GIT repo here: https://github.com/navit-gps/navit.git
Update of map data via wifi or other means.
I don't know if it can display APRS symbols.
The software can possibly be customized to do so, or a "digital layer" that is displayed over the navigation map created.
There are suggestions for a patch:
https://github.com/navit-gps/navit/issues/982

Optional software functions:
Media player (MP3 and common formats from USB key)
Audio media level control

Optional:
If the station transmits a message with a frequency, double
tapping on the message transmitted causes a CAT commando to be sent to
the radio, so it tunes VFO2 to that frequency.
Tapping it again returns it to your "home frequency",that is stored in
the options/settings dialogue.
Hamlib can be used for software interfacing of many radios.
API documentation:
http://hamlib.sourceforge.net/manuals/1.2.15/index.html

Compatibility with https://www.repeaterbook.com (import of database from
file or via wlan connection?) Database stored on SD card.


Optionally hardware:

TNC-Pi 2 for those radios that does not have a built in TNC.
( www.tnc-x.com)
