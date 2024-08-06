# Project: Subdomain Scanner and Directory Enumerations using GO


## Overview
This project aims to create a Go Package / Script to scan a a list or singular url that scans for its subdomains, and enumerates the given domains prepended with the found subdomains 
> performs various scanning operations (quickscan, deepscan) with additional functionalities such as proxy support, user-agents, directory binwalk using a .txt file


## Directory Structure

/subdomain-scanner
|-- /cmd
|   |-- main.go                  # The entry point of the script that handles CLI interactions.
|-- /pkg
|   |-- /scanner
|       |-- scanner.go           # Core logic for scanning and enumeration.
|   |-- /util
|       |-- constants.go         # Defines constants, including API endpoints, if any.
|       |-- parser.go            # Helps with parsing input and files.
|-- /internal
|   |-- /api
|       |-- client.go            # Handles third-party API interactions, if applicable.
|-- /data
|   |-- domains.txt              # Example input file listing domains to scan.
|-- /test
|   |-- scanner_test.go          # Unit tests for scanner functionalities.
|-- go.mod
|-- go.sum
|-- README.md                    # Project documentation and guidelines.
|-- PROJECT_PLAN.md              # This file outlines the project's plan and structure.

## Components and Responsabilities

### cmd/main.go
The `main.go` will act as the starting point of subscango, responsible for CLI interactions, including flag parsing and initiating the scanning process


### pkg/scanner/scanner.go
This Module will contain the core functionalities for scanning and enumerating subdomains. It includes logic to distinguis between quick and deep scans, handling concurrency for efficiency, and integrating with any defined third-party services for subdomain discovery


### pkg/util/constants.go & parser.go
Utility functions and constants that are reusable across the project such as common settings, API calls, including authentication, request throttling and parsing responses


### data/domains.txt
example input for the domains to be read and used as the argument fo the scan

### test/scanner_test.go
Unit tests to ensure the scanner logic is accurate and reliable


## Development Phases
1. **Setup Project Status**: Establish the directory and file struct
2. **Implement Core Logic**: Develop the base funcs for domain scanning and subdomain enum
3. **Integrate Third-Party Services**: Improve the command line interface to make the tool user-friendly and versatile
4. **CLI enhancements**: _*If applicable, add support for third-party services to enhance enums
5. **Testing & Documentation**: Write comprehensive tests and document usage guidelines with examples



## Technologies and Libraries
- **Go**: The primary programming language for development.
- **net/http**: To make HTTP requests, if needed for API calls.
- **os/exec**: For possibly invoking third-party tools from Go.
- **flag**: For parsing command line arguments.

## Ethical Considerations
- Gain explicit permission before scanning networks or domains.
- Adhere to rate limiting and legal guidelines of used APIs.

This project plan will evolve as development progresses.
