# UniCrypt: A Decentralized Campus Ecosystem

**Team Members:** Ihsan Aziz, Suvir Duggal, Arnav Kumar, Sahibjot Singh, Jaskaran Singh

**Project Summary:** UniCrypt is a Web3 platform that unifies campus services by linking student ID cards to a blockchain wallet, enabling secure, decentralized transactions for payments, event ticketing, and physical access control.

[Devpost Link](https://devpost.com/software/unicrypt-zl3k4o)

---

## Project Overview

* **The Problem:** University campuses rely on fragmented, centralized systems for payments, access, and events. This results in high transaction fees, security risks, and a disjointed user experience.
* **Our Solution:** We engineered a unified ecosystem using an Ethereum smart contract to manage on-chain assets (funds, tickets, credentials). A React Native mobile app provides a user wallet, while a custom IoT devices verify blockchain assets for real-world interactions like unlocking doors or making payments.

## Key Features

* **Unified Digital Wallet:** Manages campus funds, event tickets, and access keys in a single mobile app.
* **Gas-Optimized Smart Contracts:** Solidity contracts engineered to minimize transaction fees for frequent, low-cost campus transactions.
* **Physical Asset Verification:** A bespoke IoT verifier securely validates a student's on-chain assets to grant physical access or log attendance.
* **Decentralized Transactions:** Eliminates centralized payment processors, enabling direct, fee-free crypto transactions.

## Image Gallery & Demonstration

*(A GIF demonstrating the mobile app interacting with the IoT hardware is highly recommended here.)*

<p align="center">
  <img src="https://github.com/m-aziz1/hacked-2025/blob/main/assets/unicrypt-payment-machine.jpg" alt="Payment IoT Device" width="48%" />
  <img src="https://github.com/m-aziz1/hacked-2025/blob/main/assets/unicrypt-access-device.jpg" alt=" Access/Attendance Verification IoT Device" width="48%" />
</p>
<p align="center">
  <img src="https://github.com/m-aziz1/hacked-2025/blob/main/assets/unicrypt-mobile-app.jpg" alt="Mobile App" width="20%" />
  <img src="https://github.com/m-aziz1/hacked-2025/blob/main/assets/unicrypt-admin.jpg" alt="Admin Panel" width="77%" />
</p>

## Technical Architecture

| Component | Technology |
| :--- | :--- |
| **Blockchain** | Solidity, Ethereum, Web3.js |
| **Backend API** | Node.js, Express.js |
| **Mobile App** | React Native, TypeScript/JavaScript |
| **IoT Hardware** | ESP32 Microcontroller, RFID Sensors, LCD, Custom Circuitry |
| **Firmware** | C++ (Arduino Framework) |
| **Cloud & Hosting**| Amazon Web Services (AWS) |

## Technical Implementation and Challenges

Our team tackled challenges across hardware engineering, blockchain development, and full-stack integration.

* **Hardware and Firmware Engineering:** The IoT verification device was designed from the component level up.
    * **Component Selection:** We selected the ESP32 microcontroller for its integrated Wi-Fi and processing capabilities. This involved analyzing manufacturer datasheets to determine pin configurations, voltage requirements, and communication protocols for peripheral components like the RFID/NFC reader and output actuators.
    * **Firmware Development:** The device's logic was written in C++ using the Arduino framework. The firmware was responsible for initializing hardware, managing the network connection, and communicating with our backend API via HTTP requests.
    * **Hardware Debugging:** Troubleshooting the prototype required using a multimeter to verify circuit continuity and voltage levels, and employing a serial monitor to debug the device's operational state and network communication in real-time.

* **Smart Contract Development:** To ensure economic viability, we focused on gas optimization. This involved writing efficient Solidity code by minimizing state storage, optimizing data types, and carefully structuring contract logic to reduce the computational cost of on-chain transactions.

* **Full-Stack Integration:** We engineered a secure communication pathway between the physical hardware and the blockchain. The ESP32 sends a credential hash to our Node.js backend, which then uses Web3.js to query the Ethereum smart contract. This intermediary architecture prevents the need to store any private keys on the IoT device, enhancing system security.

## Future Scope

* **DAO Governance:** Implementing a Decentralized Autonomous Organization for student club management.
* **NFT Credentials:** Issuing academic certificates and awards as non-fungible tokens (NFTs).
* **DeFi Integration:** Incorporating decentralized finance protocols for student savings or micro-loans.
