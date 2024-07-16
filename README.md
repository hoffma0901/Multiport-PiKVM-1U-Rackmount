# Multiport-PiKVM-1U-Rackmount

 This is the projexct page for a multiport PiKVM in a 1U 19" rack mount format.
 It consist out of a Raspberry Pi with PiKVM, a 4 Port KVM switch and lots of 3D-printed parts

 ![multiport_PiKVM_rackmount](img\pikvm_rack.JPEG)

So far everything works fine except the atx control for multiple devices. I‘m still trying to figure out the best way to add at least 3 ports for atx control.

My overall goal was to keep it as flexible as possible, therefore the front is split into 3 parts:

1. PiKVM Frontplate with every neccessary I/O ports in order to connect to the 4 port kvm (XK-HK4401). Also the OLED info display is mounted there.

2. 4-port KVM with the input selector switches and additional USB ports

3. HDMI and USB faceplate for the KVMsource inputs.

Most of the ports are mounted with keystone elements, so it is easy to relocate or replace them with something else. The mounting plates itself are 3D printed and screwed into place from the bottom (threaded inserts).

To still have access to the GPIOs of the Pi I‘ve added a breakout board. The KVM switch remote was replaced with a direct UART connection to the Pi, so the input source can be selected via the PiKVM web interface as well.

For the power supply I went with one that outputs 5V (4A) and 12V (3A).

In the following sections you will find neccessary parts, tools and files in order to build your own multiport PiKVM.


## Parts List

In this section you will find the general parts list and tools needed in order to build the KVM yourself. I won't put direct reference links to the individual products here, since the availability may vary from country to country or the listings may change. Most of the things where purchased from Amazon. Otherwise I will leave a recommended shop or the specific name as a comment in brackets and picture for reference.

### Tools

- Clippers, wire stripper and a crimping tool for cable lugs and dupont crimps
- Superglue
- 3D printer (everything was printed with PLA and a 0.4mm nozzle, 0.2 mm layer height)
- Soldering iron, flux, solder
- Soldering iron adaptor for threaded inserts
- Power drill
- 3mm metal drill bit
- Countersink
- Center punch
  
### Parts

- Raspberry Pi 4 (I'm using the 2GB model)
- GeekPi Raspbery Pi 4 heatsink kit with a fan
- 16 GB Micro SD card with PiKVM installed
- Geekworm PiKVM-A3 Kit

- <details>
    <summary> XK-HK4401 4 Port KVM Switch (Aliexpress)</summary>

    ![4_port_kvm_switch](img\xh-hk4401-kvm-switch.jpg)

  </details>

- Keystone Modules
  - Keystone module USB C to USB C
  - Keystone module USB A to USB A
  - 5x Keystone Module HDMI to HDMI
  - 4x Keystone Module USB A to USB B (front facing USB B)
  - (5x Keystone Module CAT 6 unshielded) - WIP for the ATX control
- Noctua NF-A4x10 FLX (or any other 40mm fan)
- <details>
    <summary>60W AC to DC 12V 3A and 5V 4A</summary>

    ![60w_psu_ac_dc_12v_5v](img\psu_d60_12v_5v.jpg)
    </details>
- <details>
    <summary>C13 Socket Inlet Module with switch (AC 250V 10A)</summary>

    ![c13_inlet](img\c_13_plug.jpg)
    </details>
- <details>
    <summary>Digitus Professional DN-19 Tray-1-SW 19" Rack tray - 1U</summary>

    Dimensions: 45 x 483 x 250 mm (H x W x D)

    ![digitus_rack_tray](img\digitus_rack_tray.jpg)
    </details>
- <details>
    <summary>Daoki GPIO Extension Board Raspberry Pi</summary>

    ![gpio_extension](img\gpio_extension.jpg)
    </details>
- <details>
    <summary> 2x DollaTek Disassembled Double GPIO Adapter for Raspberry Pi</summary>

    ![gpio_adapter](img\gpio_adapter.jpg)
    </details>
-  <details>
    <summary>M2 M2.5 M3 Micro Screw Assortment, Flat Round Phillips Screws 450 Pieces</summary>

    ![screw_assortment](img\screw_assortment.jpg)
    </details>
-  <details>
    <summary>Cable Lugs Set for 0.5-6 mm² 400 Pieces</summary>

    Only the sizes "Ring M4" are needed (the open ones)

    ![cable_lugs](img\cable_lugs.jpg)
    </details>
- 4x USB A to USB B cable ca. 40cm
- 5x HDMI Cable
  - 3x 25 cm
  - 2x 40 cm
- USB A to USB C Cable ca. 25 cm
- <details>
    <summary>USB C to USB C Cable with one 90 degree angled connector < 1m</summary>

    ![usb_c_angled](img\usb_c_angled.jpg)
    </details>
- <details>
    <summary>HDMI Cable with one 90 degree angled (right) connector</summary>

    ![hdmi_angled](img\hdmi_angled.jpg)
    </details>
- 4x Wago 5-Pin Terminal
- 2x USB A Plug (male) for soldering
- 4 core data wire (4x 0.34 mm²) ca. 10-25 cm
- 3 core 1.5 mm² installation cable
- M2.5 threaded inserts
- M2.5 hex spacers/standoffs set
- 40 Pin header female
- Dupont header and crimp set
- 0.5mm² wire in different colors
