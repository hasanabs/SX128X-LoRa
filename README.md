# SX128x Arduino Library

This repository is based on the [StuartsProjects](https://github.com/StuartsProjects/SX12XX-LoRa) repository (as of the March 2024 commit) and focuses exclusively on the SX128x library, with additional features and improvements.

### Additional Features
- **Reliable Packet Transmission with Addressing**:  
  New functions `transmitReliable_addr`, `receiveReliable_addr`, `transmitReliableAutoACK_addr`, and `receiveReliableAutoACK_addr` have been added to enhance reliable communication with built-in addressing support.
- **Channel Activity Detection (CAD)**:  
  New functions `setCadParam` and `setCad` have been added to configure CAD symbol parameters and execute CAD operations. CAD facilitates LoRa preamble detection. For transmitters, it enables "listen before talk" to prevent collisions. On the receiver side, it helps decide whether to open the receive window, as the receive window tries to decode the message (cost of power consumption).
- **Advanced Ranging (AR) Mode Operation**:  
  A new function `receiveAdvancedRanging` has been added to allow us to passively overhear ranging exchanges of a point-to-point ranging exchange.