<h1 align="center">
  <img src="./img/ha_logo.jpg" alt="Bjorn's Smart Home" width="170"></a>
  <br>
  Bjorn's Home Assistant based Smart Home
</h1>

<p><font size="3">
I decided to create this page to give something back to the great Home Assistant community. I learned a lot from shared projects of other users, a good reason to share your own! Hopefully, you can find some inspiration in how I automated my home.

I'll be posting how-to's for different projects in the near future. First of all, I will list all my hardware and software used in my home automation system.</p> 

<a name="menu"></a>
<div align="center">
  <h4>
    <a href="https://github.com/bjorn-ha/smarthome/#hardware">
      Hardware
    </a>
    <span> | </span>
     <a href="https://github.com/bjorn-ha/smarthome/#software">
      Software
    </a>
    <span> | </span>
      <a href="https://github.com/bjorn-ha/smarthome/#projects">
      Projects
    </a>
  </h4>
</div>

## <a name="hardware"></a>Hardware

<a name="devices"></a>
<div align="center">
  <h4>
    <a href="https://github.com/bjorn-ha/smarthome/#networking">
      Networking
    </a>
    <span> | </span>
    <a href="https://github.com/bjorn-ha/smarthome/#servers">
      Servers
    </a>
<span> | </span>
    <a href="https://github.com/bjorn-ha/smarthome/#hubs">
      Hubs
    </a>
<span> | </span>    
     <a href="https://github.com/bjorn-ha/smarthome/#audio">
      Audio
    </a>
<span> | </span>    
     <a href="https://github.com/bjorn-ha/smarthome/#multimedia">
      Multi-Media
    </a>
<span> | </span>   
      <a href="https://github.com/bjorn-ha/smarthome/#mobile">
      Mobile Devices
    </a>
<span> | </span>     
      <a href="https://github.com/bjorn-ha/smarthome/#switches">
      Switches
    </a>
<span> | </span>     
      <a href="https://github.com/bjorn-ha/smarthome/#lights">
      Lights
    </a>
<span> | </span>          
       <a href="https://github.com/bjorn-ha/smarthome/#remotes">
      Remotes
    </a>
<span> | </span>     
       <a href="https://github.com/bjorn-ha/smarthome/#sensors">
      Sensors
    </a>
<span> | </span>    
       <a href="https://github.com/bjorn-ha/smarthome/#controllers">
      Controllers
    </a>
<span> | </span>     
       <a href="https://github.com/bjorn-ha/smarthome/#camera">
      Camera's
    </a>
</h4>
</div>

### <a name="networking"></a>Networking

<p><font size="3">For all my networking needs I am using equipment made by Ubiquity, called Unifi. Very solid performance up till now and very happy with the purchase. The following equipment makes sure that all off my smart devices have perfect coverage:</p>

