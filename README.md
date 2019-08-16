# Sandbox Internet Browsing

As per [CSE Top 10](https://cyber.gc.ca/en/guidance/top-10-it-security-actions-protect-internet-connected-networks-and-information-itsm10189) - Isolate Web-facing applications, Organizations should use virtualization to create an environment where Web-facing applications can run in isolation. Internet browsers and email clients are examples of applications that are susceptible to exploits that execute malware. Security exploits specific to such applications can be confined to this sandbox. Any malware that infects the virtualized environment cannot get out of the sandbox; therefore, the malware cannot infect the host or enterprise.

## Requirements

1. Docker installed on Windows
    a. If you have Windows 10 Pro or above, use [Docker for Desktop](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
    b. If you have Windows 7 or Windows 10 Home, use [Docker Toolbox](https://download.docker.com/win/stable/DockerToolbox.exe)
2. Install a X server software on Windows, [VCXSRV](https://sourceforge.net/projects/vcxsrv/)
3. Build the docker image ```docker build . -t firefox:latest```
4. Start docker with ```docker run -it -e DISPLAY=<ip>:0.0```

## Findings and references

Credits go to https://dev.to/darksmile92/run-gui-app-in-linux-docker-container-on-windows-host-4kde .

### Findings/Issues so far

1. Docker on firefox works but wow is it slow. 
2. You will most likely want to bump up the RAM on the docker VM that is running on your Windows machine. 
3. YouTube keeps crashing even after disabling hardware acceleration. 


