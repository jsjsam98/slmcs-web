# react-app/Dockerfile

# Base image for Node.js version 20
FROM node:20-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the React application
RUN npm run build

# Install 'serve' globally to serve the React application
RUN npm install -g serve

# Expose port 3000 to make it accessible from the host
EXPOSE 3000

# Command to serve the React app
CMD ["serve", "-s", "build"]
