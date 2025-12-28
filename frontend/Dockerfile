# Use official Node.js image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy the source code
COPY . .

# Build the frontend for production
RUN npm run build

# Expose the port Vite preview uses
EXPOSE 4173

# Start the app in preview mode (host needs to be 0.0.0.0 for Docker)
CMD ["npm", "run", "preview", "--", "--host", "0.0.0.0"]