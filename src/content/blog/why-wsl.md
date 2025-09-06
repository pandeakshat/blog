---
title: Why WSL is My Data Science & Software Engineering Daily Driver (and Why It Might Be Yours Too)
description: Why WSL is My Data Science & Software Engineering Daily Driver (and Why It Might Be Yours Too)
pubDate: 2025-06-04
heroImage: '/images/why-wsl.png'
readingTime: 5 min read
tags:
  - data-science
  - linux
  - windows
---
**TLDR:** This article shares my perspective on why Windows Subsystem for Linux (WSL) is my go-to choice over a standalone Linux installation for data science and software engineering, offering a step-by-step guide for setup, requirements, and handy tips/tricks.

My software engineering journey began roughly 15 years ago. As a teenager, I was already knee-deep in simple C++ programming, tweaking system and admin permissions to get the most out of my machine. This tinkering quickly evolved into a passion for creation, for solving problems, for finding that missing piece and ultimately, the solution.

Over this long journey, starting way back with Windows XP, I’ve had my hands on most operating systems I could get access to. Sometimes it was for experimentation, sometimes out of sheer boredom, and occasionally due to a minor inconvenience that made me just hit reset and start fresh.

More recently, this journey has been significantly streamlined by WSL. There are a lot of reasons I personally endorse and choose it, and it’s truly curated to my specific requirements and workflow. While my choices might not apply to everyone, I’m sharing them so you, the reader, can draw parallels, understand my decision, and perhaps even be inspired to experiment.

This article is structured simply: we’ll cover my personal requirements, why I chose WSL, my experiences with standalone Linux, why you might consider WSL, a roadmap and setup guide, some tips and tricks, and finally, a few key points to remember.

## My Tech Persona: Developer, Gamer, Writer, & Avid Adventurer

Let’s kick things off with my requirements. I’m a developer, a gamer, a writer, and an avid adventurer in the tech world.

**As a developer**, my needs are intermediate. Python, machine learning, local LLMs, web development, and blockchain technology. My projects don’t typically demand heavy resources, and I’m comfortable switching between GUI and CLI environments, depending on what the scenario calls for.

**My gaming rig and time** usually revolve around the MMORPG Dota 2. I also genuinely enjoy a good campaign and storyline, and I’m not overly obsessed with cutting-edge graphics.

**My writing** generally leans towards content and creative pieces — articles, poetry, and engaging discussions.

Finally, **as an avid adventurer**, I absolutely love exploring and trying out new software and applications. Sometimes they replace my current setup, and sometimes they just consume a bit of time, ultimately making me realize why my existing tools are still my preference.

## Why WSL?

So, why did I ultimately choose WSL? Well, the decision wasn’t straightforward. Most programming and development choices rarely are. I’ve navigated through dual-boot setups, standalone Linux installations, various Linux distributions, Windows without WSL, and finally, Windows with WSL. One crucial caveat here: I’m not proficient with VirtualBox, which played a role in my decision-making.

For me, WSL provided a perfect gateway into development without disrupting my general tech adventures. I love exploring Product Hunt for new innovations, I enjoy diving into old-school games, and I relish writing and sharing documentation in easily digestible formats. WSL created a distinct separation for my development work from these “general adventures.” It offered the familiar Linux terminal and code environment that I’ve refined over time, while crucially maintaining the ease of file transfers, smooth animations, visual clarity, and broad software compatibility of Windows, all with a decent level of customizability.

## My Linux Standalone/Dual-Boot Experience: The Missing Link

With a standalone or dual-boot Linux setup, I often found myself missing the instant switch between a focused coding session and simply writing in Obsidian while a video (or anime!) played in the background, or even jumping into a game filled with memories to blow off some steam. An additional factor that frequently bothered me was driver compatibility and the complexity of setting things up. While drivers in Windows were generally easier due to manufacturer requirements and Windows being the default operating system, Linux hardware installation often conjures memories of having to reset the entire system, again.

Now, I know a lot of my issues could be solved by “getting good.” However, in my opinion, there are already too many things I _have_ to get good at: coding, debugging, structuring, algorithms, ideation, deployment, writing, designing, consulting, and so much more. For my development and leisure environment, I believe in simplifying the requirements and the product to maximize ease and functionality, no matter what I’m doing. Standalone or default Linux made it difficult for my easily distracted brain to switch contexts; it often made me feel lost, and that’s simply not helpful on my journey.

## Why You Should Consider WSL: Minimal Consequences, Maximum Flexibility

So, why should _you_ consider WSL?

The easiest reason is **minimal consequences**. As long as your computer supports it, you can set up WSL, install a Linux distribution of your choice from the Microsoft Store or via the command line. Love it? Keep it. Don’t love it? Simply terminate and unregister it. The impact on your Windows system is negligible. While it functions similarly to a virtual machine, it leverages underlying Windows features rather than running an entire, separate VM system.

Second, WSL allows you to **explore and improve cross-compatibility**. You’ll become more proficient in using a Linux system, even if you eventually switch to a standalone installation, and you’ll adapt quickly. You’ll also get better at using WSL seamlessly with Windows (my favorite feature is the sheer ease of file explorer integration and file management). Finally, yes, you can still enjoy some games!

## Your WSL Roadmap & Setup Guide

Let’s get to the easiest part: the instructions!

