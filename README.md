# docker-wine-gui-app-runner
A GUI app runner on docker

courtesy of AgileDevArt https://www.youtube.com/watch?v=SZvwDqSPuTU

<!-- 
Install VcXsrv XServer or another XServer on Windows
Start wine Docker Container
Install and Run a Windows app inside a Docker Container
Use winetricks in a Docker Container
-->

Certainly! Below is a template for your project's `README.md` file. This README includes a brief introduction, instructions on how to build and run the Docker container, and information about the file structure. Feel free to modify it to better suit your project's specific details and requirements.

---

# Wine on Arch Linux Docker Container

## Overview
This project provides a Docker container setup to run Windows binary executables with a GUI on Arch Linux using Wine. It's designed to allow users to execute Windows applications in an isolated Docker environment on a Linux system.

## Getting Started

### Prerequisites
- Docker
- Docker Compose

### Installation and Running

1. **Clone the Repository:**
   ```bash
   git clone [Your Repository URL]
   cd [Your Repository Name]
   ```

2. **Build and Run the Docker Container:**
   Use Docker Compose to build and run the container:
   ```bash
   docker-compose up --build
   ```

2. **Run the Docker Container:**
   From now on you can use Docker Compose to run the container:
   ```bash
   docker-compose up
   ```

## File Structure
- `docker-compose.yml`: Docker Compose configuration file.
- `Dockerfiles/`: Directory containing Dockerfiles.
  - `Dockerfile.arch-wine64`: Dockerfile for creating the Wine on Arch Linux container.
- `LICENSE`: License file for the project.
- `README.md`: This file, containing documentation and instructions.
- `run`: Directory for windows binary executables to run.
- `scripts/`: Directory containing scripts and the docker entrypoint script.
  - `setup-and-run.sh`: Script for setting up and running the application (entrypoint).

## License
This project is licensed under the [LICENSE](LICENSE) - see the file for details.

## Authors
- [star-3gg]

## Acknowledgments
- Hat tip to anyone whose code was used
- Inspiration
- etc.
