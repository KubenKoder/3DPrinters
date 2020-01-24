# Fire protection system for 3D printers 

## Description
We want to delevlop a comprehensive fire protection sytem for 3D printers.

The goal is to have a system that gives us such peace of mind that we can allow pupils to run several printers unattended over every night in a public school in Norway, while following national and EU safety rules and not being liable if these is fire or smoke damage to the school. 

The system should be easy to replicate in similar circumstances, very easy to inspect and maintain and be resonably inexpensive. 

## Are some 3D printers already safe?
Some printer manufacturers state in their certification documents that their printers are safe for unattended (overnight) use, Ultimaker 2 for example, provided that you only use their material and correctly follow all user guides. Others make the opposite claim and say that an active printer can never be left unattended, Prusa i3 for example. We argue that these claims are not enough since we want to be able to use various printers, various filament and do some modifications to the printers. Also we are not yet comfortably convinced that the risk of accidental printer-fires is small enough based on the tough use the printers see. 

## What are the fire risks
The risky elements of the 3D-printer can be divided into three categories. 

**Risks**
* Hot end
* Heated bed
* Electronics

### Hot end
The hot end typically consist of an aluminium heat retention block with a brass nozzle tip which extrudes the molten plastic. It is electrically heated by a 40 watt heating cartridge (Prusa i3) and is typically regulated to 210-240C while printing. The heating cartridge can get reach temperatures above 750C if not regulated.

### Heated bed
A heated bed is an optional but common part of modern 3D printers and consist of a (235*235mm) plate that is heated evenly with electricity (220W) ([Creality 3D](https://www.banggood.com/no/Creality-3D-24V-220W-235235mm-Aluminum-Heated-Bed-Hot-Bed-Kit-For-Ender-3-3D-Printer-p-1335217.html))

### Electronics
Electrical faults are a common source of 3D printer fires. This is likely due to the high regulated currents for the heating elements and the "hacker" nature of their maintainers who might use cheap parts of suspect origin in their construction and modification. 

**Risks**
* Plastic parts on the printer melts which causes other dangers - PLA starts going soft and some wire insulation isn't safe above 60C.
* Ignition of flammable foreign objects - Paper ignites at 233C.
* Ignition of the 3D-printing plastic - PLA ignites at 388C [Ultimaker PLA specs](fire/UM180816_SDS_PLA-RB_V11.pdf)
* Thermal runaway - An out of control 40W heating cartridge will melt through the aluminium heat block (660C melt point) [video link](https://www.youtube.com/watch?v=qVjWg2vuWzk)

**Example problem casuses**
* The hot end cooling fan stops due to poor maintenance, this causes the plastic holder to melt and the active hot end to move out of its intended work area where it can cause damage.
* A piece of paper touches the hot end and ignites flies away and spreads the fire
* The control software settings are set wrong and the temperature is no longer regulated correctly, leading to overheating
* The software freezes so that the temperature is no longer regulated correctly, leading to overheating

### Summary
There are fire risks related to 3D printer use, we must assume that enought 3D printers might sometimes catch fire if used long enough. However there are migtigations that should reduce the chance/interval of fire incidents to within acceptable levels. 

## Mitigations
If we can detect the precursors to fire we might be able to stop the fire from catching by turning of the power supply to the printers.

**Precursors to fire**
* Smoke
* Hotter temperatures than usual

Both precursors can be detected with standard sensors that can turn of the power using a standard contactor. To ensure detection the printers should be enclosed. To increase the detection chance fans could be used to pull air from the enclosure past the sensors.

## When there is a fire
When there is a fire we want it to be noticed an put out before it causes too much damage. For this to happen we need a reliable, approved fire detections system that is connected to somebody who will absolutely be able to get access to the fire before it has grown beyond manageable bounds. This can be broked down to these things we need to do:
* Detect real fires 
* Alert the authorites
* Limit Fire progression 

### Detect "real" fires 
The area hosting all printers need to be covered by an approved fire detection system that will detect any real fire. This is not negotiable.

### Alert the authorites
The fire alarm needs to be always connected to somebody that is guaranteed to have have access to the printers and are able to respond directly, over a time span of several years time every day of the year. This means the fire department. 

### Limit fire progression 
If the fire can spread to flammable materials (filament spools etc) the fire might well too large when the fire department gets there. Either the available flammable materials need to be limited or alternatively the fire can be actively suppressed by an automatically deployed system. An automatic firefighting system will be more effective in an enclosed volume and such a container should also help prevent a fire from spreading. [Fire capsule](https://www.maritim.no/bonpet-brannslukkingsampull) [Fire capsule 2](http://bontel.com/production/show2/fire_extinguishing_device.html)

The first two are already common standard requirement but care should be taken to not accidentaly circumvent them by, for instance building a new forced ventilation system without adding smoke detectors in the ducts.

## Concept 
A generic metal cabinet housing a number of nondescript 3D printers standing on shelves. The cabinet doors are transparent. The printers are powered from electical sockets built into the cabinet. There are smoke and or heat detectors mounted to the top of the cabinet that will detect precursors to fires in any one of the printers. This is accompliced by that air can flow to the sensor past shelves or multiple sensors. If fire precursors are detected the power to the cabinet is cut off. Power can be reset with the press of a button. 

### Option: Fire suppression
Iside the cabinet a fire suppression capsule is mounted, if the inside reaches a high enough temperature the capsule activates and supresses the fire. The cabinet walls and doors should not reach critical temperatures before the capsule activates regardless of the location of the fire. [Fire capsule](https://www.maritim.no/bonpet-brannslukkingsampull), [Fire capsule 2](http://bontel.com/production/show2/fire_extinguishing_device.html)

### Option: Reduced flammable contents 
If no fire suppression system is installed the amount of flammable material in the cabinet should be reduced by storing the filament in a separate compartment. This is to reduce the speed at which the fire spreads. 

**Bonuses* 
* The cabinet can alert users of the precursor alarm being triggered in various ways, internet, lights etc. Care should be taken that these functions does not hinder the main feature of cutting the power.
* Lighting can be integrated into the cabinet
* Fume extraction can be integrated into the cabinet. As long as it does not reduces the fuction of the fire alarm connected to the authorites.

**Questions**
* Does the doors need to be self closing to prevent them being left open, reducing the detection effectiveness?
* Filament storage, should it be separate? 
* Glass doors or plastic? How much heat can plastic doors take?
* Are there cheap cabinets that can easily be used for this purpose?
* How much flammable material in the cabinet is too much?

## Notes
Even if the school does not burn to the ground it would be too much if we filled a room with nasty smoke which may happen without a fire being started.
Confined space for smoke detection and control power 

Transparent door on enclosure to see the printers in work is necessary.

If there is a fire risk, then there will eventually be a fire. 

Nothing should be stored on the cabinet. Prevent it physically.

A loose smoke sensor connected to a loose pluggable socket is likely to be used intermittently. A cabinet gives flexibillity and a clear signal over which printers are made safe for overnight printing.