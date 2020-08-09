# HomeAssistant personal config

## Screenshots

### Dashboard - Home

![Dashboard home 1](images/screenshots/dashboard-home1.png)

## Devices

<table align="center" border="0" width="100%">
  <thead>
    <tr>
      <th>Quantity</th>
      <th>Device</th>
      <th>Use</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>
        <img src="images/devices/nuc-j3455.jpg" alt="drawing" width="200" />
        <h3>Intel NUC J3455</h3>
      </td>
      <td>
        <p>Ubuntu server running Docker</p>
      </td>
    </tr>
    <tr>
      <td>2</td>
      <td>
        <img src="images/devices/google-home.jpg" alt="drawing" width="200" />
        <h3>Google Home Mini</h3>
      </td>
      <td>
        <p>Voice Assistant</p>
      </td>
    </tr>
    <tr>
      <td>1</td>
      <td>
        <img src="images/devices/echo-show.jpg" alt="drawing" width="200" />
        <h3>Echo show</h3>
      </td>
      <td>
        <p>Voice Assistant</p>
      </td>
    </tr>
    <tr>
      <td>2</td>
      <td>
        <img src="images/devices/led-controller.jpg" alt="drawing" width="200" />
        <h3>LED strip controller</h3>
      </td>
      <td>
        <p>Lights</p>
      </td>
    </tr>
    <tr>
      <td>2</td>
      <td>
        <img src="images/devices/mi-box-s.jpg" alt="drawing" width="200" />
        <h3>Mi Box S</h3>
      </td>
      <td>
        <p>TV</p>
      </td>
    </tr>
    <tr>
      <td>1</td>
      <td>
        <img src="images/devices/mi-wifi-3.jpg" alt="drawing" width="200" />
        <h3>Mi WiFi 3</h3>
      </td>
      <td>
        <p>WiFi router</p>
      </td>
    </tr>
    <tr>
      <td>1</td>
      <td>
        <img src="images/devices/rmmini.jpg" alt="drawing" width="200" />
        <h3>RM mini</h3>
      </td>
      <td>
        <p>IR Blaster</p>
      </td>
    </tr>
    <tr>
      <td>1</td>
      <td>
        <img src="images/devices/pzem.jpg" alt="drawing" width="200" />
        <h3>PZEM</h3>
      </td>
      <td>
        <p>Home power meter</p>
      </td>
    </tr>
    <tr>
      <td>3</td>
      <td>
        <img src="images/devices/sonoff-pow.jpg" alt="drawing" width="200" />
        <h3>Sonoff POW</h3>
      </td>
      <td>
        <p>Switch / Power meter</p>
      </td>
    </tr>
    <tr>
      <td>4</td>
      <td>
        <img src="images/devices/sonoff.jpg" alt="drawing" width="200" />
        <h3>Sonoff</h3>
      </td>
      <td>
        <p>Switch</p>
      </td>
    </tr>
    <tr>
      <td>1</td>
      <td>
        <img src="images/devices/sonoff-switch-2.jpg" alt="drawing" width="200" />
        <h3>Sonoff wall 2 gang</h3>
      </td>
      <td>
        <p>Lights switch</p>
      </td>
    </tr>
    <tr>
      <td>1</td>
      <td>
        <img src="images/devices/wemos.jpg" alt="drawing" width="200" />
        <h3>Wemos</h3>
      </td>
      <td>
        <p>Generic</p>
      </td>
    </tr>
    <tr>
      <td>1</td>
      <td>
        <img src="images/devices/xiaomi-bulb.jpeg" alt="drawing" width="200" />
        <h3>Xiaomi Bulb</h3>
      </td>
      <td>
        <p>Light</p>
      </td>
    </tr>
    <tr>
      <td>2</td>
      <td>
        <img src="images/devices/xiaomi-button.jpg" alt="drawing" width="200" />
        <h3>Xiaomi button</h3>
      </td>
      <td>
        <p>Action button</p>
      </td>
    </tr>
    <tr>
      <td>1</td>
      <td>
        <img src="images/devices/xiaomi-door.jpg" alt="drawing" width="200" />
        <h3>Xiaomi door sensor</h3>
      </td>
      <td>
        <p>Door sensor</p>
      </td>
    </tr>
    <tr>
      <td>1</td>
      <td>
        <img src="images/devices/xiaomi-motion.jpg" alt="drawing" width="200" />
        <h3>Xiaomi motion sensor</h3>
      </td>
      <td>
        <p>Motion sensor</p>
      </td>
    </tr>
    <tr>
      <td>2</td>
      <td>
        <img src="images/devices/xiaomi-temperature.jpg" alt="drawing" width="200" />
        <h3>Xiaomi temperature/humidity sensor</h3>
      </td>
      <td>
        <p>Temperature and humidity sensor</p>
      </td>
    </tr>
    <tr>
      <td>1</td>
      <td>
        <img src="images/devices/cc2531.jpg" alt="drawing" width="200" />
        <h3>CC2531 USB</h3>
      </td>
      <td>
        <p>Sniffer - Zigbee to MQTT</p>
      </td>
    </tr>
    <tr>
      <td>1</td>
      <td>
        <img src="images/devices/yi_dome.jpg" alt="drawing" width="200" />
        <h3>Yi Dome 1080p</h3>
      </td>
      <td>
        <p>Camera and movement detection</p>
      </td>
    </tr>
  <tbody>
</table>

## Automations

### Most important automations

#### [Notify when the water heater is ready](https://github.com/JoaquinBeceiro/home-assistant-config/blob/c82da612f44ed7adee008f6d876e8560fad946e4/config/automations/bathroom.yaml#L20-L68)

##### Automation trigger
Every time Water Heater is turned on, this automation turns on.
The Water Heater has a power meter. When this power meter reads 0w and the switch is on, this automations trigers. This automation only run if time is between **09:00HS** and **05:00HS**.

##### Automation tasks
* Play on Google Home with TTS
* Text notification with Telegram


#### [Notify power consumption daily](https://github.com/JoaquinBeceiro/home-assistant-config/blob/41c0525266fa52f0d7c0c3110407299596538b52/config/automations/energy.yaml#L5-L33)

##### Automation trigger
Every day at **23:59HS**

##### Automation tasks
* Notify each power consumption reads (Heater, WaterHeater and Refrigerator) and total of the current day