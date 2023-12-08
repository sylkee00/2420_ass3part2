# Introduction
This README outlines the steps and configurations required to complete Assignment 3 Part 2. The assignment involves augmenting a web server with various components, including a backend, a load balancer, and enhancing skills in multi-part application development, Linux file system, command-line expertise, security implementation, and application deployment.

# Repository Contents
- frontend/: Contains the HTML files for the frontend.
- backend/: Contains the binary file for the backend.
- nginx/: Contains the Nginx configuration files.
- services/: Contains the hello-server.service file.
- cloud-config/: Contains the cloud-config script (SSH key removed).

# Server Setup Instructions

## Creating Debian Servers:

Create two Debian 12 servers named **"web1"** and **"web2"**.
Ensure they have the tag **"web"**.
Add a regular user named **"web"** with *SSH access*, *bash login shell*, and *sudo group membership*.

## Configuring the Servers:

- Disable root access via SSH.
- Install **Nginx** and **UFW**.
- Set up the firewall to allow incoming and outgoing HTTP and SSH traffic.

## Frontend and Backend Setup:

- Place the HTML files from the frontend/ directory into the appropriate directory on both servers.
- The backend binary from the backend/ folder needs to be placed in a suitable directory and made executable.
- Update the Nginx configuration with the provided file in nginx/ to serve the frontend and act as a proxy for the backend.
- Place the hello-server.service file in the services/ directory and ensure it's correctly set up to start the backend service.

## Load Balancer Setup:

- Configure a Digital Ocean load balancer in front of your servers.
- Update the Nginx configuration to include location blocks with proxy_pass directives for /hey and /echo routes.

# Testing:

Use the included curl commands(check curl.md) to test your setup using the load balancer IP address.
