# Use an official Node.js runtime as a parent image
FROM node:18 

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the backend code
COPY . .

# Expose the application's port (e.g., 5000)
EXPOSE 5000

# Start the backend server
CMD ["npm", "start"]
