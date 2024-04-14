# Use an official node.js runtime as a parent image (alpine helps reducing the image overall size)
FROM node:16-alpine as builder

# Set the working directory to /app 
WORKDIR /app

# Copy both package.json and package.lock.json files to the container
COPY package*.json .

# Install project dependencies
RUN npm install --silent

# Copy the rest of the app code to the container
COPY . .

# Build the app
RUN npm run build

# Run the app
CMD [ "npm", "start"]