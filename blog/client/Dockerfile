# Use an official Node.js runtime as a parent image
FROM node:14-alpine

# Set the working directory to /app
WORKDIR /app

# Copy package.json and package-lock.json to /app
COPY package*.json ./

# Install dependencies
RUN npm install --silent

# Copy the remaining app files to /app
COPY . .

# Build the React app
RUN npm run build

# Set the command to start the server
CMD ["npm", "start"]