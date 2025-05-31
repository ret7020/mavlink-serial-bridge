# mavlink-serial-bridge

**mavlink-serial-bridge** is a **MAVLink** messages forwarder from the **serial device** (**UART**, **RS-232**, some **USB devices**, etc.) to **UDP** packets and vice versa.

## Installation

This is a port of COEX MAVLink serial to UDP bridge for LicheeRV Nano.


```bash
export COMPILER=<CROSS_COMPILERS_DIR>/gcc/riscv64-linux-musl-x86_64/bin
mkdir build
cd build
cmake -DCMAKE_TOOLCHAIN_FILE=./toolchains/riscv64.toolchain.cmake
make
```

## Configuration

Create a copy of the `example.yaml` from `/etc/mavlink-serial-bridge/`, save it in the same directory and edit, according to your requirements.

## Start the application

Run `sudo systemctl start mavlink-serial-bridge@<configuration>` to start the tool, where **configuration** is the configuration file name (without the file extension).

Run `sudo systemctl enable mavlink-serial-bridge@<configuration>` to start the tool, where **configuration** is the configuration file name (without the file extension).
