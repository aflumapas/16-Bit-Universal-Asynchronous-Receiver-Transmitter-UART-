# 16-Bit, 9600 bps UART Module in Verilog HDL

A Universal Asynchronous Receiver-Transmitter (UART) designed in Verilog HDL, featuring custom 16-bit word length support and circular FIFO data buffering.

## Overview
- **System Clock:** 50 MHz
- **Baud Rate:** 9600 bps
- **Data Frame:** 16-bit framework using a byte-multiplexing architecture

## Architecture & Modules
1. **BAUDRATE.v**: Generates $1\times$ TX ticks and $16\times$ RX oversampling ticks.
2. **TX.v**: Serializes parallel data LSB-first
3. **RX.v**: Synchronizes asynchronous input signals via a double-flop chain
4. **FIFO.v**: Circular buffer utilizing extended pointers (`ADDR_WIDTH:0`)
5. **UART_2.v**: Top-level wrapper integrating sub-modules.
