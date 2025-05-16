# Build a chat application with Open Web UI
This tutorial shows you how to create a chat application using Foundry Local and Open Web UI. When you finish, you'll have a working chat interface running entirely on your local device.

## Prerequisites
Before you start this tutorial, you need:

1) Foundry Local installed on your computer.
2) At least one model loaded with the foundry model load command, like this:
      foundry model load Phi-4-mini-instruct-cuda-gpu

## Set up Open Web UI for chat
1) Install Open Web UI by following the instructions from the Open Web UI GitHub repository:https://github.com/open-webui/open-webui.
2) Launch Open Web UI with this command in your terminal:

      open-webui serve
3) Open your web browser and go to http://localhost:8080.
4) Connect Open Web UI to Foundry Local:

    -Select Settings in the navigation menu
    -Select Connections
    -Select Manage Direct Connections
    -Select the + icon to add a connection
    -Enter http://localhost:PORT/v1 for the URL, where PORT is the port number assigned to your Foundry Local instance.
    -Type any value (like test) for the API Key, since it cannot be empty
    -Save your connection
   
![image](https://github.com/user-attachments/assets/f0a9ff35-3d8e-4b36-9db4-5e107b7a06d6)


## Start chatting with your model:
1) Your loaded models will appear in the dropdown at the top
2) Select any model from the list
3) Type your message in the input box at the bottom

👌That's it! You're now chatting with an AI model running entirely on your local device.

