# Teemo CLI

[![Go Version](https://img.shields.io/github/go-mod/go-version/iagonc/teemo-cli)](https://golang.org/)

## Overview

**SRE Toolbox CLI** is a command-line tool designed to simplify troubleshooting and automation tasks for Site Reliability Engineers (SREs). It integrates common Linux utilities to assist with debugging, monitoring, and managing systems, helping SREs quickly resolve incidents, reduce downtime, and ensure smooth operations.

With a focus on providing human-readable outputs, this CLI centralizes useful tools and abstracts complex commands, streamlining day-to-day troubleshooting tasks.

## Features

- **Service Status Check**: Verify the status of critical services using `systemctl`, restart services, or retrieve logs for debugging when issues are detected.
- **Network Debugging**: Diagnose network issues using `dig`, `ping`, `traceroute`, and `netstat` for quick connectivity checks and performance troubleshooting.
- **Log Analysis**: Retrieve and display logs from `journalctl` and `dmesg` in a user-friendly format to identify system errors and warnings quickly.
- **Resource Monitoring**: Monitor CPU, memory, and disk usage with commands like `top`, `df`, and `free` to ensure optimal resource utilization.
- **Firewall and Network Security**: Use `iptables` to inspect firewall rules and check for potential network traffic blocks or security issues.
- **Service Logs Extraction**: If a service is failing, automatically fetch the latest logs from `journalctl` to help debug the root cause of the issue.

## Installation

To install **SRE Toolbox CLI**, make sure you have [Go](https://golang.org/doc/install) installed on your system, and then follow these steps:

```bash
git clone https://github.com/your-username/project-name.git
cd project-name
go build -o sre-toolbox
```
This will generate the sre-toolbox binary which you can execute directly.

## Usage

Here are some examples of how to use the SRE Toolbox CLI:

1. **Check Service Status:**
   ```bash
   ./sre-toolbox service-check --service nginx
    ```

   This will check if the `nginx` service is active and provide logs if the service is not running.

2. **Fetch Network Debug Information:**

   ```bash
   ./sre-toolbox network-debug --tool dig --target example.com
   ```

   This will use `dig` to check DNS resolution for the target.

3. **Monitor Resource Usage:**

   ```bash
   ./sre-toolbox resource-check --type memory
   ```

   This command shows the current memory usage on the system.

4. **Extract Service Logs:**
   
   ```bash
   ./sre-toolbox logs --service nginx
   ```

   This fetches the latest logs from `journalctl` for the specified service.

## Contributing

Contributions are welcome! If you find a bug or have a feature request, please open an issue or submit a pull request. Follow the guidelines below to contribute to this project:

1. Fork the repository.
2. Create a new branch.
3. Make your changes and ensure they are well-tested.
4. Submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- Built using [Go](https://golang.org/).
- Inspiration from various Linux tools and SRE best practices.
