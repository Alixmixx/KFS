# KFS Kernel Project
## Overview

This project, KFS (Kernel From Scratch), is a 32-bit operating system kernel written in Rust, developed as part of a school project. It involves creating a minimalistic kernel that can boot using GRUB, handle basic I/O operations, manage memory, and support interrupts and a Global Descriptor Table (GDT).

## Features

- **Bootloading with GRUB**: The kernel utilizes GRUB for initial bootstrapping.
- **Assembly Language Boot Code**: Handling multiboot headers and initializing the kernel.
- **Rust-Based Kernel Code**: Core kernel functionalities implemented in Rust.
- **Linker Script Usage**: To correctly link the kernel.
- **Basic I/O Support**: Including scroll, cursor, and color support.
- **Keyboard Handling**: With support for different layouts and basic commands.
- **Memory Management**: Implementation of a memory system with paging, and separate user and kernel space.
- **Interrupt Handling**: Through an Interrupt Descriptor Table (IDT).
- **Global Descriptor Table (GDT)**: For segment descriptor definitions.

## Getting Started

### Prerequisites

- Docker
- Rust toolchain
- QEMU (for emulation)

### Building the Kernel

1. **Docker Setup**: The project uses Docker to manage the build environment. Ensure Docker is installed and running on your system.

2. **Build the Docker Image**:
    ```shell
    make docker-build
    ```

3. **Create and Start the Docker Container**:
    ```shell
    make docker-create
    make docker-start
    ```

4. **Transfer Files and Build**:
    - The `make transfer-and-build` command will transfer necessary files to the Docker container and start the build process.
    - `make` can be used to build the project after the initial setup.

5. **Run the Kernel**:
    - Use `make run` to start the kernel in QEMU.

6. **Cleaning Up**:
    - `make clean` will clean the build files.
    - `make fclean` will remove the Docker container and image.

## Project Structure

- **SRC_FILES**: Includes `Cargo.toml`, configuration JSON, linker script, and Docker-specific Makefile.
- **SRC_DIRS**: Source directories containing Rust source files and other necessary files for bootstrapping and running the kernel.

## Project Milestones

- **KFS-1**: Basic kernel setup with GRUB, ASM boot code, and I/O interface.
- **KFS-2**: Implementation of the GDT and a basic shell for debugging.
- **KFS-3**: Advanced memory management with paging and kernel panic handling.
- **KFS-4**: IDT setup and basic interrupt handling.

**Note**: This README provides a general guideline for building and running the KFS kernel. Adjustments may be necessary depending on the specific setup and requirements of your environment.

---

## Contributions
This project was made in collaboration with Lorenzo Edoardo Francesco. His invaluable contributions, encompassing insights, expertise, and dedication, were instrumental to the success of this project. His innovative problem-solving skills have been inspiring. I am immensely grateful for the knowledge and experience gained through this collaboration.
- [Lorenzo Edoardo Francesco](https://github.com/lorenzoedoardofrancesco)
