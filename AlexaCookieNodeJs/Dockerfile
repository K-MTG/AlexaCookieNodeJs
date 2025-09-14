# Use Node.js LTS
FROM node:18-alpine

# Install git (needed if npm dependencies use git URLs)
RUN apk add --no-cache git

# Set working directory
WORKDIR /usr/src/app/AlexaCookieNodeJs

# Copy package.json first
COPY AlexaCookieNodeJs/package*.json ./

# Install dependencies
RUN npm install

# Copy rest of app
COPY AlexaCookieNodeJs/ ./

# Make main script executable
RUN chmod +x ./AlexaCookie.js

# Default command
CMD ["node", "AlexaCookie.js"]
