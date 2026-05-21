# RigRunner

![Rig Runner Banner](./assets/rigrunner.png)

**RigRunner** is a tool designed to make installing **UMC OS** firmware on your **Antminer** mining rigs fast, easy, and reliable. It guides you through the deployment process so you can get your rigs up and running consistently across multiple devices with minimal effort. RigRunner is production-ready and suitable for both large scale, professional mining and hobbyist setups. It is actively maintained, and updates focus on adding support for additional Antminer models and improving the installation workflow.

Get the latest **RigRunner** software here:

[![Download](https://img.shields.io/badge/Download-blue?style=for-the-badge)](https://github.com/epicblockchain/rig-runner/releases/)

---

## How it works

[UMC OS Install Guide](./assets/RigRunner_Build_Guide_V4_UMC_OS_Installer-1.pdf)

- **Guided Install:** RigRunner guides you through the install process.  
- **Discovery:** Helps identify compatible Antminer devices on the local network.  
- **Compatibility:** Supports a wide range of Antminer models and ensures proper installation of **UMC OS** on supported devices.  
- **Efficiency:** Install **UMC OS** firmware across multiple rigs and have them up and mining in just minutes.
- **Cross-platform support:** RigRunner works on Windows, macOS, Debian, and Red Hat systems.
- **Uninstallation support:** Allows you to revert rigs back to their stock firmware in their original state.  

---

## Get UMC OS

Get **UMC OS** firmware here:

[![Download](https://img.shields.io/badge/Download-blue?style=for-the-badge)](https://github.com/epicblockchain/umcos-antminer/releases)

## Compatibility

See supported mining rigs [**here**](https://github.com/epicblockchain/umcos-antminer)

## Demo

![Demo GIF](./assets/how_to_install_umc_os.gif)

## CLI Usage (Advanced Users)

### GUI Mode

Run the RigRunner application without any arguments to launch the graphical interface:

```sh
./rig-runner
```

### CLI Mode

When you provide arguments, it automatically runs in CLI mode:

```sh
# Show help
./rig-runner --help

# Scan for devices
./rig-runner --ranges 192.168.1.0/24 scan

# Install firmware from a local file
./rig-runner --ranges 192.168.1.0/24 install -f firmware.zip

# Install firmware from GitHub release
./rig-runner --ranges 192.168.1.0/24 install --version latest

# List available firmware versions
./rig-runner list-versions

# Uninstall firmware
./rig-runner --ranges 192.168.1.0/24 uninstall -p password
```

#### CLI Options

- `--ranges <IP/CIDR>`: IPv4 CIDR ranges to scan (comma-separated)
- `--threads <N>`: Number of threads to use (default: 512)
- `--timeout <MS>`: Timeout in milliseconds (default: 2000)
- `--retries <N>`: How many times to retry connection (default: 10)
- `--max-connections <N>`: Maximum concurrent connections (default: 25)
- `-p, --umcos-password <PASSWORD>`: Password for umcOS miners
- `-l, --log-folder <PATH>`: Log file path
- `-v`: Verbose output (use `-vv` for trace output)
- `-q`: Quiet mode (use `-qq` for errors only)
