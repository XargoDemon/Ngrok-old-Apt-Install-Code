# Ngrok Old Linux APT Install Code

This repository contains the old APT install code for Ngrok on Linux. This is useful for users who need to install a previous version of Ngrok using APT.

## About

This repository provides the old APT installation code for Ngrok, a secure tunnel to localhost, which is useful for developers needing to test their webhooks or serve their local servers over the internet.

## Prerequisites

Ensure you have the following prerequisites installed:

- A Linux-based operating system
- `curl` installed

## Installation

Follow these steps to install the old version of Ngrok using APT:

1. **Add the Ngrok GPG key:**

    ```bash
    curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.asc | sudo apt-key add -
    ```

2. **Add the Ngrok APT repository:**

    ```bash
    echo "deb https://ngrok-agent.s3.amazonaws.com buster main" | sudo tee /etc/apt/sources.list.d/ngrok.list
    ```

3. **Update your package list:**

    ```bash
    sudo apt update
    ```

4. **Install Ngrok:**

    ```bash
    sudo apt install ngrok
    ```

## Usage

After installing Ngrok, you can start using it by running:

```bash
ngrok http 80


(Total) Code: curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.asc | sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null
echo "deb https://ngrok-agent.s3.amazonaws.com buster main" | sudo tee /etc/apt/sources.list.d/ngrok.list
sudo apt update
sudo apt install ngrok
