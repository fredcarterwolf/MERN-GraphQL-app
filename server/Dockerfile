# Pull Docker Hub base image
FROM node:16.13.1

# Create and Set working directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/app

# Install app dependencies
COPY package*.json ./
RUN npm ci

# Copy app to container
COPY . .

# Exports
EXPOSE 8080

# Run the "start" script in package.json
CMD ["npm", "start"]
