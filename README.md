# Hardware Accelerator for Matrix Mulitplications using Systolic Arrays
AI Accelerator for efficient convolution and matrix multiplication operations using the concept of systolic arrays. Seamlessly integrates with a CPU via AXI4 lite interfaces. Key components: AXI4 Slave/Master interfaces, Controller, Input/Weight/Output memories, 9x9 Processing Elements. Implements interrupt handling. Implemented in Verilog.

## Key Features

- **AXI4 Slave Interface**: Allows the CPU to configure and control the accelerator's operation by writing to specific registers.
- **Controller**: Orchestrates the overall operation of the AI accelerator, managing data flow and controlling the execution of convolution and matrix multiplication operations.
- **AXI4 Master Interface**: Enables the accelerator to access external memory (e.g., DRAM) for fetching input data and storing output data.
- **Input & Weight Memory**: Stores input data (e.g., images or feature maps) and convolution kernels or weights required for computation.
- **Output Memory**: Stores the results of convolution and matrix multiplication operations.
- **Processing Elements**: Each processing element constitutes a 9x9 grid, capable of performing maximum matrix multiplication of 9x9 and convolution operations with a kernel size of 3x3.
- **Interrupt Handling**: Implements interrupt mechanisms to signal task completion, enabling efficient coordination between the CPU and the accelerator.

## Design Specifications

- **Memory Map for AXI Slave Interface**: Defines the memory-mapped registers for configuring and controlling the accelerator.
- **Memory Architecture**: Utilizes a 9x9 shift register configuration for efficient storage and retrieval of data.

## Repository Contents

- Verilog files for the AI accelerator design
- Vivado IP Integrator project files
- Implementation of AXI4 interfaces with validation
- Hardware implementation for matrix operations
- Hardware implementation for convolution operations
- Software drivers for matrix and convolution operations
- Software implementation for interrupt handling
- Testing and validation scripts
