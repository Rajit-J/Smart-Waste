# Smart Waste Collection and Route Management

A C-based local web application prototype for managing waste bins, vehicles, drivers, routes, and collection simulations. A built-in HTTP server serves both the dashboard and its API.

## Features

- Bin, vehicle, and driver management.
- Route optimization and collection simulation.
- Dashboard analytics and reports.
- Local binary persistence for demo data.

## Technology

- C HTTP server (Winsock on Windows; POSIX sockets on Linux/WSL)
- HTML, CSS, and JavaScript frontend
- Makefile-based build

## Build and run on Windows

Install MSYS2 and the MinGW-w64 UCRT64 compiler and make package. Open the **MSYS2 UCRT64** terminal:

```bash
pacman -S --needed mingw-w64-ucrt-x86_64-gcc mingw-w64-ucrt-x86_64-make
cd /d/MyProjects/Smart-Waste
make
./waste_server.exe
```

Open [http://127.0.0.1:8080/dashboard](http://127.0.0.1:8080/dashboard). Stop the server with **Ctrl+C**.

## Linux / WSL

Install a C compiler and Make, then:

```bash
cd /mnt/d/MyProjects/Smart-Waste
make
PORT=8080 ./waste_server
```

Open [http://127.0.0.1:8080/dashboard](http://127.0.0.1:8080/dashboard). Stop with **Ctrl+C**.

## Important security note

This is an educational prototype. Its current authentication and password hashing are not suitable for production or internet-facing use. The source currently provides demonstration credentials when no local credential file exists. Do not reuse those credentials, do not deploy with real accounts or sensitive data, and do not commit credential files, local configuration, generated binaries, runtime data, or logs.

## Before publishing

Review the authentication implementation and local runtime files. No license is included; confirm ownership and license terms before adding one.