| Device        |Quantities           |More Info          |Image    |
| ------------- |:-------------:|:-----:|-----------:|
| Ubiquity Unifi Security Gateway | **1X** | [Secure, wired, fully managed Router.](https://www.ui.com/unifi-routing/usg/) |<img src="./img/ub_usg.png"  height="100px" />|
| Ubiquity Unifi US-8-60W 8P Switch | **2X** | [Fully managed, 8 Port Switch, 4 Port PoE.](https://www.ui.com/unifi-switching/unifi-switch-8/) |<img src="./img/ub_switch.png"  height="100px" />|
| Ubiquity Unifi CloudKey | **1X** | [Host for the Unifi Controller Software.](https://www.ui.com/unifi/unifi-cloud-key/) |<img src="./img/ub_cloudkey.jpg"  height="100px" />|
| Ubiquity Unifi AP AC Lite | **3X** | [Wifi Access Point.](https://www.ui.com/unifi/unifi-ap-ac-lite/) |<img src="./img/ub_ap.png"  height="100px" />|
| Ubiquity Unifi UAP AC-M | **1X** | [Outdoor Wifi Access Point (connected as regular AP, not mesh.](https://unifi-mesh.ui.com/#antennas) |<img src="./img/ub_outdoor.jpg"  height="100px" />|

<p><font size="3">As a side note, I bought the CloudKey before I had a 24/7 server running in my home. I wouldn't buy one now as Docker on my Synology NAS and also my Hassio server would be able to run the Unifi Controller Software in a separate container.
  
Furthermore, there are some cheaper switches at different end-points in my home. I might replace them in the future for Ubiquity switches as well.
</p>

### <a name="servers"></a>Servers

<p><font size="3">I used a Raspberry Pi 3B to run Hassio for about four months. By then it became too slow, and I wanted a more reliable solution.
</p>

| Device        |Quantities           |More Info          |Image    |
| ------------- |:-------------:|:-----:|-----------:|
| Synology DS218+ | **1X** | [Intel based Synology Storage Server and is used to run multiple containers in Docker.](https://www.synology.com/nl-nl/products/DS218+) |<img src="./img/synology.jpeg"  height="100px" />|
| Intel NUC BOXNUC6CAYH | **1X** | [Celeron Based Intel NUC, 4GB RAM, 120GB SSD.](https://ark.intel.com/content/www/us/en/ark/products/95062/intel-nuc-kit-nuc6cayh.html) |<img src="./img/nuc.jpg"  height="100px" />|

<p><font size="3">I am amazed by the performance difference between the NUC and the Rpi. I decided to buy the Celeron based NUC as I have most of my other containers running on the Synology already. With this in mind, I am only running Hassio with HassOS on the NUC (directly etched on the SSD with etcher).
</p>

### <a name="hubs"></a>Hubs

<p><font size="3">As most of my devices are directly connected to WiFi, I only needed a hub to use my Zigbee Ikea Tradfri Lights. I've tried both the Ikea Tradfri and Philips Hue bridges for a while. With the Ikea bridge, everything worked "ok" in combination with Home Assistant, but it was unstable and needed a restart every day. With the Philips Hue bridge, I was able to control the Ikea bulbs, but I noted a very annoying flickering in each of the lights. After a tip from some users, I decided to buy a Conbee USB stick to use directly in the NUC to setup a Zigbee network. This one is working great since. Another great feature about this solution is that you are able to connect any zigbee device from any brand into one network.</p>

| Device        |Quantities           |More Info          |Image    |
| ------------- |:-------------:|:-----:|-----------:|
| Dresden Elektronik Conbee II | **1X** | [Zigbee USB Router](https://phoscon.de/en/conbee2) |<img src="./img/conbee2.jpg"  height="100px" />|

<p><font size="3">The Conbee II is running on a hassio add-on called DeconZ. More information about DeconZ in the <a href="https://github.com/bjorn-ha/smarthome/#software">software</a> section of this page</p>

### <a name="audio"></a>Audio

<p><font size="3">For my audio solution I have chosen Denon Heos over Sonos purely because of a personal taste for the sound quality of the Heos over Sonos. Heos integration into Home Assistant is getting better with every update, but purely on the integration part, Sonos is still superior over Heos. 
  
Also, one of the best features of the Heos system is the battery-operated Heos 1, they are normally used in the Kitchen where they are also being charged. But when we want to watch a movie we can use the two as surround satellite speakers. When we go for a swim we take one of them with us! (Battery time approx 7 hrs)</p>

| Device        |Quantities           |More Info          |Image    |
| ------------- |:-------------:|:-----:|-----------:|
| Denon Heos 1 HS2 | **2X** | [Small Wifi Multi-room Speaker](https://www.denon.co.uk/uk/heos/heos-1-portable-wireless-speakers) |<img src="./img/heos1.jpg"  height="100px" />|
| Denon Heos 1 Go-Pack | **2X** | [Battery and splash guard for Heos 1](https://www.denon.co.uk/uk/heos/heos-1-go-packhs2) |<img src="./img/heosbatt.jpg"  height="100px" />|
| Denon Heos 7 HS2 | **1X** | [Large Wifi Multi-room Speaker](https://www.denon.co.uk/uk/heos/heos-7-wireless-speaker-system) |<img src="./img/heos7.jpg"  height="100px" />|
| Denon Heos Bar | **1X** | [Soundbar and receiver in one (4x HDMI in)](https://www.denon.co.uk/uk/heos/heos-bar) |<img src="./img/heosbar.jpeg"  height="100px" />|
| Denon Heos Subwoofer | **1X** | [Subwoofer](https://www.denon.co.uk/uk/heos/heos-subwoofer) |<img src="./img/heossub.jpg"  height="100px" />|

### <a name="multimedia"></a>Multi-Media

<p><font size="3">Other Multi-Media equipment I have integrated into hassio:
</p>
  
| Device        |Quantities           |More Info          |Image    |
| ------------- |:-------------:|:-----:|-----------:|
| Sony Bravia KDL55X8500D | **1X** | [Generic 4K 55" Bravia Television](https://www.sony-mea.com/en/electronics/support/televisions-projectors-lcd-tvs-android-/kd-55x8500d/specifications) |<img src="./img/sonytv.jpg"  height="100px" />|
| Apple TV 4K | **2X** | [Apple TV](https://www.apple.com/apple-tv-4k/) |<img src="./img/atv.jpeg"  height="100px" />|
| Google Home Mini | **1X** | [Google Home Mini](https://store.google.com/us/product/google_home_mini?hl=en-US) |<img src="./img/gmini.jpg"  height="100px" />|

<p><font size="3">The Google home mini sits on a cabinet with the microphone disabled. It's only used for Text to Speech (TTS) notifications. The moment the Heos system is supporting TTS I will remove it from my setup.
</p>

### <a name="mobile"></a>Mobile Devices

<p><font size="3">This is a list of Mobile devices connected to the setup. Most of them are used to control the HA App (beta 2.0). The two mobile phones form the backbone of my presence detection.
  
The iPad Mini is in a wall mount installed in the living room. It's being used whenever we are awake and home. Works great.</p>

| Device        |Quantities           |More Info          |Image    |
| ------------- |:-------------:|:-----:|-----------:|
| Apple iPhone | **2X** | [iPhones](https://www.apple.com/iphone/) |<img src="./img/iphone.jpg"  height="100px" />|
| Apple iPad | **3X** | [Multiple version of the iPad](https://www.apple.com/ipad/) |<img src="./img/ipad.png"  height="100px" />|
| Vogel's  PTS 1216 TabLock | **1X** | [Wall Mount for the iPad Mini 3](https://www.vogels.com/en/p/pts-1216-tablock-for-ipad-mini-1-2-3) |<img src="./img/tablock.jpg"  height="100px" />|

### <a name="switches"></a>Switches

<p><font size="3">One of the first projects within my smart home was to replace some general switches with WiFi connected switches. As I didn't had a lot of experience yet and a lot of info was available for the Sonoff basic switches, this was my way to go. Most of them are operational already for about two years and are still working without issues.</p>

| Device        |Quantities           |More Info          |Image    |
| ------------- |:-------------:|:-----:|-----------:|
| Sonoff Basic R1/R2 | **8X** | [Sonoff Basic](https://sonoff.tech/product/wifi-diy-smart-switches/basicr2) |<img src="./img/s_basic.jpg"  height="100px" />|
| Sonoff POW R2 | **2X** | [Sonoff POW R2 (used to switch 15A devices)](https://sonoff.tech/product/wifi-diy-smart-switches/powr2) |<img src="./img/s_pow.jpg"  height="100px" />|
| Sonoff S20 | **5X** | [Sonoff S20](https://sonoff.tech/product/wifi-smart-plugs/s20) |<img src="./img/s_s20.jpg"  height="100px" />|
| Sonoff 4CH Pro R2 | **1X** | [Sonoff 4CH Pro, used to switch lower voltage](https://sonoff.tech/product/wifi-diy-smart-switches/4ch-r2-pro-r2) |<img src="./img/s_4ch.jpg"  height="100px" />|

<p><font size="3">All of the switches are flashed with custom firmware. More information in the <a href="https://github.com/bjorn-ha/smarthome/#software">software</a> section of this page</p></p>

## <a name="software"></a>Software
## <a name="projects"></a>Projects
