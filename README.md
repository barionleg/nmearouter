# NMEA Router

untill start https://www.rtl-sdr.com/aisrec-windows-and-android-ais-decoder/

Written by Neal Arundale (deceased), this has been uploaded to GitHub so that others can use it.
Routes AIS and other NMEA sentences between Serial, UDP, TCP, USB, Internet, Log Files, TTY Display Windows

Overview NmeaRouter routes NMEA sentences from a Source (for example an AIS Receiver Serial Port) to a Destination (for example a Local Network Ethernet). A Source or a Destination is called a Connection. Connections can be External to the PC (for example a Serial/USB or Network) or Internal (for example a File or a Display Window). A Source is linked to a Destination by a Route (for example the data from an AIS Receiver being routed to an AIS Chart Display). The program has been developed with AIS data in mind, AIS data is encapsulated within one type of NMEA sentence. There are hundreds of different NMEA sentences of which AIS and GPS data are but two, so the Router should handle any data conforming to NMEA standards.

# Registration

Many thanks to Philippe for decoding the [registration process](https://github.com/arundaleais/nmearouter/blob/master/frmRegister.frm#L334):

* Take your serial number (e.g. 8810)
* Perform the following calculation:
```
serial + (53/serial) + (113*serial/4)
```
  * This is unlikely to be an exact number, you might have to round it (if not sure, try both!)
* Now convert this to hexadecimal
  * In google type in "... to hex" then drop the "0x"
* Finally, add `-3BE` to the end

For example with a serial of `8810`
* `8810 + 53/8810 + 113*8810/4 = 257692.50601`
* We round this up to 257693.
* `257693 to hex` in google = `0x3EE9D`
* So the final registration code is `3EE9D-3BE`
