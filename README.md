# chat-app-node-js



#!/bin/bash
apt update -y
curl -fsSL https://deb.nodesource.com/setup_18.x | bash -
apt install -y nodejs git nginx
git clone https://github.com/RahulDMane/chat-app-node-js.git /home/ubuntu/app
cd /home/ubuntu/app
npm install
PORT=3000 node server.js &
PORT=3001 node server.js &
systemctl enable nginx
systemctl start nginx
