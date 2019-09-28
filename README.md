<h1 align="center">
  <img src="./img/ha_logo.jpg" alt="Bjorn's Smart Home" width="170"></a>
  <br>
  Bjorn's Home Assistant based Smart Home
</h1>

<p><font size="3">
I decided to create this page to give something back to the great Home Assistant community. Almost all my knowledge is from different users who shared their projects. A good reason to share your own! Hopefully you can find some inspiration in what I automated in my home.
  
I'll start off with a general overview of all the equipment used for my smart home.</p> 

## Devices

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
    <a href="https://github.com/bjorn-ha/smarthome/#lights">
      Lights
    </a>
    <span> | </span>
    <a href="https://github.com/CCOSTAN/Home-AssistantConfig#mobiledevices">
      Mobile Devices
    </a>
    <span> | </span>
    <a href="https://github.com/CCOSTAN/Home-AssistantConfig#nest">
      Nest
    </a>
    <span> | </span>
    <a href="https://github.com/CCOSTAN/Home-AssistantConfig#voice">
      Voice
    </a>
    <span> | </span>
    <a href="https://github.com/CCOSTAN/Home-AssistantConfig#hubs">
      Hubs
    </a>
    <span> | </span>
    <a href="https://github.com/CCOSTAN/Home-AssistantConfig#lights">
      Lights
    </a>
    <span> | </span>
    <a href="https://github.com/CCOSTAN/Home-AssistantConfig#switches">
      Switches
    </a>
    <span> | </span>
    <a href="https://github.com/CCOSTAN/Home-AssistantConfig#landscaping">
      Landscaping
    </a>
    <span> | </span>
    <a href="https://github.com/CCOSTAN/Home-AssistantConfig#LED">
      DIY LED Lights
    </a>
    <span> | </span>
    <a href="https://github.com/CCOSTAN/Home-AssistantConfig#garage">
      Garage
    </a>
    <span> | </span>
    <a href="https://github.com/CCOSTAN/Home-AssistantConfig#TV">
      TV Streaming
    </a>
    <span> | </span>
    <a href="https://github.com/CCOSTAN/Home-AssistantConfig#security">
      Security
    </a>
    <span> | </span>
    <a href="https://github.com/CCOSTAN/Home-AssistantConfig#cameras">
      Cameras
    </a>
    <span> | </span>
    <a href="https://github.com/CCOSTAN/Home-AssistantConfig#sensors">
      Sensors
    </a>
  </h4>
</div>

### <a name="networking"></a>Networking

<p><font size="3">For all my networking needs I am using equipment made by Ubiquity, called Unifi. Very solid performance up till now and very happhy with the purchase. The following equipment makes sure that all off my smart devices have perfect coverage:</p>

| Device        |Quantities           |More Info          |Image    |
| ------------- |:-------------:|:-----:|-----------:|
| Ubiquity Unifi Security Gateway | **1X** | [Secure, wired, fully managed Router.](https://www.ui.com/unifi-routing/usg/) |<img src="./img/ub_usg.png"  height="100px" />|
| Ubiquity Unifi US-8-60W 8P Switch | **2X** | [Fully managed, 8 Port Switch, 4 Port PoE.](https://www.ui.com/unifi-switching/unifi-switch-8/) |<img src="./img/ub_switch.png"  height="100px" />|
| Ubiquity Unifi CloudKey | **1X** | [Host for the Unifi Controller Software.](https://www.ui.com/unifi/unifi-cloud-key/) |<img src="./img/ub_cloudkey.jpg"  height="100px" />|
| Ubiquity Unifi AP AC Lite | **3X** | [Wifi Access Point.](https://www.ui.com/unifi/unifi-ap-ac-lite/) |<img src="./img/ub_ap.png"  height="100px" />|
| Ubiquity Unifi UAP AC-M | **1X** | [Outdoor Wifi Access Point (connected as regular AP, not mesh.](https://unifi-mesh.ui.com/#antennas) |<img src="./img/ub_outdoor.jpg"  height="100px" />|

<p><font size="3">As a sidenote, I bought the CloudKey before I had a 24/7 server running in my home. I wouldn't buy one now as Docker on my Synology NAS and also my Hassio server would be able to run the Unifi Controller Software in a seperate container.
  
Furthermore there are some cheaper switches at different end-points in my home. I might replace them in the future for Ubiquity switches as well.
</p>

### <a name="servers"></a>Servers

<p><font size="3">I used a Raspberry Pi 3B to run Hassio for about four months. By then it became too slow, and I wanted a more reliable solution.
</p>

| Device        |Quantities           |More Info          |Image    |
| ------------- |:-------------:|:-----:|-----------:|
| Synology DS218+ | **1X** | [Intel based Synology Storage Server and is used to run multiple containers in Docker.](https://www.synology.com/nl-nl/products/DS218+) |<img src="./img/synology.jpeg"  height="100px" />|
| Intel NUC BOXNUC6CAYH | **1X** | [Celeron Based Intel NUC, 4GB RAM, 120GB SSD.](https://ark.intel.com/content/www/us/en/ark/products/95062/intel-nuc-kit-nuc6cayh.html) |<img src="./img/nuc.jpg"  height="100px" />|

<p><font size="3">I am amazed about the performace difference between the NUC and the Rpi. I decided to buy the celeron based NUC as I have most of my other containers running on the Synology already. With this in mind I am only running Hassio with HassOS on the NUC (directly etched on the SSD with etcher).
</p>

### <a name="lights"></a>Lights

<p><font size="3">For all my networking needs I am using equipment made by Ubiquity, called Unifi. Very solid performance up till now and very happhy with the purchase. The following equipment makes sure that all off my smart devices have perfect coverage:</p>

| Device        |Quantities           |More Info          |Image    |
| ------------- |:-------------:|:-----:|-----------:|
| Ubiquity Unifi Security Gateway | **1X** | [Secure, wired, fully managed Router.](https://www.ui.com/unifi-routing/usg/) |<img src="./img/ub_usg.png"  height="100px" />|
| Ubiquity Unifi US-8-60W 8P Switch | **2X** | [Fully managed, 8 Port Switch, 4 Port PoE.](https://www.ui.com/unifi-switching/unifi-switch-8/) |<img src="./img/ub_switch.png"  height="100px" />|
| Ubiquity Unifi CloudKey | **1X** | [Host for the Unifi Controller Software.](https://www.ui.com/unifi/unifi-cloud-key/) |<img src="./img/ub_cloudkey.jpg"  height="100px" />|
| Ubiquity Unifi AP AC Lite | **3X** | [Wifi Access Point.](https://www.ui.com/unifi/unifi-ap-ac-lite/) |<img src="./img/ub_ap.png"  height="100px" />|
| Ubiquity Unifi UAP AC-M | **1X** | [Outdoor Wifi Access Point (connected as regular AP, not mesh.](https://unifi-mesh.ui.com/#antennas) |<img src="./img/ub_outdoor.jpg"  height="100px" />|


