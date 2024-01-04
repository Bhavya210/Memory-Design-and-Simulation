# Memory Module (memory.vhdl)

## Overview

The `memory` module is a versatile VHDL component providing a dual-port memory structure. Designed for synchronous operation, it accommodates read (`re`) and write (`we`) operations on two distinct ports (`A` and `B`). The memory has a capacity of 256 locations, each capable of storing an 8-bit data vector.

## Functionality

- **Synchronous Operation:** The module operates synchronously with the rising edge of the clock signal (`clk`).
  
- **Addressing:** Memory access is facilitated through address vectors (`addr_a` and `addr_b`), allowing for targeted read and write operations.

- **Data Handling:** Data vectors (`data_a` and `data_b`) manage the information to be written into the memory.

- **Control Signals:** Write Enables (`we_a` and `we_b`) and Read Enables (`re_a` and `re_b`) govern write and read operations for the respective ports.

- **Output:** Output vectors (`q_a` and `q_b`) provide the data read from the specified memory addresses.

## Memory Structure

Internally, the module employs an array (`mem_array`) to represent the memory locations. During a rising clock edge, it selectively reads and writes data based on the control signals and addresses provided. The memory initializes with zero values.

## Usage

Integrate this memory module into VHDL projects requiring dual-port memory functionality. Careful attention to clock synchronization and control signal management is essential for reliable memory operations.

## Customization

Adapt the module to suit project-specific requirements. Adjust the memory size, data width, or other parameters as needed.

**Note:** Refer to the source code (`memory.vhdl`) for further details on the module's implementation.