1. Check Requirements & Compatibility

Before we dive in, let’s ensure your system is ready for WSL.

Operating System: Windows 10 version 2004 or higher (Build 19041 or higher) or Windows 11.

Virtualization: Ensure virtualization is enabled in your computer’s BIOS/UEFI settings. This is crucial for WSL to function.

2. Technical Commands to Set Up WSL

Setting up WSL is surprisingly straightforward. Open your Command Prompt or PowerShell as an administrator.

To install WSL with the default Ubuntu distribution:

wsl --install

This command will enable the necessary optional components, download the latest Linux kernel, set WSL 2 as the default, and install Ubuntu. After the installation, you’ll be prompted to restart your computer.

If you want to install a specific distribution (e.g., Debian instead of Ubuntu):

wsl --install -d <DistributionName>

To see a list of available distributions:

wsl --list --online

Once installed and after a restart, open the Ubuntu (or your chosen distro) application from your Start Menu. The first time you launch it, you’ll be prompted to create a Unix username and password.

3. General Maintenance and Recommended Installations

Once your WSL environment is set up, here are some general maintenance tips and recommended installations:

Update and Upgrade: Always start by updating your package lists and upgrading installed packages within your WSL distro.

sudo apt update

sudo apt upgrade

Install build-essential: This meta-package includes compilers (like GCC) and other tools essential for compiling software.

sudo apt install build-essential

Install Git: Version control is fundamental for any developer.

sudo apt install git

Install Zsh and Oh My Zsh (Optional, but Recommended): For a more powerful and customizable shell experience.

sudo apt install zsh

chsh -s $(which zsh)

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

4. Setup for Data Science

Here are some data science-specific steps:

Install Miniconda or Anaconda: These are excellent for managing Python environments and data science packages. Miniconda is lighter.

# Download Miniconda installer (check for the latest version on their website)

wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

bash Miniconda3-latest-Linux-x86_64.sh # Follow the prompts. Type 'yes' to initialize Miniconda.

source ~/.bashrc # or ~/.zshrc if you use Zsh

Create a Data Science Environment:

conda create -n ds_env python=3.9

conda activate ds_env

pip install numpy pandas matplotlib scikit-learn jupyterlab

Access JupyterLab from Windows: Once in your ds_env and jupyter-lab is running, you can access it from your Windows browser. The jupyter-lab output will provide a URL, often http://localhost:8888/?token=.... Copy and paste this into your Windows browser.

5. Setup for Web Development

For web development, you’ll want to set up Node.js, npm, and potentially a database.

Install Node.js via NVM (Node Version Manager): This allows you to easily switch between Node.js versions.

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh | bash

source ~/.bashrc

# or ~/.zshrc

nvm install node # Installs the latest LTS version nvm use node

Install a Database (e.g., PostgreSQL):

sudo apt install postgresql postgresql-contrib

sudo service postgresql start # Start the PostgreSQL service

sudo -u postgres psql # Connect to PostgreSQL as the postgres user

# In psql, you can create a new user and database

# CREATE USER myuser WITH PASSWORD 'mypassword';

# CREATE DATABASE mydatabase OWNER myuser; # \q (to exit psql)

6. Setup for Blockchain Development

Blockchain development often involves specific tools and compilers.

Install Solidity Compiler (Solc): Used for compiling Ethereum smart contracts.

sudo snap install solc # Install via Snap

# Or, for a PPA:

# sudo add-apt-repository ppa:ethereum/ethereum

# sudo apt update

# sudo apt install solc

Install Ganache CLI (for local Ethereum blockchain development):

npm install -g ganache-cli

Install Truffle (development framework for Ethereum):

npm install -g truffle

7. Tips & Tricks

Accessing Windows Files from WSL: Your Windows drives are mounted under /mnt/. For example, your C: drive is at /mnt/c.

Accessing WSL Files from Windows: Open File Explorer in Windows and type \wsl$\ in the address bar. You'll see your installed Linux distributions as network drives.

VS Code Integration: VS Code has excellent remote development extensions for WSL. Install the “Remote — WSL” extension in VS Code. You can then open your WSL projects directly within VS Code, and it will run the VS Code server within your WSL environment. Just type code . in your WSL terminal in a project directory.

Windows Terminal: Consider using the new Windows Terminal. It’s highly customizable and allows you to have multiple tabs for PowerShell, Command Prompt, and your WSL distributions all in one window.

Performance Tuning: If you’re running heavy workloads, you might want to adjust WSL’s memory and CPU allocation. Create or edit the .wslconfig file in your Windows user profile directory (C:\Users<YourUsername>.wslconfig).

Ini, TOML

[wsl2]

memory=8GB # Adjust as needed

processors=4 # Adjust as needed

Remember to shut down WSL for changes to take effect: wsl --shutdown in PowerShell.

Thank You & Points to Remember

Thank you for joining me on this exploration of WSL! Here are a few final points to keep in mind:

WSL is not a full Linux desktop experience: While it’s powerful, it’s not designed to fully replace a standalone Linux desktop for every use case.

Updates are crucial: Regularly update both your Windows system and your WSL distributions.

Community is your friend: If you encounter issues, the WSL community forums and Stack Overflow are excellent resources.

I hope this guide helps you navigate the exciting world of WSL and empowers your data science and software engineering journey!