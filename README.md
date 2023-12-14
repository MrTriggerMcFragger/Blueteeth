# Blueteeth
The Blueteeth system is an A2DP broadcasting solution. This device takes in audio data from a singular source (i.e. a phone or computer), and broadcasts that audio to multiple Bluetooth speakers simultaneously.

<div align="center">
  <strong><ins> Video Presentation</ins></strong>
  <br/>
  <a href="https://youtu.be/luHCMfh11go"><img src="http://img.youtube.com/vi/luHCMfh11go/0.jpg" alt="Video Presentation"></a>
</div>

## Table of contents
- [Project Directories](#project-directories)
- [Getting Started](#getting-started)
- [Theory](#theory)
- [References & Kudos](#references--kudos)

## Project Directories
| Name                                                               | Purpose                                        | 
| :--                                                                | :--                                            |
|[Blueteeth-Internal-Network-Stack](https://github.com/TragerZW/Blueteeth-Internal-Network-Stack)| Library used by both the master & slave devices that defines communications between Blueteeth devices. 
|[Blueteeth-Master](https://github.com/TragerZW/Blueteeth-Master)                                | An Arduino sketch for the master device which receives data from an audio source (i.e. a phone or computer), and relays that data to all of the slave nodes in the network over UART. 
| [Blueteeth-Slave](https://github.com/TragerZW/Blueteeth-Slave)  | An Arduino sketch for the slave nodes which receive audio data from the master node over UART, and stream that audio data to an audio sink (i.e. a Bluetooth speaker).  
|[Blueteeth-Terminal](https://github.com/Ali-Doge/Blueteeth-Terminal/tree/f47892bef948bcc814911b3085bee7de4962b158) |  
|[Blueteeth-Scanner](https://github.com/BarakBinyamin/speakerscan)                                          | An Arduino sketch for a device which scans for speakers and relays this information over UART |

## Getting Started

### Cloning The Repository
```bash
git clone https://github.com/BarakBinyamin/blueteeth.git        # Download this repo locally
cd blueteeth; git submodule update --init --remote --recursive  # Pull all the submodules too
```
>*Note: Information about an individual Arduino sketch's dependencies can be found on that sketch's repository page.*

### Wiring

#### Data Plane
![Data Plane Wiring Diagram](https://github.com/TragerZW/Blueteeth/blob/main/docs/img/Data%20Plane.png?raw=true)

#### Control Plane
![Control Plane Wiring Diagram](https://github.com/TragerZW/Blueteeth/blob/main/docs/img/Control%20Plane.png?raw=true)

>*Note: All pins in the wiring diagram are correct (they were not chosen arbitrarily to demonstrate the concept). The ESP32 board shown in the diagrams is the Teyleten Robot ESP32-Wroom Development board. For more information on these pins, look at the master and slave node repository pages.*

## References & Kudos
The following are the original contributors to the project:
- Ali Stambayev ([Ali Doge](https://github.com/Ali-Doge/))
- Barak Binyaman ([BarakBinyamin](https://github.com/BarakBinyamin/))
- James Ehrlinger ([jvEhrlinger](https://github.com/jvEhrlinger/))
- Zachary Trager MacDonald ([TragerZW](https://github.com/TragerZW/))
