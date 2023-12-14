# Blueteeth
The Blueteeth system is an A2DP broadcasting solution. This device takes in audio data from a singular source (i.e. a phone or computer), and broadcasts that audio to multiple Bluetooth speakers simultaneously.

[![Video Demo](http://img.youtube.com/vi/luHCMfh11go/0.jpg)](https://youtu.be/luHCMfh11go)


## Table of contents
- [Project Directories](#project-directories)
- [Getting Started](#getting-started)
- [Theory](#theory)
- [References & Kudos](#references--kudos)

## Project Directories
| Name                                                               | Purpose                                        | 
| :--                                                                | :--                                            |
|[Blueteeth-Internal-Network-Stack](Blueteeth-Internal-Network-Stack)| Library used by both the master & slave devices that defines communications between Blueteeth devices. 
|[Blueteeth-Master](Blueteeth-Master)                                | An Arduino sketch for the master device which receives data from an audio source (i.e. a phone or computer), and relays that data to all of the slave nodes in the network over UART. 
| [Blueteeth-Slave](Blueteeth-Slave)  | An Arduino sketch for the slave nodes which receive audio data from the master node over UART, and stream that audio data to an audio sink (i.e. a Bluetooth speaker).  
|[Blueteeth-Terminal](https://github.com/Ali-Doge/Blueteeth-Terminal/tree/f47892bef948bcc814911b3085bee7de4962b158) |  
|[Blueteeth-Scanner](speakerscan)                                          | An Arduino sketch for a device which scans for speakers and relays this information over UART |

## Getting Started

### Cloning The Repository
```bash
git clone https://github.com/BarakBinyamin/blueteeth.git        # Download this repo locally
cd blueteeth; git submodule update --init --remote --recursive  # Pull all the submodules too
```
### Wiring
>TBD

### Dependencies
Ensure that the [Blueteeth-Internal-Network-Stack](Blueteeth-Internal-Network-Stack) is in your Arduino libraries folder... 
>TBD

## Theory
>TBD

## References & Kudos
The following are the original contributors to the project:
- Ali Stambayev ([Ali Doge](https://github.com/Ali-Doge/))
- Barak Binyaman ([BarakBinyamin](https://github.com/BarakBinyamin/))
- James Ehrlinger ([jvEhrlinger](https://github.com/jvEhrlinger/))
- Zachary Trager MacDonald ([TragerZW](https://github.com/TragerZW/))
