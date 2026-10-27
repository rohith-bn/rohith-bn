# Hi, I am Rohith 👋
### Embedded Systems & Firmware Engineer | System Architecture & Deterministic Controls
📍 **Munich / Germany** | Open to Embedded Systems, Firmware & Real-Time IoT Roles

Engineering reliable, deterministic embedded software in **C (C99/C11)** and **Embedded C++** across **ARM Cortex-M (STM32)** and **wireless SoCs (ESP32)**. Focused on **first-principles system design**, bare-metal hardware abstraction, RTOS scheduling, and host-mock Test-Driven Development (TDD).

---

### 🛠️ Technical Competencies & Toolchain

- **Languages & Standards**: C (ISO C99/C11), Embedded C++, Python (automation & AST tooling), MISRA-C fundamentals, Bash
- **Silicon & Architectures**: ARM Cortex-M4/M3 (STM32), ESP32 / ESP32-C3 (RISC-V, ESP-IDF), Tensilica
- **RTOS & Scheduling**: FreeRTOS (preemptive priority scheduling, queues, semaphores), Deterministic ISR Super Loops, Zephyr RTOS fundamentals
- **Buses & Peripherals**: CAN / CAN-FD, SPI, I2C, UART, DMA circular streams, Hardware Timers / PWM, ADC
- **Protocols & Wireless**: ISO 11898-1 CAN, Wi-Fi (802.11 b/g/n, DTIM power optimization), TCP/IP, MQTT, BLE
- **Verification & Tooling**: Host-First TDD (Unity, Ceedling, GCC mocks), Logic Analyzers, Oscilloscopes, GDB, CMake, PlatformIO, Git

---

### 🧠 Engineering Methodology: AI-Augmented Systems Development

I approach firmware development through a **human-directed, AI-augmented systems engineering methodology**:
- **Architectural Ownership & Domain Leadership**: Retaining complete human responsibility for defining the physical problem space, establishing hard real-time timing budgets, enforcing safety-critical state invariants, and personally validating behavior on target silicon.
- **AI as an Architectural Sparring Partner**: I leverage agentic AI workflows to stress-test state-machine failure modes, generate formal UML/Mermaid flows, draft exhaustive host unit test suites, and accelerate technical documentation.
- **Outcome**: Delivering verified, decoupled, production-grade embedded software with high architectural velocity and zero dynamic memory allocation.

---

### 🚀 Highlighted Engineering Repositories

#### 1. [QFC-1: Flight Controller Firmware & System Design](https://github.com/rohith-bn/flight-controller-firmware-system-design)
*Deterministic 1 kHz flight stabilization firmware engineered from formal system design to bench validation.*
- **System Design**: Decomposed into 9 behavioral responsibilities and 15 decoupled C modules with zero hardware register leakage.
- **Hard Real-Time Math**: Closed-loop sense-estimate-control pipeline executing in $<300\,\mu\text{s}$ of a $1000\,\mu\text{s}$ timing budget.
- **Fail-Safe FSM**: Centralized safety gate with an unconditional, one-way latching `FAULT` state that silences motors in $<1\,\text{ms}$.
- **Verification**: **12 host unit test suites (100% passing)** and a **6-DOF Software-In-the-Loop (SIL) numerical physics simulator** before target flashing.

#### 2. [Embedded Core Components (Decoupled HAL & Drivers)](https://github.com/rohith-bn/embedded-core-components)
*Reusable, decoupled pure C embedded drivers and hardware abstraction contracts.*
- **Contract Decoupling**: Designed clean hardware abstraction seams allowing drivers to run on physical silicon or native host desktop simulators.
- **In-Memory Register Mocks**: Implemented 256-byte in-memory software mocks for I2C and SPI, allowing comprehensive edge-case testing without physical hardware attached.
- **Display Driver**: Pure C SSD1306 OLED framebuffer driver with deterministic drawing primitives and zero heap allocation.
- **Test Coverage**: 20 automated host unit tests verifying buffer boundaries and protocol error handling.

#### 3. [Automotive CAN Telemetry Node & bxCAN Filtering](https://github.com/rohith-bn/stm32-can-telemetry-node) `[Active Learning Laboratory]`
*Practical exploration of the CAN bus protocol, automotive coding standards, and hardware filtering on STM32.*
- **Learning Target**: Practical implementation of ISO 11898-1 CAN standards, automotive MISRA-C guidelines, and disciplined automotive firmware workflows.
- **Silicon Optimization**: Exploring STM32 bxCAN 14-bank hardware filter masks to route telemetry frames directly to dual hardware FIFOs at 0% CPU overhead.
- **Concurrency & Buffering**: Statically allocated circular ring buffers with atomic pointer arithmetic, decoupled from FreeRTOS telemetry tasks.
- **Verification Harness**: 69 automated host unit tests verifying filter mask math, bit-timing prescalers, and packet deserialization.

#### 4. [Developer Tooling: agentic-doc-pipeline & ELF Memory Analyzer](https://github.com/rohith-bn)
*Internal developer tools built to eliminate workflow friction and enforce memory budgets.*
- **agentic-doc-pipeline**: AST-based documentation compiler converting technical specs to DIN 5008 standards with 85% LLM token reduction.
- **ELF Memory Analyzer** `[In Development]`: Python CLI utility parsing ELF symbol tables to track Flash (`.text`, `.rodata`) and SRAM (`.data`, `.bss`) headroom with automated CI budget gates.

---

## 📬 Connect with Me

- **LinkedIn**: [linkedin.com/in/rohithbn](https://www.linkedin.com/in/rohithbn/)
- **Email**: [rohith.bn04@gmail.com](mailto:rohith.bn04@gmail.com)
