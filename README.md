# CI/CD Deployment to AWS EC2 using GitHub Actions

## Overview

This project sets up a basic CI/CD pipeline using GitHub Actions and AWS EC2.  
When code is pushed to the `main` branch, an `index.html` file is automatically deployed to an Nginx web server on EC2 via SSH.

## Stack

- AWS EC2 (Ubuntu)
- Nginx
- GitHub Actions
- SSH (key-based authentication)

## Steps

1. Created an EC2 instance and installed Nginx
2. Set up SSH key pair
3. Added private key and host IP to GitHub Secrets
4. Configured GitHub Actions to:
   - Upload `index.html` to EC2 via `scp`
   - Move it to `/var/www/html/` using `ssh`

## Result

Any push to `main` triggers deployment.  
The updated `index.html` is automatically served by Nginx without manual access.

## Next Steps

- Add Docker and reverse proxy
- Deploy a dynamic app instead of a static file
