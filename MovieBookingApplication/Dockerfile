# Use an official Node runtime as a parent image
FROM node:14-alpine

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all local files to the container
COPY . .

# Build the application
RUN npm run build

# Expose a port (usually 80 for HTTP)
EXPOSE 80

# Define a command to run the application when the container starts
CMD ["npm", "start"]
