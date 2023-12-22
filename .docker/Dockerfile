# Use a Node.js base image with a specific version
FROM node:14-alpine

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install project dependencies
RUN npm install

# Copy the entire project files to the working directory
COPY . .

RUN npm run build

# Expose the port your app runs on
EXPOSE 8080

# Define the command to run your application
CMD ["npm", "start"]
