# pulseUi-Debian-Jessie
*Hack to get Secure Pulse pulseUi working in Debian*

1. Reconfigure dpkg to support multiarch (i386):
dpkg --add-architecture i386
apt-get update

2. Install the 32 bit version of libwebkitgtk-1.0-0
sudo apt-get install libwebkitgtk-1.0-0:i386

3. Create and export the LD_LIBRARY_PATH variable:
LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/pulse
LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/lib/i386-linux-gnu
export LD_LIBRARY_PATH

Read more [here](https://forums.pulsesecure.net/topic/pulse-desktop-clients/1001595-pulse-secure-linux-ui)

