# Install Foundry Local in Your Device
Download the installer from https://github.com/microsoft/Foundry-Local/releases/tag/v0.2.9265 [This repo will be public on May 19th, 2025]

## Getting Started
1) To view available models: foundry model list
2) To run a model: foundry model run <model>

 EXAMPLES:
         foundry model run phi-3-mini-4k

Usage:
  foundry [command] [options]

Options:
  -?, -h, --help  Show help and usage information
  --version       Show version information

Commands:
  model    Discover, run and manage models
  cache    Manage the local cache
  service  Manage the local model inference service
Get Started with Foundry Local
This guide provides detailed instructions on installing, configuring, and using Foundry Local to run AI models on your device.

## Prerequisites
-A PC with sufficient specifications to run AI models locally.
-Windows 10 or later.
-Greater than 8GB RAM
-Greater than 10GB of free disk space for model caching (quantized Phi 3.2 models are ~3GB)
-Suggested hardware for optimal performance:
  -Windows 11
  -NVIDIA GPU (2000 series or newer) OR AMD GPU (6000 series or newer) OR Qualcomm Snapdragon X Elite, with 8GB or more of VRAM
  -Greater than 16GB RAM
  -Greater than 20GB of free disk space for model caching (the largest models are ~15GB)
  -Administrator access to install software

## Installation
-Download Foundry Local for your platform from the releases page.
-Install the package by following the on-screen prompts.
-After installation, access the tool via command line with foundry.
-Running Your First Model
-Open a command prompt or terminal window.

   -Run a model using the following command:

       foundry model run deepseek-r1-1.5b
       This command will:

          -Download the model to your local disk
          -Load the model into your device
## Start a chat interface
💡 TIP: Replace deepseek-r1-1.5b with any model from the catalog. Use foundry model list to see available models.

## Explore Foundry Local CLI commands
  The foundry CLI is structured into several categories:

-Model: Commands related to managing and running models
-Service: Commands for managing the Foundry Local service
-Cache: Commands for managing the local cache where models are stored
To see all available commands, use the help option:

foundry --help
💡 TIP: For a complete reference of all available CLI commands and their usage, see the Foundry Local CLI Reference

## Integrating with Applications
Foundry Local provides an OpenAI-compatible REST API at http://localhost:PORT/v1.

Note that the port will be dynamically assigned, so check the logs for the correct port.
REST API Example
curl http://localhost:5273/v1/chat/completions \
  -H "Content-Type: application/json" \
  -d '{
    "model": "deepseek-r1-1.5b-cpu",
    "messages": [{"role": "user", "content": "What is the capital of France?"}],
    "temperature": 0.7,
    "max_tokens": 50
  }'
