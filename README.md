# NESOS0.1.1-OS-
10.22.24$ 
# NESOS 0.2.1

NESOS (Nintendo Entertainment System Operating System) is a simple, experimental operating system designed to run on the NES hardware. This project provides a basic environment for NES development, allowing for multitasking, GUI management, and system scheduling. It is written entirely in 6502 assembly, taking advantage of the NES's limited hardware to implement basic OS functionalities.

## Features

- Basic task scheduling and multitasking
- PPU (Picture Processing Unit) management for rendering graphics
- Controller input handling (supports standard NES controllers)
- GUI management with windows, buttons, and basic input fields
- Dynamic memory management to allocate and deallocate tasks in memory
- Interrupt handling (NMI for VBlank, IRQ for external interrupts)

## Requirements

- **Assembler**: You need a 6502 assembler, such as [ASM6](https://github.com/qalle2/asm6) or [NESASM](https://github.com/camsaul/nesasm), to compile the code.
- **NES Emulator**: You can run this OS on an NES emulator like [FCEUX](http://www.fceux.com/web/home.html) or [Nestopia](https://www.zophar.net/nestopia).
- **CHR ROM**: A character ROM file (`charset.chr`) is required for the graphical elements (included in the repo).

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/catsanzsh/NESOS0.1.1-OS.git
    cd NESOS0.1.1-OS
    ```

2. Build the OS using your preferred assembler. For example, using `asm6`:

    ```bash
    asm6 os_NES.asm NESOS.nes
    ```

3. Run the compiled `.nes` file on an NES emulator:

    ```bash
    fceux NESOS.nes
    ```

## Usage

- **Controller Input**: Use your NES controller (or emulator controls) to interact with the system. The A/B buttons are used to navigate the GUI, while Start and Select manage system options.
- **Task Scheduling**: The OS allows simple tasks to be scheduled, switched, and run concurrently.
- **GUI**: The built-in GUI system provides a windowed environment for basic interactions.

## Project Structure

