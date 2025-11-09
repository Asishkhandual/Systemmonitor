# System Monitor (mini-top)

## Description
A lightweight C++ system monitor tool that provides real-time monitoring of CPU and memory usage, similar to the `top` command. It reads system statistics from `/proc` and displays process information with interactive sorting and process management capabilities.

## Features
- Real-time CPU and memory usage display
- Process listing with CPU%, MEM%, RSS, and process name
- Sorting by CPU usage or memory usage
- Interactive commands for sorting and process killing
- Non-blocking input with automatic refresh every 2 seconds
- Terminal-based interface with ANSI escape codes for clearing and positioning

## Requirements
- Linux operating system (uses `/proc` filesystem)
- C++ compiler (e.g., g++)
- Standard C++ libraries (included via `<bits/stdc++.h>`)
- Permissions to read `/proc` directories and send signals to processes

## Compilation
Compile the program using g++:
```
g++ main.cpp -o systemmonitor
```

## Usage
Run the compiled executable:
```
./systemmonitor
```

The tool will start monitoring and display system stats. It refreshes every 2 seconds and waits for user input.

## Commands
- `c`: Sort processes by CPU usage (default)
- `m`: Sort processes by memory usage
- `k <pid>`: Kill the process with the specified PID (sends SIGTERM)
- `q`: Quit the application
