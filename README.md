# SMPTE To ArtNet Converter

This module design for Q-SYS Core processors to convert SMPTE Timecode data into ArtNet Timecode packets and send them over ther network using UDP to mimic the behaviour of a ArtNet Timecode Packet.

## Setup Plugin

1. Add the SMPTE To ArtNet Converter (The Plugin) and SMPTE LTC Generator to your Q-SYS design.
2. Expose the Frames Out, Seconds Out, Minutes Out, Hours Out, FrameRate, and Drop Frame output pins on the SMPTE LTC Generator module.
3. Expose the Started and Stoped output pins from the SMPTE LTC Generator module.
4. Connect the exposed output pins from the SMPTE LTC Generator to the corresponding input pins on the SMPTE To the Plugin.
5. (Opional) Connect the Start and Stop Trigger output pins from the SMPTE LTC Generator to the Plugin corresponding intput pins to keep Generator and the plugin in-sync.
6. Deploy the design to your Q-SYS Core processor.

### How to Use


Configre the IP Address Text field as the ArtNet receiver device IP Address that you want to send the ArtNet Timecode packets to. ArtNet communication used port 6454 Only for any type of Art-Net packet. (Ref: www.Art-Net.info)
