# Moonstone

[![Join the chat at https://gitter.im/moonstone_cgm/Lobby](https://badges.gitter.im/moonstone_cgm/Lobby.svg)](https://gitter.im/moonstone_cgm/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)


The smallest available solution to turn your Freestyle Libre into a wireless CGM (continuous glucose monitor).

Author's note
The original idea for the Moonstone was to simply develop a custom wireless CGM board for Freestyle Libre. Since finding out about the great work and development done with LimiTTer, it was decided that possibly the least time consuming way to accomplish the idea, was to benefit from the work already accomplished. Therefore Moonstone has been designed to use the same CR95HF NFC -chip as the LimiTTer's BM019 module uses, as well as NRF52832 BLE-chip, which can be run with Arduino core. Therefore the Moonstone should be able to run with LimiTTer code, with little tweaking.

In a nutshell: 
- Moonstone is a custom pcb board consisting of 
	-CR2023 battery
	-nrf52832
	-CR95HF
- Moonstone has physical dimensions of
	- 30mm width diameter
	~ 0,8mm thick pcb + the components, total height ~1,8mm. However, when using CR2023 battery, the height of the whole system will be 23mm. + thin nfc antenna and casing. 
- Moonstone's host chip nrf52832 is programmed with (for example) J-Link mini EDU (only for non-commercial usage ~18€) through SWD interface
- Nrf52832 will be running Arduino core, with LimiTTer code, and should therefore have the same compatibility as LimiTTer (xDrip+ etc.)
- Has total BOM/component cost of ~20€ per device (when hand soldered, excluding programmer)



Next steps for the project Moonstone:

1. Review the schematics & pcb layout - OK !?
	- Fix 27 MHz component's outline
2. Order and assemble the first prototypes (OSH Park & Mouser)
	- Check with OSH Park support that everything's ok.
3. Program and verify the prototypes with Arduino core
	- Power on testing, signal integrity etc.
4. Find the proper impedance matchings for the BLE and NFC -antennas
5. Port the LimiTTer code to Moonstone
	- What are the possible modifications needed?
6. Validate the performance of BLE and NFC with Libre
	- Distances etc.
7. Design small form factor clip-on casing/mechanics (e.g. 3D printable)
	- Using the three cavities on Libre for mounting?
8. Performance optimization: 
	- Increasing the distance of BLE
	- increasing battery life, possibly dropping out the Arduino core for power optimization

All the needed information for building your own Moonstone will be updated to this page, as the project advances. Also note, that Moonstone is an unofficial and experimental DIY project, that has no connections to Abbott. At this stage there are no other plans for the manufacturing of the devices, other than having everyone order, solder and program their own devices. NOTE: ATM. THIS PROJECT REQUIRES ADEQUATE SKILLS AND TOOLS FOR SOLDERING 0402 and QFN SMD COMPONENTS, SO BE AWARE OF THIS, OR USE A PCB ASSEMBLY SERVICE TO MANUFACTURE YOUR DEVICE.

Collaborators needed!
All help is welcome, from HW, to SW and Mechanics, or whatever your expertise might be.
At this stage, there's especially a need for software developers who have access to both nrf52832 development kit and BM019 Module. These would be needed for the verification of the whole concept of using Arduino core + LimiTTer code for Moonstone, allowing already the development of the SW prior to having the HW done.

Please join our chatroom on gitter, and participate the project!
[![Join the chat at https://gitter.im/moonstone_cgm/Lobby](https://badges.gitter.im/moonstone_cgm/Lobby.svg)](https://gitter.im/moonstone_cgm/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
