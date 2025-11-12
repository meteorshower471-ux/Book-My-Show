# Use a Node.js base image
FROM node:20-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json first to leverage caching
COPY package*.json ./

# Install application dependencies
RUN npm install

# Copy the rest of the application source code
COPY . .

# Build the application (if necessary, for React/Angular frontends)
# RUN npm run build 

# The port the app runs on internally
EXPOSE 3000

# Command to start the application
CMD ["npm", "start"]
