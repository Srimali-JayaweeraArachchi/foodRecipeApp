# Use an official Node.js runtime as a parent image
FROM node:18 

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install 

# Copy the rest of the frontend code
COPY . .

# Build the React app
RUN npm run build

# Install and use an HTTP server (like serve) to serve React
RUN npm install -g serve

# Expose the frontend port (e.g., 3000)
EXPOSE 5173

# Start the frontend server
CMD ["serve", "-s", "build", "-l", "5173"]