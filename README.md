# pulseUi-Debian-Jessie
*Hack to get Secure Pulse pulseUi working in Debian*

1. Reconfigure dpkg to support multiarch (i386):
<pre>dpkg --add-architecture i386
apt-get update</pre>

2. Install the 32 bit version of `libwebkitgtk-1.0-0`
<pre>sudo apt-get install libwebkitgtk-1.0-0:i386</pre>

3. Create and export the `LD_LIBRARY_PATH` variable:
<pre>LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/pulse
LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/lib/i386-linux-gnu
export LD_LIBRARY_PATH</pre>

Read more [here](https://forums.pulsesecure.net/topic/pulse-desktop-clients/1001595-pulse-secure-linux-ui)

