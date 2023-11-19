# docker-wine-gui-app-runner
A GUI app runner on docker

courtesy of AgileDevArt https://www.youtube.com/watch?v=SZvwDqSPuTU

<!-- 
Install VcXsrv XServer or another XServer on Windows
Start wine Docker Container
Install and Run a Windows app inside a Docker Container
Use winetricks in a Docker Container
-->

# Wine on Arch Linux Docker Container

## Running Windows Binaries with GUI in Docker on Windows

To successfully run GUI applications from the Docker container on a Windows host, you will need to install and run an X11 server, such as VcXsrv XServer. This allows the Docker container to display GUI applications on your Windows desktop.

### Setting Up X11 Server

1. **Install X11 Server:**
   Download and install an X11 server application, such as VcXsrv Windows X Server, which you can find at [VcXsrv's GitHub page](https://github.com/ArcticaProject/vcxsrv) or a suitable alternative.

2. **Configure X11 Server:**
   After installation, run XLaunch (comes with VcXsrv) and configure it with the following settings:
   - Multiple windows
   - Display number: 0
   - Start no client
   - Enable `Disable access control`

3. **Run X11 Server:**
   Finish the configuration and run the X server. This will allow graphical applications from the Docker container to display on your Windows machine.

### Connect Docker to X11 Server

Before running the Docker container with `docker-compose up --build`, ensure that the DISPLAY environment variable in your `docker-compose.yml` is set correctly to interface with the host's X11 server. Usually, this would be `DISPLAY=host.docker.internal:0.0`.

### Additional Notes

- Firewall or Antivirus software on your Windows machine might block the connection from the Docker container to the X11 server. If you encounter issues, consider adjusting these settings.
- The performance and compatibility may vary depending on the Windows binary application and the X11 server's configuration.

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
