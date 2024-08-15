# Use an official Node.js runtime as a parent image
FROM node:14

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose port
EXPOSE 3000

# Set environment variables
ENV DB_DIALECT=mariadb
ENV DB_USER=todo-admin
ENV DB_PW=admin-pw
ENV DB_HOST=mariadb:3306
ENV DB_NAME=tododot

# Start the application
CMD ["node", "bin/www"]
