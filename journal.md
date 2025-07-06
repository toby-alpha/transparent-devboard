
# (not so) Transparent Devboard

*i unfortunately am currently abandoning the transparent idea, but I've contacted a few manufactures to try and make it happen*

## Day 1 - Schematic

![HOW CAN I USE THE ESP32-C3-MINI-1-N4 Module WITH ARDUINO (WITHOUT DEV  BOARD) - 3rd Party Boards - Arduino Forum](https://europe1.discourse-cdn.com/arduino/original/4X/8/4/9/849fa995cb05b433f0d6eac78392bffbdf19fc35.jpeg)

I'll be basing the dev-board off this module, the ESP-32 C3 Mini. I think the mini form factor is pretty good, while also having alot of great features. I chose to use this module, rather than a custom chip set just in order to increase the reliability of it, but also have it so that the costs were less.

I want to keep this pretty simple, but here are the requirements I set out with.

- Low Profile
- Small Footprint
- Breaks out all GPIO
- More than 1 WS2812B LED
- Power LED
- Programmable Regular LED (Selectable)
- 
![GT-USB-7058](https://ik.imagekit.io/mibltjb36/gtusb7058.jpeg)

To keep inline with the slim/low-profile criteria, I'll be using this USB port, and honestly, I've wanted to use this part for a while. I think it adds a pretty unique spin on the board.

![image](https://i.ibb.co/QFqXj0wD/image.png)

For the voltage regulator, I didn't really like the bulkiness of the AMS1117-3.3, so I rather went with the AP2112K-3.3. This provides a much smaller form factor, but limits the output current to 600mA compared to 1A.

![image](https://i.ibb.co/9HZ6HCqL/image.png)

![image](https://i.ibb.co/RT2tM8MK/image.png)

I then added the standard LEDs, with a jumper on the user one in case it didn't need to be used, the the pin could be used for the GPIO instead.

For the WS2812B led, I went with a much smaller one, helping to fit the criteria of the board. I think these look much better as well, taking up less space.

![XL-2020RGBC-WS2812B-fullview](https://jlcpcb.com/api/file/downloadByFileSystemAccessId/8583717432758714368)

![image](https://i.ibb.co/Y7ZJDc9Z/image.png)

![image](https://i.ibb.co/Ps6kyVQJ/image.png)

I then have buttons for both EN and Boot. I chose to use a slightly larger component, but I think these will give a more premium and tactile feedback to the user when using the board.

![TSA343G00D-250J2-fullview](https://jlcpcb.com/api/file/downloadByFileSystemAccessId/8583016525192441856)

At the moment, I've just got some placeholder headers in, as I'll end up selecting the final number based on the board size/shape later.

I decided not to do say a battery charging circuit or something similar to be able to cut down on the board size, 

### Time Spent - 3 Hours (5/07/25)

## Day 1.5 - Layout

I've started out with this rough layout of the board, deciding where the key components need to be placed. I didn't really want the PCB antenna hanging off the edge, so I'm going to do a copper exclusion zone underneath, I'll have to see how this goes in terms of effectiveness.

![image](https://i.ibb.co/h1rbbvrd/image.png)

The USB-C port, and both buttons are located at the bottom. The LEDS then sit above those buttons, with their associated capacitors and resistors.

![image](https://i.ibb.co/hx8RNymT/image.png)

I packed everything in pretty closely, and really like how this looks. Yet, 2 big problems. 1, it'll probably require 4 layers.. meaning making it transparent will be hard. and 2. there is this big open gap in the middle.

To address the first, I'll first be making a regular, rigid version, and then afterwards maybe pursuing a less feature filled transparent one, so ultimately, I want to continue with the board as it is now.

Secondly, there is the big gap of dead space in the middle that kinda harms how the board looks. To fill this, I'll be using a STEMMA QT/ QUICC connector, to allow for easy connection to I2C using the JST SH connector. 

![image](https://i.ibb.co/Tx99k31p/image.png)

This solution turned out very well, and I really like how all the components fit together on the board. The grid-type layout makes it seem very professional, and polished.

![image](https://i.ibb.co/WvPnK6jQ/image.png)

The STEMMA-QT port really was able to tie it together, and it now looks pretty cohesive. The board outline is sorta tentative at the moment, but I really like the size as well.

### Time Spent - 2 Hours (5/07/25)
