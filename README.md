# WebRTSP HDMI ReStreamer

### Hardware requirements
1. Raspberry Pi Zero/3/4
2. Attached Toshiba TC358743 based HDMI to CSI-2 adapter
3. Some HDMI source attached to HDMI input

### Install
1. Open `config.txt` for edit (with something like `sudoedit /boot/firmware/config.txt`) and add following to the end of file:
```
dtoverlay=tc358743
dtoverlay=tc358743-audio
```
2. Install `WebRTSP HDMI ReStreamer` snap:
```
sudo snap install webrtsp-hdmi-restreamer --edge
```
3. Attach required snap interfaces:
```
sudo snap connect webrtsp-hdmi-restreamer:camera
sudo snap connect webrtsp-hdmi-restreamer:media-control
```
4. Reboot Raspberry Pi
5. Open in browser `http://rpi.address:5080/`
